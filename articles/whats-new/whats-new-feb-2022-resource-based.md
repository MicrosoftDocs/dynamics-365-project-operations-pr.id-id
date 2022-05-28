---
title: Yang baru di bulan Februari 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Ini topik memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Operasi Proyek Februari 2022 untuk skenario berbasis sumber daya / non-stok.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600838"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Februari 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Ini topik berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Proyek dalam Dataverse versi lingkungan 4.28.0.120
- Manajemen proyek dan akuntansi dalam lingkungan Dynamics 365 Finance versi 10.0.24

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

- Pada rilis ini, Anda dapat menambahkan hingga 300 anggota tim ke satu proyek. Sebelumnya, batas jumlah anggota tim adalah 150. Untuk informasi selengkapnya, lihat [Batas proyek](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Pembaruan peta penulisan ganda Operasi Proyek

Daftar berikut menunjukkan peta dual-write yang telah dimodifikasi atau ditambahkan dalam rilis Project Operations Februari 2022.

| Peta entitas | Pembaruan versi | Komentar |
| --- | --- | --- |
| Proyek Operasi Operasi Proyek biaya entitas ekspor (msdyn\_ biaya) | 1.0.0.3 | Diperluas untuk sinkronisasi aktivitas proyek ke Dataverse. |

Untuk daftar saat ini dan versi peta penulisan ganda Operasi Proyek, lihat [Versi peta penulisan ganda Operasi Proyek](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel di luar kotak, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti petunjuk di kolom Tabel hilang di [bagian peta di bagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Tulis Ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan harga | 2415109 | Nilai default di **bidang Persyaratan** pembayaran operasi harus berupa catatan pelanggan kontrak proyek dan catatan faktur proforma. |
| Penagihan dan harga | 2497369 | Koreksi material harus mengikuti nilai tanggal dalam **parameter Koreksi**. |
| Penagihan dan harga | 2498697 | Meningkatkan konfigurasi keamanan untuk **penarikan entri Waktu**. |
| Penagihan dan harga | 2513824 | Untuk skenario berbasis sumber daya, ID kategori transaksi tidak boleh melebihi 28 karakter dalam Operasi Proyek. |
| Penagihan dan harga | 2517455 | Tindakan **transaksi** refresh invoice line tidak boleh dipicu beberapa kali secara bersamaan untuk invoice yang sama. |
| Penagihan dan harga | 2517465 | Tindakan **Nonaktifkan detail** baris faktur diblokir karena tidak didukung. |
| Penagihan dan harga | 2556660 | Memperbaiki pemeriksaan efektivitas tanggal yang dilakukan pada daftar harga yang dilampirkan ke catatan parameter proyek. |
|   Manajemen peluang | 2369202 | Mengoreksi logika bisnis yang memverifikasi bahwa daftar harga yang memiliki tanggal efisiensi yang tumpang tindih dapat dilampirkan ke kontrak proyek yang sama. |
|   Manajemen peluang | 2385965 | Mengoreksi perilaku pada tab Pelanggan di **halaman kontrak** Proyek saat **Anda memilih** Simpan dan tutup **.** |
| Waktu dan pengeluaran | 2538503 | Tugas proyek harus tersedia di **entitas aktual** Proyek setelah laporan pengeluaran diposting. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Selama impor catatan kredit vendor, terjadi kesalahan. Pesan kesalahan menyatakan, "Jumlah retainage tidak boleh lebih dari jumlah bersih yang tersisa." |
| Manajemen proyek dan akuntansi | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jika proposal faktur mencakup transaksi biaya nol jumlah yang merupakan aktual penjualan yang tidak ditagih, faktur tidak dapat terjadi. |
| Manajemen proyek dan akuntansi | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Biaya yang diposting tidak benar setelah harga pembelian diperbarui dan **Aktifkan manajemen** perubahan diaktifkan.|
| Manajemen proyek dan akuntansi | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Perkiraan posting untuk proyek harga tetap menggunakan mata uang dan jumlah yang salah dalam voucher perkiraan, bahkan ketika **fitur Aktifkan mata uang kontrak proyek untuk perhitungan** perkiraan diaktifkan. |
| Manajemen proyek dan akuntansi | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **Ekstensi\_ ProjDMFDataPopulation** tidak boleh melakukan panggilan untuk mengaktifkan pelacakan perubahan tanpa menangkap pengecualian untuk entitas yang memiliki kunci konfigurasi yang tidak diaktifkan. |
| Manajemen proyek dan akuntansi | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Pekerjaan batch diperbaiki ketika beberapa jurnal lanjutan diposting dan terjadi kesalahan. |
| Perjalanan dan Pengeluaran | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Karena masalah penyelesaian yang terkait dengan uang muka pada laporan pengeluaran, jumlah pajak tidak tercakup sebagai bagian dari uang muka. |
| Perjalanan dan Pengeluaran | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informasi pajak penjualan tidak termasuk dalam **laporan Transaksi Biaya - Pasca.**. |
| Perjalanan dan Pengeluaran | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Pelanggaran **kebijakan pengeluaran yang diperlukan** penerima tanda terima salah menunjukkan peringatan pada laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transaksi proyek tidak termasuk pajak penjualan yang tidak dapat dipulihkan dalam jumlah total penjualan ketika transaksi adalah hasil dari biaya mileage. |
| Perjalanan dan Pengeluaran | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Saat baris terperinci memiliki pajak, Anda tidak dapat mengubah tanggal baris itemisasi, dan kesalahan status dokumen sumber terjadi. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

Fitur [yang dihapus atau tidak digunakan lagi di Operasi](removed-depreciated-features-project.md) Proyek topik menjelaskan fitur yang telah dihapus atau tidak digunakan lagi untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan mungkin akan dihapus dalam pembaruan mendatang.

Pengumuman penghentian akan muncul di [fitur Yang dihapus atau tidak digunakan lagi di Operasi](removed-depreciated-features-project.md) Proyek topik 12 bulan sebelum fitur apa pun dihapus dari produk.

Untuk melanggar perubahan yang hanya mempengaruhi waktu kompilasi, tetapi kompatibel dengan sandbox dan lingkungan produksi, waktu penghentian akan kurang dari 12 bulan. Biasanya, perubahan ini adalah pembaruan fungsional yang harus dilakukan pada kompiler.
