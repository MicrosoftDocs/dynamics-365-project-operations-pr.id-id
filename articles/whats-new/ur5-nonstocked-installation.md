---
title: Perbarui Project Operations di lingkungan Finance Anda
description: Artikel ini memberikan informasi tentang cara memperbarui Project Operations di lingkungan Dynamics 365 Finance Anda.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030039"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Perbarui Project Operations di lingkungan Finance Anda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Artikel ini memberikan informasi tentang cara memperbarui Dynamics 365 Project Operations di lingkungan Dynamics 365 Finance Anda. Ada tiga prosedur yang diperlukan untuk memperbarui Project Operations untuk Pembaruan 5 (UR5):

- [Impor paket ke proyek pratinjau](#import)
- [Terapkan pembaruan](#apply)
- [Perbarui lingkungan Dataverse Anda](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Impor paket ke proyek LCS Anda

1. Masuk ke [Lifecycle Services (LCS)](https://lcs.dynamics.com/) sebagai Pemilik Proyek atau manajer Lingkungan.
2. Dari daftar proyek, pilih proyek LCS Anda.
3. Pada halaman **Proyek**, dalam grup **Lingkungan**, buka lingkungan yang akan diperbarui.
4. Pastikan lingkungan berjalan. Jika belum dimulai, mulai lingkungan.
5. Di bagian **Rilis baru** dalam **Pembaruan yang tersedia**, pilih **Lihat pembaruan** untuk 10.0.15.

![tombol Lihat pembaruan.](media/view-update.png)

6. Pada halaman **pembaruan biner**, pilih **Simpan paket**.
7. Pada halaman **Tinjau dan simpan pembaruan**, pilih **Simpan paket**.
8. Pada panel **Simpan paket ke pustaka aset** yang terbuka, masukkan nama paket, lalu pilih **Simpan paket**.
9. Setelah LCS selesai menyimpan paket, tombol **Selesai** diaktifkan. Pilih **Selesai**. LCS akan memverifikasi paket. Verifikasi dapat berlangsung selama beberapa menit atau hingga satu jam.


## <a name="apply-the-package-update"></a><a name="apply"></a>Terapkan pembaruan paket

1. Di LCS, pada halaman **rincian Lingkungan**, pilih **Pertahankan** > **Terapkan Pembaruan**.
2. Dari daftar, pilih paket yang Anda simpan sebelumnya, lalu pilih **Terapkan**.
3. Pilih **Ya** untuk mengkonfirmasikan bahwa Anda ingin menyebarkan paket.

![Kotak dialog Konfirmasikan penyebaran paket.](media/confirm-package-deployment.png)

4. Pilih **Ya** untuk mengkonfirmasikan bahwa Anda ingin memperbarui aplikasi.

![Kotak dialog Konfirmasikan pembaruan aplikasi.](media/confirm-application-update.png)

Penyebaran dan pembaruan aplikasi akan dimulai. 

Pada halaman **rincian Lingkungan**, di sudut kanan atas, status lingkungan akan diperbarui ke **Pelayanan**. Dalam waktu sekitar dua jam, pembaruan akan selesai. Informasi rilis aplikasi akan diperbarui ke **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** dan status lingkungan akan diperbarui ke **Disebarkan**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Perbarui lingkungan Dataverse Anda

1. Masuk ke [pusat admin Power Platform](https://admin.powerplatform.com/).
2. Dalam daftar, cari dan buka lingkungan yang digunakan untuk menginstal Project Operations.
3. Pada halaman **Lingkungan**, pilih **Sumber Daya** > **aplikasi Dynamics 365**.
4. Dalam daftar, cari **Microsoft Dynamics 365 Project Operations**, dan di kolom **Status**, pilih **Tersedia Pembaruan**.
5. Pilih kotak centang **Saya menyetujui ketentuan layanan**, lalu pilih **Perbarui**. Versi terbaru solusi akan diinstal.

Setelah penginstalan selesai, Anda akan memiliki versi yang 4.5.0.134 diinstal.

## <a name="configure-new-features"></a>Mengonfigurasi fitur baru

### <a name="enable-dual-write-mapping"></a>Aktifkan pemetaan Tulis Ganda

Setelah menyelesaikan pembaruan Finance dan lingkungan Dataverse, Anda dapat mengaktifkan pemetaan penulisan gandasar yang diperlukan. Selesaikan prosedur berikut ini untuk mengaktifkan pemetaan tulis ganda.

- [Memperbarui pengaturan keamanan di lingkungan Customer Engagement](#security)
- [Segarkan entitas data](#refresh)
- [Memperbarui dan menjalankan pemetaan penulisan ganda](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Memperbarui pengaturan keamanan di lingkungan Dataverse

Pembaruan berikut pada hak istimewa keamanan entitas diperlukan sebagai bagian dari pembaruan UR5.

1. Di lingkungan Dataverse Anda, buka **Pengaturan**, dan di grup **Sistem**, pilih **Keamanan**.

![Pengaturan Lingkungan Dataverse.](media/Picture21.png)

2. Pilih **Peran Keamanan**.
3. Dari daftar peran, pilih **pengguna aplikasi penulisan ganda** dan pilih tab **Entitas Kustom**. 
4. Pastikan peran memiliki izin **Baca** dan **Lampirkan ke** untuk:

      - **Jenis Nilai Tukar Mata Uang**
      - **Bagan Akun** 
      - **Kalender Fiskal** 
      - **Buku besar**

5. Setelah peran keamanan diperbarui, buka **Pengaturan** > **Keamanan** > **Tim**. Pastikan peran **pengguna aplikasi penulisan ganda** telah diterapkan ke tim. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>segarkan entitas data dari pembaruan

1. Di lingkungan Finance, buka ruang kerja **manajemen Data**, lalu buka halaman **parameter Kerangka Kerja**.
2. Pada tab **Pengaturan entitas**, pilih **Segarkan daftar entitas**.
3. Pilih **Tutup** untuk mengkonfirmasi penyegaran entitas.

 > [!NOTE]
 > Proses ini akan berlangsung kira-kira 20 menit untuk diselesaikan. Anda akan diberi tahu setelah pembaruan selesai.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Perbarui pemetaan Tulis Ganda

1. Di ruang kerja **manajemen Data**, pilih **Tulis ganda**.
2. Pilih **Terapkan solusi**, pilih kedua solusi dalam daftar, lalu pilih **Terapkan**.
3. Pada halaman **Tulis ganda**, pilih peta tabel berikut, lalu pilih **Berhenti**.

    - **Aktual Integrasi Project Operations (msdyn_actuals)**
    - **Kategori pengeluaran proyek integrasi Project Operations (msdyn_expensecategories)**
    - **entitas ekspor pengeluaran proyek aktual integrasi Project Operations (msdyn_expenses)**

4. Pada halaman **versi peta tabel**, terapkan versi baru peta untuk masing-masing dari ketiga entitas.
5. Pada halaman **Penulisan ganda**, pilih jalankan untuk memulai ulang peta.
6. Dari daftar peta, pilih peta **buku besar (msdyn_ledgers)** dengan semua prasyarat dan pilih kotak centang **Sinkronisasi awal**. 
7. Di bidang **Induk untuk sinkronisasi awal**, pilih **aplikasi keuangan dan operasi**, lalu pilih **Jalankan**.
 
 ![Sinkronisasi peta buku besar.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]