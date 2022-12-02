---
title: Membuat dan mengonfirmasi jurnal entri
description: artikel ini menyediakan informasi tentang cara membuat dan mengonfirmasikan jurnal entri di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912336"
---
# <a name="create-and-confirm-entry-journals"></a>Membuat dan mengonfirmasi jurnal entri

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda menggunakan rekaman harian Entri untuk merekam aktual secara langsung di Microsoft Dynamics 365 Project Operations. Saat menggunakan rekaman harian Entri, Anda tidak perlu memasukkan log penggunaan Waktu, Pengeluaran, dan bahan di Project Operations.

Satu jurnal Entri memungkinkan Anda membuat beberapa baris jurnal. Bila jurnal dikonfirmasi, maka baris jurnal entri akan merekam aktual untuk rincian berikut:

- Biaya atau pendapatan, tergantung pada jenis transaksi yang dipilih.
- Kelas transaksi yang dipilih. Kelas yang tersedia adalah **Waktu**, **Pengeluaran**, **Bahan**, **Panjar**, **Tahapan**, dan **Pajak**.
- Proyek dan/atau tugas yang dipilih di baris jurnal.

Ikuti langkah-langkah berikut untuk membuat jurnal Entri dalam Project Operations.

1. Buka **Penjualan** \> **Transaksi** \> **jurnal**.
2. Pada halaman daftar **jurnal entri**, pada Panel Tindakan, pilih **Baru** untuk membuat sebuah jurnal.
3. Pada halaman **Jurnal baru** pada bidang **Deskripsi**, masukkan deskripsi untuk jurnal.
4. Pastikan bahwa bidang **Jenis Jurnal** diatur ke **Entri**, dan kemudian pilih **Simpan**. Setelah jurnal Entri baru disimpan, tab **Baris Jurnal** seharusnya muncul pada halaman jurnal.
5. Pada tab **Baris jurnal**, pada toolbar di atas kisi, pilih **Baru** untuk membuat baris jurnal Entri.
6. Di kotak dialog **Buat cepat** untuk membuat baris jurnal entri, atur bidang seperti dijelaskan dalam tabel berikut.

    | Bidang | Description | Dampak Fungsional |
    | --- | --- | --- |
    | Kelas Transaksi | Baris jurnal dapat diklasifikasi ke dalam salah satu dari enam kelas transaksi: **Waktu**, **Pengeluaran**, **Bahan**, **Panjar**, **Tahapan**, atau **Pajak**. | Kelas transaksi **pajak** telah tidak digunakan lagi di Project Operations. <br> Jika Anda membuat kelas transaksi **Pajak**, maka kelas tersebut tidak akan diproses dengan faktur atau dalam perhitungan biaya atau pendapatan. **Tahapan** adalah kelas transaksi hanya pendapatan. <br>Kelas **transaksi Panjar** menunjukkan uang muka yang diterima dari pelanggan. Buku harus selalu dibuat sebagai pasangan dari baris jurnal penjualan yang ditagih dan penjualan yang belum ditagih. |
    | Jenis Transaksi | Jenis transaksi **Biaya**, **Penjualan Interorg**, dan **biaya unit sumber daya** harus digunakan untuk merekam biaya.<br> Jenis transaksi **Penjualan Belum Tertagih** dan **Penjualan Ditagih** harus digunakan untuk merekam pendapatan. | Kelas transaksi **Panjar** hanya berfungsi dengan jenis transaksi **Penjualan Belum Tertagih** dan **Penjualan Ditagih**.<br> Kelas transaksi **tahapan** hanya berfungsi dengan jenis transaksi **Penjualan Ditagih**. <br>Jenis **transaksi biaya unit sumber daya** dan **Penjualan interorg** berlaku hanya untuk kelas transaksi **Waktu** dan ini hanya tersedia di jurnal Entri dalam skenario penyebaran Lite dan bukan ketika menyebarkan Project Operations dalam skenario Sumber Daya/Non persediaan. |
    | Pilih Produk | Bila kelas transaksi **Bahan** dipilih, bidang ini memungkinkan Anda menentukan apakah transaksi bahan yang Anda buat dengan baris jurnal adalah produk yang ada atau produk pilihan. | Jika Anda memilih **produk pilihan**, Anda dapat memasukkan nama produk. |
    | Produk | Referensi ke produk dari katalog. | |
    | Description | Deskripsi baris jurnal untuk membantu memudahkan identifikasi. | Untuk baris jurnal penjualan yang belum tertagih, nilainya akan digunakan sebagai deskripsi saat rincian baris faktur dibuat. |
    | Deskripsi Eksternal | Deskripsi baris jurnal yang dapat digunakan untuk berbagi dengan pemangku kepentingan eksternal. | Untuk baris jurnal penjualan yang belum tertagih, nilainya akan digunakan sebagai deskripsi eksternal saat rincian baris faktur dibuat. Faktur yang dikirim ke pelanggan juga dapat ditampilkan. |
    | Jenis Penagihan | Nilai yang menunjukkan apakah baris jurnal akan dihitung sebagai komponen yang dibebankan, gratis, atau tidak dibebankan pada proyek. | Pada alur biasa, jenis penagihan diambil dari persyaratan yang disetujui dan diatur pada kontrak. Namun, bila Anda merekam baris jurnal, Anda dapat memasukkan nilai di bidang ini. |
    | Tanggal Dokumen | Gunakan tanggal saat transaksi terjadi. | |
    | Tanggal Mulai | Gunakan tanggal saat transaksi terjadi. | Bidang ini digunakan untuk perbandingan dengan tanggal pembuatan faktur untuk transaksi jenis **Penjualan Belum Tertagih**. Perbandingan ini akan membantu Anda menentukan apakah transaksi akan bertanggal di masa mendatang atau di masa lalu. Hanya transaksi bertanggal di masa lalu yang akan ditambahkan ke faktur. |
    | Tanggal Akhir | Gunakan tanggal saat transaksi terjadi. | |
    | Tanggal Akuntansi | Gunakan tanggal saat dampak akuntansi akan direkam. | |
    | Pelanggan Baris Kontrak | Secara default, jika baris kontrak hanya memiliki satu pelanggan, bidang ini diatur ke pelanggan pada baris kontrak saat baris jurnal disimpan. Jika baris kontrak memiliki beberapa pelanggan, pilih pelanggan yang benar pada baris kontrak. | Jika sistem tidak dapat menentukan pelanggan baris kontrak pada baris jurnal, dan jika kosong pada aktual **jenis Penjualan Belum Tertagih** yang dibuat dari baris jurnal, aktual tidak akan ditagih. |
    | Project | Pilih proyek untuk merekam aktual. | Berdasarkan proyek, kelas transaksi, dan tugas yang dipilih, sistem akan mencoba menentukan kontrak, baris kontrak, dan pelanggan baris kontrak. |
    | Tugas | Pilih tugas untuk merekam aktual. | Jika Anda mengaitkan tugas dengan baris kontrak selama konfigurasi kontrak, sistem akan menggunakan tugas yang dipilih, bersama dengan kelas proyek dan transaksi, untuk menentukan pelanggan kontrak, baris kontrak, dan baris kontrak. |
    | Kategori Transaksi | Pilih kategori transaksi untuk merekam aktual. | Untuk pengeluaran, kategori transaksi yang dipilih menentukan harga default yang akan dimasukkan pada baris jurnal saat disimpan. |
    | Peran | Bidang ini relevan untuk baris jurnal Waktu. Pilih peran sumber daya yang meluangkan waktu pada proyek dan/atau tugas. | Untuk baris jurnal waktu, jika Anda menggunakan konfigurasi siap pakai untuk entri biaya sumber daya default dan tingkat tagihan, peran yang dipilih akan digunakan bersama dengan unit sumber daya untuk menentukan harga default yang akan dimasukkan pada baris jurnal saat disimpan. Jika Anda menggunakan konfigurasi kustom untuk entri harga default, Anda harus memeriksa konfigurasi tersebut untuk menentukan apakah bidang **Peran** digunakan untuk memasukkan nilai harga default. |
    | Subkontrak | Jika baris jurnal mewakili kapasitas subkontrak atau pengeluaran atau bahan yang disubkontrakkan, pilih subkontrak yang relevan. | Bila baris jurnal Biaya dicatat, subkontrak yang dipilih akan menentukan daftar harga yang digunakan untuk memasukkan biaya unit default. |
    | Baris Subkontrak | Jika baris jurnal mewakili kapasitas subkontrak atau pengeluaran atau bahan yang disubkontrakkan, pilih baris subkontrak yang relevan. | Bila baris jurnal biaya direkam, baris subkontrak yang dipilih akan memastikan bahwa perhitungan kapasitas yang tersedia pada baris subkontrak dihitung dengan benar. |
    | Metode Jumlah | Bidang ini diatur ke **Kalikan Kuantitas dengan Harga** secara default. Bila metode ini digunakan, jumlah akan dihitung sebagai *Kuantitas* × *Harga*. Metode lain yang didukung adalah **Harga Tetap**. Bila metode ini digunakan, harga akan diatur ke jumlah dan kuantitas tidak akan digunakan dalam perhitungan. | |
    | Jadwal Unit dan Unit | Bersama-sama, jadwal unit dan unit mengidentifikasi unit kuantitas. | Kombinasi unit dan kategori transaksi digunakan untuk memasukkan harga default untuk pengeluaran. Dalam konfigurasi default Project Operations, kombinasi unit, peran, dan unit sumber daya digunakan untuk memasukkan harga default untuk waktu. Jika Anda memiliki konfigurasi kustom untuk entri harga default, maka akan digunakan bersama dengan unit. Kombinasi produk dan unit digunakan untuk memasukkan harga default untuk bahan. |
    | Jumlah | Masukkan kuantitas. | |
    | Harga | Jika harga dibiarkan kosong saat baris jurnal dibuat, nilai yang relevan akan digunakan untuk memasukkan harga default, tergantung pada kelas transaksi. Jika harga dimasukkan saat baris jurnal dibuat, maka harga tersebut akan digunakan. | |
    | Pajak | Masukkan jumlah pajak. | Tergantung pada jumlah pajak yang dimasukkan, jumlah yang diperluas akan dihitung sebagai *Pajak* + *Jumlah*. |

## <a name="confirm-an-entry-journal"></a>Mengkonfirmasikan jurnal Entri

Setelah Anda memasukkan semua baris jurnal di sebuah jurnal Entri, Anda dapat mengkonfirmasikan jurnal. Proses ini akan merekam setiap baris jurnal sebagai aktual pada proyek yang sesuai.

Setelah jurnal dikonfirmasi, Anda tidak dapat lagi mengeditnya atau salah satu barisnya.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Aktual yang dibuat oleh Konfirmasi jurnal Entri

Ada beberapa perbedaan utama antara aktual yang dibuat oleh konfirmasi jurnal Entri dan aktual yang dibuat selama persetujuan log Waktu, Pengeluaran, dan Penggunaan bahan dan konfirmasi faktur di Project Operations:

- Jurnal harian tidak menggunakan koneksi transaksi untuk menghubungkan biaya aktual dengan aktual penjualan yang belum tertagih. Aktual yang dibuat saat log Waktu, Pengeluaran, dan Penggunaan bahan disetujui selalu menggunakan koneksi transaksi untuk menautkan aktual biaya dan aktual penjualan yang belum tertagih.
- Jurnal harian tidak menggunakan asal transaksi untuk menghubungkan biaya aktual dengan aktual penjualan yang belum tertagih ke rekaman asal. Aktual yang dibuat saat log Waktu, Pengeluaran, dan Penggunaan bahan disetujui selalu menggunakan asal transaksi untuk menautkan aktual biaya dan aktual penjualan yang belum tertagih ke entri waktu asal.
- Bila aktual penjualan belum ditagih yang dibuat oleh konfirmasi jurnal Entri ditagihkan, aktual penjualan ter ditagih yang dibuat selama konfirmasi faktur ditautkan ke aktual penjualan belum tertagih, dengan cara yang sama dengan aktual penjualan belum ditagih yang dibuat saat log Waktu, Pengeluaran, dan penggunaan bahan disetujui.
- Baris jurnal entri yang dibuat selama waktu yang dimasukkan oleh sumber daya antar-organisasional tidak menyebabkan aktual **biaya unit sumber daya** dan jenis **Penjualan Interorg** dibuat secara otomatis. Aklien ini harus dibuat secara manual. Perilaku ini berbeda dengan perilaku entri waktu yang direkam oleh sumber daya antar-organisasional. Dalam hal ini, bila waktu disetujui, aplikasi secara otomatis membuat aktual jenis **Biaya** pada proyek dan aktual **biaya unit sumber daya** danjenis **Penjualan Interorg** pada divisi pemilik karyawan. Selanjutnya, sambungan transaksi akan digunakan untuk menghubungkan aktual tersebut bersama-sama dan asal transaksi untuk menghubungkannya ke entri waktu asal.
- Bila jurnal Entry dikonfirmasi, maka mereka akan membuat aktual. Namun, jurnal koreksi tidak dapat digunakan untuk mengoreksi aktual tersebut. Perilaku ini berbeda dengan perilaku untuk aktual yang dibuat ketika log waktu, pengeluaran, dan penggunaan bahan disetujui. Dalam hal ini, aplikasi ini memungkinkan Anda menggunakan jurnal koreksi untuk mengoreksi aktual agar dapat memperbaiki kesalahan apa pun, asalkan aktual tersebut belum ditagihkan. Jika mereka telah ditagih, Anda tetap dapat mengoreksi aktual jika Anda memproses kredit penuh yang sebenarnya kepada pelanggan.

> [!NOTE]
> Jurnal harian tidak menjalankan aturan default yang tegas. Oleh karena itu, gunakan jurnal entri ini sesedikit mungkin, dan hati-hatilah untuk memastikan Anda tidak membuat data keuangan yang rusak dalam sistem Anda. Bila anda bisa, gunakan log waktu, pengeluaran, dan penggunaan bahan, konfigurasi tahapan, dan panjar pada kontrak proyek, dan proses konfirmasi faktur proyek, bukan entri jurnal untuk membuat aktual.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
