---
title: Memigrasikan tonggak penagihan yang ditagih penuh saat cutover
description: Ini topik menjelaskan cara memigrasikan tonggak penagihan dengan harga tetap yang telah ditagih kepada pelanggan untuk kontrak proyek terbuka sebelum tanggal go-live.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576274"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Memigrasikan tonggak penagihan yang ditagih penuh saat cutover

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

## <a name="scenario"></a>Skenario

Contoso akan ditayangkan dengan Microsoft Dynamics 365 Project Operations untuk skenario sumber daya / non-stok. Sebagai bagian dari kegiatan cutover, tim implementasi harus memigrasikan kontrak proyek terbuka dari sistem lama. Beberapa kontrak proyek termasuk jalur kontrak yang menggunakan metode penagihan harga tetap dan telah ditagih sebagian kepada pelanggan akhir. Tim implementasi harus memigrasikan tonggak penagihan ini saat **faktur Pelanggan diposting**, karena mereka harus dimasukkan dalam total nilai kontrak untuk tujuan pengakuan pendapatan. Namun, saldo pelanggan dalam Piutang dan Buku Besar tidak boleh terpengaruh.

## <a name="solution"></a>Solusi

### <a name="prerequisites"></a>Prasyarat

- Dynamics 365 Finance 10.0.24 atau yang lebih baru harus diinstal.
- Lingkungan di mana langkah-langkah migrasi akan diselesaikan harus dalam mode pemeliharaan. Tidak ada kegiatan lain yang harus dilakukan saat tonggak sedang bermigrasi.
- Langkah-langkah migrasi harus diikuti persis seperti yang dijelaskan di sini dan hanya dapat digunakan untuk aktivitas cutover. Microsoft tidak mendukung penggunaan lain dari kemampuan ini.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Membuat versi cutover dari tonggak garis kontrak integrasi Operasi Proyek peta penulisan ganda 

1. Pastikan bahwa pemetaan target untuk **entitas tonggak garis** kontrak integrasi Operasi Proyek sudah terbaru. 

    1. Di Bidang Keuangan, buka **entitas** Data Management \>**Data**, dan pilih **entitas tonggak garis** kontrak integrasi Operasi Proyek. 
    2. Pilih **Ubah pemetaan** target. 
    3. **Pada halaman Penahapan peta ke target**, pilih **Hasilkan pemetaan**, lalu konfirmasikan bahwa Anda ingin membuat pemetaan.

2. Hentikan dan segarkan **tonggak** garis kontrak integrasi Operasi Proyek (**msdyn\_ contractlinescheduleofvalues**) peta penulisan ganda. 

    1. **Buka Manajemen data** \> **Dual-write**, pilih peta, dan buka detailnya. 
    2. Pilih **Berhenti**, dan tunggu hingga sistem menghentikan peta. 
    3. Pilih **Refresh tabel**.

3. Tambahkan pemetaan untuk status transaksi.

    1. Pilih **Tambahkan pemetaan**.
    2. Pada baris baru, di **kolom aplikasi** Keuangan dan Operasi, pilih **bidang TRANSSTATUS \[TRANSSTATUS\]**.
    3. Di **Microsoft Dataverse** kolom, pilih **msdyn\_ invoicestatus \[Status\]** faktur.
    4. Di **kolom Tipe** peta, pilih panah kanan (**\>**).
    5. Dalam kotak dialog yang muncul, di **bidang Sinkronkan arah**, pilih **Dataverse aplikasi Keuangan dan Operasi**.
    6. Pilih **Tambahkan transformasi**.
    7. **Di bidang Ubah tipe**, pilih **ValueMap**.
    8. Pilih **Tambahkan pemetaan** nilai.
    9. Di bidang kiri, masukkan **4**. Di bidang kanan, masukkan **192350001**. 
    10. Pilih **Simpan**, lalu tutup kotak dialog.

4. Pilih **Simpan untuk** menyimpan versi peta dual-write. 
5. **Di panel Tambahkan tabel**, di **bidang Publisher**, pilih **Penayang default**.
6. Di **bidang Versi**, masukkan versi.
7. Di **bidang Deskripsi**, masukkan catatan tentang versi cutover peta ini. 
8. Pilih **Simpan**.
9. Mulai peta.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Memigrasikan tonggak yang ditagih ke Dataverse lingkungan

1. Di lingkungan Operasi Dataverse Proyek, buat tonggak sejarah yang memiliki status **faktur Siap untuk faktur**. Pada titik ini, jangan memigrasikan tonggak apa pun yang belum ditagih.

    > [!NOTE]
    > Sebelum Anda memigrasikan tonggak penagihan, pastikan bahwa dimensi keuangan yang terkait dengan garis kontrak proyek ditetapkan seperti yang diharapkan. Dimensi keuangan tidak dapat diedit setelah migrasi selesai.

2. Setelah semua tonggak dimigrasikan, hentikan peta tulis ganda berikut:

    - Tonggak garis kontrak integrasi Operasi Proyek (msdyn\_ contractlinescheduleofvalues)
    - Aktual Integrasi Project Operations (msdyn\_actuals)
    - Proposal faktur proyek V2 (faktur)

    Untuk menghentikan peta, ikuti langkah-langkah berikut:

    1. Di Bidang Keuangan, buka **Manajemen data** \> **Dual-write**, pilih peta, dan buka detailnya.
    2. Pilih **Berhenti**, dan tunggu hingga sistem menghentikan peta.

3. Di lingkungan Operasi Dataverse Proyek, buat dan konfirmasikan faktur pro-forma untuk pencapaian penagihan. 

    1. Di peta situs, buka kontrak proyek, pilih kontrak, lalu pilih **Buat faktur**.
    2. Setelah faktur dibuat, buka dari **menu Faktur** di peta situs, lalu pilih **Konfirmasi**.

    Langkah ini membuat catatan yang diperlukan di Dataverse lingkungan. Namun, itu tidak mempengaruhi keuangan dan piutang, karena peta dual-write yang terdaftar sebelumnya dihentikan.

4. Setelah semua faktur pro-forma dikonfirmasi, kembalikan semua peta dual-write ke keadaan awal mereka.

    1. Perbarui versi **tonggak** garis kontrak integrasi Operasi Proyek (**msdyn\_ contractlinescheduleofvalues**) peta tulis ganda kembali ke aslinya. 
    2. Pilih peta tulis ganda dalam daftar peta, pilih **Versi peta tabel**, lalu pilih versi asli peta tabel.
    3. Pilih **Simpan**.
    4. Mulai ulang peta dual-write berikut:

        - Tonggak garis kontrak integrasi Operasi Proyek (msdyn\_ contractlinescheduleofvalues)
        - Aktual Integrasi Project Operations (msdyn\_actuals)
        - Proposal faktur proyek V2 (faktur)

Tonggak sejarah sekarang dimigrasikan, dan sistem siap untuk langkah selanjutnya dalam aktivitas cutover.
