---
title: Membuat faktur proforma manual
description: Topik ini menyediakan informasi tentang membuat faktur proforma.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3289b8bcaddaebe1a3657b5902c1d324f9e0fd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287782"
---
# <a name="create-a-manual-proforma-invoice"></a>Membuat faktur proforma manual

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Faktur memberikan tingkat persetujuan kepada manajer proyek kedua sebelum membuat faktur untuk pelanggan. Tingkat persetujuan pertama diselesaikan saat entri waktu dan pengeluaran yang diajukan anggota tim proyek disetujui.

Dynamics 365 Project Operations tidak dirancang untuk menghasilkan faktur untuk pelanggan, karena alasan berikut:

- Tidak berisi informasi pajak.
- Tidak dapat mengkonversi mata uang lain ke mata uang faktur dengan menggunakan nilai tukar yang dikonfigurasi dengan benar.
- Tidak dapat memformat faktur dengan benar sehingga dapat dicetak.

Namun, Anda dapat menggunakan sistem keuangan atau akuntansi untuk membuat faktur sisi Pelanggan yang menggunakan informasi dari proposal faktur yang dibuat.

## <a name="creating-project-invoices"></a>Membuat Faktur Proyek

Faktur proyek dapat dibuat satu per satu atau dalam jumlah besar. Anda dapat membuatnya secara manual, atau dapat dikonfigurasi sehingga dibuat dalam jalur otomatis.

### <a name="manually-create-project-invoices"></a>Buat Faktur Proyek secara manual 

Dari halaman daftar **kontrak proyek**, Anda dapat membuat faktur proyek secara terpisah untuk setiap kontrak proyek, atau Anda dapat membuat faktur secara massal untuk beberapa kontrak proyek.

Ikuti langkah ini untuk membuat faktur untuk kontrak proyek tertentu.

- Pada halaman daftar **kontrak proyek**, buka kontrak proyek, lalu pilih **buat faktur**.

    Faktur dibuat untuk semua transaksi untuk kontrak proyek yang dipilih yang memiliki status **siap untuk faktur**. Transaksi ini mencakup waktu, pengeluaran, tonggak waktu, dan baris kontrak berbasis produk.

Ikuti langkah berikut untuk membuat faktur secara massal.

1. Pada halaman daftar **kontrak proyek**, pilih satu atau beberapa kontrak proyek yang harus Anda buat faktur, lalu pilih **buat faktur proyek**.

    Pesan peringatan akan menginformasikan bahwa mungkin ada penundaan sebelum faktur dibuat. Proses ini juga ditampilkan.

2. Pilih **OK** untuk menutup kotak pesan.

    Faktur dibuat untuk semua transaksi di baris kontrak yang memiliki status **siap untuk faktur**. Transaksi ini mencakup waktu, pengeluaran, tonggak waktu, dan baris kontrak berbasis produk.

3. Untuk melihat faktur yang dihasilkan, buka **Sales** \> **Penagihan** \> **Faktur**. Anda akan melihat satu faktur untuk setiap kontrak proyek.

### <a name="set-up-automated-creation-of-project-invoices"></a>Mengkonfigurasi pembuatan faktur proyek secara otomatis 

Ikuti langkah berikut untuk mengkonfigurasi faktur otomatis yang berjalan.

1. Buka **Pengaturan** \> **Pekerjaan bets**.
2. Membuat batch pekerjaan, dan namai **Project operations buat faktur**. Nama pekerjaan batch harus mencakup istilah "Create Invoices".
3. Di bidang **jenis pekerjaan**, pilih **tidak ada**. Secara default, **frekuensi harian** dan opsi **aktif** diatur ke **ya**.
4. Pilih **Jalankan alur kerja**. Di kotak dialog **mencari rekaman**, Anda akan melihat tiga alur kerja:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pilih **ProcessRunCaller** dan kemudian pilih **Tambahkan**.
6. Pilih **OK** di kotak dialog berikutnya. Alur kerja **tidur** diikuti dengan alur kerja **proses**.

    Anda juga dapat memilih **ProcessRunner** di langkah 5. Kemudian, bila Anda memilih **OK**, alur kerja **proses** diikuti dengan alur kerja **tidur**.

Alur kerja **ProcessRunCaller** dan **ProcessRunner** membuat faktur. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** adalah alur kerja yang benar-benar membuat faktur. Ia melalui semua baris kontrak pembuatan faktur, dan membuat faktur untuk baris tersebut. Untuk menentukan baris kontrak yang harus dibuat faktur, pekerjaan akan melihat tanggal faktur berjalan untuk baris kontrak. Jika baris kontrak milik satu kontrak memiliki tanggal yang sama saat menjalankan faktur, transaksi digabungkan menjadi satu faktur yang memiliki dua baris faktur. Jika tidak ada transaksi untuk membuat faktur, pekerjaan akan melompati pembuatan faktur.

Setelah **ProcessRunner** selesai berjalan, maka ia memanggil **ProcessRunCaller**, menyediakan waktu berakhir, dan ditutup. **ProcessRunCaller** kemudian memulai timer yang berjalan selama 24 jam dari waktu berakhir yang ditentukan. Di akhir timer, **ProcessRunCaller** ditutup.

Pekerjaan proses batch untuk membuat faktur adalah pekerjaan berulang. Jika proses batch ini dijalankan berkali-kali, beberapa instans pekerjaan dibuat dan menyebabkan kesalahan. Oleh karena itu, Anda harus memulai proses batch hanya satu kali, dan Anda harus me-restart hanya jika berhenti berjalan.

> [!NOTE]
> Faktur bets hanya berjalan untuk baris kontrak proyek yang dikonfigurasi dengan jadwal faktur. Baris kontrak dengan metode penagihan harga tetap harus mengonfigurasikan tonggak waktu. Baris kontrak proyek dengan metode waktu dan materi penagihan akan memerlukan pengaturan jadwal faktur berdasarkan tanggal. Hal yang sama berlaku untuk baris kontrak berbasis proyek.      
 
### <a name="edit-a-draft-invoice"></a>Mengedit faktur draft

Bila Anda membuat faktur draf proyek, Semua transaksi penjualan yang tidak ditagih yang dibuat saat entri waktu dan pengeluaran disetujui akan ditarik ke faktur. Anda dapat melakukan penyesuaian berikut saat faktur masih dalam tahap draf:

- Hapus atau edit rincian baris faktur.
- Edit dan sesuaikan jenis kuantitas dan penagihan.
- Tambahkan waktu, pengeluaran, dan biaya secara langsung sebagai transaksi pada faktur. Anda dapat menggunakan fitur ini jika baris faktur dipetakan ke baris kontrak yang memungkinkan untuk kelas transaksi ini.

Pilih **konfirmasikan** untuk mengonfirmasi faktur. Tindakan konfirmasi adalah tindakan satu arah. Bila Anda memilih **konfirmasikan**, sistem akan membuat faktur hanya baca dan membuat aktual penjualan yang ditagih dari setiap detail baris faktur untuk setiap baris faktur. Jika detail baris faktur merujuk penjualan yang belum ditagih, sistem juga akan membalikkan penjualan yang belum ditagih. (Detail baris faktur apa pun yang dibuat dari entri waktu atau biaya akan merujuk pada penjualan yang belum ditagih.) Sistem integrasi buku besar dapat menggunakan pembalikan ini untuk membalikkan pekerjaan proyek dalam proses (WIP) untuk tujuan akuntansi.

### <a name="correct-a-confirmed-invoice"></a>Koreksi faktur dikonfirmasi

Faktur yang Dikonfirmasi dapat diedit (dikoreksi). Setelah Anda memperbaiki faktur yang telah dikonfirmasi, faktur draf perbaikan baru akan dibuat. Karena asumsi adalah bahwa Anda ingin membalikkan semua transaksi dan kuantitas dari faktur asli, faktur perbaikan ini mencakup semua transaksi dari faktur asli, dan semua kuantitas di atasnya adalah 0 (nol).

Jika transaksi tidak memerlukan koreksi, Anda dapat menghapusnya dari draf faktur perbaikan. Jika Anda ingin membalikkan atau mengembalikan hanya kuantitas parsial, Anda dapat mengedit bidang **kuantitas** pada detail baris. Jika Anda membuka detail baris faktur, Anda dapat melihat jumlah faktur asli. Selanjutnya, Anda dapat mengedit kuantitas faktur saat ini sehingga lebih kecil atau lebih besar dari kuantitas faktur asli.

Setelah Anda mengonfirmasikan faktur koreksi, aktual penjualan yang belum ditagih asli dibalik, dan aktual penjualan baru yang ditagih dibuat. Jika kuantitas dikurangi, perbedaannya akan menyebabkan penjualan baru yang belum ditagih juga dibuat. Misalnya, jika penjualan tagihan asli selama delapan jam, dan detail baris faktur perbaikan memiliki kuantitas kurang dari enam jam, baris penjualan asli yang ditagih dibalikkan dan dua aktual baru dibuat:

- Penjualan yang ditagih untuk enam jam.
- Tagihan penjualan yang belum ditagih untuk dua jam yang tersisa. Transaksi ini dapat ditagih nanti atau ditandai sebagai tidak dikenakan biaya, tergantung pada negosiasi dengan pelanggan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]