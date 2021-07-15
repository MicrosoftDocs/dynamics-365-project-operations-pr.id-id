---
title: Yang baru atau berubah di Project Operations, Mei 2021 untuk skenario berbasis stok/produksi
description: Topik ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam skenario Project Operations yang dirilis Pada Bulan Mei 2021 untuk skenario berbasis produksi/stok.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: cfb418606f4186c5371c36946f75c9d946047a61
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334553"
---
# <a name="whats-new-or-changed-in-project-operations-may-2021-for-stockedproduction-based-scenarios"></a>Yang baru atau berubah di Project Operations, Mei 2021 untuk skenario berbasis stok/produksi

**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

- Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi version 10.0.19
 
### <a name="quality-updates"></a>Pembaruan kualitas
                                                                                                                                                                                  
| Area fitur                      | Nomor Referensi| Pembaruan kualitas                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manajemen proyek dan akuntansi | [529751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529751) | Impor gagal saat validasi entitas dinonaktifkan untuk baris jurnal item proyek.                                                                                                                                                   |
| Manajemen proyek dan akuntansi | [550565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550565) | Ada masalah performa laporan akun WIP yang terkait dengan pencarian **GeneralJournalEntry**.                                                                                                                                  |
| Manajemen proyek dan akuntansi | [539044](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539044) | Dimensi keuangan tidak ditemukan di proyek WIP.                                                                                                                                                                                                    |
| Manajemen proyek dan akuntansi | [540903](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540903) | Posting proposal faktur gagal karena   **ProjBudgetAllocationLineIdSales** yang salah ditetapkan ke **ProjBudgetReductionHistory**.                                                                                                                           |
| Manajemen proyek dan akuntansi | [547090](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547090) | Setelah mengimpor file XML, jurnal Umum menampilkan nomor voucher yang salah.                                                                                                                                                              |
| Manajemen proyek dan akuntansi | [552160](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552160) | Kesalahan terjadi pada template struktur perincian kerja.                                                                                                                                                                                          |
| Manajemen proyek dan akuntansi | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Catatan formulir** dan **konfigurasi Formulir** tidak dapat dilihat dalam konfigurasi manajemen proyek di entitas hukum Finance ketika terintegrasi dengan Project Operations.                                                                                                             |
| Manajemen proyek dan akuntansi | [553313](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553313) | Membatalkan pesanan penjualan antarperusahaan gagal dengan kesalahan berikut, "Tidak dapat mengedit rekaman di baris Pesanan pembelian (PurchLine). Konflik pembaruan terjadi karena proses pengguna lain menghapus rekaman atau mengubah satu atau beberapa bidang di rekaman." |
| Manajemen proyek dan akuntansi | [553775](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553775) | Penyesuaian transaksi proyek menciptakan dimensi keuangan yang salah untuk biaya proyek.                                                                                                                                                          |
| Manajemen proyek dan akuntansi | [556751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=556751) | Faktur vendor memiliki petunjuk tambahan saat memproses pesanan pembelian yang tersambung ke proyek.                                                                                                                                                 |
| Manajemen proyek dan akuntansi | [557925](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557925) | Baris lembar waktu tidak dapat disetujui dan kesalahan berikut terjadi, "Kondisi aktivasi untuk alur kerja, tidak valid. Laporkan masalah ini ke administrator sistem."                                                                          |
| Manajemen proyek dan akuntansi | [559266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559266) | Jika Anda menerima pesan kesalahan, "Tidak dapat mengubah kontrak proyek karena ada transaksi untuk proyek terkait XXXXXX", Anda tetap dapat mengubah kontrak pada tingkat proyek.                                                                           |
| Manajemen proyek dan akuntansi | [560432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560432) | Jika Anda menerima kesalahan, "Kuantitas tidak dapat ditagih karena transaksi inventaris dengan status Dikurangkan tidak memadai", faktur pesanan pembelian tidak dapat diposting setelah penghitungan ulang inventaris dijalankan.                             |
| Manajemen proyek dan akuntansi | [562013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=562013) | Bila alur kerja permintaan sumber daya diaktifkan, ada masalah performa saat mencoba membuka halaman dengan kontrol ketersediaan sumber daya proyek.                                                                                                               |
| Manajemen proyek dan akuntansi | [488320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488320) | Status faktur berubah ke **Tidak Dapat Ditagih** setelah Anda menambahkan aturan penagihan untuk menentukan proyek lain ke kontrak proyek.                                                                                                                                |
| Manajemen proyek dan akuntansi | [515219](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515219) | Kesalahan terjadi saat Anda menghapus faktur pembayaran di muka dari pesanan pembelian proyek dan parameter **Posting biaya pembayaran di muka terhadap proyek** diaktifkan.                                                                                                        |
| Manajemen proyek dan akuntansi | [526439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526439) | Ketika Anda memposting faktur pesanan pembelian proyek, kesalahan terjadi karena tanda item otomatis tidak ada.                                                                                                                            |
| Manajemen proyek dan akuntansi | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Deskripsi default untuk PPN kosong saat jenis posting sama dengan pajak penjualan untuk voucer faktur proyek.                                                                                                                                           |
| Manajemen proyek dan akuntansi | [530352](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530352) | Pesanan pembelian proyek akan menampilkan kesalahan jika Anda menghapus pesanan penjualan persyaratan item terkait yang dibatalkan.                                                                                                                                 |
| Manajemen proyek dan akuntansi | [530651](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530651) | Ketika Anda menandai dan membatalkan tanda pesanan pembelian item proyek, referensi akan hilang.                                                                                                                                                               |
| Manajemen proyek dan akuntansi | [533023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533023) | Ada masalah nilai default kuantitas yang dikurangi saat mencetak daftar pilihan untuk persyaratan item proyek.                                                                                                                                                 |
| Manajemen proyek dan akuntansi | [535493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535493) | Harga penjualan yang dihitung tidak benar jika terjadi pengiriman berlebih.                                                                                                                                                                                 |
| Manajemen proyek dan akuntansi | [541329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541329) | Kesalahan beban diposting saat penyimpanan dirilis tanpa kuantitas faktur pada proposal faktur.                                                                                                                                                |
| Manajemen proyek dan akuntansi | [541997](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541997) | Bila Anda membuat periode lembar waktu, periode pertama ditampilkan sebagai minggu 53.                                                                                                                                                                         |
| Manajemen proyek dan akuntansi | [542043](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542043) | Jenis proyek default dalam parameter integrasi Dynamics 365 Project Service Automation harus adalah Waktu dan Bahan dan Harga Tetap.                                                                                                         |
| Manajemen proyek dan akuntansi | [543096](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543096) | Menghapus proposal faktur dengan aturan penagihan akan menghasilkan posting.                                                                                                                                                                              |
| Manajemen proyek dan akuntansi | [543463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543463) | Estimasi akhir tentang proses penghapusan dengan menggunakan metode persentase selesai tidak dapat dihilangkan karena sistem tidak mengenali pendapatan.                                                                                                                                      |
| Manajemen proyek dan akuntansi | [543938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543938) | Bila Anda memposting estimasi proyek, rekaman estimasi posting tidak dibuat.                                                                                                                                                                            |
| Manajemen proyek dan akuntansi | [546885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546885) | Akun utama pada faktur vendor tertunda tidak ditemukan selama faktur antarperusahaan.                                                                                                                                                               |
| Manajemen proyek dan akuntansi | [547885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547885) | Jika kontrak mencakup persyaratan item, Anda tidak dapat menambahkan sumber dana kedua.                                                                                                                                                         |
| Manajemen proyek dan akuntansi | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | Sistem membuat revisi pada anggaran proyek untuk semua proyek saat Anda menggunakan **Proyek** > **Anggaran** > **Revisi** > **Baru** > **Impor**.                                                                                                                         |
| Manajemen proyek dan akuntansi | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) |  Jika Anda menyesuaikan transaksi dengan mata uang transaksi dan akuntansi yang berbeda, entri posting dan buku besar umum salah.                                                                                                                                       |
| Manajemen proyek dan akuntansi | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Komitmen Biaya dinyatakan berlebihan dengan jumlah pajak yang tidak dapat dikurangkan.                                                                                                                                                                                   |
| Manajemen proyek dan akuntansi | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Tidak ada dimensi yang diambil saat Anda membuat faktur posting untuk transaksi.                                                                                                                                                                  |
| Manajemen proyek dan akuntansi | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | Metode **PurchTotals.purchNewTotalAmount()** dipanggil bila Anda membuat faktur vendor tertunda yang tidak ditautkan dengan pesanan pembelian, yang mengakibatkan masalah performa.                                                                                   |
| Manajemen proyek dan akuntansi | [563694](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563694) | Kolom **anggaran yang Digunakan** dan **Sisa anggaran** menunjukkan jumlah yang salah pada saldo anggaran proyek.                                                                                                                                                |
| Manajemen proyek dan akuntansi | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Transaksi diposting dua kali saat penagihan berbasis tugas digunakan di Dataverse dengan Project Operations.                                                                                                                                         |
| Manajemen proyek dan akuntansi | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Persentase lengkap untuk pengakuan pendapatan salah saat menggunakan Project Operations.                                                                                                                                                  |
| Manajemen proyek dan akuntansi | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Akrual pendapatan digandakan ketika Anda menggunakan faktur vendor tertunda dalam skenario terintegrasi Project Operations.                                                                                                                                          |
| Manajemen proyek dan akuntansi | [569736](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569736) | Posting lembar waktu proyek akan membuat transaksi duplikat.                                                                                                                                                                        |
| Manajemen proyek dan akuntansi | [569819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569819) | Kesalahan terjadi saat Anda memposting jurnal pemakaian item terhadap perintah kerja.                                                                                                                                  |
| Manajemen proyek dan akuntansi | [571197](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571197) | Pesanan produksi proyek tidak dapat diselesaikan karena kesalahan berikut, "Referensi objek tidak diatur ke instans objek."                                                                                                                           |
| Manajemen proyek dan akuntansi | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Tidak dapat memposting jurnal integrasi jika aturan profil pendapatan diatur ke **konfigurasi Grup**.                                                                                                                                                           |
| Manajemen proyek dan akuntansi | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Faktur pembelian tidak dapat diposting untuk pesanan pembelian proyek yang memiliki baris dengan beberapa satuan pengukuran.                                                                                                                                             |
| Manajemen proyek dan akuntansi | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Dimensi keuangan default pada proyek tidak dapat diperbarui menggunakan entitas data **proyek V2**.                                                                                                                                                          |
| Manajemen proyek dan akuntansi | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Tidak dapat membuat nota kredit untuk pesanan penjualan proyek bila pajak memiliki mata uang yang berbeda dari mata uang perusahaan.                                                                                                                     |
| Manajemen proyek dan akuntansi | [574104](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574104) | Terjadi masalah saat proposal faktur dibuat dengan lebih dari 100 aturan penagihan.                                                                                                                                                                  |
| Manajemen proyek dan akuntansi | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Proses batch pembuatan estimasi proyek memerlukan waktu terlalu lama untuk diselesaikan.                                                                                                                                                                      |
| Manajemen proyek dan akuntansi | [577785](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577785) | Saat Anda menjalankan fungsi, **Isi sumber daya proyek di semua perusahaan**, kesalahan berikut terjadi, "Nama objek tidak valid ResRollupCalendar."                                                                                                                                   |
| Manajemen proyek dan akuntansi | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Saat Anda menghapus kontrak, alamat yang terkait dengan pelanggan juga dihapus.                                                                                                                                                                    |
| Perjalanan dan Pengeluaran                  | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Kondisi alur kerja persetujuan laporan pengeluaran tidak dievaluasi dengan benar.                                                                                                                                                                           |
| Perjalanan dan Pengeluaran                  | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Kebijakan laporan pengeluaran tidak mengevaluasi ID proyek dengan benar.                                                                                                                                                                                   |
| Perjalanan dan Pengeluaran                  | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Tindakan, **Pecah ke pribadi** untuk transaksi pengeluaran antarperusahaan tidak berfungsi dengan benar.                                                                                                                                                                |
| Perjalanan dan Pengeluaran                  | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Kadang justifikasi baris laporan pengeluaran dihapus ketika permintaan perjalanan dihapus. Hal ini terjadi ketika recID laporan pengeluaran dan permintaan perjalanan sama.                                                            |
| Perjalanan dan Pengeluaran                  | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Ada masalah dengan aplikasi seluler Pengeluaran saat bidang **ID Proyek** diperlukan oleh kebijakan laporan pengeluaran.                                                                                                                                                |
| Perjalanan dan Pengeluaran                  | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Saat Anda mencoba mengedit pengeluaran antarperusahaan yang terkait dengan proyek, pesan kesalahan berikut terjadi, "Referensi objek tidak diatur ke instans objek."                                                                           |
| Perjalanan dan Pengeluaran                  | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Setelah laporan pengeluaran diposting, mata uang dan jumlah yang salah tercantum di buku besar pembantu.                                                                                                                                                                |
| Perjalanan dan Pengeluaran                  | [555462](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5355462) | Komitmen biaya untuk proyek tidak dirilis setelah menutup permintaan perjalanan dengan komitmen biaya.                                                                                                                                              |
| Perjalanan dan Pengeluaran                  | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Peningkatan telah dilakukan pada fitur, Hapus transaksi kartu kredit.                                                                                                                                                                                           |
| Perjalanan dan Pengeluaran                  | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Pajak penjualan yang tercakup dalam laporan pengeluaran tidak secara konsisten dihitung bila mata uang pelaporan yang berbeda ditentukan dalam entitas hukum.                                                                                                         |
| Perjalanan dan Pengeluaran                  | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Kinerja terpengaruh saat menambahkan pengeluaran perjalanan tunai baru.                                                                                                                                                                                         |
| Perjalanan dan Pengeluaran                  | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Aturan kebijakan pengeluaran tidak dipicu pada laporan pengeluaran.                                                                                                                                                                                            |
| Perjalanan dan Pengeluaran                  | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Mengunggah kategori bersama baru dengan menggunakan Kerangka Kerja Manajemen Data akan menghilangkan semua subkategori untuk semua kategori bersama.                                                                                                                         |
| Perjalanan dan Pengeluaran                  | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Ketika Anda membuat baris pengeluaran dan kemudian memilih kategori, pesan kesalahan berikut terjadi, "Kombinasi dari grup pajak penjualan DOM dan grup pajak penjualan item STD tidak valid."                                                                  |
| Perjalanan dan Pengeluaran                  | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Ada masalah sinkronisasi di aplikasi seluler Pengeluaran. 

### <a name="regulatory-updates"></a>Pembaruan wajib
Untuk informasi tentang pembaruan wajib untuk aplikasi Finance and Operations, lihat [pembaruan wajib](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke Lifecycle Services (LCS) dan melihat pembaruan peraturan yang telah direncanakan menggunakan alat pencarian Masalah. Pencarian Masalah memungkinkan Anda mencari berdasarkan negara, jenis fitur, dan rilis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]