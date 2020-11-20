---
title: Menerapkan konfigurasi demo dan data konfigurasi - lite
description: Topik ini menyediakan informasi tentang cara menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401267"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations - lite 

_**Penyebaran sederhana - menangani faktur proforma_

## <a name="prerequisites"></a>Prasyarat

Sebelum Anda memulai konfigurasi, Anda harus memiliki lingkungan Common Data Service (CDS) yang tersedia untuk Dynamics 365 Project Operations.


## <a name="instructions"></a>Petunjuk

1. Unduh [paket data induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Arahkan ke folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* dan Jalankan file eksekusi, *DataMigrationUtility*.
3. Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.
5. Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.
6. Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.

![Masuk untuk konfigurasi](./media/2ConfigurationSignin.png)

7. Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan kemudian pilih **masuk**.
8. Pada halaman 4, pilih file zip, *MasterAndSetupData* dari folder yang dibongkar, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![File Zip](./media/3ZipFile.png)

![Pilih file](./media/4SelectAFile.png)

9. Setelah file zip dipilih, pilih **impor data**.

![Impor data](./media/5ImportData.png)

10. Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda. Setelah selesai, keluar dari Wizard CMT. 
11. Periksa organisasi Anda untuk data dalam 20 entitas berikut:

-   Mata uang
-   Akun
-   Unit Organisasi
-   Kontak
-   Grup pajak
-   Grup Pelanggan
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

![Impor Selesai](./media/6CompleteImport.png)
