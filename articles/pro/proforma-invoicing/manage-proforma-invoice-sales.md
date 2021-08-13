---
title: Mengelola faktur proyek proforma
description: Laporan topik memberikan informasi tentang bagaimana bekerja dengan faktur proyek proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f14cf9d5ee25247500180081b8f407ee311db481a5ef5eac330e75d45baba54a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997430"
---
# <a name="manage-a-proforma-project-invoice"></a>Mengelola faktur proyek proforma 

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Dynamics 365 Project Operations, faktur proforma dibuat sebagai perpanjangan faktur di Dynamics 365 Sales. Namun, ada banyak perbedaan dalam proses faktur antara Sales dan Project Operations ketika menyangkut faktur. Misalnya, Anda tidak dapat membuat faktur baru dari halaman **daftar faktur** dalam Project Operations, namun dimungkinkan melakukannya di Sales. Perbedaan dan ekstensi ini tersedia untuk mendukung proses faktur untuk proyek yang berbeda dari faktur tipikal untuk perintah penjualan.

> [!IMPORTANT]
> Karena perbedaan ini, jangan gunakan faktur di Sales dan Project Operations secara bergantian.

## <a name="invoice-header"></a>Header faktur

Informasi berikut tersedia di header proforma faktur dalam Project Operations.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| **ID faktur** | tab **Ringkasan** | ID yang otomatis dibuat bila faktur proforma dibuat. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini digunakan sebagai referensi untuk setiap faktur proforma. |
| **Nama** | tab **Ringkasan** | Atur ke nama kontrak proyek secara default. Bidang ini dapat diedit oleh pengguna. | &nbsp;  |
| **Mata Uang** | tab **Ringkasan** | Atur ke mata uang kontrak proyek secara default. Bidang hanya baca yang terkunci dari pengeditan. |&nbsp; |
| **Daftar harga** | tab **Ringkasan** | Atur ke daftar harga kontrak proyek secara default. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Peluang** | tab **Ringkasan** | Referensi ke peluang yang ditautkan. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp;  |
| **Kontrak** | tab **Ringkasan** | Referensi ke kontrak proyek yang ditautkan. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Pelanggan** | tab **Ringkasan** | Referensi ke kontrak proyek yang ditautkan. Bidang hanya baca yang terkunci dari pengeditan. |&nbsp;  |
| **Keterangan** | tab **Ringkasan** | Bidang teks yang menjelaskan faktur. Bidang ini dapat diedit oleh pengguna. | &nbsp; |
| **Tagih ke** dan bidang terkait | **tab Ringkasan** | Default diatur dari pelanggan kontrak proyek. Bidang ini dapat diedit oleh pengguna.  | &nbsp; |
| **Status** | tab **Ringkasan** | Mengatur pilihan berikut: **aktif**, **tertutup**, **berbayar**, dan **dibatalkan**, serta dapat diedit oleh pengguna. | Status tidak didukung untuk Project Operations mencakup **ditutup** dan **dibatalkan**. </br> Status diatur ke **aktif** saat faktur dibuat. </br>Status harus ditetapkan ke **dibayar** hanya setelah faktur dikonfirmasi. |
| **Status Faktur Proyek** | tab **Ringkasan** | Mengatur pilihan berikut: **Draf**, **Sedang ditinjau**, dan **Dikonfirmasi**, serta dapat diedit oleh pengguna. | Di status **draf** dan **sedang ditinjau**, faktur dapat diedit. Faktur tidak dapat diedit setelah dikonfirmasi. |
| **Jumlah Detail** | tab **Ringkasan** | Jumlah nilai pada semua baris faktur setelah uang muka dan pengurangan. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini digunakan untuk menghitung jumlah akhir. |
| **diskon (%)** | tab **Ringkasan** | Bidang ini dapat diedit untuk memasukkan persentase diskon. Bidang ini tidak didukung oleh fungsi Project Operations. | Bidang ini tidak didukung. |
| **Jumlah Diskon** | tab **Ringkasan** | Bidang ini dapat diedit untuk memasukkan jumlah diskon. Bidang ini tidak didukung oleh fungsi Project Operations. | Bidang ini tidak didukung. |
| **jumlah biaya pra-pengangkutan** | **tab Ringkasan** | Jumlah total faktur setelah diskon diterapkan. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini digunakan untuk menghitung jumlah akhir. |
| **Jumlah Pengangkutan** | tab **Ringkasan** | Bidang ini dapat diedit untuk memasukkan jumlah pengangkutan. Bidang ini tidak didukung oleh fungsi Project Operations. | Bidang ini tidak didukung. |
| **Total Pajak** | tab **Ringkasan** | Pajak total dari semua baris faktur pada faktur. Bidang hanya baca yang terkunci dari pengeditan. | Tidak ada. |
| **Jumlah Total** | tab **Ringkasan** | Jumlah dari nilai setelah diskon dan pajak. | Jumlahnya adalah nilai yang harus dibayar pelanggan. |
## <a name="project-based-invoice-lines"></a>Baris faktur berbasis proyek

Dalam Project Operations, selalu ada satu baris faktur untuk setiap baris kontrak proyek. Baris faktur dibuat meskipun tidak ada aktual. Informasi berikut tersedia di baris faktur proforma.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| **ID faktur** | Tab **umum** | Referensi ke ID faktur. Bidang hanya baca yang terkunci dari pengeditan. | Tautan ID faktur dapat digunakan untuk menavigasi kembali ke header faktur. |
| **Nama** | Tab **umum** | Nama baris faktur ditetapkan secara default dari nama baris kontrak. Bidang ini dapat diedit oleh pengguna. | &nbsp; |
| **Project** | Tab **umum** | Proyek pada baris kontrak proyek terkait. Bidang hanya baca yang terkunci dari pengeditan. | Tautan proyek dapat digunakan untuk menavigasi ke proyek. |
| **Metode Penagihan** | Tab **umum** | Metode penagihan pada baris kontrak proyek terkait. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Jumlah Baris Kontrak** | Tab **umum** | Nilai kontrak pada baris kontrak proyek terkait. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Ditagih Hingga Sekarang** | Tab **umum** | Jumlah nilai pada semua rincian baris faktur dari faktur ini. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Jumlah** | Tab **umum** | Jumlah nilai pada semua rincian baris faktur kena biaya dari faktur ini. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini digunakan untuk menghitung jumlah akhir pada header faktur. |
| **Pajak** | Tab **umum** | Jumlah nilai pajak pada semua rincian baris faktur dari baris faktur ini. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini digunakan untuk menghitung jumlah pajak akhir pada header faktur. |
| **Jumlah Kelipatan** | Tab **umum** | Jumlah nilai total (**pajak + nilai**) pada semua rincian baris faktur kena biaya dari baris faktur ini. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini digunakan untuk menghitung jumlah akhir pada header faktur. |


## <a name="invoice-line-details"></a>Detail Baris Faktur

Setiap baris faktur dalam faktur proyek mencakup rincian baris faktur. Rincian baris ini terkait dengan aktual penjualan belum ditagih dan tonggak pencapaian yang terkait dengan baris kontrak yang dirujuk oleh baris faktur. Semua transaksi ini ditandai **siap untuk faktur**.

Untuk baris **Faktur Waktu dan Bahan**, rincian baris faktur dikelompokkan ke dalam **Dikenakan Biaya**, **Tidak Kena Biaya**, dan **Gratis** pada halaman **Baris Faktur**. Rincian **baris faktur kena biaya** menghasilkan jumlah total baris faktur. **Aktual Tidak Kena Biaya** dan **Gratis** tidak akan ditambahkan ke total baris faktur.

Untuk baris **Faktur Harga Tetap**, rincian baris faktur dibuat dari tahapan yang ditandai sebagai **Siap untuk faktur** pada baris kontrak terkait. Setelah detail baris faktur dibuat dari tonggak pencapaian, status penagihan pada tonggak pencapaian diperbarui ke **faktur pelanggan dibuat**.

### <a name="edit-invoice-line-details"></a>Edit Rincian Baris Faktur

Bidang berikut tersedia pada detail baris faktur yang didukung oleh aktual penjualan yang belum ditagih:

| Bidang | KETERANGAN | Dampak hilir |
| --- | --- | --- |
| **Baris Faktur** | Referensi ke **ID Baris faktur**. Bidang Hanya Baca, dikunci untuk pengeditan. | Tautan ini dapat digunakan untuk menavigasi kembali ke header faktur. |
| **Keterangan** | Keterangan rincian baris Faktur. Diatur secara default dari bidang **komentar internal** pada **entri waktu**, dan dari bidang **Deskripsi** pada **entri pengeluaran**. Bidang ini dapat diedit oleh pengguna.| &nbsp; |
| **Deskripsi Eksternal** | Keterangan rincian baris Faktur. Diatur secara default dari bidang **komentar eksternal** pada **entri waktu**, dan bidang **Deskripsi** pada **entri pengeluaran**. Bidang ini dapat diedit oleh pengguna. | Deskripsi ini dapat digunakan untuk menentukan jenis faktur tercetak yang akan dikirim kepada pelanggan. Dalam Project Operations, faktur proforma tidak memiliki semua fungsi yang diperlukan untuk mengkonfigurasi pengaturan cetak untuk faktur. |
| **Tanggal Mulai** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh aktual sumber. |
| **Project** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Diatur secara default ke proyek di baris kontrak terkait. |
| **Tugas** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh aktual sumber. Daftar drop-down menampilkan semua tugas yang terkait dengan baris kontrak proyek terkait.  |
| **Kategori Transaksi** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh sumber aktual. |
| **Peran** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh aktual sumber. |
| **Sumber Daya Dapat Dipesan** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh sumber aktual. |
| **Unit Sumber Daya** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh aktual sumber. |
| **Kuantitas** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh aktual sumber. |
| **Jadwal Unit** | Untuk detail baris faktur untuk waktu, hal ini selalu diatur ke waktu dan tidak dapat diedit. Untuk pengeluaran, ini diatur secara default dari aktual pengeluaran sumber. Bidang hanya baca yang terkunci dari pengeditan. | Ditetapkan secara default ke **waktu** pada detail baris faktur baru yang tidak didukung oleh aktual. |
| **Unit** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh aktual sumber |
| **Harga** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Bidang ini dapat diedit pada detail baris faktur baru yang tidak didukung oleh aktual sumber. Jika nilai tidak dimasukkan, maka akan diatur secara default setelah **Simpan**. |
| **Mata Uang** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Diatur secara default dari header faktur saat membuat detail faktur baru tanpa dukungan aktual.  Bidang hanya baca yang terkunci dari pengeditan. |
| **Jumlah** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Dihitung sebagai **kuantitas \* harga** saat membuat detail faktur baru tanpa aktual pendukung. Hal ini dihitung setelah **Simpan**. Bidang hanya baca yang terkunci dari pengeditan. |
| **Pajak** | Ditetapkan secara default dari aktual sumber. Bidang ini dapat diedit oleh pengguna | Bidang dapat diedit oleh pengguna saat membuat detail baris faktur baru tanpa aktual pendukung. |
| **Jumlah Kelipatan** | Bidang hitung dihitung sebagai **jumlah + pajak**. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Jenis Penagihan** | Ditetapkan secara default dari aktual sumber. Bidang ini dapat diedit oleh pengguna. | Memilih **Kena biaya** menambahkan baris ke total baris faktur. **Gratis** dan **tidak dikenakan biaya** akan mengecualikannya dari total baris faktur. |
| **Pilih Produk** | Diatur secara default dari aktual sumber, bidang ini hanya bisa dibaca. | Bila Anda membuat detail baris faktur baru tanpa mendukung aktual, bidang ini dapat diedit. |
| **Produk** | Diatur secara default dari aktual sumber, bidang ini hanya bisa dibaca. | Bila Anda membuat detail baris faktur baru tanpa mendukung aktual, bidang ini dapat diedit jika bidang **Pilih Produk** diatur ke **produk yang ada**. |
| **Nama Produk** | Diatur secara default dari aktual sumber, bidang ini hanya bisa dibaca. | Pada detail baris faktur baru, dengan ID produk dipilih dari katalog, bidang ini diatur ke nama produk. Untuk produk pilihan, bidang diatur ke tulis nama. |
| **Tulis Deskripsi** | Diatur secara default dari aktual sumber, bidang ini hanya bisa dibaca. | Bila Anda membuat detail baris faktur baru tanpa mendukung aktual, Anda dapat menambahkan penulisan dalam deskripsi untuk produk. |
| **Jenis Transaksi** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Diatur secara default ke **penjualan yang ditagih** dan dikunci saat membuat **detail baris faktur baru** tanpa aktual pendukung.  |
| **Kelas Transaksi** | Ditetapkan secara default dari aktual sumber. Bidang hanya baca yang terkunci dari pengeditan. | Diatur secara default berdasarkan apakah pengguna memilih untuk membuat detail baris faktur **Waktu**, **Pengeluaran**, **Bahan**, atau **Ongkos** sekaligus membuat **detail baris Faktur** baru tanpa bantuan aktual. Dikunci dari pengeditan. |

Bidang berikut tersedia pada detail baris faktur yang didukung oleh tonggak pencapaian:

| Bidang | KETERANGAN | Dampak hilir |
| --- | --- | --- |
| **Baris Faktur** | Referensi ke **ID Baris faktur**. Bidang hanya baca yang terkunci dari pengeditan. | Tautan ini dapat digunakan untuk menavigasi kembali ke header faktur. |
| **Keterangan** | Keterangan rincian baris Faktur. Diatur secara default dari deskripsi tonggak pencapaian sumber. | &nbsp; |
|**Deskripsi Eksternal** | Deskripsi detail baris faktur yang diatur secara default dari deskripsi tonggak pencapaian sumber. | Bidang ini dapat digunakan untuk menentukan jenis faktur tercetak yang akan dikirim kepada pelanggan. Faktur proforma dalam Project Operations tidak memiliki semua fungsi yang diperlukan untuk mengkonfigurasi pengaturan cetak untuk faktur. |
| **Tanggal Mulai** | Ditetapkan secara default dari tanggal **tonggak pencapaian** pada tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Project** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Tugas** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Kategori Transaksi** | Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Peran** | Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Sumber Daya Dapat Dipesan** | Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Unit Sumber Daya** | Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Jadwal Unit** | Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Unit** | Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Harga** | Diatur secara default dari jumlah di tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Mata Uang** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. |&nbsp; |
| **Jumlah** | Diatur secara default dari jumlah di tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Pajak** | Diatur secara default dari jumlah pajak di tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Jumlah Kelipatan** | Diatur secara default dari jumlah kelipatan di tonggak pencapaian sumber. Bidang ini dapat diedit oleh pengguna | &nbsp; |
| **Jenis Penagihan** | Selalu diatur secara default ke **Kena biaya**. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Jenis Transaksi** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |
| **Kelas Transaksi** | Ditetapkan secara default dari tonggak pencapaian sumber. Bidang hanya baca yang terkunci dari pengeditan. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Buat Detail Baris Faktur baru

Pada baris faktur waktu dan material, Anda dapat membuat rincian baris faktur baru. Rincian baris faktur ini tidak didukung oleh aktual. Pada baris faktur waktu dan material Anda dapat memilih **baru** untuk membuat rincian baris faktur baru untuk kelas transaksi yang disertakan pada baris kontrak.

## <a name="refresh-invoice-transactions"></a>Segarkan Transaksi Faktur

Jika Anda memiliki aktual yang masuk setelah faktur dibuat, Anda dapat menyertakan aktual ini pada faktur.

1. Pada **tampilan akumulasi penagihan**, tandai data sebagai **siap untuk faktur**.   
2. Buka faktur proforma dan, pada **tindakan** pita, klik **Segarkan transaksi baris faktur**.

  Hal ini membuat rincian baris faktur untuk setiap aktual yang tanggalnya terlewat dan ditandai sebagai **siap faktur**; namun tidak termasuk dalam faktur.

## <a name="product-based-invoice-lines"></a>Baris faktur berbasis produk

Di Project Operations, Anda dapat membuat baris faktur untuk produk yang tidak berlaku untuk setiap proyek atau untuk semua proyek bersama-sama dengan baris faktur berbasis proyek. Baris faktur ini dibuat sebagai baris kontrak berbasis produk dan setelah ditandai sebagai siap faktur, mereka ditambahkan sebagai baris faktur berbasis produk.

Setelah menambahkan baris faktur berbasis produk, mereka tidak dapat diubah. Namun, mereka dapat dihapus dari faktur proforma draf.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
