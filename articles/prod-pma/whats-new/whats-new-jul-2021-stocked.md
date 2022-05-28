---
title: Yang baru atau berubah di Project Operations, Juli 2021 untuk skenario berbasis stok/produksi
description: Topik ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam skenario Project Operations yang dirilis Pada Bulan Juli 2021 untuk skenario berbasis produksi/stok.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: db5bb27650d65bb68f45f95cb2562f4b773ddcea
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597066"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Yang baru atau berubah di Project Operations, Juli 2021 untuk skenario berbasis stok/produksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

- Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi 10.0.20
 
### <a name="quality-updates"></a>Pembaruan kualitas
                                                                                                                                                                                  
| Area fitur                      | Nomor Referensi| Pembaruan kualitas                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manajemen proyek dan akuntansi | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Rekaman komitmen biaya dari permintaan pembelian akan dihapus segera setelah pesanan pembelian dirilis dari edisi permintaan pembelian.                                                                           |
| Manajemen proyek dan akuntansi | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Validasi anggaran terjadi dua kali pada permintaan pembelian. Duplikasi ini berarti bahwa permintaan ulang tidak dapat ditutup dan pesanan pembelian terkait tidak dibuat.                                                                                                                        |
| Manajemen proyek dan akuntansi | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Aturan penagihan **Persentase untuk ditagih** tidak dapat diselesaikan karena masalah pembulatan.                                                                              |
| Manajemen proyek dan akuntansi | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Bila Anda menyesuaikan transaksi dan persentase memiliki desimal, biaya dan harga penjualan tidak disesuaikan dengan benar.                                      |
| Manajemen proyek dan akuntansi | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Penjelajah sumber akuntansi menampilkan jam untuk satu baris lembar waktu untuk beberapa baris lembar waktu dengan aktivitas yang berbeda.                                      |
| Manajemen proyek dan akuntansi | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Tampilan yang tersimpan dan personalisasi detail baris lembar waktu menyebabkan sistem selalu membuka rincian untuk lembar waktu pertama dalam daftar saat mencoba membuka lembar waktu.  |
| Manajemen proyek dan akuntansi | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Node root proyek akan hilang dan rekaman struktur rincian kerja dihapus setelah impor.                                                                                             |
| Manajemen proyek dan akuntansi | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Bila item diterima dan dikeluarkan sebagian dari kebutuhan item, sistem akan memperbarui keseimbangan pemakaian anggaran yang salah. |
| Manajemen proyek dan akuntansi | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Pesanan pembelian panjar tidak menampilkan total dengan benar di panel **Total** atau kisi **faktur Tertunda**.                                                                  |
| Manajemen proyek dan akuntansi | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Saat menutup inventaris, penyesuaian biaya item proyek diposting ke akun neraca, bukan akun laba dan rugi.                                                            |
| Manajemen proyek dan akuntansi | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Sebuah proyek mem-posting voucher transaksi dan memperkirakan penggunaan voucher USD sebagai mata uang akuntansi, namun jumlahnya menunjukkan jumlah yang setara dengan CAD.              |
| Manajemen proyek dan akuntansi | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Komitmen biaya dengan persyaratan item dan pesanan pembelian salah dalam proses faktur pesanan pembelian dengan tanda terima produk parsial dan faktur parsial.       |
| Manajemen proyek dan akuntansi | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Penyesuaian proyek tidak memperbarui jumlah penjualan dengan benar dengan biaya tidak langsung.                                                                                    |
| Manajemen proyek dan akuntansi | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabel **Lembar Waktu** tidak memiliki relasi yang ditentukan dengan tampilan **Pekerja/Sumber Daya**.                                                                                   |
| Manajemen proyek dan akuntansi | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Tidak dapat mengisi bidang **Nomor aktivitas** saat Anda memilihnya dari menu drop-down untuk lembar waktu antarperusahaan.                                                                 |
| Manajemen proyek dan akuntansi | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Anda tidak dapat menambahkan bidang **Tujuan** atau **Deskripsi Aktivitas** yang dipersonalkan ke halaman berikut: **Postingan Transaksi proyek**, **Pembuatan proposal faktur**, atau **Proposal faktur**.  |
| Manajemen proyek dan akuntansi | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Kontrol tanggal pengiriman yang salah diberikan saat Anda membuat persyaratan item dengan menggunakan manajemen data (**ProjSalesItemRequirementEntity**).                                              |
| Manajemen proyek dan akuntansi | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Bila Anda memilih ID kontrak proyek di Finance, lingkungan terintegrasi Project Operations akan membuka halaman untuk membuat rekaman baru, bukan membuka kontrak proyek yang ada.                                                                                                                 |
| Manajemen proyek dan akuntansi | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Label, "@SYS4083080" ("Tidak dapat menemukan rekaman Pekerja unik yang terkait dengan nilai yang dimasukkan") tidak diterjemahkan ke Denmark.                                |
| Manajemen proyek dan akuntansi | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Bidang **grup pajak penjualan Item** tidak dapat diedit di proposal faktur.                                                                               |
| Manajemen proyek dan akuntansi | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Komitmen Biaya dinyatakan berlebihan dengan jumlah pajak yang tidak dapat dikurangkan.                                                                                                    |
| Manajemen proyek dan akuntansi | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Memposting lembar waktu antarperusahaan dengan beberapa proyek dan dimensi keuangan yang berbeda menghasilkan nilai tidak terduga dalam buku besar umum.                             |
| Manajemen proyek dan akuntansi | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Baris proposal faktur diduplikasikan karena beberapa instans dari proses periodik, **Impor dari penahapan** yang berjalan pada waktu yang sama.                                      |
| Manajemen proyek dan akuntansi | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Terjadi kesalahan dalam posting proposal faktur nota kredit, sehingga transaksi pada voucher tidak seimbang.    |
| Manajemen proyek dan akuntansi | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Biaya komitmen proyek menjadi salah setelah faktur tertunda yang ditahan dirilis.                                                                             |
| Manajemen proyek dan akuntansi | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Anda tidak dapat membuat nota kredit untuk pesanan penjualan proyek bila pajak memiliki mata uang yang berbeda dari mata uang perusahaan.                                      |
| Manajemen proyek dan akuntansi | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Menghapus kontrak juga akan menghapus alamat yang terkait dengan pelanggan.                                                                                     |
| Manajemen proyek dan akuntansi | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Proposal faktur yang berasal dari koreksi transaksi waktu negatif tidak dapat diposting.                                                                    |
| Perjalanan dan Pengeluaran                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Pajak dihitung secara berbeda dalam laporan pengeluaran.                                                                                                                  |
| Perjalanan dan Pengeluaran                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Pembaruan rilis **DB72_Expense.updateTrvExpTransProjTransId()**   tidak memungkinkan **trvExpTrans.ReferenceDataAreaId** untuk membuat urutan nomor baru.                    |
| Perjalanan dan Pengeluaran                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Jumlah yang diberkas tidak ditampilkan dengan bidang wajib.                                                                                                             |
| Perjalanan dan Pengeluaran                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Peningkatan dalam kinerja melampirkan pengeluaran ke laporan pengeluaran menggunakan antarmuka pengguna Pengeluaran Nuansa Baru.                                                            |
| Perjalanan dan Pengeluaran                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Anda dapat menghapus laporan pengeluaran yang diposting.                                                                                           |
| Perjalanan dan Pengeluaran                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Pesan kebijakan Pengeluaran ditampilkan beberapa kali.                                                                                                       |
| Perjalanan dan Pengeluaran                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Bidang **Metode pembayaran** tercakup di panel **Pengeluaran baru**.                                                                                                      |
| Perjalanan dan Pengeluaran                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Alat **status dokumen Atur Ulang Pengeluaran** harus mengatur ulang status laporan pengeluaran menjadi **Draf** jika alur kerja tidak ditemukan. 

### <a name="regulatory-updates"></a>Pembaruan wajib
Untuk informasi tentang pembaruan peraturan untuk aplikasi Keuangan dan Operasi, lihat [Pembaruan peraturan](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke Lifecycle Services (LCS) dan melihat pembaruan peraturan yang telah direncanakan menggunakan alat pencarian Masalah. Pencarian Masalah memungkinkan Anda mencari berdasarkan negara, jenis fitur, dan rilis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
