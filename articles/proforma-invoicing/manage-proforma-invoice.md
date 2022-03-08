---
title: Mengelola faktur berbasis proyek proforma
description: Laporan topik memberikan informasi tentang bagaimana mengelola dan bekerja dengan faktur berbasis proyek proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cba74c14f6d039dce0650f25ee04cbe35ec8f668b774cdaaa3bbf1aab99cb44d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989330"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Mengelola faktur berbasis proyek proforma

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Di Dynamics 365 Project Operations, faktur proforma dibuat sebagai perpanjangan faktur di Dynamics 365 Sales. Namun, ada banyak perbedaan dalam proses faktur antara Sales dan Project Operations ketika menyangkut faktur. Misalnya, Anda tidak dapat membuat faktur baru dari halaman **daftar faktur** dalam Project Operations, namun dimungkinkan melakukannya di Sales. Perbedaan dan ekstensi ini tersedia untuk mendukung proses faktur untuk proyek yang berbeda dari faktur tipikal untuk perintah penjualan.

> [!IMPORTANT]
> Karena perbedaan ini, jangan gunakan faktur di Sales dan Project Operations secara bergantian.

## <a name="invoice-header"></a>Header faktur

Informasi berikut tersedia di header proforma faktur dalam Project Operations.

| Bidang | Lokasi | KETERANGAN |
| --- | --- | --- | 
| **ID Faktur** | tab **Ringkasan** | ID yang otomatis dibuat bila faktur proforma dibuat. Bidang hanya baca yang terkunci dari pengeditan. Bidang ini digunakan sebagai referensi untuk setiap faktur proforma. |
| **Nama** | tab **Ringkasan** | Atur ke nama kontrak proyek secara default. Bidang ini dapat diedit. | 
| **Mata uang** | tab **Ringkasan** | Atur ke mata uang kontrak proyek secara default. Bidang hanya baca yang terkunci dari pengeditan. |
| **Daftar harga** | tab **Ringkasan** | Atur ke daftar harga kontrak proyek secara default. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Peluang** | tab **Ringkasan** | Referensi ke peluang yang ditautkan. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Kontrak** | tab **Ringkasan** | Referensi ke kontrak proyek yang ditautkan. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Pelanggan** | tab **Ringkasan** | Referensi ke kontrak proyek yang ditautkan. Bidang hanya baca yang terkunci dari pengeditan. |
| **Keterangan** | tab **Ringkasan** | Bidang teks yang menjelaskan faktur. Bidang ini dapat diedit. | 
| **Tagih ke** dan bidang terkait | **tab Ringkasan** | Default diatur dari pelanggan kontrak proyek. Bidang ini dapat diedit.  | 
| **Status** | tab **Ringkasan** | Menentukan pilihan berikut: **Aktif**, **Ditutup**, **Dibayar**, dan **Dibatalkan**, serta dapat diedit. Status tidak didukung untuk Project Operations mencakup **ditutup** dan **dibatalkan**. </br> Status diatur ke **aktif** saat faktur dibuat. </br>Status harus ditetapkan ke **dibayar** hanya setelah faktur dikonfirmasi.  | 
| **Status Faktur Proyek** | tab **Ringkasan** | Menentukan pilihan berikut: **Draf**, **Dalam tinjauan**, dan **Terkonfirmasi**, dan dapat diedit. Di status **draf** dan **sedang ditinjau**, faktur dapat diedit. Faktur tidak dapat diedit setelah dikonfirmasi. | 
| **Jumlah Detail** | tab **Ringkasan** | Jumlah nilai pada semua baris faktur setelah uang muka dan pengurangan. Bidang hanya baca yang terkunci dari pengeditan.  Bidang ini digunakan untuk menghitung jumlah akhir. | 
| **diskon (%)** | tab **Ringkasan** | Bidang ini dapat diedit untuk memasukkan persentase diskon. Bidang ini tidak didukung oleh fungsi Project Operations. Bidang ini tidak didukung.|  
| **Jumlah Diskon** | tab **Ringkasan** | Bidang ini dapat diedit untuk memasukkan jumlah diskon. Bidang ini tidak didukung oleh fungsi Project Operations. Bidang ini tidak didukung. |  
| **jumlah biaya pra-pengangkutan** | **tab Ringkasan** | Jumlah total faktur setelah diskon diterapkan. Bidang hanya baca yang terkunci dari pengeditan. Bidang ini digunakan untuk menghitung jumlah akhir.  | 
| **Jumlah Pengangkutan** | tab **Ringkasan** | Bidang ini dapat diedit untuk memasukkan jumlah pengangkutan. Bidang ini tidak didukung oleh fungsi Project Operations. Bidang ini tidak didukung. |
| **Total Pajak** | tab **Ringkasan** | Pajak total dari semua baris faktur pada faktur. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Jumlah Total** | tab **Ringkasan** | Jumlah dari nilai setelah diskon dan pajak. Jumlahnya adalah nilai yang harus dibayar pelanggan. | 

## <a name="project-based-invoice-lines"></a>Baris faktur berbasis proyek

Dalam Project Operations, selalu ada satu baris faktur untuk setiap baris kontrak proyek. Baris faktur dibuat meskipun tidak ada aktual. Informasi berikut tersedia di baris faktur proforma.

| Bidang | Lokasi | KETERANGAN | 
| --- | --- | --- |
| **ID Faktur** | Tab **umum** | Referensi ke ID faktur. Bidang hanya baca yang terkunci dari pengeditan. Tautan ID faktur dapat digunakan untuk menavigasi kembali ke header faktur. | 
| **Nama** | Tab **umum** | Nama baris faktur ditetapkan secara default dari nama baris kontrak. Bidang ini dapat diedit. |
| **Project** | Tab **umum** | Proyek pada baris kontrak proyek terkait. Bidang hanya baca yang terkunci dari pengeditan. Tautan proyek dapat digunakan untuk menavigasi ke proyek. | 
| **Metode Penagihan** | Tab **umum** | Metode penagihan pada baris kontrak proyek terkait. Bidang hanya baca yang terkunci dari pengeditan. |
| **Jumlah Baris Kontrak** | Tab **umum** | Nilai kontrak pada baris kontrak proyek terkait. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Ditagih Hingga Sekarang** | Tab **umum** | Jumlah nilai pada semua rincian baris faktur dari faktur ini. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Jumlah** | Tab **umum** | Jumlah nilai pada semua rincian baris faktur kena biaya dari faktur ini. Bidang hanya baca yang terkunci dari pengeditan. Bidang ini digunakan untuk menghitung jumlah akhir pada header faktur. | 
| **Pajak** | Tab **umum** | Jumlah nilai pajak pada semua rincian baris faktur dari baris faktur ini. Bidang hanya baca yang terkunci dari pengeditan. Bidang ini digunakan untuk menghitung jumlah pajak akhir pada header faktur. | 
| **Jumlah Kelipatan** | Tab **umum** | Jumlah nilai total (**pajak + nilai**) pada semua rincian baris faktur kena biaya dari baris faktur ini. Bidang hanya baca yang terkunci dari pengeditan. Bidang ini digunakan untuk menghitung jumlah akhir pada header faktur. |

## <a name="invoice-line-details"></a>Detail Baris Faktur

Setiap baris faktur dalam faktur proyek mencakup rincian baris faktur. Rincian baris ini terkait dengan aktual penjualan belum ditagih dan tonggak pencapaian yang terkait dengan baris kontrak yang dirujuk oleh baris faktur. Semua transaksi ini ditandai **siap untuk faktur**.

Untuk baris **Faktur Waktu dan Bahan**, rincian baris faktur dikelompokkan ke dalam **Dikenakan Biaya**, **Tidak Kena Biaya**, dan **Gratis** pada halaman **Baris Faktur**. Rincian **baris faktur kena biaya** menghasilkan jumlah total baris faktur. Aktual **gratis** dan **aktual tidak kena biaya** tidak menghasilkan total baris faktur.

Untuk baris **Faktur Harga Tetap**, rincian baris faktur dibuat dari tahapan yang ditandai sebagai **Siap untuk faktur** pada baris kontrak terkait. Setelah detail baris faktur dibuat dari tonggak pencapaian, status penagihan pada tonggak pencapaian diperbarui ke **faktur pelanggan dibuat**.

### <a name="edit-invoice-line-details"></a>Edit Rincian Baris Faktur

Bidang berikut tersedia pada detail baris faktur yang didukung oleh aktual penjualan yang belum ditagih.

| Bidang | KETERANGAN |
| --- | --- | 
| **Baris Faktur** | Referensi ke **ID Baris faktur**. Bidang ini hanya dapat dibaca dan dikunci untuk pengeditan. Tautan ini dapat digunakan untuk menavigasi kembali ke header faktur. | 
| **Keterangan** | Keterangan rincian baris Faktur. Diatur secara default dari bidang **komentar internal** pada **entri waktu**, dan dari bidang **Deskripsi** pada **entri pengeluaran**. Bidang ini dapat diedit.| 
| **Deskripsi Eksternal** | Keterangan rincian baris Faktur. Diatur secara default dari bidang **komentar eksternal** pada **entri waktu**, dan bidang **Deskripsi** pada **entri pengeluaran**. Bidang ini dapat diedit. Deskripsi ini dapat digunakan untuk menentukan jenis faktur tercetak yang akan dikirim kepada pelanggan. Dalam Project Operations, faktur proforma tidak memiliki semua fungsi yang diperlukan untuk mengkonfigurasi pengaturan cetak untuk faktur. | 
| **Tanggal Mulai** | Bidang ini hanya baca yang diatur secara default dari aktual sumber. |
| **Project** | Bidang ini hanya baca yang diatur secara default dari aktual sumber ke proyek pada baris kontrak terkait. |  
| **Tugas** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Kategori Transaksi** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Peran** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |  
| **Sumber Daya yang Dapat Dipesan** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Perusahaan Sumber Daya** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Unit Sumber Daya** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Quantity** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |  
| **Jadwal Unit** | Untuk detail baris faktur untuk waktu, hal ini selalu diatur ke waktu dan tidak dapat diedit. Untuk pengeluaran, ini diatur secara default dari aktual pengeluaran sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Unit** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |  
| **Harga** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Mata uang** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Jumlah** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Pajak** | Ditetapkan secara default dari aktual sumber. Bidang ini dapat diedit.| 
| **Jumlah Kelipatan** | Bidang hitung dihitung sebagai **jumlah + pajak**. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Jenis Penagihan** | Ditetapkan secara default dari aktual sumber. Bidang ini dapat diedit. Memilih **Kena biaya** menambahkan baris ke total baris faktur. **Gratis** dan **tidak dikenakan biaya** akan mengecualikannya dari total baris faktur.| 
| **Pilih Produk** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Produk** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Nama Produk** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |  
| **Tulis Deskripsi** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Jenis Transaksi** | Bidang ini hanya baca yang diatur secara default dari aktual sumber ke **Penjualan Tertagih**. |  
| **Kelas Transaksi** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | 

Bidang berikut tersedia pada detail baris faktur yang didukung oleh tonggak pencapaian.

| Bidang | KETERANGAN |
| --- | --- | 
| **Baris Faktur** | Referensi ke **ID Baris faktur**. Bidang hanya baca yang terkunci dari pengeditan. Tautan ini dapat digunakan untuk menavigasi kembali ke header faktur.  | 
| **Keterangan** | Keterangan rincian baris Faktur. Diatur secara default dari deskripsi tonggak pencapaian sumber. | 
|**Deskripsi Eksternal** | Deskripsi detail baris faktur yang diatur secara default dari deskripsi tonggak pencapaian sumber. Bidang ini dapat digunakan untuk menentukan jenis faktur tercetak yang akan dikirim kepada pelanggan. Faktur proforma dalam Project Operations tidak memiliki semua fungsi yang diperlukan untuk mengkonfigurasi pengaturan cetak untuk faktur. | 
| **Tanggal Mulai** | Ditetapkan secara default dari tanggal **tonggak pencapaian** pada tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Project** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Tugas** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Kategori Transaksi** | Bidang hanya baca yang terkunci dari pengeditan. |
| **Peran** | Bidang hanya baca yang terkunci dari pengeditan. | 
| **Sumber Daya Dapat Dipesan** | Bidang hanya baca yang terkunci dari pengeditan. | 
| **Unit Sumber Daya** | Bidang hanya baca yang terkunci dari pengeditan. | 
| **Jadwal Unit** | Bidang hanya baca yang terkunci dari pengeditan. | 
| **Unit** | Bidang hanya baca yang terkunci dari pengeditan. | 
| **Harga** | Diatur secara default dari jumlah di tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Mata Uang** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Jumlah** | Diatur secara default dari jumlah di tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Pajak** | Diatur secara default dari jumlah pajak di tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. |
| **Jumlah Kelipatan** | Diatur secara default dari jumlah kelipatan di tonggak pencapaian sumber. Bidang ini dapat diedit. | 
| **Jenis Penagihan** | Selalu diatur secara default ke **Kena biaya**. Bidang hanya baca yang terkunci dari pengeditan. |
| **Jenis Transaksi** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | 
| **Kelas Transaksi** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | 

## <a name="refresh-invoice-transactions"></a>Segarkan Transaksi Faktur

Jika Anda memiliki aktual yang masuk setelah faktur dibuat, Anda dapat menyertakan aktual ini pada faktur.

1. Pada **tampilan akumulasi penagihan**, tandai data sebagai **siap untuk faktur**.   
2. Buka faktur proforma draf dan, pada pita **Tindakan**, pilih **Refresh Transaksi Baris Faktur**.

  Rincian baris faktur dibuat untuk aktual yang sebelumnya yang lewat tanggal dan ditandai sebagai **Siap Faktur**, namun tidak tercakup pada faktur.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
