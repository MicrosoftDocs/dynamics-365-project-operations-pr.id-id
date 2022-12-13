---
title: Penyesuaian proyek
description: Artikel ini menyediakan informasi tentang penyesuaian proyek.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788367"
---
# <a name="project-adjustments"></a>Penyesuaian proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

## <a name="adjustments-overview"></a>Gambaran umum penyesuaian

Anda dapat mengkonfigurasi Microsoft Dynamics 365 Project Operations sehingga pengguna dapat membuat perubahan pada transaksi yang diposting. Anda dapat menyesuaikan transaksi proyek satu per satu, atau Anda dapat memilih beberapa transaksi sekaligus dalam daftar semua transaksi proyek. Penyesuaian proyek digunakan, misalnya, untuk memperbarui status yang dapat ditagih secara massal, menghitung ulang biaya setelah perubahan konfigurasi, atau memperbarui sumber pendanaan.

Pengguna dapat mengakses fungsi penyesuaian proyek dengan beberapa cara:

- Dengan menggunakan **halaman transaksi** Adjust yang dapat diakses dari **Project Management dan accounting** \> **Setup**.
- Dengan menggunakan **tombol Adjustment** pada **halaman Posted project transactions** yang dapat diakses dari **Project Management dan accounting** \> **Transactions**.
- Dengan menggunakan **tombol Penyesuaian** pada **halaman Transaksi** proyek yang diposting dalam konteks proyek. Halaman ini dapat diakses dari **Manajemen Proyek dan akuntansi** \> **Semua proyek**.

Untuk memungkinkan penyesuaian, Anda harus mengaktifkan satu atau beberapa status transaksi dari **Manajemen Proyek dan Manajemen Proyek akuntansi dan paramater** \> **akuntansi** pada tab Umum **di** bawah bagian **Izinkan penyesuaian status** transaksi. Contoh status transaksi termasuk transaksi yang diposting, transaksi yang ditagih, atau transaksi yang dihilangkan. Status transaksi apa pun yang diatur ke **Tidak** akan memiliki transaksi dalam status tersebut yang tidak akan muncul dalam proses penyesuaian yang dapat dipilih untuk penyesuaian.

Opsi konfigurasi yang bernama **Selalu buat transaksi** penyesuaian saat ini tersedia di Manajemen proyek dan parameter akuntansi. Anda dapat menonaktifkan opsi ini untuk memperbarui transaksi asli alih-alih membuat transaksi baru selama penyesuaian dalam subset skenario. Telah diumumkan bahwa parameter ini akan tidak digunakan lagi pada 1 Maret 2023. Setelah 1 Maret 2023, sistem akan selalu berperilaku seolah-olah opsi diaktifkan.

## <a name="adjustments-process-flow"></a>Penyesuaian alur proses

Langkah-langkah berikut menunjukkan alur umum untuk penyesuaian pemrosesan.

1.  **Buka halaman Penyesuaian** proyek.
2. Pilih **Pilih** untuk mencari transaksi yang memenuhi kriteria penyesuaian yang diharapkan.
3. Dalam daftar transaksi, pilih semua transaksi atau subset transaksi untuk penyesuaian.
4. Pilih **Sesuaikan**, dan ubah atribut pada baris. Atau, jika nilai ditentukan secara manual selama entri transaksi, Anda dapat memilih untuk memasukkan nilai sistem default.
5. Daftar transaksi dikembalikan, dan tanda centang muncul di **kolom Penyesuaian** tertunda untuk menunjukkan di mana perubahan dilakukan. Setiap penyesuaian yang memiliki perubahan tertunda ditampilkan di bagian bawah halaman. Di sana, Anda dapat membuat perubahan terperinci tambahan di luar apa yang ditampilkan di halaman sebelumnya.
6. Pilih **Posting** untuk memposting transaksi penyesuaian.

Tergantung pada konfigurasi, transaksi baru biasanya dibuat untuk penyesuaian.

- Kolom **Status** Faktur dari transaksi asli diatur ke **Disesuaikan**.
- Transaksi pembalikan dibuat untuk membalikkan transaksi asli, dan **bidang Status** diatur ke **Disesuaikan**.
- Transaksi baru dibuat yang memiliki perubahan yang dibuat selama proses penyesuaian.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Memilih beberapa transaksi proyek yang diposting sekaligus untuk penyesuaian dan catatan kredit

Fitur baru yang diperkenalkan dalam rilis 10.0.30 memungkinkan pemilihan beberapa transaksi untuk penyesuaian sekaligus dari **halaman Transaksi** proyek yang diposting.

Sebelum Anda dapat menggunakan fitur ini, fitur ini harus diaktifkan di sistem Anda. Admin dapat menggunakan **ruang kerja Manajemen** fitur untuk memeriksa status fitur dan mengaktifkannya jika diperlukan.  **Di ruang kerja Manajemen** fitur, cari dan pilih Multi-pilih transaksi proyek yang diposting untuk penyesuaian dan catatan **kredit, lalu pilih** **Aktifkan sekarang**.

Fitur ini memungkinkan fungsionalitas utama berikut:

- Ini dapat diakses dari halaman transaksi yang diposting dalam proyek dengan menggunakan tombol Penyesuaian **yang ada** .
- Ini memungkinkan kontrol pemilihan multi-baris pada **halaman Transaksi** proyek yang diposting. Anda bisa menerapkan filter ke halaman daftar dan memilih catatan Anda sebelum memulai penyesuaian.
- Ini menonaktifkan **tombol Penyesuaian** jika ada satu transaksi yang tidak dapat disesuaikan, atau jika Anda memilih kombinasi catatan kredit dan jurnal bersama-sama alih-alih satu per satu.
- Karena penambahan kontrol pilih multi-baris, **link Biaya** komitmen di pita tidak lagi dinonaktifkan jika beberapa baris dipilih.
- Ini menambahkan pesan peringatan berikut: "Anda telah memilih lebih dari (nomor yang dipilih) catatan untuk penyesuaian. Melanjutkan tindakan ini mungkin memerlukan waktu. Apakah Anda yakin ingin melanjutkan tindakan ini?"

Fitur ini juga menghapus langkah 2 dari alur proses yang telah dijelaskan sebelumnya dalam artikel ini. Oleh karena itu, setiap transaksi yang dipilih sebelum **halaman transaksi** Adjust dibuka akan dimasukkan dalam daftar transaksi untuk penyesuaian. Anda tidak perlu menggunakan **tombol Pilih** untuk mencarinya.

> [!NOTE] 
> Bahkan jika fitur ini dinonaktifkan, Anda masih dapat memilih beberapa rekaman untuk penyesuaian. Namun, hanya satu catatan yang akan *tetap dipilih*, dan **kotak dialog Pilih transaksi** akan muncul segera setelah Anda memilih untuk membuka penyesuaian.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Menyesuaikan status transaksi yang dapat diaktifkan atau dinonaktifkan untuk penyesuaian

Status berikut dapat diaktifkan atau dinonaktifkan pada tab Umum **pada**  **halaman Manajemen proyek dan parameter** akuntansi:

- Di-posting
- Proposal faktur
- Ditagihkan
- Diperkirakan
- Dihilangkan
- Saldo awal (jam)

## <a name="adjustment-parameters"></a>Parameter penyesuaian

Parameter ini tercantum pada halaman Manajemen proyek dan parameter **akuntansi pada**  **tab Umum** di bawah **grup Penyesuaian** dan akan mengubah perilaku tentang bagaimana penyesuaian diproses. 

| Nama Parameter | Description |
|----------------|-------------
| Selalu buat transaksi penyesuaian | Jika parameter ini diaktifkan, proses penyesuaian akan selalu membuat transaksi pembalikan baru dan transaksi baru yang disesuaikan ketika ada dampak keuangan atau pelaporan. Jika parameter dinonaktifkan, proses penyesuaian akan memperbarui transaksi asli alih-alih membuat pembalikan dan transaksi baru untuk skenario seperti pembaruan teks transaksi. |
| Bidang Autoupdate | Jika parameter ini diaktifkan, sistem akan menghitung ulang harga biaya dan harga penjualan. |
| Menggunakan tanggal penyesuaian sebagai proyek baru | Parameter ini digunakan untuk memindahkan transaksi ke periode fiskal masa depan sebelum sistem mendukung fungsi ini. Kami tidak menyarankan Anda menggunakannya, karena ini mengubah tanggal bisnis transaksi dan tidak akan digunakan lagi dalam rilis mendatang. |
| Izinkan aktivitas tertutup | Biasanya, transaksi tidak dapat dibuat untuk aktivitas tertutup. Jika parameter ini diaktifkan, perilaku tersebut akan diganti. Oleh karena itu, penyesuaian dapat dibuat untuk kegiatan tertutup. |
