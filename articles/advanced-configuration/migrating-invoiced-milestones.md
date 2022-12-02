---
title: Memigrasikan tahapan penagihan yang sepenuhnya terfaktur saat transisi usaha
description: Artikel ini menjelaskan cara memigrasi tahapan penagihan dengan harga tetap yang telah ditagihkan kepada pelanggan untuk kontrak proyek terbuka sebelum tanggal tayang.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028706"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Memigrasikan tahapan penagihan yang sepenuhnya terfaktur saat transisi usaha

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

## <a name="scenario"></a>Skenario

Contoso akan melakukan publikasi dengan Microsoft Dynamics 365 Project Operations untuk skenario sumber daya/non-persediaan. Sebagai bagian dari aktivitas transisi usaha, tim implementasi harus memigrasikan kontrak proyek terbuka dari sistem lama. Beberapa kontrak proyek mencakup baris kontrak yang menggunakan metode penagihan harga tetap dan telah sebagian ditagih ke pelanggan akhir. Tim penerapan harus memigrasi tahapan penagihan ini sebagai **faktur Pelanggan yang diposting**, karena harus tercakup dalam nilai kontrak total untuk tujuan pengenalan pendapatan. Namun, saldo pelanggan dalam piutang dagang dan buku besar umum tidak boleh terpengaruh.

## <a name="solution"></a>Solusi

### <a name="prerequisites"></a>Prasyarat

- Dynamics 365 Finance 10.0.24 atau yang lebih baru harus diinstal.
- Lingkungan tempat langkah migrasi akan diselesaikan harus dalam mode pemeliharaan. Tidak ada aktivitas lain yang harus dilakukan saat tahapan dimigrasi.
- Langkah-langkah migrasi harus diikuti persis seperti dijelaskan di sini dan dapat digunakan hanya untuk aktivitas transisi usaha. Microsoft tidak mendukung penggunaan kemampuan ini lagi.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Membuat versi transisi usaha dari tahapan baris kontrak integrasi Project Operations dengan peta penulisan ganda 

1. Pastikan bahwa pemetaan target untuk entitas **tahapan baris kontrak integrasi Project Operations** merupakan yang terbaru. 

    1. Di Finance, buka **Manajemen Data** \> **entitas Data**, dan pilih entitas **tahapan baris kontrak integrasi Project Operations**. 
    2. Pilih **Modifikasikan pemetaan target**. 
    3. Pada halaman **petakan penahapan ke target**, pilih **Buat pemetaan**, lalu konfirmasikan bahwa Anda ingin membuat pemetaan.

2. Hentikan dan segarkan peta penulisan ganda **tahapan Baris kontrak integrasi Project Operations** (**msdyn\_contractlinescheduleofvalues**) 

    1. Buka **Manajemen Data** \> **Penulisan ganda**, pilih peta, dan buka rinciannya. 
    2. Pilih **Berhenti**, lalu tunggu hingga sistem menghentikan peta. 
    3. Pilih **Segarkan tabel**.

3. Tambahkan pemetaan untuk status transaksi.

    1. Pilih **tambahkan pemetaan**.
    2. Pada baris baru, pada kolom **aplikasi keuangan dan operasi**, pilih bidang **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Di kolom **Microsoft Dataverse**, pilih **msdyn\_invoicestatus \[status faktur\]**.
    4. Di kolom **Jenis peta**, pilih panah kanan (**\>**).
    5. Dalam kotak dialog yang muncul, pada bidang **arahan Sinkronisasi**, pilih **Dataverse ke aplikasi keuangan dan operasi**.
    6. Pilih **Tambahkan Transformasi**.
    7. Di bidang **jenis transformasi**, pilih **ValueMap**.
    8. Pilih **Tambahkan pemetaan nilai**.
    9. Pada bidang kiri, masukkan **4**. Pada bidang kanan, masukkan **192350001**. 
    10. Pilih **Simpan**, lalu tutup kotak dialog.

4. Pilih **Simpan sebagai** untuk menyimpan versi peta penulisan ganda. 
5. Di panel **Tambah tabel**, di bidang **Penerbit**, pilih **penerbit Default**.
6. Di bidang **versi**, masukkan versi.
7. Pada bidang **Deskripsi**, masukkan catatan tentang versi peta transisi usaha ini. 
8. Pilih **Simpan**.
9. Mulai peta.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Memigrasikan tahapan penagihan ke lingkungan Dataverse

1. Di lingkungan Project Operations Dataverse, buat tahapan yang memiliki status faktur **Siap untuk faktur**. Pada titik ini, jangan migrasikan tahapan yang belum ditagih.

    > [!NOTE]
    > Sebelum Anda memigrasi tahapan penagihan, pastikan dimensi keuangan yang terkait dengan baris kontrak proyek diatur sebagaimana harapkan. Dimensi keuangan tidak dapat diedit setelah migrasi selesai.

2. Setelah semua tahapan dimigrasi, hentikan peta penulisan ganda berikut:

    - Tahapan baris kontak integrasi Project Operations (msdyn\_contractlinescheduleofvalues)
    - Aktual Integrasi Project Operations (msdyn\_actuals)
    - Proposal faktur proyek V2 (faktur)

    Untuk menghentikan peta, ikuti langkah berikut ini:

    1. Di finance, buka **Manajemen Data** \> **Penulisan ganda**, pilih peta, dan buka rinciannya.
    2. Pilih **Berhenti**, lalu tunggu hingga sistem menghentikan peta.

3. Di lingkungan Project Operations Dataverse, buat dan konfirmasikan faktur pro-forma untuk tahapan penagihan. 

    1. Di peta situs, buka kontrak proyek, pilih kontrak, lalu pilih **Buat faktur**.
    2. Setelah faktur dibuat, buka dari menu **Faktur** di peta situs, lalu pilih **Konfirmasi**.

    Langkah ini akan membuat rekaman yang diperlukan di lingkungan Dataverse. Namun, hal ini tidak mempengaruhi keuangan dan piutang dagang, karena peta penulisan ganda yang terdaftar sebelumnya dihentikan.

4. Setelah semua faktur pro-forma dikonfirmasi, kembalikan semua peta penulisan ganda ke kondisi awal mereka.

    1. Perbarui versi peta penulisan ganda **tahapan Baris kontrak integrasi Project Operations** (**msdyn\_contractlinescheduleofvalues**) ke semula. 
    2. Pilih peta tulis ganda dalam daftar peta, pilih **versi peta tabel**, lalu pilih versi asli peta tabel.
    3. Pilih **Simpan**.
    4. Hidupkan ulang peta penulisan ganda berikut:

        - Tahapan baris kontak integrasi Project Operations (msdyn\_contractlinescheduleofvalues)
        - Aktual Integrasi Project Operations (msdyn\_actuals)
        - Proposal faktur proyek V2 (faktur)

Tahap selanjutnya dimigrasi, dan sistem siap melakukan langkah-langkah berikutnya dalam aktivitas transisi usaha.
