---
title: Membuat dan mengonfirmasi jurnal entri
description: Artikel ini menyediakan informasi tentang cara membuat dan mengonfirmasi jurnal Entri di Microsoft Dynamics 365 Project Operations.
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

Anda menggunakan jurnal Entri untuk merekam aktual secara langsung di Microsoft Dynamics 365 Project Operations. Saat Anda menggunakan jurnal Entri, Anda tidak perlu memasukkan log penggunaan Waktu, Pengeluaran, dan Material di Operasi Proyek.

Satu jurnal Entri memungkinkan Anda membuat beberapa baris jurnal. Ketika jurnal dikonfirmasi, baris jurnal Entri mencatat yang sebenarnya untuk detail berikut:

- Biaya atau pendapatan, tergantung pada jenis transaksi yang dipilih.
- Kelas transaksi yang dipilih. Kelas yang tersedia adalah **Waktu**, **Pengeluaran**, **Material**, **Retainer**, **Milestone**, dan **Pajak**.
- Proyek dan/atau tugas yang dipilih pada baris jurnal.

Ikuti langkah-langkah ini untuk membuat jurnal Entri di Project Operations.

1. **Buka Jurnal** Transaksi \>**Penjualan**.\>**·**
2. **Pada halaman daftar Jurnal** entri, pada Panel Tindakan, pilih **Baru** untuk membuat jurnal.
3. **Pada halaman Jurnal** baru, di **bidang Deskripsi**, masukkan deskripsi jurnal.
4. Pastikan bahwa **bidang Jenis** jurnal diatur ke **Entri**, lalu pilih **Simpan**. Setelah jurnal Entri baru disimpan, **tab baris** Jurnal akan muncul di halaman jurnal.
5. Pada tab **Baris** jurnal, pada toolbar di atas kisi, pilih **Baru** untuk membuat baris Jurnal entri.
6. Dalam kotak **dialog Buat** cepat untuk membuat baris Jurnal entri, atur bidang seperti yang dijelaskan dalam tabel berikut ini.

    | Bidang | Deskripsi | Dampak Fungsional |
    | --- | --- | --- |
    | Kelas Transaksi | Baris jurnal dapat diklasifikasikan ke dalam salah satu dari enam kelas transaksi: **Waktu**, **Beban**, **Material**, **Retainer**, **Milestone**, atau **Pajak**. | Kelas **transaksi Pajak** telah tidak digunakan lagi dalam Operasi Proyek. <br> Jika Anda membuat **kelas transaksi Pajak**, kelas tersebut tidak akan diproses dengan faktur atau dalam perhitungan biaya atau pendapatan. **Milestone** adalah kelas transaksi khusus pendapatan. <br>Kelas **transaksi Retainer** mewakili uang muka yang diterima dari pelanggan. Itu harus selalu dibuat sebagai sepasang penjualan yang ditagih dan jalur jurnal penjualan yang tidak ditagih. |
    | Jenis Transaksi | Jenis **transaksi Biaya**, **Penjualan** Interorg, dan **Sumber Daya unit biaya** harus digunakan untuk mencatat biaya.<br> Jenis **transaksi Penjualan** Yang Tidak Ditagih dan **Penjualan yang Ditagih** harus digunakan untuk mencatat pendapatan. | Kelas **transaksi Retainer** hanya berfungsi dengan **jenis transaksi Unbilled Sales** dan **Billed Sales**.<br> Kelas **transaksi Milestone** hanya berfungsi dengan **jenis transaksi Billed Sales**. <br>Jenis **transaksi biaya** unit Penjualan **dan** Sumber Daya Interorg hanya berlaku untuk **kelas transaksi Waktu** dan ini hanya dapat diterbangkan pada jurnal Entri di scneario penyebaran Lite dan bukan saat menyebarkan Operasi Proyek dalam skenario Sumber Daya / Non stok. |
    | Pilih Produk | **Saat kelas transaksi Material** dipilih, bidang ini memungkinkan Anda menentukan apakah transaksi material yang Anda buat di baris jurnal adalah produk yang sudah ada atau produk tulis-masuk. | Jika Anda memilih **Produk** tulis-masuk, Anda dapat memasukkan nama untuk produk tersebut. |
    | Produk | Referensi ke produk dari katalog. | |
    | Deskripsi | Deskripsi baris jurnal untuk membantu memudahkan identifikasi. | Untuk baris jurnal penjualan yang tidak ditagih, nilainya akan digunakan sebagai deskripsi saat detail baris faktur dibuat. |
    | Deskripsi eksternal | Deskripsi baris jurnal yang dapat digunakan untuk berbagi dengan pemangku kepentingan eksternal. | Untuk baris jurnal penjualan yang tidak ditagih, nilainya akan digunakan sebagai deskripsi eksternal saat detail baris faktur dibuat. Itu juga dapat muncul pada faktur yang dikirim ke pelanggan. |
    | Jenis Penagihan | Nilai yang menunjukkan apakah baris jurnal akan dihitung sebagai komponen yang dikenakan biaya, gratis, atau tidak dikenakan biaya pada proyek. | Dalam alur tipikal, jenis penagihan berasal dari persyaratan yang disepakati yang ditetapkan pada kontrak. Namun, saat Anda merekam baris jurnal, Anda bisa memasukkan nilai di bidang ini. |
    | Tanggal Dokumen | Gunakan tanggal ketika transaksi terjadi. | |
    | Tanggal Mulai | Gunakan tanggal ketika transaksi terjadi. | Bidang ini digunakan untuk perbandingan dengan tanggal pembuatan faktur untuk transaksi jenis **Penjualan Yang Tidak Ditagih**. Perbandingan ini akan membantu Anda memutuskan apakah transaksi tersebut akan datang atau tanggal lalu. Hanya transaksi tanggal lalu yang akan ditambahkan ke faktur. |
    | Tanggal Akhir | Gunakan tanggal ketika transaksi terjadi. | |
    | Tanggal Akuntansi | Gunakan tanggal ketika dampak akuntansi akan dicatat. | |
    | Pelanggan garis kontrak | Secara default, jika garis kontrak hanya memiliki satu pelanggan, bidang ini diatur ke pelanggan pada garis kontrak ketika baris jurnal disimpan. Jika garis kontrak memiliki beberapa pelanggan, pilih pelanggan yang benar di jalur kontrak. | Jika sistem tidak dapat menentukan pelanggan garis kontrak pada baris jurnal, dan jika kosong pada jenis Penjualan **Tidak Ditagih yang sebenarnya** yang dibuat dari baris jurnal, yang sebenarnya tidak akan ditagih. |
    | Project | Pilih proyek untuk merekam aktual aktif. | Berdasarkan proyek yang dipilih, kelas transaksi, dan tugas, sistem akan mencoba menentukan kontrak, garis kontrak, dan pelanggan garis kontrak. |
    | Tugas | Pilih tugas untuk merekam aktual aktif. | Jika Anda mengaitkan tugas dengan jalur kontrak selama penyiapan kontrak, sistem akan menggunakan tugas yang dipilih, bersama dengan kelas proyek dan transaksi, untuk menentukan kontrak, garis kontrak, dan pelanggan garis kontrak. |
    | Kategori Transaksi | Pilih kategori transaksi untuk mencatat aktual aktif. | Untuk pengeluaran, kategori transaksi yang dipilih menentukan harga default yang akan dimasukkan pada baris jurnal saat disimpan. |
    | Peran | Bidang ini relevan dengan garis jurnal Time. Pilih peran sumber daya yang menghabiskan waktu untuk proyek dan/atau tugas. | Untuk baris jurnal Time, jika Anda menggunakan konfigurasi out-of-box untuk entri biaya sumber daya default dan tarif tagihan, peran yang dipilih digunakan bersama dengan unit sumber daya untuk menentukan harga default yang akan dimasukkan pada baris jurnal saat disimpan. Jika Anda menggunakan konfigurasi kustom untuk entri harga default, Anda harus meninjau konfigurasi tersebut **untuk menentukan apakah bidang Peran** digunakan untuk memasukkan nilai harga default. |
    | Subkontrak | Jika baris jurnal mewakili kapasitas yang disubkontrakkan, atau biaya atau materi yang disubkontrakkan, pilih subkontrak yang relevan. | Ketika baris jurnal Cost dicatat, subkontrak yang dipilih akan menentukan daftar harga yang digunakan untuk memasukkan biaya unit default. |
    | Baris subkontrak | Jika baris jurnal mewakili kapasitas yang disubkontrakkan, atau biaya atau materi yang disubkontrakkan, pilih baris subkontrak yang relevan. | Ketika baris jurnal Cost dicatat, baris subkontrak yang dipilih akan memastikan bahwa perhitungan kapasitas yang tersedia pada baris subkontrak dihitung dengan benar. |
    | Metode Jumlah | Secara default, bidang ini diatur ke **Kalikan Kuantitas Menurut Harga**. Ketika metode ini digunakan, jumlahnya akan dihitung sebagai *Kuantitas* × *Harga*. Metode lain yang didukung adalah **Harga** Tetap. Ketika metode ini digunakan, harga akan diatur ke jumlah, dan kuantitas tidak akan digunakan dalam perhitungan. | |
    | Jadwal Unit dan Unit | Bersama-sama, jadwal unit dan unit mengidentifikasi unit kuantitas. | Kombinasi unit dan kategori transaksi digunakan untuk memasukkan harga default untuk pengeluaran. Dalam konfigurasi default Operasi Proyek, kombinasi unit, peran, dan unit sumber daya digunakan untuk memasukkan harga default untuk waktu. Jika Anda memiliki konfigurasi khusus untuk entri harga default, itu akan digunakan bersama dengan unit. Kombinasi produk dan unit digunakan untuk memasukkan harga default untuk bahan. |
    | Jumlah | Masukkan kuantitas. | |
    | Harga | Jika harga dibiarkan kosong saat baris jurnal dibuat, nilai yang relevan akan digunakan untuk memasukkan harga default, tergantung pada kelas transaksi. Jika harga dimasukkan saat baris jurnal dibuat, harga tersebut akan digunakan. | |
    | Pajak | Masukkan jumlah pajak apa pun. | Tergantung pada jumlah pajak yang dimasukkan, jumlah yang diperpanjang akan dihitung sebagai *Jumlah* + *Pajak*. |

## <a name="confirm-an-entry-journal"></a>Konfirmasikan jurnal Entri

Setelah Anda memasukkan semua baris jurnal dalam jurnal Entri, Anda dapat mengonfirmasi jurnal tersebut. Proses ini akan mencatat setiap baris jurnal sebagai aktual pada proyek yang sesuai.

Setelah jurnal dikonfirmasi, Anda tidak dapat lagi mengeditnya atau salah satu barisnya.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Aktual yang dibuat oleh konfirmasi jurnal Entri

Ada beberapa perbedaan utama antara aktual yang dibuat oleh konfirmasi jurnal Entri dan aktual yang dibuat selama persetujuan log penggunaan Waktu, Pengeluaran, dan Material serta konfirmasi faktur dalam Operasi Proyek:

- Jurnal entri tidak menggunakan koneksi transaksi untuk menghubungkan biaya aktual dengan aktual penjualan yang belum ditagih. Aktual yang dibuat ketika waktu, pengeluaran, dan log penggunaan Material disetujui selalu menggunakan koneksi transaksi untuk menghubungkan biaya dan aktual penjualan yang tidak ditagih.
- Jurnal entri tidak menggunakan asal transaksi untuk menghubungkan biaya aktual dan aktual penjualan yang tidak ditagih ke catatan asal mana pun. Aktual yang dibuat ketika log penggunaan Waktu, Pengeluaran, dan Material disetujui selalu menggunakan asal transaksi untuk menghubungkan biaya dan aktual penjualan yang tidak ditagih ke entri waktu asal.
- Ketika aktual penjualan yang tidak ditagih yang dibuat oleh konfirmasi jurnal Entri ditagih, aktual penjualan yang ditagih yang dibuat selama konfirmasi faktur ditautkan ke aktual penjualan yang tidak ditagih, dengan cara yang mirip dengan aktual penjualan yang tidak ditagih yang dibuat ketika waktu, pengeluaran, dan log penggunaan Material disetujui.
- Baris jurnal entri yang dibuat untuk waktu yang dimasukkan oleh sumber daya antar-organisasi tidak menyebabkan aktual **biaya** unit Sumber Daya dan **jenis Penjualan** Interorg dibuat secara otomatis. Aktual ini harus dibuat secara manual. Perilaku ini berbeda dari perilaku untuk entri waktu yang dicatat oleh sumber daya antar-organisasi. Dalam hal ini, ketika waktu disetujui, aplikasi secara otomatis membuat aktual dari **jenis Biaya** pada proyek dan aktual dari **biaya** unit Sumber Daya dan **jenis Penjualan** Interorg pada divisi pemilik karyawan. Kemudian menggunakan koneksi transaksi untuk menghubungkan aktual tersebut bersama-sama dan asal transaksi untuk menghubungkannya ke entri waktu asal.
- Ketika jurnal Entri dikonfirmasi, mereka membuat aktual. Namun, jurnal Koreksi tidak dapat digunakan untuk mengoreksi aktual tersebut. Perilaku ini berbeda dari perilaku untuk aktual yang dibuat ketika waktu, pengeluaran, dan log penggunaan material disetujui. Dalam hal ini, aplikasi ini memungkinkan Anda menggunakan jurnal Koreksi untuk memperbaiki aktual untuk memperbaiki kesalahan apa pun, asalkan aktual tersebut belum ditagih. Jika mereka telah ditagih, Anda masih dapat memperbaiki yang sebenarnya jika Anda memproses kredit penuh yang sebenarnya kepada pelanggan.

> [!NOTE]
> Jurnal entri tidak menerapkan aturan default yang ketat. Oleh karena itu, gunakan Jurnal Entri ini sesedikit mungkin, dan berhati-hatilah dan berhati-hatilah untuk memastikan bahwa Anda tidak membuat data keuangan yang rusak di sistem Anda. Kapan pun Anda bisa, gunakan log penggunaan Waktu, Pengeluaran, dan Material, pengaturan tonggak sejarah dan retainer pada kontrak proyek, dan proses konfirmasi faktur proyek alih-alih jurnal Entri untuk membuat aktual.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
