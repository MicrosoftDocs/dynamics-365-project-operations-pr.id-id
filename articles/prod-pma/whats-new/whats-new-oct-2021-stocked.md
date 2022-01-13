---
title: Apa yang baru atau berubah dalam Operasi Proyek, Oktober 2021 untuk skenario berbasis stok / produksi
description: Ini topik memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Operasi Proyek Oktober 2021 untuk skenario berbasis stok / produksi.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818321"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Apa yang baru atau berubah dalam Operasi Proyek, Oktober 2021 untuk skenario berbasis stok / produksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Topik ini berlaku untuk komponen dan versi Microsoft berikut Dynamics 365 Project Operations:

- Manajemen proyek dan akuntansi dalam lingkungan Dynamics 365 Finance versi 10.0.22
 
## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
|--------------|------------------|----------------|
| Manajemen proyek dan akuntansi | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Pekerjaan proyek dalam proses (WIP) dan jumlah pendapatan yang masih harus dibayar tidak dibalik dengan benar ketika faktur pelanggan antar perusahaan diposting. |
| Manajemen proyek dan akuntansi | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **Mencegah penutupan proyek jika ada fungsi transaksi terbuka tidak** berfungsi. |
| Manajemen proyek dan akuntansi | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikasi penagihan pada faktur teks gratis tidak secara otomatis mengisi dimensi dari proyek saat fungsi tersebut diaktifkan. |
| Manajemen proyek dan akuntansi | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Dalam skenario non-intercompany, WIP dan jumlah pendapatan yang masih harus dibayar tidak dibalik dengan benar ketika faktur proyek diposting. |
| Manajemen proyek dan akuntansi | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Nilai debit dan kredit dialihkan saat add-in Microsoft Excel digunakan dengan jurnal biaya Proyek dan **bidang tipe akun Offset diatur ke** **Proyek**. |
| Manajemen proyek dan akuntansi | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Jumlah yang diposting dalam transaksi proyek dilebih-lebihkan pada pesanan pembelian proyek yang mencakup item yang ditebar dan yang memiliki jumlah pajak yang tidak dapat dikurangkan ketika **UseTax** ditandai. |
| Manajemen proyek dan akuntansi | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem ini membagi jumlah antara laporan laba rugi proyek dan laporan WIP proyek. |
| Manajemen proyek dan akuntansi | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventaris on-hand salah setelah persyaratan item yang dikembalikan sebagian disesuaikan. |
| Manajemen proyek dan akuntansi | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nama sumber daya diduplikasi dalam Operasi Proyek saat diedit di Microsoft Project. |
| Manajemen proyek dan akuntansi | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Laporan biaya antar perusahaan yang memiliki biaya antar perusahaan yang harus dibayar yang tertunda pertama kali diposting ke **jenis posting biaya Wip** Proyek. Namun, selama pemrosesan, biaya terkait perkiraan diposting ke **jenis posting biaya Proyek** alih-alih **jenis posting biaya Intercompany yang** diharapkan. |
| Manajemen proyek dan akuntansi | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Hasil retainase vendor dalam transaksi biaya proyek tidak ditampilkan. |
| Manajemen proyek dan akuntansi | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Lembar waktu harus membulatkan jumlah transaksi dalam mata uang transaksi ke sejumlah tempat desimal tertentu pada semua distribusi akuntansi dan entri alokasi jurnal umum. |
| Manajemen proyek dan akuntansi | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Jumlah persyaratan item proyek secara otomatis diperbarui ketika pesanan yang direncanakan dikukuhkan. |
| Manajemen proyek dan akuntansi | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Nomor voucher, saldo vendor jenis transaksi, dan nomor rekening tidak dapat dibalik pada faktur pembayaran di muka dari pesanan pembelian. |
| Manajemen proyek dan akuntansi | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktur vendor antar komplotany rusak saat integrasi faktur vendor diaktifkan. |
| Manajemen proyek dan akuntansi | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Ketika Anda membuat jurnal biaya Proyek, jumlah biaya ditampilkan di **bidang** Kredit. |
| Manajemen proyek dan akuntansi | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Ketentuan pembayaran pada faktur proyek tidak berfungsi seperti yang diharapkan. |
| Manajemen proyek dan akuntansi | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Voucher lembar waktu dapat digunakan kembali ketika urutan nomor diatur sebagai kontinu. |
| Manajemen proyek dan akuntansi | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PRANCIS: **Logika jumlah retensi** Manual tidak sesuai dengan logika jumlah retensi otomatis dalam proposal faktur kontrak **Proyek**. |
| Manajemen proyek dan akuntansi | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ketika retensi vendor dirilis, posting voucher memiliki baris tambahan yang salah. |
| Manajemen proyek dan akuntansi | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ketika **bidang tanggal Faktur** pada halaman Buat proposal faktur **diubah**, kesalahan berikut mungkin terjadi: "Referensi objek tidak diatur ke contoh objek." |
| Manajemen proyek dan akuntansi | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Kesalahan terjadi ketika Anda mencoba menyetujui lembar waktu dari **alur kerja TSLine,** dan ada kebijakan lembar waktu untuk hari Sabtu dan Minggu. |
| Manajemen proyek dan akuntansi | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Jenis item proyek saldo awal dikecualikan dari **ringkasan transaksi proposal Faktur ketika total faktur proposal faktur** dihitung. |
| Manajemen proyek dan akuntansi | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Jika biaya konsumsi pada pesanan produksi proyek adalah 0 (nol), kesalahan berikut terjadi ketika Anda mencoba memperkirakan: "Berusaha untuk membagi dengan nol." |
| Manajemen proyek dan akuntansi | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikasi Project Timesheet Mobile untuk Android berhenti merespons. Masalah ini terkait dengan **TimeEntryDataManager ArgumentNullException**. |
| Manajemen proyek dan akuntansi | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Jurnal integrasi Operasi Proyek gagal ketika Anda mempostingnya, karena akun kehilangan dimensi. Namun, akun yang kehilangan dimensi bukanlah akun tempat Anda memposting. |
| Manajemen proyek dan akuntansi | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filter **ToDate** dalam pencarian tidak dibersihkan saat dihapus dari **kotak dialog Pilih pada halaman Biaya** **posting**. |
| Manajemen proyek dan akuntansi | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Reset semua distribusi** gagal dan menunjukkan kesalahan untuk lembar waktu yang dibuat untuk proyek tipe Waktu **saja**. |
| Manajemen proyek dan akuntansi | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Proyek tidak dapat diedit pada faktur vendor yang tertunda saat kategori pengadaan ditetapkan ke** item. |
| Manajemen proyek dan akuntansi | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panel navigasi hilang jika Anda tidak masuk ke Dataverse Operasi Proyek. |
| Manajemen proyek dan akuntansi | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Untuk transaksi penyesuaian proyek antar komplotany, ada masalah di perusahaan tujuan. |
| Manajemen proyek dan akuntansi | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Biaya yang berkomitmen untuk proyek menghitung jumlah dan harga biaya yang salah jika pesanan pembelian diproses oleh **proses pesanan pembelian akhir tahun di buku besar** Umum. |
| Manajemen proyek dan akuntansi | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ketika pesanan produksi proyek yang memiliki pesanan berkualitas dilaporkan selesai, kesalahan berikut terjadi: "Tidak ada transaksi virtual yang ditandai dengan transaksi inventaris." |
| Manajemen proyek dan akuntansi | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Ketika faktur hutang Akun terkait proyek diposting, kesalahan berikut terjadi: "Proyek teks yang disebutkan - biaya - item tidak ada." |
| Manajemen proyek dan akuntansi | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Biaya tidak langsung dua kali lipat ketika Anda memperoleh pendapatan secara manual. |
| Manajemen proyek dan akuntansi | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Pendapatan yang masih harus dibayar dan posting WIP tidak menghasilkan transaksi. |
| Manajemen proyek dan akuntansi | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivasi harga yang tertunda gagal untuk item biaya standar ketika pesanan pembelian proyek yang diterima ada. |
| Manajemen proyek dan akuntansi | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai yang dibalik WIP dari posting faktur berbeda dari nilai WIP asli yang diposting dari entri waktu. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ada masalah posting untuk pendapatan faktur proyek dalam kasus punggawa terapan di mana transaksi pada voucher tidak seimbang. |
| Manajemen proyek dan akuntansi | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Pembuatan perkiraan setelah proposal faktur diposting memblokir impor jalur koreksi dalam Operasi Proyek. |
| Manajemen proyek dan akuntansi | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modifikasi catatan tonggak yang sepenuhnya ditagih seharusnya tidak mungkin dilakukan. |
| Manajemen proyek dan akuntansi | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Ketika biaya otomatis digunakan, faktur pelanggan antarkompeti untuk lembar waktu tidak dapat diposting, dan pesan kesalahan ditampilkan. |
| Manajemen proyek dan akuntansi | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamat pada subproyek tidak diperbarui dengan benar. |
| Manajemen proyek dan akuntansi | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Harga biaya pada persyaratan item diperbarui dengan harga pembelian untuk pesanan pembelian konsolidasi. |
| Manajemen proyek dan akuntansi | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Biaya yang diposting tidak benar setelah harga pembelian diperbarui dan parameter **Aktifkan manajemen perubahan** diaktifkan. |
| Perjalanan dan Pengeluaran | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua biaya pengguna dapat dilihat ketika Anda mencari kategori di aplikasi seluler Expense. |
| Perjalanan dan Pengeluaran | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah yang salah pada transaksi vendor dan transaksi pajak penjualan diposting dari biaya yang dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Pesan peringatan yang tidak relevan ditampilkan saat Anda menyegarkan halaman laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Approver interim yang salah digunakan ketika Anda menghapus approver sementara dan kemudian mengirimkan kembali melalui alur kerja. |
| Perjalanan dan Pengeluaran | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Terjadi kesalahan posting yang terkait dengan pengaturan jarak tempuh. |
| Perjalanan dan Pengeluaran | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribusi tidak memperbarui badan hukum ketika transaksi yang tidak terikat ditambahkan kembali ke laporan pengeluaran atas biaya antar perusahaan. |

### <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan peraturan untuk aplikasi Keuangan dan Operasi, lihat [Pembaruan](/dynamics365/finance/localizations/regulatory-updates) peraturan. Anda juga dapat masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan alat pencarian Masalah untuk melihat pembaruan peraturan yang direncanakan. Pencarian masalah memungkinkan Anda mencari berdasarkan negara atau wilayah, jenis fitur, dan rilis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]