---
title: Apa yang baru atau berubah dalam Operasi Proyek, Oktober 2021 untuk skenario berbasis stok/produksi
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Oktober 2021 Operasi Proyek untuk skenario berbasis stok/produksi.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933680"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Apa yang baru atau berubah dalam Operasi Proyek, Oktober 2021 untuk skenario berbasis stok/produksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Manajemen dan akuntansi proyek dalam lingkungan Dynamics 365 Finance versi 10.0.22
 
## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
|--------------|------------------|----------------|
| Manajemen proyek dan akuntansi | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Pekerjaan proyek dalam proses (WIP) dan jumlah pendapatan yang masih harus dibayar tidak dibalik dengan benar ketika faktur pelanggan antar perusahaan diposting. |
| Manajemen proyek dan akuntansi | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Fungsi **Cegah penutupan proyek jika ada** transaksi terbuka tidak berfungsi. |
| Manajemen proyek dan akuntansi | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikasi penagihan pada faktur teks gratis tidak secara otomatis mengisi dimensi dari proyek saat fungsi tersebut diaktifkan. |
| Manajemen proyek dan akuntansi | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Dalam skenario non-antar perusahaan, WIP dan jumlah pendapatan yang masih harus dibayar tidak dibalik dengan benar saat faktur proyek diposting. |
| Manajemen proyek dan akuntansi | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Nilai debit dan kredit dialihkan ketika Microsoft Excel add-in digunakan dengan jurnal biaya Proyek dan **bidang Jenis** akun Offset diatur ke **Proyek**. |
| Manajemen proyek dan akuntansi | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Jumlah yang diposting dalam transaksi proyek dilebih-lebihkan pada pesanan pembelian proyek yang mencakup item yang ditebar dan yang memiliki jumlah pajak yang tidak dapat dikurangkan saat **UseTax** ditandai. |
| Manajemen proyek dan akuntansi | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem membagi jumlah antara laporan laba rugi proyek dan laporan dan laporan WIP proyek. |
| Manajemen proyek dan akuntansi | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventaris di tangan salah setelah persyaratan barang yang dikembalikan sebagian disesuaikan. |
| Manajemen proyek dan akuntansi | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nama sumber daya digandakan dalam Operasi Proyek saat diedit di Microsoft Project. |
| Manajemen proyek dan akuntansi | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Laporan biaya antar perusahaan yang memiliki akun yang harus dibayar antar perusahaan menunggu biaya faktur vendor pertama kali diposting ke **jenis posting biaya** Project WIP. Namun, selama pemrosesan, biaya terkait perkiraan diposting ke **jenis posting biaya** Proyek alih-alih jenis posting biaya **Intercompany yang diharapkan**. |
| Manajemen proyek dan akuntansi | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Hasil penyimpanan vendor dalam transaksi biaya proyek tidak ditampilkan. |
| Manajemen proyek dan akuntansi | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Lembar waktu harus membulatkan jumlah transaksi dalam mata uang transaksi ke jumlah tempat desimal tertentu pada semua distribusi akuntansi dan entri alokasi jurnal umum. |
| Manajemen proyek dan akuntansi | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Jumlah persyaratan item proyek diperbarui secara otomatis ketika pesanan yang direncanakan ditegakkan. |
| Manajemen proyek dan akuntansi | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Nomor voucher, saldo vendor jenis transaksi, dan nomor akun tidak dapat dibalik pada faktur pembayaran di muka dari pesanan pembelian. |
| Manajemen proyek dan akuntansi | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktur vendor antar perusahaan rusak saat integrasi faktur vendor diaktifkan. |
| Manajemen proyek dan akuntansi | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Saat Anda membuat jurnal pengeluaran Proyek, jumlah biaya ditampilkan di **bidang Kredit**. |
| Manajemen proyek dan akuntansi | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Ketentuan pembayaran pada faktur proyek tidak berfungsi seperti yang diharapkan. |
| Manajemen proyek dan akuntansi | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Voucher lembar waktu dapat digunakan kembali ketika urutan angka diatur sebagai kontinu. |
| Manajemen proyek dan akuntansi | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PRANCIS: Logika **Jumlah** retensi manual tidak cocok dengan **logika Jumlah** retensi otomatis dalam proposal faktur kontrak proyek. |
| Manajemen proyek dan akuntansi | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ketika retensi vendor dirilis, posting voucher memiliki baris tambahan yang salah. |
| Manajemen proyek dan akuntansi | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **Ketika bidang Tanggal** faktur pada **halaman Buat proposal** faktur diubah, kesalahan berikut mungkin terjadi: "Referensi objek tidak diatur ke contoh objek." |
| Manajemen proyek dan akuntansi | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Kesalahan terjadi ketika Anda mencoba menyetujui lembar waktu dari **alur kerja TSLine**, dan ada kebijakan lembar waktu untuk hari Sabtu dan Minggu. |
| Manajemen proyek dan akuntansi | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Jenis item proyek saldo awal dikecualikan dari **ringkasan** transaksi proposal Faktur ketika total faktur dari proposal faktur dihitung. |
| Manajemen proyek dan akuntansi | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Jika biaya konsumsi pada pesanan produksi proyek adalah 0 (nol), kesalahan berikut terjadi ketika Anda mencoba memperkirakan: "Mencoba membagi dengan nol." |
| Manajemen proyek dan akuntansi | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikasi Project Timesheet Mobile untuk Android berhenti merespons. Masalah ini terkait **dengan TimeEntryDataManager ArgumentNullException**. |
| Manajemen proyek dan akuntansi | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Jurnal integrasi Operasi Proyek gagal saat Anda mempostingnya, karena akun tidak memiliki dimensi. Namun, akun yang kehilangan dimensi bukanlah akun yang Anda posting. |
| Manajemen proyek dan akuntansi | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filter **ToDate** dalam pencarian tidak dikosongkan saat dihapus dari **kotak dialog Pilih** di **halaman Biaya** posting. |
| Manajemen proyek dan akuntansi | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Reset semua distribusi** gagal dan memperlihatkan kesalahan untuk lembar waktu yang dibuat untuk proyek tipe **Waktu saja**. |
| Manajemen proyek dan akuntansi | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Proyek** tidak dapat diedit pada faktur vendor yang tertunda saat kategori pengadaan ditetapkan ke item. |
| Manajemen proyek dan akuntansi | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panel navigasi hilang jika Anda tidak masuk ke Operasi Dataverse Proyek. |
| Manajemen proyek dan akuntansi | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Untuk transaksi penyesuaian proyek antar perusahaan, ada masalah di perusahaan tujuan. |
| Manajemen proyek dan akuntansi | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Biaya yang berkomitmen untuk suatu proyek menghitung jumlah dan harga biaya yang salah jika pesanan pembelian diproses oleh **proses** akhir tahun pesanan Pembelian di buku besar Umum. |
| Manajemen proyek dan akuntansi | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ketika pesanan produksi proyek yang memiliki pesanan berkualitas dilaporkan sebagai selesai, kesalahan berikut terjadi: "Tidak ada transaksi virtual yang ditandai dengan transaksi inventaris." |
| Manajemen proyek dan akuntansi | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Ketika faktur hutang Akun terkait proyek diposting, kesalahan berikut terjadi: "Teks yang disebutkan Proyek - biaya - item tidak ada." |
| Manajemen proyek dan akuntansi | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Biaya tidak langsung digandakan ketika Anda memperoleh pendapatan secara manual. |
| Manajemen proyek dan akuntansi | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Memperoleh pendapatan dan posting WIP tidak menghasilkan transaksi. |
| Manajemen proyek dan akuntansi | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivasi harga tertunda gagal untuk item biaya standar ketika ada pesanan pembelian proyek yang diterima. |
| Manajemen proyek dan akuntansi | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai terbalik WIP dari posting faktur berbeda dari nilai WIP asli yang diposting dari entri waktu. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ada masalah posting untuk pendapatan yang ditagih proyek dalam kasus retainer yang diterapkan di mana transaksi pada voucher tidak seimbang. |
| Manajemen proyek dan akuntansi | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Pembuatan perkiraan setelah proposal faktur diposting memblokir impor jalur koreksi dalam Operasi Proyek. |
| Manajemen proyek dan akuntansi | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modifikasi catatan tonggak pencapaian yang ditagih sepenuhnya seharusnya tidak dimungkinkan. |
| Manajemen proyek dan akuntansi | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Saat biaya otomatis digunakan, faktur pelanggan antar perusahaan untuk lembar waktu tidak dapat diposting, dan pesan kesalahan ditampilkan. |
| Manajemen proyek dan akuntansi | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamat pada subproyek tidak diperbarui dengan benar. |
| Manajemen proyek dan akuntansi | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Harga biaya pada persyaratan item diperbarui dengan harga pembelian untuk pesanan pembelian konsolidasi. |
| Manajemen proyek dan akuntansi | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Biaya yang diposting tidak benar setelah harga pembelian diperbarui dan parameter **Aktifkan manajemen** perubahan diaktifkan. |
| Perjalanan dan Pengeluaran | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua pengeluaran pengguna dapat dilihat saat Anda mencari kategori di aplikasi seluler Pengeluaran. |
| Perjalanan dan Pengeluaran | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah yang salah pada transaksi vendor dan transaksi pajak penjualan diposting dari pengeluaran yang dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Pesan peringatan yang tidak relevan ditampilkan saat Anda me-refresh halaman laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pemberi persetujuan sementara yang salah digunakan saat Anda menghapus pemberi persetujuan sementara lalu mengirim ulang melalui alur kerja. |
| Perjalanan dan Pengeluaran | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Terjadi kesalahan posting yang terkait dengan pengaturan jarak tempuh. |
| Perjalanan dan Pengeluaran | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribusi tidak memperbarui badan hukum ketika transaksi yang tidak dilampirkan ditambahkan kembali ke laporan pengeluaran pada biaya antar perusahaan. |

### <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan peraturan untuk aplikasi Keuangan dan Operasi, lihat [Pembaruan peraturan](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan alat pencarian Masalah untuk melihat pembaruan peraturan yang direncanakan. Pencarian masalah memungkinkan Anda menelusuri menurut negara atau wilayah, jenis fitur, dan rilis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
