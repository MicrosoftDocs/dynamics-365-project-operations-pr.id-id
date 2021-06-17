---
title: Yang baru di bulan November 2020 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Topik ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis November 2020 penyebaran Project Operations Lite untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f6b14a1cbe7f3d41c86aedaf863434214f911eaa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995625"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan November 2020 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

- Lingkungan Project Operations di CDS versi 4.4.0.70
- Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi version 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Pembaruan ke Project Operations untuk skenario berbasis sumber daya/tanpa stok

### <a name="project-operations-on-cds"></a>Project Operations di CDS

| Area fitur                 | Nomor Referensi | Pembaruan kualitas                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Manajemen peluang       | 2036993          | Baris estimasi dan baris kontrak penetapan sumber daya diperbarui saat memenangkan kuotasi saat jenis baris kuotasi adalah **semua tugas**.                                                 |
| Penagihan dan harga          | 2070392          | Baris kontrak proyek pada faktur meningkat setiap kali **Segarkan transaksi faktur** dipilih.                                                                         |
| Perencanaan proyek             | 2043336          | Tidak dapat menghapus rekaman anggota tim proyek.                                                                                                                                  |
| Perencanaan proyek             | 2046013          | Perilaku yang tidak konsisten untuk kolom Tag estimasi selama beban vs. pada perubahan jenis fase waktu.                                                                                   |
| Perencanaan proyek             | 2046647          | Waktu mulai dan berakhir nonaktif satu jam bila persyaratan sumber daya dihasilkan dari anggota tim proyek.                                                                      |
| Perencanaan proyek             | 2053879          | (Per peluncuran CDS mendatang) PublishUnassignedAssignments melanggar upaya untuk menyimpan tugas ketika kesalahan, "nilai yang dilewatkan untuk ConditionOperator.In kosong".                       |
| Perencanaan proyek             | 2055501          | Meninggalkan **tanggal mulai proyek** kosong menyebabkan kegagalan dalam jadwal.                                                                                                      |
| Perencanaan proyek             | 2066817          | Tidak dapat membuat sumber daya umum menggunakan pemilih orang pada tab **tugas**.                                                                                                   |
| Perencanaan proyek             | 2067034          | Tombol **Lihat rincian** tidak tersedia di halaman **rincian tugas**.                                                                                                       |
| Manajemen sumber daya          | 2046667          | Anggota tim umum tidak dihapus bahkan setelah semua sumber daya terpenuhi.                                                                                                    |
| Entri pengeluaran cepat dan waktu | 2047499          | Tombol **baru** pada halaman entri waktu akan membuka halaman **tanda tangan email baru**.                                                                                               |
| Entri pengeluaran cepat dan waktu | 2059859          | Pop-up tidak terduga dibuka saat membuat entri pengeluaran.                                                                                                                         |
| Lainnya                        | 2044181          | (Menghapus instalasi pesanan pembelian) Saat Anda mencoba untuk menghapus instalasi solusi inti layanan msdyn_ProjectServiceCore_Patch dan msdyn Project Service, kesalahan "Rekaman tidak tersedia"terjadi.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur        | Nomor Referensi | Pembaruan kualitas                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengakuan pendapatan | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Persentase estimasi proyek selesai salah ketika kontrak menggunakan mata uang asing dan persentase kemajuan kerja untuk metode yang lengkap.                     |
| Pengakuan pendapatan | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Tidak dapat memposting perkiraan dengan metode penyelesaian **biaya yang sebenarnya**.                                                                                                    |
| Pengakuan pendapatan | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminasi gagal karena kesalahan ketidakseimbangan voucher saat mata uang perusahaan dan mata uang transaksi berbeda.                                              |
| Manajemen pengeluaran  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Untuk pengguna non-admin, nilai pencarian untuk kolom baris pengeluaran seperti **id proyek** dan **kategori pengeluaran** tidak ditampilkan dengan benar dalam bingkai konektor data. |
| Manajemen pengeluaran  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Default properti baris tidak ditampilkan untuk kategori pengeluaran.                                                                                                         |
| Manajemen pengeluaran  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integrasi pengeluaran harus mencakup properti baris dari laporan pengeluaran.                                                                                             |
| Faktur           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Tidak dapat memposting proposal faktur proyek karena pesan kesalahan yang menyatakan bahwa kombinasi FD tidak divalidasi.                                                    |
| Faktur           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Tidak dapat melihat transaksi dari halaman rincian **faktur**.                                                                                                              |
| Faktur           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Baris proposal faktur dapat dihapus.                                                                                                                                  |
| Akuntansi proyek  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Item menu **Perkiraan** tidak dapat dilihat di halaman daftar **proyek**.                                                                                                   |
| Akuntansi proyek  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Tidak dapat membuka **Pernyataan proyek**   > **transaksi dan perkiraan**.                                                                                                       |
| Akuntansi proyek  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Menyesuaikan akuntansi** tidak diaktifkan untuk transaksi proyek yang ditagih.                                                                                                  |
| Akuntansi proyek  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Rincian akuntansi tidak disertakan pada tabel **ProjCDSActualsImport** ketika jurnal **integrasi**   diposting.                                                  |
| Akuntansi proyek  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Entri perkiraan proyek ganda saat Anda menghapus dan kemudian menyesuaikan penetapan sumber daya.                                                                            |
| Akuntansi proyek  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Memilih tautan ID proyek tidak membuka URL tautan dalam CDS.                                                                                                         |
| Akuntansi proyek  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Tidak dapat memperbarui tanggal mulai pada tugas di CDS.                                                                                                                           |
| Akuntansi proyek  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Mengaktifkan fitur, beberapa baris kontrak tidak dimungkinkan tanpa integrasi CDS.                                                                                   |

### <a name="regulatory-updates"></a>Pembaruan wajib
Untuk informasi tentang pembaruan wajib untuk aplikasi Finance and Operations, lihat [pembaruan wajib](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke LCS dan melihat pembaruan regulasi yang direncanakan dengan menggunakan alat pencarian Masalah. Pencarian Masalah memungkinkan Anda mencari berdasarkan negara, jenis fitur, dan rilis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]