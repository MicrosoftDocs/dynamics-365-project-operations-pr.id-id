---
title: Pengaturan kontrak proyek
description: Topik ini memberikan informasi tentang bidang yang berdampak pada baris kontrak dan informasi tentang kontrak yang dirangkum di semua item baris.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4c04ff004febf3a07b329bf375e38acb43d19887
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277612"
---
# <a name="project-contract-settings"></a>Pengaturan kontrak proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini menyediakan informasi tentang bidang yang berlaku untuk seluruh kontrak proyek termasuk pengaturan yang mempengaruhi semua baris kontrak. Informasi tentang kontrak yang diringkas di seluruh item baris untuk mendorong KPI dari kontrak proyek juga disertakan.

Tabel berikut berisi daftar bidang pada kontrak proyek yang unik untuk Dynamics 365 Project Operations atau memiliki beberapa perubahan penting dalam perilaku dari perintah penjualan di Dynamics 365 Sales.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| Tipe | Tab **ringkasan** (tersembunyi) | Ini adalah bidang rangkaian pilihan dengan pilihan berikut:</br>- **berbasis Pekerjaan** (tersedia hanya bila Project Operations diinstal)</br>- **berbasis item** (tersedia hanya bila Project Operations dan Sales diinstal)</br>- **Berbasis pemeliharaan layanan** (tersedia saat Dynamics 365 Field Service diinstal) | Dalam Project Operations, nilai bidang ini di-default ke **berbasis pekerjaan**, dan mengklasifikasikan kontrak sebagai kontrak berbasis proyek. Kontrak harus berbasis proyek untuk memungkinkan semua ekstensi dan fungsi khusus proyek. |
| Perusahaan Pemilik | tab **Ringkasan** | Entitas hukum yang memperhitungkan biaya dan pendapatan yang Diperoleh dari proyek yang terkait dengan kontrak proyek ini. Ketika kontrak dibuat dari kuotasi, bidang ini disalin dari bidang yang sesuai pada rekaman kuotasi. | Perusahaan pemilik setara dengan konsep entitas hukum dalam modul **manajemen proyek dan akuntansi** Project Operations. Semua biaya dan pendapatan yang Diperoleh dari proyek ini akan diperhitungkan dalam buku besar perusahaan pemilik. |
| Pelanggan | tab **Ringkasan** | Referensi pada perusahaan atau rekaman akun pelanggan. Ketika kontrak dibuat dari kuotasi, bidang ini disalin dari bidang yang sesuai pada rekaman kuotasi. | Mata uang pada default kontrak proyek berdasarkan mata uang pelanggan. Mata uang dapat diubah sebelum kontrak disimpan. |
| Manajer Akun | tab **Ringkasan** | Nama Manajer akun untuk penawaran ini. Ketika kontrak dibuat dari kuotasi, bidang ini disalin dari bidang yang sesuai pada rekaman kuotasi. | Manajer akun bertanggung jawab untuk mengelola hubungan dengan pelanggan melalui penyelesaian proyek ini. Berdasarkan rekaman sumber daya yang dapat dipesan terkait dengan manajer akun, unit kontrak ter-default pada kontrak proyek. |
| Unit Kontrak | tab **Ringkasan** | Unit organisasi yang bertanggung jawab atas pengiriman proyek yang terkait dengan kontrak ini. Ketika kontrak dibuat dari kuotasi, bidang ini disalin dari bidang yang sesuai pada rekaman kuotasi. | Unit kontrak adalah divisi perusahaan yang akan melaksanakan proyek. Setiap unit kontrak memiliki mata uang, dan mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang timbul selama proyek. |
| Daftar Harga Produk | tab **Ringkasan** | Daftar harga ini digunakan untuk default harga pada baris kontrak berdasarkan produk. Daftar pilihan tarik-turun untuk bidang ini menampilkan daftar daftar harga dengan mata uang daftar harga yang sesuai dengan mata uang pada kontrak. Ketika kontrak dibuat dari kuotasi, bidang ini disalin dari bidang yang sesuai pada rekaman kuotasi. Di kontrak proyek, bidang ini diatur default dari rekaman akun namun dapat diubah. | Tidak ada relevansi hilir untuk bidang ini. |
| Mata uang | tab **Ringkasan** | Mata uang yang digunakan untuk melaporkan nilai transaksi ini dan mata uang di mana pelanggan akan ditagih. Ketika kontrak dibuat dari kuotasi, bidang ini disalin dari bidang yang sesuai pada rekaman kuotasi. Di kontrak proyek, bidang ini diatur default dari rekaman akun namun dapat diubah. | Setelah kontrak disimpan, bidang ini tidak lagi dapat diedit. Bidang ini digunakan untuk men-default daftar harga proyek dan produk di kontrak. Mata uang pada kontrak digunakan untuk disesuaikan dengan mata uang pada daftar harga. |
| Batas Jangan terlampaui | tab **Ringkasan** | Bidang ini menunjukkan batas negosiasi tentang nilai akhir yang disepakati pelanggan untuk penawaran ini. | Batas ini dievaluasi selama eksekusi dan berlaku di semua item baris dan proyek yang terkait dengan transaksi ini. |
| Tanggal Pengiriman yang Diminta | tab **Ringkasan** | Ketika kontrak dibuat dari kuotasi proyek, bidang ini disalin dari bidang yang sesuai pada rekaman kuotasi proyek. | Tanggal ini digunakan sebagai tanggal akhir untuk membuat jadwal faktur. |

KPI berikut tersedia di tab **kinerja kontrak** pada kontrak proyek.

| Bidang | Lokasi | KETERANGAN |
| --- | --- | --- |
| Nilai Kontrak | Kontrak keseluruhan | Nilai total kontrak proyek. |
| Jumlah yang Ditagih | Kontrak keseluruhan | Jumlah dari nilai pada semua faktur terhadap kontrak ini. |
| Biaya Dikenakan | Kontrak keseluruhan | Jumlah semua aktual biaya yang dicatat pada semua proyek yang dipetakan ke kontrak. |
| Margin Kotor | Kontrak keseluruhan | Jumlah ditagih-biaya yang timbul hingga tanggal/jumlah ditagih |
| Margin yang Diharapkan | Kontrak keseluruhan | (Nilai kontrak - Estimasi biaya)/Estimasi biaya nilai kontrak = jumlah semua estimasi biaya pada semua proyek yang dipetakan ke kontrak.|
| Nilai Kontrak | Baris berbasis proyek | Nilai baris kontrak. |
| Jumlah yang Ditagih | Baris berbasis proyek | Untuk baris kontrak harga tetap: jumlah dari nilai pada semua aktual tonggak penjualan yang ditagih pada baris kontrak ini pada berbagai faktur yang dibuat untuk kontrak ini. Untuk baris kontrak waktu dan bahan: jumlah dari nilai pada semua aktual yang ditagih dan kena biaya pada baris kontrak ini pada berbagai faktur yang dibuat untuk kontrak ini. |
| Biaya Dikenakan | Baris berbasis proyek | Jumlah semua aktual biaya yang dicatat pada semua proyek yang dipetakan ke baris kontrak. |
| Margin Kotor | Baris berbasis proyek | (Jumlah ditagih-biaya yang timbul hingga tanggal)/jumlah ditagih |
| Margin yang Diharapkan | Baris berbasis proyek | (Jumlah baris kontrak dalam mata uang dasar - Estimasi biaya untuk baris kontrak dalam mata uang dasar)/jumlah baris kontrak dalam mata uang dasar |
| Biaya Dikenakan | Detail baris berbasis proyek | Waktu: Jumlah nilai di aktual biaya waktu yang dicatat untuk peran ini pada proyek yang dipetakan ke baris kontrak ini. Pengeluaran: Jumlah nilai di semua aktual biaya waktu pengeluaran yang dicatat untuk kategori ini pada proyek yang dipetakan ke baris kontrak ini. |
| Kuantitas Tercatat | Detail baris berbasis proyek | Waktu: Semua kuantitas waktu pada aktual biaya waktu untuk peran pada proyek yang dipetakan ke baris kontrak ini. Pengeluaran: Semua kuantitas untuk kategori pengeluaran ini pada aktual biaya pengeluaran di proyek dipetakan ke baris kontrak ini. |
| Jumlah yang Ditagih | Detail baris berbasis proyek | Untuk baris kontrak harga tetap, bidang ini dibiarkan kosong pada tingkat detail dan hanya ditampilkan pada tingkat baris kontrak. Untuk baris kontrak waktu dan material, penghitungan diselesaikan pada tingkat rincian. Rincian menunjukkan jumlah dari nilai pada semua baris pendapatan yang ditagih terhadap baris kontrak ini yang dikenakan biaya. |
| Kuantitas yang Ditagih | Detail baris berbasis proyek | Untuk baris kontrak harga tetap, bidang ini dibiarkan kosong pada tingkat detail dan hanya ditampilkan pada tingkat baris kontrak. Untuk baris kontrak waktu dan material, penghitungan diselesaikan pada tingkat rincian untuk waktu dan pengeluaran. Waktu: jumlah jam pada semua baris pendapatan yang ditagih untuk peran ini terhadap baris kontrak ini yang dikenakan biaya. Pengeluaran: Semua kuantitas untuk kategori pengeluaran ini pada aktual biaya pengeluaran di proyek dipetakan ke baris kontrak ini. |
| Nilai Kontrak | Baris berbasis produk | Nilai baris kontrak dari baris kontrak berbasis produk ini. |
| Jumlah yang Ditagih | Baris berbasis produk | Jumlah dari nilai pada semua baris faktur terhadap baris kontrak berbasis produk ini pada berbagai faktur yang dibuat untuk kontrak ini. |
| Biaya Dikenakan | Baris berbasis produk | Jumlah semua aktual biaya yang dicatat untuk baris kontrak berbasis produk. |
| Margin Kotor | Baris berbasis proyek | Jumlah ditagih-biaya yang timbul hingga tanggal/jumlah ditagih |
| Margin yang Diharapkan | Baris berbasis produk | (Nilai baris kontrak - Estimasi biaya untuk baris kontrak)/nilai baris kontrak |


[!INCLUDE[footer-include](../includes/footer-banner.md)]