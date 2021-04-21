---
title: Faktur proyek proforma
description: Laporan topik memberikan informasi tentang faktur proyek di Project Operations.
author: rumant
manager: Annbe
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d08e2b0422a991aa4c98ae5d1e0f60aa0eb9daa6
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867180"
---
# <a name="proforma-project-pnvoices"></a>Faktur proyek proforma

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur proyek proforma memberikan tingkat persetujuan kepada manajer proyek kedua sebelum membuat faktur untuk pelanggan. Tingkat persetujuan pertama diselesaikan saat entri waktu, pengeluaran, dan bahan yang diajukan anggota tim proyek disetujui.

Penyebaran Dynamics 365 Project Operations Lite tidak dirancang untuk menghasilkan faktur sisi pelanggan. Daftar berikut ini menunjukkan mengapa faktur tidak dapat dibuat:

- Tidak berisi informasi pajak.
- Tidak dapat mengkonversi mata uang lain ke mata uang faktur.
- Tidak dapat memformat faktur untuk dicetak dengan benar.

Namun, Anda dapat menggunakan sistem keuangan atau akuntansi untuk membuat faktur sisi Pelanggan yang menggunakan informasi dalam proposal faktur yang dihasilkan.

## <a name="creating-project-invoices"></a>Membuat Faktur Proyek

Faktur proyek dapat dibuat satu per satu atau dalam jumlah besar. Anda dapat membuatnya secara manual, atau dapat dikonfigurasi sehingga dibuat dalam jalur otomatis.

### <a name="manually-create-project-invoices"></a>Buat Faktur Proyek secara manual 

Di halaman daftar **kontrak proyek**, Anda dapat membuat faktur proyek secara terpisah untuk setiap kontrak proyek, atau Anda dapat membuat faktur secara massal untuk beberapa kontrak proyek.

   - Untuk membuat faktur untuk kontrak proyek spesifik, di halaman daftar **kontrak proyek**, buka kontrak proyek, lalu pilih **buat faktur**.

   Faktur dibuat untuk semua transaksi untuk kontrak proyek yang dipilih yang memiliki status **siap untuk faktur**. Transaksi ini mencakup waktu, pengeluaran, bahan, tonggak prestasi, baris kontrak berbasis produk, dan baris jurnal penjualan belum tertagih lainnya yang mungkin telah dikonfirmasi.

Untuk membuat faktur secara massal:

1. Pada halaman daftar **kontrak proyek**, pilih satu atau beberapa kontrak proyek untuk membuat fakturnya, lalu pilih **buat faktur proyek**.
2. Pesan peringatan akan menginformasikan bahwa mungkin ada penundaan sebelum faktur dibuat. Proses ini juga ditampilkan. Pilih **OK** untuk menutup kotak pesan.

   Faktur dibuat untuk semua transaksi di baris kontrak yang memiliki status **siap untuk faktur**. Transaksi ini mencakup waktu, pengeluaran, bahan, tonggak prestasi, baris kontrak berbasis produk, dan baris jurnal penjualan belum tertagih lainnya yang mungkin telah dikonfirmasi.

3. Lihat faktur yang dihasilkan, dengan membuka **Sales** \> **Penagihan** \> **Faktur**. Anda akan melihat satu faktur untuk setiap kontrak proyek.

### <a name="set-up-automated-creation-of-project-invoices"></a>Mengkonfigurasi pembuatan faktur proyek secara otomatis 

Ikuti langkah berikut untuk mengkonfigurasi faktur otomatis yang berjalan.

1. Buka **Pengaturan** \> **Pekerjaan bets**.
2. Membuat batch pekerjaan, dan namai **Project operations buat faktur**. Nama pekerjaan batch harus mencakup istilah "Create Invoices".
3. Di bidang **jenis pekerjaan**, pilih **tidak ada**. Secara default, **frekuensi harian** dan opsi **aktif** diatur ke **ya**.
4. Pilih **Jalankan alur kerja**. Di kotak dialog **mencari rekaman**, Anda akan melihat alur kerja berikut ini:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pilih **ProcessRunCaller** dan kemudian pilih **Tambahkan**.
6. Pilih **OK** di kotak dialog berikutnya. Alur kerja **tidur** diikuti dengan alur kerja **proses**.

    Anda juga dapat memilih **ProcessRunner** di langkah 5. Kemudian, bila Anda memilih **OK**, alur kerja **proses** diikuti dengan alur kerja **tidur**.

Alur kerja **ProcessRunCaller** dan **ProcessRunner** membuat faktur. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** adalah alur kerja yang membuat faktur. Alur kerja ini melalui semua baris kontrak pembuatan faktur, dan membuat fakturnya. Untuk menentukan baris kontrak yang harus dibuat faktur, alur kerja akan melihat tanggal faktur berjalan untuk baris kontrak. Jika baris kontrak milik satu kontrak memiliki tanggal yang sama saat menjalankan faktur, transaksi digabungkan menjadi satu faktur yang memiliki dua baris faktur. Jika tidak ada transaksi untuk membuat faktur, tidak ada faktur yang dibuat.

Setelah **ProcessRunner** selesai berjalan, maka ia memanggil **ProcessRunCaller**, menyediakan waktu berakhir, dan ditutup. **ProcessRunCaller** kemudian memulai timer yang berjalan selama 24 jam dari waktu berakhir yang ditentukan. Di akhir timer, **ProcessRunCaller** ditutup.

Pekerjaan proses batch untuk membuat faktur adalah pekerjaan berulang. Jika proses batch ini dijalankan berkali-kali, beberapa instans pekerjaan dibuat dan dapat menyebabkan kesalahan. Untuk mengatasi masalah ini, mulai proses batch hanya satu kali, dan cukup restart jika berhenti berjalan.

> [!NOTE]
> Faktur bets hanya berjalan untuk baris kontrak proyek yang dikonfigurasi dengan jadwal faktur. Baris kontrak dengan metode penagihan harga tetap harus mengonfigurasikan tonggak waktu. Baris kontrak proyek dengan metode waktu dan materi penagihan akan memerlukan pengaturan jadwal faktur berdasarkan tanggal. Hal yang sama berlaku untuk baris kontrak berbasis proyek.      
 
### <a name="edit-a-draft-invoice"></a>Mengedit faktur draft

Bila Anda membuat faktur draf proyek, Semua transaksi penjualan yang tidak ditagih yang dibuat saat entri waktu dan pengeluaran disetujui akan ditarik ke faktur. Anda dapat melakukan penyesuaian berikut saat faktur masih dalam tahap draf:

- Hapus atau edit rincian baris faktur.
- Edit dan sesuaikan jenis kuantitas dan penagihan.
- Tambahkan waktu, pengeluaran, bahan, dan biaya secara langsung sebagai transaksi pada faktur. Anda dapat menggunakan fitur ini jika baris faktur dipetakan ke baris kontrak yang memungkinkan untuk kelas transaksi ini.

Pilih **konfirmasikan** untuk mengonfirmasi faktur. Tindakan ini adalah tindakan satu arah. Bila Anda memilih **konfirmasikan**, faktur menjadi hanya baca dan membuat aktual penjualan yang ditagih dari setiap detail baris faktur untuk setiap baris faktur. Jika detail baris faktur merujuk penjualan yang belum ditagih, aktual penjualan belum tertagih dibalik. Setiap detail baris faktur yang dibuat dari entri penggunaan waktu, pengeluaran, atau bahan akan mereferensikan aktual penjualan belum tertagih. Sistem integrasi buku besar dapat menggunakan pembalikan ini untuk membalikkan pekerjaan dalam proses proyek (WIP) untuk keperluan akuntansi.

### <a name="correct-a-confirmed-invoice"></a>Koreksi faktur dikonfirmasi

Faktur yang Dikonfirmasi dapat diedit. Setelah Anda memperbaiki faktur yang telah dikonfirmasi, faktur draf perbaikan baru akan dibuat. Karena asumsi adalah bahwa Anda ingin membalikkan semua transaksi dan kuantitas dari faktur asli, faktur perbaikan ini mencakup semua transaksi dari faktur asli, dan semua kuantitas di atasnya adalah nol.

Jika ada transaksi yang tidak memerlukan koreksi, Anda dapat menghapusnya dari draf faktur perbaikan. Jika Anda ingin membalikkan atau mengembalikan hanya kuantitas parsial, Anda dapat mengedit bidang **kuantitas** pada detail baris. Jika Anda membuka detail baris faktur, Anda dapat melihat jumlah faktur asli. Selanjutnya, Anda dapat mengedit kuantitas faktur saat ini sehingga lebih kecil atau lebih besar dari kuantitas faktur asli.

Setelah Anda mengonfirmasikan faktur koreksi, aktual penjualan yang belum ditagih asli dibalik, dan aktual penjualan baru yang ditagih dibuat. Jika kuantitas dikurangi, perbedaannya akan menyebabkan penjualan baru yang belum ditagih dibuat. Misalnya, jika penjualan tagihan asli selama delapan jam, dan detail baris faktur perbaikan memiliki kuantitas kurang dari enam jam, baris penjualan asli yang ditagih dibalikkan dan dua aktual baru dibuat:

- Penjualan yang ditagih untuk enam jam.
- Tagihan penjualan yang belum ditagih untuk dua jam yang tersisa. Transaksi ini dapat ditagih nanti atau ditandai sebagai tidak dikenakan biaya, tergantung pada negosiasi dengan pelanggan.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
