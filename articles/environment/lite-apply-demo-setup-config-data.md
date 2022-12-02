---
title: Menerapkan konfigurasi demo dan data konfigurasi - lite
description: Artikel ini menyediakan informasi tentang cara menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/07/2022
ms.locfileid: "9409994"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations - lite 

_**Penyebaran sederhana - menangani faktur proforma_



## <a name="prerequisites"></a>Prasyarat

Sebelum Anda memulai konfigurasi, Anda harus memiliki lingkungan Dataverse yang tersedia untuk Dynamics 365 Project Operations.


## <a name="instructions"></a>Petunjuk

1. Unduh [paket data induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Navigasikan ke folder *ProjOpsSampleSetupData - CE hanya CMT* dan jalankan file eksekusi, *DataMigrationUtility*.
3. Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.

    ![Migrasi Konfigurasi.](./media/1ConfigurationMigration.png)

4. Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.
5. Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.
6. Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.

   ![Masuk untuk konfigurasi.](./media/2ConfigurationSignin.png)

7. Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan kemudian pilih **masuk**.
8. Pada halaman 4, pilih file zip, *SampleSetupAndConfigData* dari folder yang tidak dibongkar, *ProjOpsSampleSetupData - CE hanya CMT*.

   ![File Zip.](./media/3ZipFile.png)

   ![Pilih file.](./media/4SelectAFile.png)

9. Setelah file zip dipilih, pilih **impor data**.

   ![Impor Data.](./media/5ImportData.png)

10. Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda. Setelah selesai, keluar dari Wizard CMT. 
11. Periksa organisasi Anda untuk data dalam 18 entitas berikut:

    -   Mata uang
    -   Akun
    -   Unit Organisasi
    -   Kontak
    -   Unit
    -   Grup Unit
    -   Daftar Harga
    -   Daftar Harga Parameter Proyek 
    -   Frekuensi Faktur
    -   Kategori Sumber Daya yang Dapat Dipesan
    -   Kategori Transaksi
    -   Kategori Pengeluaran
    -   Harga Peran
    -   Harga Kategori Transaksi
    -   Karakteristik
    -   Sumber Daya Dapat Dipesan
    -   Keterkaitan Kategori Sumber Daya yang Dapat Dipesan
    -   Karakteristik Sumber Daya yang Dapat Dipesan

    ![Impor Selesai.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
