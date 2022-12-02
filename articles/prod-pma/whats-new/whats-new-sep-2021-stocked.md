---
title: Yang baru atau diubah di Project Operations, September 2021 untuk skenario berbasis stok/produksi
description: Artikel ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis September 2021 penyebaran Project Operations Lite untuk skenario berbasis produksi/stok.
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
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Yang baru atau diubah di Project Operations, September 2021 untuk skenario berbasis stok/produksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.21
 
## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
|---|---|---|
| Manajemen proyek dan akuntansi | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jika peran manajer pembelian diberikan akses ke satu entitas hukum, ia juga mendapatkan akses ke semua proyek di semua entitas hukum. |
| Manajemen proyek dan akuntansi | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Masalah pembulatan pajak Pertambahan Nilai (PPN) terjadi saat nota kredit diselesaikan dengan faktur proyek asli. |
| Manajemen proyek dan akuntansi | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Gunakan anggaran proyek alternatif untuk verifikasi anggaran. |
| Manajemen proyek dan akuntansi | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Grup harga **jam harga penjualan** tidak dihitung pada struktur perincian kerja untuk kuotasi proyek. |
| Manajemen proyek dan akuntansi | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Penghapusan estimasi gagal bila fitur **Aktifkan mata uang kontrak proyek untuk perhitungan perkiraan** diaktifkan. |
| Manajemen proyek dan akuntansi | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorisasi pajak penjualan berdasarkan kuantitas ditambahkan ke jumlah harga penjualan saat use tax digunakan di grup pajak penjualan dari jurnal pengeluaran proyek. |
| Manajemen proyek dan akuntansi | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Pajak kondisional tidak dihitung dengan benar untuk pembayaran terakhir saat penyimpanan vendor dan pembayaran di muka diterapkan ke faktur pesanan pembelian. |
| Manajemen proyek dan akuntansi | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Pelacakan penyesuaian tidak berfungsi untuk jurnal saldo Awal. |
| Manajemen proyek dan akuntansi | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Alokasi revisi anggaran proyek berdasarkan periode** dibagi ke seluruh periode anggaran. Saat alokasi diajukan, rekaman tidak dihapus. |
| Manajemen proyek dan akuntansi | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Posting Pekerjaan dalam proses (WIP) ke buku besar umum memiliki jumlah yang salah. |
| Manajemen proyek dan akuntansi | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Persetujuan jurnal jam proyek tidak berfungsi. |
| Manajemen proyek dan akuntansi | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Harga penjualan penyesuaian proyek tidak diperbarui dengan biaya tidak langsung saat batas dana tidak disebutkan. |
| Manajemen proyek dan akuntansi | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Persyaratan item tidak dapat dibuat saat header tabel Penjualan ditagihkan dan pesanan pembelian pendukung untuk baris yang ada telah diselesaikan. |
| Manajemen proyek dan akuntansi | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Jumlah penyimpanan untuk aturan penagihan yang memiliki tahapan untuk proyek lain tidak diposting dalam ID proyek terkait yang dipilih untuk tahapan. Namun diposting dengan proyek pertama. |
| Manajemen proyek dan akuntansi | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Ketika Anda memilih **Set Dimensi keuangan** pada proposal faktur, kesalahan berikut terjadi: "Tidak dapat mengonversikan objek jenis 'Dynamics.AX.Application.FormIntControl' to type 'Dynamics.AX.Application.FormStringControl'." |
| Manajemen proyek dan akuntansi | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Laporan **faktur proyek** melewatkan baris. |
| Manajemen proyek dan akuntansi | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Kesalahan terjadi saat Anda menghitung kontrol biaya untuk proyek investasi. |
| Manajemen proyek dan akuntansi | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metode **ProjTable::InitFromCustTable - canDeletePostalAddress** menyebabkan masalah performa. |
| Manajemen proyek dan akuntansi | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Pesan kesalahan harus lebih jelas daripada "Kesalahan tidak terduga". |
| Manajemen proyek dan akuntansi | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Pekerjaan batch posting faktur Proyek memproses dan memposting proposal faktur meskipun baris faktur belum dibuat. |
| Manajemen proyek dan akuntansi | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Masalah pembulatan terjadi saat kunci konfigurasi lisensi sektor publik dinonaktifkan. Biaya atau harga penjualan yang salah dibuat pada jam lembar waktu untuk kontrak yang memiliki beberapa sumber pendanaan. |
| Manajemen proyek dan akuntansi | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Harga penjualan proyek pada pesanan pembelian proyek yang ditagih telah salah dihitung ketika model harga penjualan adalah **Rasio Kontribusi**. |
| Manajemen proyek dan akuntansi | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem tidak mempertimbangkan hari aktif di antara saat menghitung tingkat tenaga kerja yang efektif untuk karyawan. |
| Manajemen proyek dan akuntansi | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Kesalahan posting terjadi di lembar waktu antarperusahaan karena kesalahan validasi berikut: "Tidak ada mitra perdagangan yang dikonfigurasi untuk entitas hukum." |
| Manajemen proyek dan akuntansi | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Deskripsi dari pesanan pembelian yang memiliki kategori pengeluaran tidak diambil dalam daftar transaksi proyek yang diposting. |
| Manajemen proyek dan akuntansi | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Ada konversi yang salah pada jurnal Item yang diposting ke proyek. |
| Manajemen proyek dan akuntansi | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Anda dapat mengkonfirmasikan pesanan pembelian meskipun batas dana telah terlampaui. |
| Manajemen proyek dan akuntansi | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Bagian **Koreksi/Batalkan faktur** di faktur teks bebas akan hilang saat ID proyek dipilih. |
| Manajemen proyek dan akuntansi | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Ada masalah performa saat proposal faktur proyek diposting dari pesanan penjualan proyek yang mencakup item persediaan. |
| Manajemen proyek dan akuntansi | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Faktur pembelian proyek tidak dapat diposting karena kesalahan berikut terjadi: "Fungsi AccDistProcessorPostingEktension.createForProjectRevenueLine telah dipanggil dengan keliru." |
| Manajemen proyek dan akuntansi | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Perbarui ke pembuatan pekerjaan batch perkiraan proyek untuk mendukung pelaksanaan beberapa sub-tugas. |
| Manajemen proyek dan akuntansi | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status lembar waktu tidak dapat diperbarui ke **Draf** saat alur kerja terjebak dalam status **Dibatalkan**. |
| Manajemen proyek dan akuntansi | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Jumlah penyimpanan tidak dihitung dalam proposal faktur nota kredit jika ada beberapa baris. |
| Manajemen proyek dan akuntansi | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Saat Anda mencoba mengubah jumlah faktur yang dihasilkan dari pesanan pembelian, kesalahan berikut terjadi: "Transaksi pada voucher tidak seimbang sesuai XX/XX/XXXX. (mata uang akuntansi: 0,00 - mata uang pelaporan: 0,01)." |
| Manajemen proyek dan akuntansi | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Ada masalah performa saat proposal faktur proyek diposting dalam mode neraca, karena bergabung dengan **GeneralJournalAccountEntry**. |
| Manajemen proyek dan akuntansi | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Ada masalah performa saat lembar waktu diposting. |
| Manajemen proyek dan akuntansi | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarki estimasi biaya dari struktur perincian pekerjaan dijajarkan dengan keliru setelah semua tugas diperluas atau setelah satu tugas diperluas secara manual. |
| Manajemen proyek dan akuntansi | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Template Excel kuotasi proyek tidak dapat ditambahkan ke menu **Buka di Excel**. |
| Manajemen proyek dan akuntansi | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Nomor pengecualian pajak untuk entitas hukum tidak disertakan pada faktur proyek cetak. |
| Manajemen proyek dan akuntansi | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Ada kesalahan Saat Anda menyesuaikan proyek terkait dengan baris kredit, Tidak ada data Keuangan yang diperbarui di unit inventaris. |
| Manajemen proyek dan akuntansi | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Setelah menerapkan KB 461935, Anda tidak dapat memposting estimasi jika beralih ke urutan angka terus-menerus. |
| Manajemen proyek dan akuntansi | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** menyebabkan aplikasi seluler Project timesheet untuk Android berhenti merespons. |
| Manajemen proyek dan akuntansi | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai WIP yang dikembalikan dari posting faktur berbeda dengan nilai WIP asli yang diposting dari entri waktu. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Dalam kasus panjar diterapkan, Transaksi voucher tidak seimbang ketika pendapatan yang ditagih untuk proyek diposting. |
| Manajemen proyek dan akuntansi | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Bila fitur **peningkatan performa penjadwalan sumber daya proyek** diaktifkan, nilai desimal tidak dibulatkan dengan benar untuk ketersediaan dan kapasitas sumber daya. |
| Manajemen proyek dan akuntansi | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Bila fitur **Buat estimasi proyek menggunakan beberapa tugas batch** diaktifkan, pembuatan estimasi dalam batch yang memiliki beberapa subtugas hanya berfungsi untuk periode saat ini. |
| Perjalanan dan Pengeluaran | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Kebijakan permintaan perjalanan diabaikan dan alur kerja disetujui tanpa kesalahan. |
| Perjalanan dan Pengeluaran | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikasi seluler Expense tidak menyimpan informasi berikut pada baris pengeluaran:</p><ul><li>ID proyek</li><li>Apakah pengeluaran dapat ditagih</li><li>Nomor Aktivitas</li></ul> |
| Perjalanan dan Pengeluaran | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Bidang **Tanda Terima Terlampir** diatur ke **Ya** meskipun tidak ada tanda terima terlampir ke baris pengeluaran. |
| Perjalanan dan Pengeluaran | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Kesalahan terjadi saat Anda mengubah kategori pengeluaran ke **Pribadi**. |
| Perjalanan dan Pengeluaran | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Setelah transaksi kartu kredit dipecah ke pengeluaran pribadi, Anda tidak dapat mengedit pengeluaran induk atau melampirkan tanda terima. |
| Perjalanan dan Pengeluaran | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Kebijakan pengeluaran untuk transaksi antar perusahaan yang memiliki ID Proyek tidak berfungsi dengan benar. |
| Perjalanan dan Pengeluaran | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informasi Tanggal posting tidak ditemukan untuk laporan pengeluaran yang diposting. |
| Perjalanan dan Pengeluaran | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Ada masalah metode pembayaran dalam aplikasi seluler Expense. |
| Perjalanan dan Pengeluaran | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Permintaan perjalanan yang dibuat untuk satu pekerja dapat digunakan untuk laporan pengeluaran pekerja lain sebelum tanggal delegasi. |
| Perjalanan dan Pengeluaran | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Saat Anda membuat pengeluaran, perubahan ke nilai dimensi keuangan tidak diperbarui dengan benar di tingkat distribusi akuntansi di ruang kerja **manajemen Pengeluaran**. |
| Perjalanan dan Pengeluaran | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status persetujuan baris pengeluaran utama tidak tersinkronisasi dengan status persetujuan alur kerja baris terperinci. |
| Perjalanan dan Pengeluaran | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Kesalahan terjadi jika Anda memposting laporan pengeluaran dan pemulihan pajak diaktifkan. |
| Perjalanan dan Pengeluaran | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegasi tidak dapat menghapus dokumen pengeluaran untuk karyawan yang diberhentikan. |
| Perjalanan dan Pengeluaran | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Penghapusan baris pengeluaran memerlukan waktu lebih lama dari yang diperkirakan dan mempengaruhi kinerja. |
| Perjalanan dan Pengeluaran | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** menyebabkan rekaman **TaxUncommitted** tak bertuan, hanya karena **SourceDocumentLine** dihapus. |
| Perjalanan dan Pengeluaran | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** tidak memperhatikan **trvExpTrans.ReferenceDataAreaId** untuk membuat urutan nomor baru. |

## <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan wajib untuk aplikasi keuangan dan operasi, lihat [pembaruan wajib](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan alat pencarian masalah untuk melihat pembaruan peraturan yang telah direncanakan. Pencarian Masalah memungkinkan Anda mencari berdasarkan negara atau kawasan, jenis fitur, dan rilis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
