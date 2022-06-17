---
title: Yang baru di bulan Maret 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Maret 2022 Operasi Proyek untuk skenario berbasis sumber daya/non-stok.
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

- Operasi Proyek dalam Dataverse versi lingkungan 4.30.0.99
- Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi 10.0.25

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Per diem sekarang didukung di ruang kerja pengeluaran modern yang baru dan dirancang ulang. Perusahaan yang menggunakan per diem dapat mengaktifkan fitur ini untuk memberi pengguna cara mudah untuk mengirimkan dan diganti untuk biaya per diem mereka. Untuk informasi selengkapnya, lihat [Biaya per diem](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Daftar berikut menunjukkan peta tulis ganda yang telah dimodifikasi atau ditambahkan dalam rilis Operasi Proyek Maret 2022.

| **Peta entitas** | **Pembaruan versi** | **Komentar** |
| --- | --- | --- |
| Proyek Operasi integrasi proyek vendor baris faktur baris ekspor entitas msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Pemetaan diperbarui untuk menyelaraskan dengan entitas baris faktur vendor di Dataverse. <br>Jangan aktifkan versi pemetaan 1.0.0.4. Ini akan siap digunakan dalam kombinasi dengan lingkungan Keuangan versi 10.0.26 dalam pembaruan bulanan berikutnya. |

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel out-of-box, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti instruksi di [bagian Kolom tabel hilang di](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) peta bagian Panduan pemecahan masalah penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Waktu dan pengeluaran | 2388011 | Tampilkan komentar penolakan kepada pengirim entri waktu selama persetujuan massal. |
| Perencanaan dan pelacakan proyek | 2495294 | Detail proyek tidak boleh dapat diedit di **halaman Detail** tugas. |
| Penagihan dan harga | 2499605 | Tonggak kontrak yang dibuat dari tonggak kutipan salah ditandai sebagai baca-saja. |
| Perencanaan dan pelacakan proyek | 2506050 | Set operasi tetap tertunda selama satu jam jika tidak ada perubahan untuk disimpan. Set kemudian ditandai secara salah sebagai **Gagal**, sedangkan itu harus segera diselesaikan. |
| Penagihan dan harga | 2507401 | Unit kontrak default salah dimasukkan pada proyek karena caching yang salah. |
| Penagihan dan harga | 2541660 | **Validasi** Pembuatan Pesanan Penjualan dalam penulisan ganda harus hanya untuk pesanan berbasis proyek. |
| Penagihan dan harga | 2552745 | Pajak tidak dibagi antara pelanggan yang telah menyiapkan aturan penagihan terpisah. |
| Penagihan dan harga | 2558859 | Pesan kesalahan yang ditingkatkan saat dimensi harga disiapkan. |
| Penagihan dan harga | 2558933 | **Impor dari Perkiraan** Proyek gagal ketika **proyek\_ msdyn** ditambahkan sebagai dimensi harga. |
| Penagihan dan harga | 2559101 | Penghapusan parameter proyek tidak diblokir dan menyebabkan masalah. |
|   Manajemen peluang | 2570390 | Plug-in tulis ganda memaksa jenis akun pada kutipan, pesanan, dan peluang untuk menjadi **Pelanggan**, bahkan ketika jenis akun itu tidak benar. |
| Penagihan dan harga | 2586097 | Biaya aktual yang ditagih terpisah tidak dibalik ketika proyek dihapus dari jalur kontrak proyek. |
| Penagihan dan harga | 2589619 | Pajak atas materi write-in disebarkan ke aktual penjualan yang tidak ditagih dan faktur. |
|   Manajemen peluang | 2594015 | Kutipan tidak dapat ditutup sebagai won untuk pelanggan yang memiliki **ketentuan pembayaran Net60**. |
| Perencanaan dan pelacakan proyek | 2595841 | Di Project for the Web, pengguna menerima pesan galat tentang msdyn **actualstart\_ yang hilang** saat mereka membuat permintaan sumber daya baru. |
| Waktu dan Pengeluaran | 2602511 | Bidang **Ditolak oleh** untuk entri waktu memperlihatkan **Sistem** alih-alih pengguna bernama sebagai penolak. |
| Waktu dan Pengeluaran | 2602528 | Pemberi persetujuan proyek dapat menyetujui waktu pada proyek yang tidak tercantum sebagai pemberi persetujuan. |
| Penagihan dan harga | 2608550 | Faktur koreksi dapat dikonfirmasi bahkan jika tidak ada perubahan pada aslinya. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Ada ketidakcocokan antara Keuangan dan Operasi Proyek dalam panjang yang **diizinkan dari bidang ID** Kategori. |
| Manajemen proyek dan akuntansi | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Proyek harga tetap tidak dapat dihilangkan ketika **bidang Faktur** pada akun diatur ke **Untung dan Rugi** dan **prinsip persentase** Selesai digunakan. |
| Manajemen proyek dan akuntansi | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Grup pajak penjualan default yang salah dimasukkan dari penyiapan proyek pada jalur pengeluaran di jurnal integrasi Operasi Proyek. |
| Manajemen proyek dan akuntansi | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Anda tidak dapat mengedit dimensi header proposal faktur proyek dalam penyebaran terintegrasi dengan Operasi Proyek. |
| Manajemen proyek dan akuntansi | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Faktur vendor antar perusahaan tidak boleh diintegrasikan dengan Dataverse. |
| Manajemen proyek dan akuntansi | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Ada ketidakcocokan dalam mata uang saldo pelanggan dan mata uang pelaporan. |
| Manajemen proyek dan akuntansi | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Anda dapat memposting faktur proyek meskipun pelanggan ditangguhkan untuk semua faktur. |
| Manajemen proyek dan akuntansi | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Tombol **Hapus semua baris** hilang dari proposal faktur proyek yang memiliki **tampilan Header** dan **Baris**. |
| Manajemen proyek dan akuntansi | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Ketika Anda memposting faktur vendor, kesalahan berikut terjadi: "Tanggal akuntansi untuk faktur harus dalam tahun akuntansi yang sama dengan pesanan yang dibeli terkait. Jalankan proses akhir tahun pesanan pembelian atau ubah tanggal ke tahun akuntansi saat ini." |
| Perjalanan dan Pengeluaran | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Biaya komitmen untuk sebuah proyek tidak dirilis setelah biaya komitmen permintaan perjalanan dilepaskan. |
| Perjalanan dan Pengeluaran | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kesalahan berikut terjadi ketika Anda mengirimkan laporan pengeluaran: "Stack Trace: Perusahaan tidak ada." |
| Perjalanan dan Pengeluaran | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | PROJECT ID **default** tidak dimasukkan pada laporan pengeluaran saat **parameter Require activity for journal** dipilih pada project. |
| Perjalanan dan Pengeluaran | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Tombol **Post Expenses** tidak berfungsi dengan benar di Project Operations untuk skenario resource/non-stocked. |
| Perjalanan dan Pengeluaran | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Ada masalah dengan **Tarif per mil** untuk laporan biaya jarak tempuh yang mencakup penumpang. |
| Perjalanan dan Pengeluaran | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Tarif jarak tempuh biaya untuk karyawan tidak ditotal dengan benar ketika dua jenis kendaraan yang berbeda digunakan dalam **kategori biaya tingkat** tarif Mileage. |
| Perjalanan dan Pengeluaran | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Pencarian untuk **bidang Proyek** pada jalur permintaan perjalanan tidak mengembalikan daftar proyek yang benar. |
| Perjalanan dan Pengeluaran | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Mileage dalam ulasan** menunjukkan peringatan pada laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Layanan pengenalan karakter optik (OCR) tanda terima tidak berfungsi karena masalah dengan URL layanan OCR biaya. |
| Perjalanan dan Pengeluaran | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | **Ketika fitur Kemampuan untuk merinci pengeluaran berulang dengan cepat** diaktifkan, jumlah pada baris itemisasi pada laporan pengeluaran berubah jumlah setiap kali **halaman Itemize** dibuka. |
| Perjalanan dan Pengeluaran | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Anda tidak dapat menghapus laporan pengeluaran jika daftar sementara memiliki lebih dari satu pemberi persetujuan. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

Artikel Fitur [yang dihapus atau tidak digunakan lagi dalam Operasi](removed-depreciated-features-project.md) Proyek menjelaskan fitur yang telah dihapus atau tidak digunakan lagi untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan mungkin akan dihapus di pembaruan mendatang.

Pengumuman penghentian akan muncul di [artikel Fitur yang dihapus atau tidak digunakan lagi di Operasi](removed-depreciated-features-project.md) Proyek 12 bulan sebelum fitur apa pun dihapus dari produk.

Untuk perubahan yang melanggar yang hanya memengaruhi waktu kompilasi, tetapi biner kompatibel dengan kotak pasir dan lingkungan produksi, waktu penghentian akan kurang dari 12 bulan. Biasanya, perubahan ini adalah pembaruan fungsional yang harus dilakukan pada kompiler.
