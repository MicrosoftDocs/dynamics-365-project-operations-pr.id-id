---
title: Yang baru di Mei 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Pembaruan topik ini menyediakan informasi tentang pembaruan kualitas yang tersedia di rilis Project Operations Mei 2021 untuk skenario berbasis sumber daya/non stok.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07ae18faef6acb9d64b889bbfdba89de0c96a453
ms.sourcegitcommit: d48dce64f6c5b16db3250096715c9d9f92a81971
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083930"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di Mei 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

- Project Operations pada versi lingkungan Dynamics 365 Dataverse 4.10.0.186
- Manajemen proyek dan akuntansi di lingkungan aplikasi Finance and Operations versi 10.0.18

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- [Mode penjadwalan](../project-management/scheduling-modes.md): Manajer proyek dapat menentukan apakah proyek harus dikelola menggunakan durasi tetap, pekerjaan tetap, atau mode penjadwalan unit tetap.
- [Mengkonfigurasikan jarak tempuh menggunakan tingkat tarif jarak tempuh](../expense/set-up-mileage.md): Memperbarui tingkat jarak tempuh untuk laporan pengeluaran karyawan.

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Daftar berikut menampilkan peta penulisan ganda yang telah dimodifikasi atau ditambahkan dalam rilis Project Operations Mei 2021.

| Peta entitas | Pembaruan versi | Komentar |
| --- | --- | --- |
| Sumber dana proyek (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Mensinkronisasi persyaratan pembayaran pelanggan kontrak proyek. |
| Proposal faktur proyek V2 (faktur) | 1.0.0.3 | Mensinkronisasi persyaratan pembayaran faktur proforma. |
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Pembaruan kualitas |
| Projects V2 (msdyn\_projects) | 1.0.0.2 | Pembaruan kualitas |

Selalu jalankan versi peta terbaru di lingkungan Anda dan mengaktifkan semua peta tabel terkait saat memperbarui solusi Project Operations Dataverse dan versi solusi aplikasi Finance and Operations Anda. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta pada kolom  **Versi**  pada halaman  **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md).

Jika Anda menemui masalah saat memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan Harga | 2227635 | Nilai dalam **grup Unit** dan bidang **Unit** secara default dari produk di kisi **Estimasi Bahan**. |
| Penagihan dan Harga | 2234127 | Bidang **ID Tugas** sekarang diintegrasikan ke aktual proyek Dataverse saat faktur vendor diposting. |
| Penagihan dan Harga | 2235564 | Menyimpan baris jurnal memastikan bahwa mata uang yang ditampilkan di entri baris jurnal mencocokkan mata uang default ke baris setelah menyimpannya. |
| Penagihan dan Harga | 2246671 | Membuat transaksi yang tidak kena biaya selama pemfakturan membalik rekaman penjualan belum tertagih asli dan membuat rekaman penjualan belum tertagih baru sebagai tidak kena biaya. |
| Penagihan dan Harga | 2264042 | Koreksi faktur yang valid tidak boleh diblokir jika ada rincian koreksi faktur yang tidak valid di lingkungan. |
| Penagihan dan Harga | 2146367 | Pemetaan penulisan ganda header faktur proyek diperluas untuk mencakup persyaratan pembayaran. |
|   Manajemen peluang | 2086888 | Jangan tambahkan peran dan kategori yang dinonaktifkan sebelum Anda menyalin kuotasi ke peran dan kategori yang dikenakan biaya dari kuotasi yang baru disalin. |
|   Manajemen peluang | 2234376 | Bidang hanya baca menjadi abu-abu di kisi **Estimasi Bahan**. |
|   Manajemen peluang | 2238337 | Kuotasi berdasarkan kontak dapat disimpan meskipun tidak terkait dengan daftar harga proyek. |
|   Manajemen peluang | 2239810 | Menutup kuotasi sebagai kalah juga menutup proyek terkait dan membatalkan pemesanan apa pun. |
| Perencanaan dan Pelacakan Proyek | 2099559 | Menambahkan validasi tambahan untuk kesehatan sistem sebelum kisi **tugas Proyek** terbuka. |
| Perencanaan dan Pelacakan Proyek | 2178987 | Memperbaiki kesalahan sementara yang terjadi saat memilih **Tahapan Berikutnya** pada halaman **Proyek**. |
| Manajemen sumber daya | 2224817 | Fungsi untuk memperluas default pemesanan ke status pemesanan yang benar. |
| Entri waktu | 2202476 | Halaman **Entri Waktu** sekarang menggunakan kontrol kisi reaksi dan memperbaiki masalah seperti ketidaksejajaran kisi. |
| Entri waktu | 2223377 | Entri waktu disembunyikan dari bagian **Terkait** pada halaman **Sumber Daya yang Dapat Dipesan** untuk menghindari kebingungan tentang penggunaan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations untuk skenario berbasis sumber daya: tidak dapat mengkonversi ke menang karena kesalahan integrasi. |
| Manajemen proyek dan akuntansi | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations, kesalahan terjadi saat Anda mencoba mengaitkan baris kontrak ke ID proyek karena pemeriksaan tumpang tindih baris kontrak dan jenis transaksi. |
| Manajemen proyek dan akuntansi | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** mengatur alamat faktur sumber dana dari pelanggan yang berbeda. |
| Perjalanan dan Pengeluaran | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Kesalahan posting terkait konfigurasi jarak tempuh dapat terjadi. |
| Perjalanan dan Pengeluaran | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Fungsi, **Dipisah ke pribadi** tidak berfungsi untuk transaksi pengeluaran mata uang luar negeri. |
| Perjalanan dan Pengeluaran | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Nilai drop-down kategori pengeluaran menampilkan kategori yang salah untuk delegasi, meskipun merupakan sumber daya. |
| Perjalanan dan Pengeluaran | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Anda tidak dapat menyimpan laporan pengeluaran antarperusahaan karena kesalahan **validasi Sumber Daya/kategori**. |
| Perjalanan dan Pengeluaran | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Penghitungan tingkat jarak tempuh yang salah dalam posting laporan pengeluaran memiliki baris terpisah. |
| Perjalanan dan Pengeluaran | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Anda tidak dapat memposting laporan pengeluaran antarperusahaan ketika pajak penjualan disertakan dan jenis akun ofset pengimbang pada metode pembayaran adalah **Pekerja**. |
| Perjalanan dan Pengeluaran | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Kembalikan entitas data **TrvRequisitionLine** dan indeks unik terkait. |
| Perjalanan dan Pengeluaran | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Laporan pengeluaran mendukung pembuatan dan pembaruan baris dokumen sumber. |
| Perjalanan dan Pengeluaran | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Jurnal buku besar pembantu keliru ditampilkan dalam skenario antarperusahaan jika pajak penjualan diposting ke entitas hukum tujuan. |
| Perjalanan dan Pengeluaran | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: estimasi pengeluaran tidak akan dihapus dari Finance bila dihapus dari Dataverse. |
| Perjalanan dan Pengeluaran | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Bila kategori pengeluaran adalah kategori non-proyek, dimensi keuangan yang dipilih pada halaman **Pengeluaran** tidak disalin ke laporan pengeluaran. |
