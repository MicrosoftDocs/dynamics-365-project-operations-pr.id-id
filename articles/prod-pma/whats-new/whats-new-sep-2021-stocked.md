---
title: Apa yang baru atau berubah dalam Operasi Proyek, September 2021 untuk skenario yang ditebar/berbasis produksi
description: Topik ini memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Operasi Proyek September 2021 untuk skenario yang ditebar/berbasis produksi.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582024"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Apa yang baru atau berubah dalam Operasi Proyek, September 2021 untuk skenario yang ditebar/berbasis produksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Ini topik berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Manajemen proyek dan akuntansi dalam lingkungan Dynamics 365 Finance versi 10.0.21
 
## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
|---|---|---|
| Manajemen proyek dan akuntansi | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jika peran Manajer pembelian diberikan akses ke satu badan hukum, peran tersebut juga mendapatkan akses ke semua proyek di semua badan hukum. |
| Manajemen proyek dan akuntansi | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Masalah pembulatan pajak pertambahan nilai (PPN) terjadi saat nota kredit diselesaikan terhadap faktur proyek asli. |
| Manajemen proyek dan akuntansi | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Gunakan anggaran proyek alternatif untuk verifikasi anggaran. |
| Manajemen proyek dan akuntansi | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Grup **harga jam** penjualan tidak dihitung pada struktur perincian kerja untuk kutipan proyek. |
| Manajemen proyek dan akuntansi | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Eliminasi estimasi gagal saat **fitur Aktifkan mata uang kontrak proyek untuk perhitungan** estimasi diaktifkan. |
| Manajemen proyek dan akuntansi | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorisasi pajak penjualan berdasarkan kuantitas ditambahkan ke jumlah harga penjualan ketika pajak penggunaan digunakan pada kelompok pajak penjualan jurnal biaya Proyek. |
| Manajemen proyek dan akuntansi | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Pajak bersyarat tidak dihitung dengan benar untuk pembayaran terakhir saat retensi dan pembayaran di muka vendor diterapkan untuk membeli faktur pesanan. |
| Manajemen proyek dan akuntansi | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Jejak penyesuaian tidak berfungsi untuk jurnal Saldo awal. |
| Manajemen proyek dan akuntansi | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Alokasi revisi anggaran proyek berdasarkan periode** dibagi di semua periode anggaran. Saat alokasi diajukan, catatan tidak dihapus. |
| Manajemen proyek dan akuntansi | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Posting work in process (WIP) ke buku besar memiliki jumlah yang salah. |
| Manajemen proyek dan akuntansi | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Persetujuan jurnal Jam Proyek tidak berfungsi. |
| Manajemen proyek dan akuntansi | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Harga penjualan penyesuaian proyek tidak diperbarui dengan biaya tidak langsung saat batas pendanaan tidak ditandai. |
| Manajemen proyek dan akuntansi | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Persyaratan item tidak dapat dibuat saat header tabel Penjualan ditagih dan pesanan pembelian dukungan untuk baris yang ada telah diselesaikan. |
| Manajemen proyek dan akuntansi | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Jumlah retensi untuk aturan penagihan yang memiliki tonggak sejarah untuk proyek lain tidak diposting di ID proyek terkait yang dipilih untuk tonggak sejarah. Sebaliknya, itu diposting dengan proyek pertama. |
| Manajemen proyek dan akuntansi | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Saat Anda memilih **Dimensi keuangan yang ditetapkan** pada proposal faktur, kesalahan berikut terjadi: "Tidak dapat melemparkan objek tipe 'Dynamics.AX. Application.FormIntControl' untuk mengetik 'Dynamics.AX. Application.FormStringControl'." |
| Manajemen proyek dan akuntansi | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Laporan **faktur** Proyek melewati garis. |
| Manajemen proyek dan akuntansi | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Kesalahan terjadi ketika Anda menghitung kontrol biaya untuk proyek investasi. |
| Manajemen proyek dan akuntansi | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metode **ProjTable:: InitFromCustTable - canDeletePostalAddress** menyebabkan masalah kinerja. |
| Manajemen proyek dan akuntansi | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Pesan kesalahan harus lebih jelas daripada "Kesalahan tak terduga.". |
| Manajemen proyek dan akuntansi | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Faktur proyek memposting proses pekerjaan batch dan memposting proposal faktur meskipun baris faktur belum dibuat. |
| Manajemen proyek dan akuntansi | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Masalah pembulatan terjadi saat kunci konfigurasi lisensi sektor publik dimatikan. Biaya atau harga penjualan yang salah dihasilkan pada jam timesheet untuk kontrak yang memiliki beberapa sumber pendiri. |
| Manajemen proyek dan akuntansi | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Harga penjualan proyek pada pesanan pembelian proyek yang ditagih salah dihitung ketika model harga penjualan adalah **rasio** Kontribusi. |
| Manajemen proyek dan akuntansi | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem ini tidak mempertimbangkan hari-hari aktif di antaranya ketika menghitung tingkat tenaga kerja yang efektif untuk seorang karyawan. |
| Manajemen proyek dan akuntansi | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Kesalahan posting terjadi pada lembar waktu antar perusahaan karena kesalahan validasi berikut: "Tidak ada mitra dagang yang dikonfigurasi untuk badan hukum." |
| Manajemen proyek dan akuntansi | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Deskripsi dari pesanan pembelian yang memiliki kategori pengeluaran tidak diambil dalam daftar transaksi proyek yang diposting. |
| Manajemen proyek dan akuntansi | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Ada konversi yang salah pada jurnal Item yang diposting ke proyek. |
| Manajemen proyek dan akuntansi | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Anda dapat mengkonfirmasi pesanan pembelian bahkan jika batas pendanaan telah terlampaui. |
| Manajemen proyek dan akuntansi | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Bagian **Koreksi/Batalkan faktur** pada faktur teks gratis menghilang saat ID proyek dipilih. |
| Manajemen proyek dan akuntansi | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Ada masalah kinerja ketika proposal faktur proyek diposting dari pesanan penjualan proyek yang mencakup item yang ditebar. |
| Manajemen proyek dan akuntansi | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Faktur pembelian proyek tidak dapat diposting karena kesalahan berikut terjadi: "Fungsi AccDistProcessorProjectExtension.createForProjectRevenueLine telah salah dipanggil." |
| Manajemen proyek dan akuntansi | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Perbarui ke pembuatan pekerjaan batch perkiraan proyek untuk mendukung eksekusi beberapa subtugas. |
| Manajemen proyek dan akuntansi | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status lembar waktu tidak dapat diperbarui ke **Draf** saat alur kerja macet dalam status **Dibatalkan**. |
| Manajemen proyek dan akuntansi | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Jumlah retensi tidak dihitung dalam proposal faktur catatan kredit jika ada beberapa baris. |
| Manajemen proyek dan akuntansi | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Ketika Anda mencoba mengubah jumlah pada faktur yang dihasilkan dari pesanan pembelian, kesalahan berikut terjadi: "Transaksi pada voucher tidak seimbang sesuai XX / XX / XXXX. (mata uang akuntansi: 0,00 - mata uang pelaporan: 0,01)." |
| Manajemen proyek dan akuntansi | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Ada masalah kinerja ketika proposal faktur proyek diposting dalam mode batch, karena bergabung dengan **GeneralJournalAccountEntry**. |
| Manajemen proyek dan akuntansi | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Ada masalah kinerja saat lembar waktu diposting. |
| Manajemen proyek dan akuntansi | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarki estimasi biaya dari struktur perincian kerja tidak selaras dengan benar setelah semua tugas diperluas atau setelah satu tugas diperluas secara manual. |
| Manajemen proyek dan akuntansi | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Templat Excel kutipan proyek tidak dapat ditambahkan ke **menu Buka di Excel**. |
| Manajemen proyek dan akuntansi | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Nomor bebas pajak untuk badan hukum tidak termasuk dalam faktur proyek yang dicetak. |
| Manajemen proyek dan akuntansi | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Tidak ada data keuangan yang diperbarui dalam kesalahan unit inventaris saat proyek disesuaikan sehubungan dengan jalur kredit. |
| Manajemen proyek dan akuntansi | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Setelah menerapkan KB 461935, Anda tidak dapat memposting perkiraan jika Beralih ke urutan angka kontinu. |
| Manajemen proyek dan akuntansi | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** menyebabkan aplikasi Android seluler lembar waktu Proyek berhenti merespons. |
| Manajemen proyek dan akuntansi | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai yang dibalik WIP dari posting faktur berbeda dari nilai WIP yang awalnya diposting dari entri waktu. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Dalam kasus retainer yang diterapkan, transaksi pada voucher tidak seimbang ketika pendapatan yang ditagih untuk sebuah proyek diposting. |
| Manajemen proyek dan akuntansi | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | **Saat fitur peningkatan** kinerja penjadwalan sumber daya Proyek diaktifkan, nilai desimal dibulatkan secara tidak benar untuk ketersediaan dan kapasitas sumber daya. |
| Manajemen proyek dan akuntansi | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | **Saat fitur Buat estimasi proyek menggunakan beberapa tugas** batch diaktifkan, pembuatan estimasi dalam batch yang memiliki beberapa subtugas hanya berfungsi untuk periode saat ini. |
| Perjalanan dan Pengeluaran | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Kebijakan permintaan perjalanan diabaikan, dan alur kerja disetujui tanpa kesalahan. |
| Perjalanan dan Pengeluaran | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikasi Biaya Seluler tidak menyimpan informasi berikut pada saluran pengeluaran:</p><ul><li>ID proyek</li><li>Apakah biaya tersebut dapat ditagih</li><li>Nomor aktivitas</li></ul> |
| Perjalanan dan Pengeluaran | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Bidang **tanda terima** terlampir diatur ke **Ya** meskipun tidak ada tanda terima yang dilampirkan ke garis pengeluaran. |
| Perjalanan dan Pengeluaran | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Kesalahan terjadi saat Anda mengubah kategori pengeluaran menjadi **Pribadi**. |
| Perjalanan dan Pengeluaran | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Anda tidak dapat melampirkan tanda terima dan mengedit biaya orang tua setelah transaksi kartu kredit dibagi menjadi pengeluaran pribadi. |
| Perjalanan dan Pengeluaran | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Kebijakan pengeluaran untuk transaksi antar perusahaan yang memiliki ID proyek tidak berfungsi dengan benar. |
| Perjalanan dan Pengeluaran | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informasi tanggal yang diposting tidak ada untuk laporan pengeluaran yang diposting. |
| Perjalanan dan Pengeluaran | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Ada masalah metode pembayaran di aplikasi seluler Expense. |
| Perjalanan dan Pengeluaran | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Permintaan perjalanan yang dibuat untuk satu pekerja dapat digunakan untuk laporan pengeluaran pekerja lain sebelum tanggal delegasi. |
| Perjalanan dan Pengeluaran | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Saat Anda membuat pengeluaran, perubahan pada nilai dimensi keuangan tidak diperbarui dengan benar di tingkat distribusi akuntansi di **ruang kerja manajemen** Pengeluaran. |
| Perjalanan dan Pengeluaran | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status persetujuan jalur pengeluaran utama tidak disinkronkan dengan status persetujuan alur kerja baris terperinci. |
| Perjalanan dan Pengeluaran | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Kesalahan terjadi jika Anda memposting laporan pengeluaran dan pemulihan pajak diaktifkan. |
| Perjalanan dan Pengeluaran | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegasi tidak dapat menghapus dokumen pengeluaran untuk karyawan yang diberhentikan. |
| Perjalanan dan Pengeluaran | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Penghapusan garis pengeluaran membutuhkan waktu lebih lama dari yang diharapkan dan mempengaruhi kinerja. |
| Perjalanan dan Pengeluaran | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** menyebabkan catatan taxuncommitted **yatim piatu**, karena hanya **SourceDocumentLine** yang dihapus. |
| Perjalanan dan Pengeluaran | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** tidak menghormati **trvExpTrans.ReferenceDataAreaId** untuk membuat urutan nomor baru. |

## <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan peraturan untuk aplikasi Keuangan dan Operasi, lihat [Pembaruan peraturan](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan alat pencarian Masalah untuk melihat pembaruan peraturan yang direncanakan. Pencarian masalah memungkinkan Anda mencari berdasarkan negara atau wilayah, jenis fitur, dan rilis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
