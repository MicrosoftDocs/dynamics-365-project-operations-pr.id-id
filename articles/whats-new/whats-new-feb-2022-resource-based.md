---
title: Yang baru di bulan Februari 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis Februari 2022 penyebaran Project Operations Lite untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932990"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Februari 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.28.0.120
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.24

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

- Pada rilis ini, Anda dapat menambahkan hingga 300 anggota tim ke satu proyek. Sebelumnya, batas jumlah anggota tim adalah 150. Untuk informasi selengkapnya, lihat [batas proyek](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Daftar berikut menampilkan peta penulisan ganda yang telah dimodifikasi atau ditambahkan dalam rilis Project Operations Februari 2022.

| Peta entitas | Pembaruan versi | Komentar |
| --- | --- | --- |
| Entitas ekspor pengeluaran proyek integrasi Project Operations (msdyn\_expenses) | 1.0.0.3 | Diperluas untuk sinkronisasi aktivitas proyek ke Dataverse. |

Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan harga | 2415109 | Nilai default dalam bidang **persyaratan pembayaran Operasi** harus merupakan rekaman pelanggan kontrak proyek dan rekaman faktur proforma. |
| Penagihan dan harga | 2497369 | Koreksi bahan harus mengikuti nilai tanggal dalam parameter **Koreksi**. |
| Penagihan dan harga | 2498697 | Meningkatkan konfigurasi keamanan untuk **penarikan entri waktu**. |
| Penagihan dan harga | 2513824 | Untuk skenario berbasis sumber daya, ID kategori transaksi tidak boleh melebihi 28 karakter dalam Project Operations. |
| Penagihan dan harga | 2517455 | Tindakan **Segarkan transaksi baris faktur** tidak boleh dibolehkan dipicu beberapa kali bersamaan untuk faktur yang sama. |
| Penagihan dan harga | 2517465 | Tindakan **Nonaktifkan rincian baris faktur** diblokir karena tidak didukung. |
| Penagihan dan harga | 2556660 | Memperbaiki pemeriksaan efektivitas tanggal yang dilakukan pada daftar harga yang dilampirkan ke rekaman parameter proyek. |
|   Manajemen peluang | 2369202 | Mengoreksi logika bisnis yang memverifikasi bahwa daftar harga yang memiliki tanggal efektivitas tumpang tindih dapat dilampirkan ke kontrak proyek yang sama. |
|   Manajemen peluang | 2385965 | Mengoreksi perilaku pada tab **Pelanggan** pada halaman **kontrak proyek** saat Anda memilih **Simpan dan tutup**. |
| Waktu dan pengeluaran | 2538503 | Tugas proyek harus tersedia dalam entitas **aktual Proyek** setelah laporan pengeluaran diposting. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Selama impor nota kredit vendor, terjadi kesalahan. Pesan kesalahan menyatakan, "Jumlah ditahan tidak dapat lebih dari jumlah netto yang tersisa". |
| Manajemen proyek dan akuntansi | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jika proposal faktur mencakup transaksi biaya jumlah nol yang merupakan aktual penjualan belum tertagih, faktur tidak dapat terjadi. |
| Manajemen proyek dan akuntansi | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Biaya yang diposting tidak benar setelah harga pembelian diperbarui dan **Mengaktifkan manajemen perubahan** diaktifkan.|
| Manajemen proyek dan akuntansi | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Perkiraan posting untuk proyek harga tetap menggunakan mata uang dan jumlah yang salah dalam perkiraan voucher, bahkan saat fitur **Aktifkan mata uang kontrak proyek untuk perhitungan perkiraan** diaktifkan. |
| Manajemen proyek dan akuntansi | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** tidak boleh membuat panggilan untuk mengaktifkan pelacakan perubahan tanpa menangkap pengecualian untuk entitas yang memiliki tombol konfigurasi yang tidak diaktifkan. |
| Manajemen proyek dan akuntansi | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Pekerjaan kumpulan diperbaiki saat beberapa jurnal lanjutan diposting dan terjadi kesalahan. |
| Perjalanan dan Pengeluaran | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Karena masalah penyelesaian yang terkait dengan uang muka pada laporan pengeluaran, jumlah pajak tidak tercakup sebagai bagian dari uang muka. |
| Perjalanan dan Pengeluaran | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informasi pajak penjualan tidak tercakup dalam laporan **Pengeluaran - Transaksi yang diposting**. |
| Perjalanan dan Pengeluaran | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Pelanggaran kebijakan pengeluaran **Penerimaan Diperlukan** keliru menampilkan peringatan pada laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transaksi proyek tidak mencakup pajak penjualan yang tidak dapat dipulihkan dalam jumlah penjualan total saat transaksi merupakan hasil dari pengeluaran jarak tempuh. |
| Perjalanan dan Pengeluaran | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Bila baris terperinci memiliki pajak, Anda tidak dapat mengubah tanggal baris itemisasi dan terjadi kesalahan status dokumen sumber. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

artikel [Fitur yang dihilangkan atau tidak digunakan lagi di Project Operations](removed-depreciated-features-project.md) menjelaskan fitur yang telah dihilangkan atau ditolak untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan akan dihapus pada pembaruan mendatang.

Pengumuman pembatalan akan muncul dalam artikel [fitur yang Dihilangkan atau ditolak di Project Operations](removed-depreciated-features-project.md) 12 bulan sebelum fitur apa pun dihapus dari produk.

Untuk perubahan menonjol yang hanya mempengaruhi waktu kompilasi, namun merupakan biner yang kompatibel dengan lingkungan sandbox dan produksi, waktu deprekasi akan kurang dari 12 bulan. Biasanya, perubahan ini adalah pembaruan fungsi yang harus dibuat untuk kompiler.
