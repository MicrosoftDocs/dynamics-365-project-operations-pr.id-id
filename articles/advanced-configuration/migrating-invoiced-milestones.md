---
title: Memigrasikan tonggak penagihan yang ditagih sepenuhnya di cutover
description: Artikel ini menjelaskan cara memigrasikan tonggak penagihan dengan harga tetap yang telah ditagihkan kepada pelanggan untuk kontrak proyek terbuka sebelum tanggal tayang.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Memigrasikan tonggak penagihan yang ditagih sepenuhnya di cutover

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

## <a name="scenario"></a>Skenario

Contoso akan ditayangkan dengan Microsoft Dynamics 365 Project Operations untuk skenario sumber daya/non-stok. Sebagai bagian dari kegiatan cutover, tim pelaksana harus memigrasikan kontrak proyek terbuka dari sistem lama. Beberapa kontrak proyek termasuk jalur kontrak yang menggunakan metode penagihan harga tetap dan telah ditagih sebagian kepada pelanggan akhir. Tim implementasi harus memigrasikan tonggak penagihan ini seperti **yang diposting** faktur Pelanggan, karena mereka harus dimasukkan dalam total nilai kontrak untuk tujuan pengakuan pendapatan. Namun, saldo nasabah dalam piutang dan buku besar tidak boleh terpengaruh.

## <a name="solution"></a>Solusi

### <a name="prerequisites"></a>Prasyarat

- Dynamics 365 Finance 10.0.24 atau yang lebih baru harus diinstal.
- Lingkungan tempat langkah-langkah migrasi akan selesai harus dalam mode pemeliharaan. Tidak ada aktivitas lain yang harus dilakukan saat tonggak sejarah sedang dimigrasikan.
- Langkah-langkah migrasi harus diikuti persis seperti yang dijelaskan di sini dan hanya dapat digunakan untuk aktivitas cutover. Microsoft tidak mendukung penggunaan lain dari kemampuan ini.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Membuat versi cutover dari pencapaian garis kontrak integrasi Operasi Proyek peta tulis ganda 

1. Pastikan bahwa pemetaan target untuk **entitas pencapaian** garis kontrak integrasi Operasi Proyek adalah yang terbaru. 

    1. Di Keuangan, buka **entitas** Data Manajemen \>**Data**, dan pilih **entitas tonggak garis** kontrak integrasi Operasi Proyek. 
    2. Pilih **Ubah pemetaan** target. 
    3. **Pada halaman Pementasan peta ke target**, pilih **Buat pemetaan**, lalu konfirmasikan bahwa Anda ingin membuat pemetaan.

2. Hentikan dan refresh **tonggak jalur** kontrak integrasi Operasi Proyek (**msdyn\_ contractlinescheduleofvalues**) peta tulis ganda. 

    1. Buka **Manajemen data** \> **Tulis** ganda, pilih peta, dan buka detailnya. 
    2. Pilih **Berhenti**, dan tunggu hingga sistem menghentikan peta. 
    3. Pilih **Refresh tabel**.

3. Tambahkan pemetaan untuk status transaksi.

    1. Pilih **Tambahkan pemetaan**.
    2. Di baris baru, di kolom Aplikasi keuangan dan operasi, pilih **bidang TRANSSTATUS TRANSSTATUS** **.\[\]**
    3. **Microsoft Dataverse** Di kolom, pilih **status\_ Faktur invoicestatus \[msdyn\]**.
    4. Di **kolom Tipe peta**, pilih panah kanan (**\>**).
    5. Dalam kotak dialog yang muncul, di **bidang Arah** sinkronisasi, pilih **Dataverse ke aplikasi** Keuangan dan Operasi.
    6. Pilih **Tambahkan transformasi**.
    7. Di **bidang Transformasi tipe**, pilih **ValueMap**.
    8. Pilih **Tambahkan pemetaan** nilai.
    9. Di bidang kiri, masukkan **4**. Di bidang kanan, masukkan **192350001**. 
    10. Pilih **Simpan**, lalu tutup kotak dialog.

4. Pilih **Simpan sebagai** untuk menyimpan versi peta tulis ganda. 
5. Di **panel Tambahkan tabel**, di **bidang Penerbit**, pilih **Penerbit** default.
6. Di **bidang Versi**, masukkan versi.
7. Di **bidang Deskripsi**, masukkan catatan tentang versi cutover peta ini. 
8. Pilih **Simpan**.
9. Mulai peta.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Memigrasikan tonggak pencapaian yang ditagih ke Dataverse lingkungan

1. Di lingkungan Operasi Dataverse Proyek, buat tonggak pencapaian yang memiliki status **faktur Siap untuk faktur**. Pada titik ini, jangan migrasikan tonggak pencapaian apa pun yang belum ditagih.

    > [!NOTE]
    > Sebelum Anda memigrasikan tonggak penagihan, pastikan bahwa dimensi keuangan yang terkait dengan garis kontrak proyek ditetapkan seperti yang diharapkan. Dimensi keuangan tidak dapat diedit setelah migrasi selesai.

2. Setelah semua tonggak pencapaian dimigrasikan, hentikan peta tulis ganda berikut:

    - Tonggak jalur kontrak integrasi Operasi Proyek (msdyn\_ contractlinescheduleofvalues)
    - Aktual Integrasi Project Operations (msdyn\_actuals)
    - Proposal faktur proyek V2 (faktur)

    Untuk menghentikan peta, ikuti langkah-langkah berikut:

    1. Di Keuangan, buka **Manajemen** \> **data Tulis ganda**, pilih peta, dan buka detailnya.
    2. Pilih **Berhenti**, dan tunggu hingga sistem menghentikan peta.

3. Di lingkungan Operasi Dataverse Proyek, buat dan konfirmasi faktur pro-forma untuk tonggak penagihan. 

    1. Di peta situs, buka kontrak proyek, pilih kontrak, lalu pilih **Buat faktur**.
    2. Setelah faktur dibuat, buka dari menu **Faktur** di peta situs, lalu pilih **Konfirmasi**.

    Langkah ini membuat catatan yang diperlukan di Dataverse lingkungan. Namun, hal itu tidak mempengaruhi keuangan dan piutang, karena peta tulis ganda yang tercantum sebelumnya dihentikan.

4. Setelah semua faktur pro-forma dikonfirmasi, kembalikan semua peta tulis ganda ke keadaan awal.

    1. Perbarui versi **tonggak garis** kontrak integrasi Operasi Proyek (**msdyn\_ contractlinescheduleofvalues**) peta tulis ganda kembali ke aslinya. 
    2. Pilih peta tulis ganda di daftar peta, pilih **Versi peta tabel**, lalu pilih versi asli peta tabel.
    3. Pilih **Simpan**.
    4. Mulai ulang peta tulis ganda berikut:

        - Tonggak jalur kontrak integrasi Operasi Proyek (msdyn\_ contractlinescheduleofvalues)
        - Aktual Integrasi Project Operations (msdyn\_actuals)
        - Proposal faktur proyek V2 (faktur)

Tonggak sejarah sekarang dimigrasikan, dan sistem siap untuk langkah selanjutnya dalam aktivitas cutover.
