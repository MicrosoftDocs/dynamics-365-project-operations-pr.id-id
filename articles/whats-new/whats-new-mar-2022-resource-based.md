---
title: Yang baru di bulan Maret 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Ini topik memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Operasi Proyek Maret 2022 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600746"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Maret 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Ini topik berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Proyek dalam Dataverse versi lingkungan 4.30.0.99
- Manajemen proyek dan akuntansi dalam lingkungan Dynamics 365 Finance versi 10.0.25

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Per diem sekarang didukung di ruang kerja pengeluaran modern yang baru dan ditata ulang. Perusahaan yang menggunakan per diem dapat mengaktifkan fitur ini untuk memberi pengguna cara mudah untuk mengirimkan dan diganti untuk biaya per diem mereka. Untuk informasi lebih lanjut, lihat [Pengeluaran per diem](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Daftar berikut menunjukkan peta dual-write yang telah dimodifikasi atau ditambahkan dalam rilis Project Operations Maret 2022.

| **Peta entitas** | **Pembaruan versi** | **Komentar** |
| --- | --- | --- |
| Proyek Operasi integrasi proyek vendor faktur baris entitas ekspor msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Pemetaan diperbarui agar selaras dengan entitas baris faktur vendor di Dataverse. <br>Jangan aktifkan 1.0.0.4 versi pemetaan. Ini akan siap digunakan dalam kombinasi dengan lingkungan Keuangan versi 10.0.26 di pembaruan bulanan berikutnya. |

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel di luar kotak, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti petunjuk di kolom Tabel hilang di [bagian peta di bagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Tulis ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Waktu dan pengeluaran | 2388011 | Tampilkan komentar penolakan kepada pengirim entri waktu selama persetujuan massal. |
| Perencanaan dan pelacakan proyek | 2495294 | Detail proyek tidak boleh diedit di **halaman Detail** tugas. |
| Penagihan dan harga | 2499605 | Tonggak kontrak yang dibuat dari tonggak kutipan salah ditandai sebagai baca-saja. |
| Perencanaan dan pelacakan proyek | 2506050 | Set operasi tetap tertunda selama satu jam jika tidak ada perubahan untuk disimpan. Set kemudian salah ditandai sebagai **Gagal**, sedangkan itu harus segera diselesaikan. |
| Penagihan dan harga | 2507401 | Unit kontrak default salah dimasukkan pada proyek karena caching yang salah. |
| Penagihan dan harga | 2541660 | **Validasi** Pembuatan Pesanan Penjualan dalam penulisan ganda harus hanya untuk pesanan berbasis proyek. |
| Penagihan dan harga | 2552745 | Pajak tidak dibagi antara pelanggan yang telah menyiapkan aturan penagihan terpisah. |
| Penagihan dan harga | 2558859 | Pesan kesalahan yang ditingkatkan saat dimensi harga disiapkan. |
| Penagihan dan harga | 2558933 | **Impor dari Estimasi** Proyek gagal saat **proyek MSDYN\_** ditambahkan sebagai dimensi harga. |
| Penagihan dan harga | 2559101 | Penghapusan parameter proyek tidak diblokir dan menyebabkan masalah. |
|   Manajemen peluang | 2570390 | Plug-in dual-write memaksa jenis akun pada kutipan, pesanan, dan peluang untuk menjadi **Pelanggan**, bahkan ketika jenis akun itu tidak benar. |
| Penagihan dan harga | 2586097 | Split billed cost actuals tidak dibalik ketika sebuah proyek dihapus dari garis kontrak proyek. |
| Penagihan dan harga | 2589619 | Pajak atas materi penulisan disebarkan ke aktual penjualan dan faktur yang tidak ditagih. |
|   Manajemen peluang | 2594015 | Kutipan tidak dapat ditutup sebagai won untuk pelanggan yang memiliki **persyaratan pembayaran Net60**. |
| Perencanaan dan pelacakan proyek | 2595841 | Di Project for the Web, pengguna menerima pesan kesalahan tentang msdyn **actualstart\_ yang hilang** saat mereka membuat permintaan sumber daya baru. |
| Waktu dan Pengeluaran | 2602511 | Bidang **ditolak oleh** untuk entri waktu menunjukkan **Sistem**, bukan pengguna bernama sebagai penolak. |
| Waktu dan Pengeluaran | 2602528 | Pemberi persetujuan proyek dapat menyetujui waktu pada proyek di mana mereka tidak terdaftar sebagai pemberi persetujuan. |
| Penagihan dan harga | 2608550 | Faktur koreksi dapat dikonfirmasi meskipun tidak ada perubahan pada aslinya. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Ada ketidakcocokan antara Keuangan dan Operasi Proyek dalam panjang yang diizinkan dari **bidang ID** Kategori. |
| Manajemen proyek dan akuntansi | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Proyek harga tetap tidak dapat dihilangkan ketika **bidang Faktur** akun On diatur ke **Laba dan Rugi** dan **prinsip persentase** Selesai digunakan. |
| Manajemen proyek dan akuntansi | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Grup pajak penjualan default yang salah dimasukkan dari penyiapan proyek pada jalur pengeluaran di jurnal integrasi Operasi Proyek. |
| Manajemen proyek dan akuntansi | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Anda tidak dapat mengedit dimensi header proposal faktur proyek dalam penyebaran terintegrasi dengan Operasi Proyek. |
| Manajemen proyek dan akuntansi | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Faktur vendor antar perusahaan tidak boleh diintegrasikan dengan Dataverse. |
| Manajemen proyek dan akuntansi | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Ada ketidakcocokan dalam mata uang saldo pelanggan dan mata uang pelaporan. |
| Manajemen proyek dan akuntansi | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Anda dapat memposting faktur proyek bahkan jika pelanggan ditahan untuk semua faktur. |
| Manajemen proyek dan akuntansi | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Tombol **Hapus semua baris** hilang dari proposal faktur proyek yang memiliki **tampilan Header** dan **Lines**. |
| Manajemen proyek dan akuntansi | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Saat Anda memposting faktur vendor, kesalahan berikut terjadi: "Tanggal akuntansi untuk faktur harus berada di tahun akuntansi yang sama dengan pesanan yang dibeli terkait. Jalankan proses akhir tahun pesanan pembelian atau ubah tanggal ke tahun akuntansi saat ini. |
| Perjalanan dan Pengeluaran | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Biaya yang berkomitmen untuk sebuah proyek tidak dirilis setelah biaya komitmen permintaan perjalanan dirilis. |
| Perjalanan dan Pengeluaran | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kesalahan berikut terjadi saat Anda mengirimkan laporan pengeluaran: "Stack Trace: Perusahaan tidak ada." |
| Perjalanan dan Pengeluaran | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | ID Proyek default **tidak dimasukkan pada laporan pengeluaran saat** aktivitas Require untuk parameter jurnal **dipilih pada** proyek. |
| Perjalanan dan Pengeluaran | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Tombol **Pasca Pengeluaran** tidak berfungsi dengan benar di Operasi Proyek untuk skenario sumber daya/non-stok. |
| Perjalanan dan Pengeluaran | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Ada masalah dengan **Tarif per mil** untuk laporan biaya mileage yang mencakup penumpang. |
| Perjalanan dan Pengeluaran | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Tarif mileage biaya untuk karyawan tidak dijumlahkan dengan benar saat dua jenis kendaraan yang berbeda digunakan dalam **kategori biaya tingkat** mileage. |
| Perjalanan dan Pengeluaran | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Pencarian untuk **bidang Proyek** pada jalur permintaan perjalanan tidak mengembalikan daftar proyek yang benar. |
| Perjalanan dan Pengeluaran | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Mileage dalam ulasan** menunjukkan peringatan pada laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Layanan pengenalan karakter optik (OCR) tanda terima tidak berfungsi karena masalah dengan URL layanan OCR biaya. |
| Perjalanan dan Pengeluaran | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | **Ketika fitur Kemampuan untuk merinci pengeluaran berulang dengan cepat** diaktifkan, jumlah pada garis itemisasi pada laporan pengeluaran berubah jumlah setiap kali **halaman Itemize** dibuka. |
| Perjalanan dan Pengeluaran | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Anda tidak dapat menghapus laporan pengeluaran saat daftar interim memiliki lebih dari satu pemberi persetujuan. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

Fitur [yang dihapus atau tidak digunakan lagi di Operasi](removed-depreciated-features-project.md) Proyek topik menjelaskan fitur yang telah dihapus atau tidak digunakan lagi untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan mungkin akan dihapus dalam pembaruan mendatang.

Pengumuman penghentian akan muncul di [fitur Yang dihapus atau tidak digunakan lagi di Operasi](removed-depreciated-features-project.md) Proyek topik 12 bulan sebelum fitur apa pun dihapus dari produk.

Untuk melanggar perubahan yang hanya mempengaruhi waktu kompilasi, tetapi kompatibel dengan sandbox dan lingkungan produksi, waktu penghentian akan kurang dari 12 bulan. Biasanya, perubahan ini adalah pembaruan fungsional yang harus dilakukan pada kompiler.
