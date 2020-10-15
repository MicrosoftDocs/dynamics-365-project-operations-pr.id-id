---
title: Menerapkan konfigurasi demo dan data konfigurasi
description: Topik ini menyediakan informasi tentang cara menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948917"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Menerapkan konfigurasi demo dan data konfigurasi untuk penyebaran Project Operations Lite -menangani faktur proforma

_**Penyebaran sederhana - menangani faktur proforma_

1. Unduh [paket data induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Arahkan ke folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* dan Jalankan file eksekusi, *DataMigrationUtility*.
3. Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. Di Halaman 2 CMT Wizard, pilih **Office 365** sebagai **jenis penyebaran**.
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

- Mata uang
- Unit Organisasi
- Kontak
- Grup pajak
- Grup Pelanggan
- Unit
- Grup Unit
- Daftar Harga
- Daftar Harga Parameter Proyek
- Frekuensi Faktur
- Rincian Frekuensi Faktur
- Kategori Sumber Daya yang Dapat Dipesan
- Kategori Transaksi
- Kategori Pengeluaran
- Harga Peran
- Harga Kategori Transaksi
- Karakteristik
- Sumber Daya Dapat Dipesan
- Keterkaitan Kategori Sumber Daya yang Dapat Dipesan
- Karakteristik Sumber Daya yang Dapat Dipesan

![Impor Selesai](./media/6CompleteImport.png)
