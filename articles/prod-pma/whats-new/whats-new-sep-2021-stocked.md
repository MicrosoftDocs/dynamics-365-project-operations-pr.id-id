---
title: Apa yang baru atau berubah dalam Operasi Proyek, September 2021 untuk skenario berbasis stok/produksi
description: Artikel ini memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis September 2021 Operasi Proyek untuk skenario berbasis stok/produksi.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029856"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Apa yang baru atau berubah dalam Operasi Proyek, September 2021 untuk skenario berbasis stok/produksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Manajemen dan akuntansi proyek dalam lingkungan Dynamics 365 Finance versi 10.0.21
 
## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
|---|---|---|
| Manajemen proyek dan akuntansi | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jika peran Manajer pembelian diberikan akses ke satu badan hukum, itu juga mendapatkan akses ke semua proyek di semua badan hukum. |
| Manajemen proyek dan akuntansi | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Masalah pembulatan pajak pertambahan nilai (PPN) terjadi saat nota kredit diselesaikan terhadap faktur proyek asli. |
| Manajemen proyek dan akuntansi | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Gunakan anggaran proyek alternatif untuk verifikasi anggaran. |
| Manajemen proyek dan akuntansi | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Grup **harga jam** penjualan tidak dihitung pada struktur rincian pekerjaan untuk kutipan proyek. |
| Manajemen proyek dan akuntansi | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Eliminasi estimasi gagal ketika **fitur Aktifkan mata uang kontrak proyek untuk perhitungan** perkiraan diaktifkan. |
| Manajemen proyek dan akuntansi | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorisasi pajak penjualan berdasarkan kuantitas ditambahkan ke jumlah harga penjualan saat pajak penggunaan digunakan pada grup pajak penjualan jurnal biaya Proyek. |
| Manajemen proyek dan akuntansi | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Pajak bersyarat tidak dihitung dengan benar untuk pembayaran terakhir saat retensi dan pembayaran di muka vendor diterapkan pada faktur pesanan pembelian. |
| Manajemen proyek dan akuntansi | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Jejak penyesuaian tidak berfungsi untuk jurnal saldo Awal. |
| Manajemen proyek dan akuntansi | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Alokasi revisi anggaran proyek berdasarkan periode** dibagi di semua periode anggaran. Saat alokasi dikirimkan, catatan tidak dihapus. |
| Manajemen proyek dan akuntansi | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Posting work in process (WIP) ke buku besar memiliki jumlah yang salah. |
| Manajemen proyek dan akuntansi | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Persetujuan jurnal Project hour tidak berfungsi. |
| Manajemen proyek dan akuntansi | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Harga penjualan penyesuaian proyek tidak diperbarui dengan biaya tidak langsung ketika batas pendanaan tidak ditandai. |
| Manajemen proyek dan akuntansi | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Persyaratan item tidak dapat dibuat saat header tabel Penjualan ditagih dan pesanan pembelian dukungan untuk baris yang ada telah diselesaikan. |
| Manajemen proyek dan akuntansi | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Jumlah retensi untuk aturan penagihan yang memiliki tonggak pencapaian untuk project lain tidak diposting di ID project terkait yang dipilih untuk pencapaian tersebut. Sebaliknya, itu diposting dengan proyek pertama. |
| Manajemen proyek dan akuntansi | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Ketika Anda memilih **Dimensi keuangan yang ditetapkan** pada proposal faktur, kesalahan berikut terjadi: "Tidak dapat mentransmisikan objek jenis 'Dynamics.AX. Application.FormIntControl' untuk mengetik 'Dynamics.AX. Application.FormStringControl'." |
| Manajemen proyek dan akuntansi | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **Laporan faktur** Proyek melewati baris. |
| Manajemen proyek dan akuntansi | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Kesalahan terjadi ketika Anda menghitung kontrol biaya untuk proyek investasi. |
| Manajemen proyek dan akuntansi | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metode **ProjTable:: InitFromCustTable - canDeletePostalAddress** menyebabkan masalah kinerja. |
| Manajemen proyek dan akuntansi | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Pesan kesalahan harus lebih jelas daripada "Kesalahan tak terduga." |
| Manajemen proyek dan akuntansi | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Faktur proyek memposting proses pekerjaan batch dan memposting proposal faktur meskipun baris faktur belum dibuat. |
| Manajemen proyek dan akuntansi | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Masalah pembulatan terjadi ketika kunci konfigurasi lisensi sektor Publik dinonaktifkan. Biaya atau harga penjualan yang salah dihasilkan pada jam lembar waktu untuk kontrak yang memiliki beberapa sumber pendiri. |
| Manajemen proyek dan akuntansi | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Harga penjualan proyek pada pesanan pembelian proyek yang ditagih salah dihitung ketika model harga penjualan adalah **rasio** Kontribusi. |
| Manajemen proyek dan akuntansi | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem tidak mempertimbangkan hari-hari aktif di antaranya ketika menghitung tingkat tenaga kerja efektif untuk seorang karyawan. |
| Manajemen proyek dan akuntansi | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Kesalahan posting terjadi pada lembar waktu antar perusahaan karena kesalahan validasi berikut: "Tidak ada mitra dagang yang dikonfigurasi untuk badan hukum." |
| Manajemen proyek dan akuntansi | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Deskripsi dari pesanan pembelian yang memiliki kategori pengeluaran tidak diambil dalam daftar transaksi proyek yang diposting. |
| Manajemen proyek dan akuntansi | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Ada konversi yang salah pada jurnal Item yang diposting ke proyek. |
| Manajemen proyek dan akuntansi | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Anda dapat mengonfirmasi pesanan pembelian meskipun batas pendanaan telah terlampaui. |
| Manajemen proyek dan akuntansi | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Bagian **Koreksi/Batalkan faktur** pada faktur teks gratis menghilang saat ID proyek dipilih. |
| Manajemen proyek dan akuntansi | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Ada masalah kinerja ketika proposal faktur proyek diposting dari pesanan penjualan proyek yang mencakup item yang ditebar. |
| Manajemen proyek dan akuntansi | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Faktur pembelian proyek tidak dapat diposting karena kesalahan berikut terjadi: "Fungsi AccDistProcessorProjectExtension.createForProjectRevenueLine telah salah dipanggil." |
| Manajemen proyek dan akuntansi | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Perbarui pada pembuatan pekerjaan batch perkiraan proyek untuk mendukung eksekusi beberapa subtugas. |
| Manajemen proyek dan akuntansi | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status lembar waktu tidak dapat diperbarui ke **Draf** saat alur kerja terjebak dalam status **Dibatalkan**. |
| Manajemen proyek dan akuntansi | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Jumlah retensi tidak dihitung dalam proposal faktur nota kredit jika ada beberapa baris. |
| Manajemen proyek dan akuntansi | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Ketika Anda mencoba mengubah jumlah pada faktur yang dihasilkan dari pesanan pembelian, kesalahan berikut terjadi: "Transaksi pada voucher tidak seimbang sesuai XX/XX/XXXX. (mata uang akuntansi: 0,00 - mata uang pelaporan: 0,01)." |
| Manajemen proyek dan akuntansi | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Ada masalah kinerja ketika proposal faktur proyek diposting dalam mode batch, karena bergabung dengan **GeneralJournalAccountEntry**. |
| Manajemen proyek dan akuntansi | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Ada masalah kinerja saat lembar waktu diposting. |
| Manajemen proyek dan akuntansi | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarki perkiraan biaya dari struktur rincian kerja tidak diselaraskan dengan benar setelah semua tugas diperluas atau setelah satu tugas diperluas secara manual. |
| Manajemen proyek dan akuntansi | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Template Excel kutipan proyek tidak bisa ditambahkan ke menu **Buka di Excel**. |
| Manajemen proyek dan akuntansi | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Nomor bebas pajak untuk badan hukum tidak disertakan pada faktur proyek yang dicetak. |
| Manajemen proyek dan akuntansi | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Tidak ada data keuangan yang diperbarui dalam kesalahan unit inventaris ketika sebuah proyek disesuaikan sehubungan dengan jalur kredit. |
| Manajemen proyek dan akuntansi | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Setelah menerapkan KB 461935, Anda tidak dapat memposting perkiraan jika beralih ke urutan angka berkelanjutan. |
| Manajemen proyek dan akuntansi | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** menyebabkan aplikasi Android seluler lembar waktu Proyek berhenti merespons. |
| Manajemen proyek dan akuntansi | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai terbalik WIP dari posting faktur berbeda dari nilai WIP yang awalnya diposting dari entri waktu. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Dalam kasus retainer yang diterapkan, transaksi pada voucher tidak seimbang ketika pendapatan yang ditagih untuk suatu proyek diposting. |
| Manajemen proyek dan akuntansi | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | **Saat fitur Peningkatan** performa penjadwalan sumber daya proyek diaktifkan, nilai desimal salah dibulatkan untuk ketersediaan dan kapasitas sumber daya. |
| Manajemen proyek dan akuntansi | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | **Ketika fitur Buat perkiraan proyek menggunakan beberapa tugas** batch diaktifkan, pembuatan perkiraan dalam batch yang memiliki beberapa subtugas hanya berfungsi untuk periode saat ini. |
| Perjalanan dan Pengeluaran | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Kebijakan permintaan perjalanan diabaikan, dan alur kerja disetujui tanpa kesalahan. |
| Perjalanan dan Pengeluaran | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikasi Pengeluaran Seluler tidak menyimpan informasi berikut di jalur pengeluaran:</p><ul><li>ID proyek</li><li>Apakah biaya tersebut dapat ditagih</li><li>Nomor aktivitas</li></ul> |
| Perjalanan dan Pengeluaran | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Bidang **Tanda terima** terlampir diatur ke **Ya** meskipun tidak ada tanda terima yang dilampirkan ke baris pengeluaran. |
| Perjalanan dan Pengeluaran | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Kesalahan terjadi ketika Anda mengubah kategori pengeluaran menjadi **Pribadi**. |
| Perjalanan dan Pengeluaran | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Anda tidak dapat melampirkan tanda terima dan mengedit pengeluaran orang tua setelah transaksi kartu kredit dibagi menjadi pengeluaran pribadi. |
| Perjalanan dan Pengeluaran | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Kebijakan pengeluaran untuk transaksi antar perusahaan yang memiliki ID proyek tidak berfungsi dengan benar. |
| Perjalanan dan Pengeluaran | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informasi tanggal yang diposting tidak ada untuk laporan pengeluaran yang diposting. |
| Perjalanan dan Pengeluaran | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Ada masalah metode pembayaran di aplikasi seluler Pengeluaran. |
| Perjalanan dan Pengeluaran | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Permintaan perjalanan yang dibuat untuk satu pekerja dapat digunakan untuk laporan pengeluaran pekerja lain sebelum tanggal delegasi. |
| Perjalanan dan Pengeluaran | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Saat Anda membuat pengeluaran, perubahan pada nilai dimensi keuangan tidak diperbarui dengan benar pada tingkat distribusi akuntansi di **ruang kerja Manajemen** pengeluaran. |
| Perjalanan dan Pengeluaran | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status persetujuan baris pengeluaran utama tidak disinkronkan dengan status persetujuan alur kerja baris yang diperinci. |
| Perjalanan dan Pengeluaran | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Kesalahan terjadi jika Anda memposting laporan pengeluaran dan pemulihan pajak diaktifkan. |
| Perjalanan dan Pengeluaran | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegasi tidak dapat menghapus dokumen pengeluaran untuk karyawan yang diberhentikan. |
| Perjalanan dan Pengeluaran | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Penghapusan garis pengeluaran membutuhkan waktu lebih lama dari yang diharapkan dan memengaruhi kinerja. |
| Perjalanan dan Pengeluaran | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** menyebabkan catatan TaxUncommitted **yatim piatu**, karena hanya **SourceDocumentLine** yang dihapus. |
| Perjalanan dan Pengeluaran | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** tidak menghormati **trvExpTrans.ReferenceDataAreaId** untuk membuat urutan angka baru. |

## <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan peraturan untuk aplikasi keuangan dan operasi, lihat [Pembaruan peraturan](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan alat pencarian Masalah untuk melihat pembaruan peraturan yang direncanakan. Pencarian masalah memungkinkan Anda menelusuri menurut negara atau wilayah, jenis fitur, dan rilis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
