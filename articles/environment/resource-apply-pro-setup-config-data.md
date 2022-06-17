---
title: Pengaturan dan penerapan data konfigurasi di Common Data Service
description: Artikel ini menyediakan informasi tentang menyiapkan dan menerapkan data konfigurasi dalam Operasi Proyek.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2c918425e9a6c5fe8888ed8a4258ca59f0464828
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928022"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Pengaturan dan penerapan data konfigurasi di Common Data Service 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_



## <a name="prerequisites"></a>Prasyarat

Sebelum Anda mulai mengkonfigurasi data dalam Common Data Service (CDS), prasyarat berikut harus dipenuhi:

1.  Menyediakan lingkungan CDS dan lingkungan Dynamics 365 Finance untuk Operasi Proyek.
2.  Informasi badan hukum dari Dynamics 365 Finance dibagikan ke lingkungan CDS. Ini berarti bahwa entitas **perusahaan** dalam CDS memiliki rekaman perusahaan berikut:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Menginstal data pengaturan dan konfigurasi

1. Unduh, buka blokir, dan buka [Paket paket data pengaturan dan konfigurasi](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Arahkan ke folder zip terbuka dan Jalankan file eksekusi, *DataMigrationUtility*.
3. Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.

![Migrasi Konfigurasi.](./media/1ConfigurationMigration.png)

4. Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.
5. Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.
6. Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.

![Masuk untuk konfigurasi.](./media/2ConfigurationSignin.png)

7. Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan pilih **masuk**.
8. Pada halaman 4, pilih file zip, *SampleSetupAndConfigData* dari folder yang telah dibongkar.

![Pilihan file zip.](./media/3ZipFile.png)

![Pilih file.](./media/4SelectAFile.png)

9. Setelah file zip dipilih, pilih **impor data**.

![Impor Data.](./media/5ImportData.png)

10. Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda. Setelah impor selesai, keluar dari Wizard CMT. 
11. Periksa organisasi Anda untuk data dalam 26 entitas berikut:

  - Mata uang
  - Bagan Akun
  - Kalender Fiskal
  - Jenis Nilai Tukar Mata Uang
  - Hari Pembayaran
  - Jadwal Pembayaran
  - Persyaratan Pembayaran
  - Unit Organisasi
  - Kontak
  - Grup pajak
  - Grup Pelanggan
  - Grup Vendor
  - Unit
  - Grup Unit
  - Daftar Harga
  - Daftar Harga Parameter Proyek
  - Frekuensi Faktur
  - Kategori Sumber Daya yang Dapat Dipesan
  - Kategori Transaksi
  - Kategori Pengeluaran
  - Harga Peran
  - Harga Kategori Transaksi
  - Karakteristik
  - Sumber Daya Dapat Dipesan
  - Keterkaitan Kategori Sumber Daya yang Dapat Dipesan
  - Karakteristik Sumber Daya yang Dapat Dipesan

![Impor Selesai.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Memperbarui konfigurasi Project Operations

1. Telusuri ke lingkungan CE. Anda dapat menemukannya dengan membuka [Pusat admin Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih lingkungan, lalu memilih **buka lingkungan**. 

![Buka Lingkungan.](./media/7OpenEnvironment.png)

2. Buka **proyek** > **sumber daya**, lalu pilih **baru** untuk membuat sumber daya yang dapat dipesan untuk pengguna Anda.

![Sumber Daya yang Dapat Dipesan.](./media/8BookableResources.png)

3. Pada tab **Umum**, pilih pengguna admin. Verifikasikan bahwa zona waktu sesuai dengan yang Anda miliki. 

![Sumber Daya Dapat Dipesan Baru.](./media/9NewBookableResource.png)

4. Pada tab **penjadwalan**, di bidang **perusahaan**, pilih perusahaan **USPM**, lalu pilih **Simpan**. 

![Tab Penjadwalan.](./media/10SchedulingTab.png)

5. Pilih tab **Jam kerja**.  

![Jam Kerja.](./media/11WorkHours.png)

6. Klik dua kali pada nilai yang ada di kalender dan pilih **Edit** > **semua aktivitas dalam rangkaian**. 

![Kalender Kerja.](./media/12WorkCalendar.png)

7. Ubah jam kerja menjadi hari kerja selama delapan (8) jam, tandai akhir pekan sebagai hari non-kerja, dan pastikan zona waktu cocok dengan Anda. 
8. Pilih **Simpan dan Tutup**.

![Perbarui Kalender.](./media/13UpdateCalendar.png)

9. Buka **pengaturan** > **template kalender** dan pilih **baru**.
 
 ![Template Kalender.](./media/14CalendarTemplates.png)
 
 10. Masukkan nama, pilih sumber daya template yang Anda buat, lalu pilih **Simpan**. 
 
 ![Simpan Template kalender.](./media/15SaveCalendarTemplate.png)
 
 11. Buka **parameter** dan klik dua kali rekaman. 
 
 ![Parameter Proyek.](./media/16ProjectParameters.png)
 
12. Perbarui bidang berikut:

 - **Perusahaan Default**: USPM
 - **Unit organisasi default**:Aswono Robotics global
 - **Frekuensi faktur**: hari ketujuh dan terakhir
 - **Template jam kerja**: Ubah ke template yang Anda buat.

13. Pilih **Simpan**. 

![Pembaruan Parameter Proyek.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
