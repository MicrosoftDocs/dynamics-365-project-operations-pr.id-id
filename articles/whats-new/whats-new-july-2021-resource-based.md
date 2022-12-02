---
title: Yang baru di bulan Juli 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam skenario Project Operations yang dirilis Pada Bulan Juli 2021 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c004a6adc265f8f02fc557700d9b88a174c221c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931702"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Juli 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Artikel ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

   - Project Operations di lingkungan Microsoft Dataverse versi 4.12.0.148 or 4.12.0.152.
   - Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.20.

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- Kemampuan bagi administrator untuk melihat log PSS dan log Rangkaian Operasi dari menu pengaturan. Log disimpan selama 90 hari.

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini.

Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta pada halaman **Penulisan ganda** pada kolom **Versi**. Aktifkan versi baru peta dengan memilih **versi peta Tabel**, memilih versi terbaru, lalu menyimpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Yang Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) di panduan pemecahan masalah Penulisan Ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| **Area fitur**              | **Nomor Referensi** | **Pembaruan kualitas**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Penagihan dan Harga           | 2224046              | Bidang **Kelas Transaksi** dapat diedit pada tab **Rincian Baris Kuotasi**, namun terkunci jika Anda bekerja dari halaman **Rincian Baris Kuotasi**.                                                                     |
| Penagihan dan Harga           | 2224400              | Tindakan **Tutup Kuotasi Sebagai Menang** gagal bila kuotasi tidak memiliki tahapan tanggal.                                                                                                                                    |
| Penagihan dan Harga           | 2234089              | Bila Anda memasukkan deskripsi produk secara manual, deskripsi produk akan dihapus setelah Anda memasukkan kuantitas untuk perkiraan bahan.                                                                                                                         |
| Penagihan dan Harga           | 2234100              | Kisi **Konfigurasi Penagihan Tugas** tidak mencakup kolom **Bahan** dan nilainya pada tab **Penagihan Tugas** proyek.                                                                                                       |
| Penagihan dan Harga           | 2277409              | ID produk tidak tersedia pada detail baris kontrak untuk baris jenis bahan.                                                                                                                                        |
| Penagihan dan Harga           | 2281728              | Membuat baris kontrak secara tidak perlu mengevaluasi ulang aktual yang menyebabkan peningkatan signifikan pada volume data yang mempengaruhi kinerja.                                                                                |
| Penagihan dan Harga           | 2298668              | Baris jurnal yang terkait dengan pengeluaran yang ditarik dan dihapus tidak akan dihilangkan.                                                                                                                                     |
| Penagihan dan Harga           | 2300192              | Bila beberapa pengguna mengedit faktur, rincian baris faktur baru dapat dibuat pada faktur terkonfirmasi.                                                                                   |
| Penagihan dan Harga           | 2301569              | Faktur tidak dapat dikoreksi jika panjar jumlah \$0 telah diterapkan.                                                                                                                                        |
| Penagihan dan Harga           | 2307965              | Kesalahan terjadi jika harga kategori dibuat dengan nilai yang tidak ada.                                                                                                                           |
| Penagihan dan Harga           | 2326870              | Kesalahan terjadi di **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** jika **producttypecode** nihil.                                                                            |
| Penagihan dan Harga           | 2332732              | Kesalahan terjadi jika tahapan baris kontrak dibuat tanpa baris pesanan.                                                                                                                |
| Perencanaan dan Pelacakan Proyek | 2181094              | API Penjadwalan Proyek sekarang mendukung Log PSS dan Log Rangkaian Operasi yang disimpan selama 90 hari.                                                                                                                  |
| Perencanaan dan Pelacakan Proyek | 2254201              | Label **Mode Jadwal** diperbarui dengan rincian yang mendeskripsikan logika default.                                                                                                                                      |
| Perencanaan dan Pelacakan Proyek | 2300252              | Cache respons **openProject** diperbarui dan mencakup pemilik token dalam kunci cache, **Url dasar**, dan **Url Segmen** sehingga **Url Permintaan** selalu dapat dibuat ulang jika **Url dasar** berubah. |
| Perencanaan dan Pelacakan Proyek | 2301312              | **msdyn_membershipstatus** telah dihilangkan dari tampilan **Team Member Proyek**.                                                                                                                                        |
| Perencanaan dan Pelacakan Proyek | 2302759              | Produk tidak perlu diambil pada tab **Penugasan Sumber Daya**, **Estimasi**, dan **Estimasi Pengeluaran**.                                                                                                        |
| Perencanaan dan Pelacakan Proyek | 2308050              | **CopyProject** gagal dengan kesalahan, "Gagal menyuruh token untuk berbicara ke layanan jarak jauh".                                                                                                                           |
| Perencanaan dan Pelacakan Proyek | 2322650              | Tampilan **Daftar Tugas Proyek** telah diperbarui untuk menampilkan tanggal tugas secara default.                                                                                                            |
| Perencanaan dan Pelacakan Proyek | 2327266              | **CopyProject** menghasilkan kesalahan, "Kunci tidak ditemukan dalam kamus" saat menyalin estimasi.                                                                                                      |
| Perencanaan dan Pelacakan Proyek | 2328123              | **CopyProject** menghasilkan kesalahan, "Gagal menyuruh token untuk berbicara ke layanan jarak jauh".                                                                                                                          |
| Perencanaan dan Pelacakan Proyek | 2336258              | **CopyProject** dengan keliru menyalin nama posisi sumber daya.                                                                                                                                                 |
| Penagihan dan Harga           | 2224476              | Bidang **Sumber Daya yang Dapat Dipesan** tidak di-default dengan benar ke pengguna yang masuk pada halaman **Penggunaan Bahan**.                                                                                                            |
| Manajemen sumber daya           | 2277249              | Kesalahan terjadi saat persyaratan sumber daya berbasis non-proyek diperbarui.                                                                                                            |
| Manajemen sumber daya           | 2323869              | Pemanfaatan sumber daya tidak mengenali sumber daya terfilter dengan benar.                                                                                                                                             |
| Waktu dan Pengeluaran              | 2176538              | Operator filter yang salah diterapkan ke kontrol **Entri Waktu**.                                                                                                                                                   |
| Waktu dan Pengeluaran              | 2177462              | Menghapus entri waktu di kisi tidak memperbarui status tombol **Kirim**, **Tarik**, **Hapus**, dan **Edit Entri** seperti yang diharapkan.                                                                                        |
| Waktu dan Pengeluaran              | 2299985              | **TimeEntriesImportSourceResourceAssignment** tidak mempertahankan waktu mulai/berakhir dari kontur penetapan.                                                                                                  |
| Waktu dan Pengeluaran              | 2318426              | Setelah entri waktu dikirim, bidang yang terkunci tetap dapat diedit.                                                                                                                                   |
| Waktu dan Pengeluaran              | 2323749              | Kesalahan terjadi saat pengeluaran dibuat dari tab **Terkait** sumber daya yang dapat dipesan.                                                                                                      |
| Waktu dan Pengeluaran              | 2327678              | Saat Anda membuat entri waktu dari tab **Terkait** dari sumber daya yang dapat dipesan, sumber daya induk tidak diteruskan ke kontrol entri waktu.                                                                            |
| Umum                       | 2296857              | Pelacakan progres untuk pekerjaan yang berjalan lama.                                                                                                                                                                        |
| Umum                       | 2253682              | Solusi penulisan ganda Project Operations tidak harus diinstal bila inti penulisan ganda diinstal di lingkungan tanpa solusi orkestrasi penulisan ganda.                                                |
| Umum                       | 2316420              | Penyediaan inti Project Service gagal jika unit bisnis pengguna aplikasi diubah.                                                                                                                     |
| Umum                       | 2376405              | Memperbaiki masalah pembaruan yang didorong penerbit (Pembaruan kualitas tersedia dalam versi 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur                      | Nomor Referensi | Pembaruan kualitas                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manajemen proyek dan akuntansi | 4620267          | Tidak dapat mempersonalkan formulir untuk menambahkan bidang **Tujuan** ke halaman **Postingan Transaksi proyek**, **Pembuatan proposal faktur**, dan **Proposal faktur**.                                                                                                                                                                                         |
| Manajemen proyek dan akuntansi | 4613449          | Bila Anda memilih ID kontrak proyek di Finance, lingkungan terintegrasi Project Operations akan membuka halaman untuk membuat rekaman baru, bukan halaman untuk kontrak proyek yang sudah dibuat.                                                                                                                                           |
| Manajemen proyek dan akuntansi | 4614445          | Di penyebaran skenario terintegrasi Project Operations, Anda tidak dapat mengedit bidang **grup pajak penjualan Item** di proposal faktur yang diimpor dari penahapan. Grup pajak penjualan item harus dapat diedit untuk proposal faktur terbuka dari semua jenis transaksi termasuk cicilan, jam, pengeluaran, biaya, dan item. |
| Manajemen proyek dan akuntansi |                  | Tidak dapat memposting proposal faktur yang berasal dari koreksi transaksi waktu negatif.                                                                                                                                                                                                                                              |
| Manajemen proyek dan akuntansi |                  | Baris proposal faktur diduplikasikan karena beberapa proses berkala **Impor dari penahapan** yang berjalan pada waktu yang sama.                                                                                                                                                                                                                |

