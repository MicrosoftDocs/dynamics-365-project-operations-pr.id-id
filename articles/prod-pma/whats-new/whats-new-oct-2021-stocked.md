---
title: Yang baru atau diubah di Project Operations, Oktober 2021 untuk skenario berbasis stok/produksi
description: Artikel ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis oktober 2021 penyebaran Project Operations Lite untuk skenario berbasis produksi/stok.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029947"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Yang baru atau diubah di Project Operations, Oktober 2021 untuk skenario berbasis stok/produksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.22
 
## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
|--------------|------------------|----------------|
| Manajemen proyek dan akuntansi | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Jumlah pendapatan yang masih harus dibayar dan pekerjaan proyek (WIP) tidak dibalik dengan benar saat faktur pelanggan antarperusahaan diposting. |
| Manajemen proyek dan akuntansi | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Fungsi **Cegah penutupan proyek jika ada transaksi terbuka** tidak berfungsi. |
| Manajemen proyek dan akuntansi | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Pengelompokan penagihan pada faktur teks bebas tidak secara otomatis mengisi dimensi dari proyek saat fungsi diaktifkan. |
| Manajemen proyek dan akuntansi | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Dalam skenario antarperusahaan, Jumlah pendapatan yang masih harus dibayar dan pekerjaan proyek (WIP) tidak dibalik dengan benar saat faktur proyek diposting. |
| Manajemen proyek dan akuntansi | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Nilai debit dan kredit beralih bila add-in Microsoft Excel digunakan dengan jurnal pengeluaran proyek dan bidang **jenis akun Offset** diatur ke **proyek**. |
| Manajemen proyek dan akuntansi | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Jumlah yang diposting dalam transaksi proyek berlebihan pada pesanan pembelian proyek yang mencakup item persediaan dan yang memiliki jumlah pajak yang tidak bisa dikurangkan ketika **UseTax** ditandai. |
| Manajemen proyek dan akuntansi | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem memecah jumlah antara laporan laba dan rugi proyek dan laporan WIP proyek. |
| Manajemen proyek dan akuntansi | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventaris di tangan salah setelah persyaratan item yang dikembalikan sebagian disesuaikan. |
| Manajemen proyek dan akuntansi | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nama sumber daya diduplikasikan dalam Project Operations saat diedit di Microsoft Project. |
| Manajemen proyek dan akuntansi | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Laporan pengeluaran antarperusahaan yang memiliki biaya faktur vendor tertunda antarperusahaan piutang dagang pertama kali diposting ke jenis posting **biaya WIP Proyek**. Namun, selama pemrosesan, biaya terkait perkiraan diposting ke jenis posting **biaya Proyek**, bukan jenis posting **biaya antarperusahaan** yang diharapkan. |
| Manajemen proyek dan akuntansi | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Panjar Vendor menyebabkan transaksi pengeluaran proyek tidak ditampilkan. |
| Manajemen proyek dan akuntansi | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Lembar waktu harus mengumpulkan jumlah transaksi dalam mata uang transaksi ke angka tempat desimal yang ditentukan pada semua distribusi akuntansi dan entri jurnal umum. |
| Manajemen proyek dan akuntansi | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Kuantitas persyaratan item proyek secara otomatis diperbarui saat pesanan terencana ditegaskan. |
| Manajemen proyek dan akuntansi | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Nomor voucher, jenis transaksi saldo vendor, dan nomor akun tidak dapat dibalik pada faktur pembayaran di muka pesanan pembelian. |
| Manajemen proyek dan akuntansi | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktur vendor antarperusahaan rusak saat integrasi faktur vendor diaktifkan. |
| Manajemen proyek dan akuntansi | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Saat Anda membuat jurnal pengeluaran proyek, jumlah biaya ditampilkan di bidang **Kredit**. |
| Manajemen proyek dan akuntansi | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Persyaratan pembayaran pada faktur proyek tidak berfungsi sebagaimana yang diharapkan. |
| Manajemen proyek dan akuntansi | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Voucher lembar waktu dapat digunakan kembali bila urutan nomor diatur sebagai kontinu. |
| Manajemen proyek dan akuntansi | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PRANCIS: Logika **jumlah penyimpanan** manual tidak sesuai dengan logika jumlah **penyimpanan otomatis** di proposal faktur kontrak proyek. |
| Manajemen proyek dan akuntansi | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Saat penyimpanan vendor dirilis, posting voucher memiliki baris tambahan yang salah. |
| Manajemen proyek dan akuntansi | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ketika bidang **tanggal faktur** di halaman **Buat proposal faktur** diubah, kesalahan berikut mungkin terjadi: "Referensi objek tidak diatur ke instans objek." |
| Manajemen proyek dan akuntansi | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Kesalahan terjadi saat Anda mencoba menyetujui lembar waktu dari alur kerja **TSLine**, dan ada kebijakan lembar waktu untuk Sabtu dan Ahad. |
| Manajemen proyek dan akuntansi | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Jenis item proyek keseimbangan awal tidak termasuk dalam **ringkasan transaksi proposal faktur** saat total faktur proposal faktur dihitung. |
| Manajemen proyek dan akuntansi | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Jika biaya pemakaian untuk pesanan produksi proyek adalah 0 (nol), kesalahan berikut terjadi saat Anda mencoba memperkirakan: "Mencoba membagi dengan nol". |
| Manajemen proyek dan akuntansi | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikasi seluler Project Timesheet untuk Android berhenti merespons. Masalah ini terkait dengan **TimeEntryDataManager ArgumentNull Database**. |
| Manajemen proyek dan akuntansi | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Jurnal integrasi Project Operations gagal diposting ketika Anda mempostingnya, karena akun tidak memiliki dimensi. Namun, akun yang tidak memiliki dimensi tersebut bukan akun yang Anda posting. |
| Manajemen proyek dan akuntansi | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filter **ToDate** dalam pencarian tidak dikosongkan saat filter dihapus dari kotak dialog **Pilih** pada halaman **posting Biaya**. |
| Manajemen proyek dan akuntansi | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Atur ulang semua distribusi** gagal dan menampilkan kesalahan untuk lembar waktu yang dibuat untuk proyek jenis **Hanya Waktu**. |
| Manajemen proyek dan akuntansi | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Proyek** tidak dapat diedit pada faktur vendor tertunda jika kategori pengadaan ditetapkan ke item. |
| Manajemen proyek dan akuntansi | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panel navigasi tidak ada jika Anda tidak masuk ke Project Operations Dataverse. |
| Manajemen proyek dan akuntansi | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Untuk transaksi penyesuaian proyek antarperusahaan, ada masalah di perusahaan tujuan. |
| Manajemen proyek dan akuntansi | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Biaya komitmen proyek menghitung kuantitas dan harga biaya yang salah jika pesanan pembelian diproses oleh **proses akhir tahun pesanan Pembelian** di buku besar umum. |
| Manajemen proyek dan akuntansi | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ketika pesanan produksi proyek yang memiliki pesanan kualitas dilaporkan sebagai selesai, kesalahan berikut terjadi: "Tidak ada transaksi virtual yang ditandai dengan transaksi inventaris." |
| Manajemen proyek dan akuntansi | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Ketika faktur biaya Akun yang terkait dengan proyek dikirim, kesalahan berikut terjadi: "Teks Enumerasi Proyek - biaya - item tidak ada." |
| Manajemen proyek dan akuntansi | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Biaya tidak langsung akan meningkat dua kali lipat bila Anda memperoleh pendapatan secara manual. |
| Manajemen proyek dan akuntansi | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Pendapatan yang masih harus diperoleh dan posting WIP tidak menghasilkan transaksi. |
| Manajemen proyek dan akuntansi | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivasi harga tertunda gagal untuk item biaya standar ketika pesanan pembelian proyek yang diterima ada. |
| Manajemen proyek dan akuntansi | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai WIP yang dikembalikan dari posting faktur berbeda dengan nilai WIP asli yang diposting dari entri waktu. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ada masalah posting dengan pendapatan tertagih proyek dalam kasus panjar diterapkan di mana Transaksi voucher tidak seimbang. |
| Manajemen proyek dan akuntansi | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Pembuatan perkiraan setelah proposal faktur diposting memblok impor baris koreksi di Project Operations. |
| Manajemen proyek dan akuntansi | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modifikasi rekaman tahapan yang ditagih penuh tidak boleh dilakukan. |
| Manajemen proyek dan akuntansi | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Bila tagihan otomatis digunakan, faktur pelanggan antarperusahaan untuk lembar waktu tidak dapat diposting, dan pesan kesalahan ditampilkan. |
| Manajemen proyek dan akuntansi | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamat pada subproyek tidak diperbarui dengan benar. |
| Manajemen proyek dan akuntansi | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Harga biaya pada persyaratan item diperbarui dengan harga pembelian untuk pesanan pembelian terkonsolidasi. |
| Manajemen proyek dan akuntansi | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Biaya yang diposting tidak benar setelah harga pembelian diperbarui dan parameter **Mengaktifkan manajemen perubahan** diaktifkan. |
| Perjalanan dan Pengeluaran | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua pengeluaran pengguna dapat dilihat saat Anda mencari kategori dalam aplikasi seluler Expense. |
| Perjalanan dan Pengeluaran | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Kesalahan Jumlah transaksi vendor dan transaksi pajak penjualan diposting dari pengeluaran yang dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Pesan Peringatan yang tidak relevan ditampilkan saat Anda me-refresh halaman laporan Pengeluaran. |
| Perjalanan dan Pengeluaran | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pemberi izin interim yang salah digunakan saat Anda menghapus pemberi izin interim, lalu mengirimkan ulang melalui alur kerja. |
| Perjalanan dan Pengeluaran | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Terjadi kesalahan terkait konfigurasi jarak tempuh. |
| Perjalanan dan Pengeluaran | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribusi tidak memperbarui entitas hukum ketika transaksi yang tidak dilampirkan ditambahkan kembali ke laporan pengeluaran pada pengeluaran antarperusahaan. |

### <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan wajib untuk aplikasi keuangan dan operasi, lihat [pembaruan wajib](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan alat pencarian masalah untuk melihat pembaruan peraturan yang telah direncanakan. Pencarian Masalah memungkinkan Anda mencari berdasarkan negara atau kawasan, jenis fitur, dan rilis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
