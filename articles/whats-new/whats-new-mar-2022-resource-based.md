---
title: Yang baru di bulan Maret 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis Maret 2022 penyebaran Project Operations Lite untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910910"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Maret 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.30.0.99
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.25

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Uang saku kini didukung dalam ruang kerja pengeluaran modern yang baru dan konsep ulang. Perusahaan yang menggunakan uang saku dapat mengaktifkan fitur ini untuk memberikan cara mudah untuk pengguna mengajukan dan mendapatkan penggantian untuk biaya uang saku. Untuk informasi lebih lanjut lihat [pengeluaran uang saku](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Daftar berikut menampilkan peta penulisan ganda yang telah dimodifikasi atau ditambahkan dalam rilis Project Operations Maret 2022.

| **Peta entitas** | **Pembaruan versi** | **Komentar** |
| --- | --- | --- |
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Pemetaan diperbarui untuk selaras dengan entitas baris faktur vendor di Dataverse <br>Jangan aktifkan versi pemetaan 1.0.0.4. Aplikasi ini akan siap digunakan bersama lingkungan Finance versi 10.0.26 dalam pembaruan bulanan berikutnya. |

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Waktu dan pengeluaran | 2388011 | Tampilkan komentar penolakan untuk pemohon entri waktu selama persetujuan massal. |
| Perencanaan dan pelacakan proyek | 2495294 | Rincian proyek tidak boleh diedit pada halaman **rincian Tugas**. |
| Penagihan dan harga | 2499605 | Tahapan kontrak yang dibuat dari tahapan kuotasi tidak ditandai dengan benar sebagai hanya baca. |
| Perencanaan dan pelacakan proyek | 2506050 | Rangkaian operasi tetap tertunda selama satu jam jika tidak ada perubahan untuk disimpan. Rangkaian kemudian salah ditandai sebagai **Gagal**, padahal harus segera diselesaikan. |
| Penagihan dan harga | 2507401 | Unit kontrak default tidak dimasukkan dengan benar di proyek penembolokan yang salah. |
| Penagihan dan harga | 2541660 | **Validasi Pembuatan Pesanan Penjualan** di penulisan ganda harus hanya untuk pesanan berbasis proyek. |
| Penagihan dan harga | 2552745 | Pajak tidak dipecah antara pelanggan yang telah menyiapkan aturan penagihan terpisah. |
| Penagihan dan harga | 2558859 | memperbaiki pesan kesalahan saat dimensi harga disiapkan. |
| Penagihan dan harga | 2558933 | **Impor dari Estimasi Proyek** gagal saat **msdyn\_project** ditambahkan sebagai dimensi harga. |
| Penagihan dan harga | 2559101 | Penghapusan parameter proyek tidak diblokir dan menyebabkan masalah. |
|   Manajemen peluang | 2570390 | Plug-in penulisan ganda akan mendukung jenis akun pada kuotasi, pesanan, dan peluang sebagai **Pelanggan**, Meskipun jenis akun tersebut tidak benar. |
| Penagihan dan harga | 2586097 | Aktual biaya terbagi tidak dibalik saat proyek dihapus dari baris kontrak proyek. |
| Penagihan dan harga | 2589619 | Pajak bahan pilihan disebarkan ke aktual penjualan belum tertagih dan faktur. |
|   Manajemen peluang | 2594015 | Kuotasi tidak dapat ditutup sebagai menang untuk pelanggan yang memiliki persyaratan pembayaran **Net60**. |
| Perencanaan dan pelacakan proyek | 2595841 | Di Project for the Web, pengguna menerima pesan kesalahan tentang **msdyn\_actualstart** yang hilang ketika mereka membuat permintaan sumber daya baru. |
| Waktu dan Pengeluaran | 2602511 | Bidang **Ditolak oleh** untuk entri waktu menampilkan **Sistem** , bukan pengguna bernama sebagai penolak. |
| Waktu dan Pengeluaran | 2602528 | Pemberi izin proyek dapat menyetujui waktu pada proyek yang tidak terdaftar sebagai pemberi izin. |
| Penagihan dan harga | 2608550 | Faktur koreksi dapat dikonfirmasi meskipun tidak ada perubahan pada yang asli. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Terdapat ketidakcocokan antara Finance dan Project Operations pada panjang bidang **ID Kategori** yang diizinkan. |
| Manajemen proyek dan akuntansi | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Proyek harga tetap tidak dapat dihilangkan bila bidang **faktur cicilan** diatur ke **Laba dan Rugi** dan prinsip **persentase Diselesaikan** digunakan. |
| Manajemen proyek dan akuntansi | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Grup pajak penjualan default yang salah dimasukkan dari konfigurasi proyek pada baris pengeluaran di jurnal integrasi Project Operations. |
| Manajemen proyek dan akuntansi | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Anda tidak dapat mengedit dimensi header proposal faktur proyek dalam penyebaran terintegrasi dengan Project Operations. |
| Manajemen proyek dan akuntansi | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Faktur vendor antarperusahaan tidak boleh diintegrasikan dengan Dataverse. |
| Manajemen proyek dan akuntansi | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Terdapat ketidakcocokan pada saldo mata uang pelanggan dan mata uang pelaporan. |
| Manajemen proyek dan akuntansi | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Anda dapat memposting faktur proyek meskipun pelanggan ditahan untuk semua faktur. |
| Manajemen proyek dan akuntansi | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Tombol **Hapus semua baris** hilang dari proposal faktur proyek yang memiliki tampilan **Header** dan **Baris**. |
| Manajemen proyek dan akuntansi | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Ketika Anda memposting faktur vendor, kesalahan berikut terjadi: "Tanggal akuntansi untuk faktur harus dalam tahun akuntansi yang sama dengan pesanan pembelian terkait. Jalankan proses pemesanan pembelian akhir tahun atau ubah tanggal ke tahun akuntansi saat ini." |
| Perjalanan dan Pengeluaran | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Komitmen biaya untuk proyek tidak dirilis setelah permintaan perjalanan dengan komitmen biaya dirilis. |
| Perjalanan dan Pengeluaran | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kesalahan berikut terjadi saat Anda mengirimkan laporan pengeluaran "Pelacakan Stack: perusahaan tidak ada". |
| Perjalanan dan Pengeluaran | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | **ID Proyek** default tidak dimasukkan pada laporan pengeluaran saat parameter **Memerlukan aktivitas untuk jurnal** dipilih pada proyek. |
| Perjalanan dan Pengeluaran | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Tombol **Posting Pengeluaran** tidak berfungsi dengan benar dalam Project Operations untuk skenario sumber daya/non-persediaan. |
| Perjalanan dan Pengeluaran | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Ada masalah **Tarif per mil** untuk laporan pengeluaran jarak tempuh yang mencakup penumpang. |
| Perjalanan dan Pengeluaran | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Tingkat jarak tempuh pengeluaran untuk karyawan tidak dijumlahkan dengan benar bila dua jenis kendaraan yang berbeda digunakan dalam kategori pengeluaran **tingkat tarif jarak tempuh**. |
| Perjalanan dan Pengeluaran | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Pencarian untuk bidang **Proyek** pada baris permintaan perjalanan tidak memberikan daftar proyek yang benar. |
| Perjalanan dan Pengeluaran | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Jarak tempuh dalam tinjauan** menunjukkan peringatan pada laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Layanan pengenalan karakter optis (OCR) tanda terima tidak berfungsi karena masalah URL layanan OCR pengeluaran. |
| Perjalanan dan Pengeluaran | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ketika fitur **Kemampuan untuk membuat item pengeluaran berulang dengan cepat** diaktifkan, jumlah pada baris itemisasi di laporan pengeluaran mengubah jumlah setiap kali halaman **Itemizisasi** dibuka. |
| Perjalanan dan Pengeluaran | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Anda tidak dapat menghapus laporan pengeluaran bila daftar interim memiliki lebih dari satu pemberi izin. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

artikel [Fitur yang dihilangkan atau tidak digunakan lagi di Project Operations](removed-depreciated-features-project.md) menjelaskan fitur yang telah dihilangkan atau ditolak untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan akan dihapus pada pembaruan mendatang.

Pengumuman pembatalan akan muncul dalam artikel [fitur yang Dihilangkan atau ditolak di Project Operations](removed-depreciated-features-project.md) 12 bulan sebelum fitur apa pun dihapus dari produk.

Untuk perubahan menonjol yang hanya mempengaruhi waktu kompilasi, namun merupakan biner yang kompatibel dengan lingkungan sandbox dan produksi, waktu deprekasi akan kurang dari 12 bulan. Biasanya, perubahan ini adalah pembaruan fungsi yang harus dibuat untuk kompiler.
