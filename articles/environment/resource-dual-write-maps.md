---
title: Versi peta penulisan ganda Project Operations
description: Daftar topik ini menyediakan daftar peta penulisan ganda yang diperlukan untuk Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938998"
---
# <a name="project-operations-dual-write-map-versions"></a>Versi peta penulisan ganda Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Menggunakan Dynamics 365 Project Operations untuk skenario sumber daya/non-stok memerlukan rangkaian peta penulisan ganda untuk dijalankan di lingkungan. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Peta prasyarat: Solusi orkestrasi penulisan ganda

Peta berikut adalah prasyarat yang diperlukan untuk solusi Project Operations. Pastikan untuk menjalankan peta yang terdaftar di tabel berikut dan peta tabel terkait di lingkungan Anda.

| Peta tabel | Sinkronisasi awal |
| --- | --- |
| Buku Besar (msdyn_ledgers) | Memerlukan sinkronisasi awal untuk peta tabel dan semua prasyarat. Master untuk sinkronisasi awal adalah aplikasi Finance and Operations. |
| Entitas hukum (cdm_companies) | Tidak wajib. Sistem akan mengisi entitas ini secara otomatis bila lingkungan ditautkan menggunakan penulisan ganda. |
| Pelanggan V3 (akun) | Tidak diperlukan untuk provisi. |
| Vendor V2 (msdyn_vendors) | Tidak diperlukan untuk provisi. |

1. Dari daftar peta, pilih peta buku besar **(msdyn\_ledgers)** dengan semua prasyarat dan pilih kotak centang **Sinkronisasi awal**. Pada bidang **Master untuk sinkronisasi awal**, pilih **aplikasi Finance and Operations** untuk peta buku besar dan semua peta prasyarat. Pilih **Jalankan**.

![Sinkronisasi peta buku besar](media/DW6.png)

1. Ikuti langkah-langkah yang sama untuk semua peta tabel tersisa yang tercantum pada tabel di atas. Jangan pilih kotak centang **Sinkronisasi awal** saat menjalankan peta tersebut.

## <a name="project-operations-dual-write-maps"></a>Peta Penulisan Ganda Project Operations

Peta berikut adalah diperlukan untuk solusi Project Operations.

| **Peta entitas** | **Versi terbaru** | **Sinkronisasi awal** |
| --- | --- | --- |
| Entitas integrasi untuk Relasi transaksi proyek (msdyn\_transactionconnections) | 1.0.0.0 | Tidak diperlukan untuk provisi. |
| Header kontrak proyek (pesanan penjualan) | 1.0.0.1 | Tidak diperlukan untuk provisi. |
| Baris kontrak proyek (salesorderdetails) | 1.0.0.0 | Tidak diperlukan untuk provisi. |
| Sumber dana proyek (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Tidak diperlukan untuk provisi. |
| Tabel integrasi Project Operations untuk estimasi bahan (msdyn\_estimatelines) | 1.0.0.0 | Tidak diperlukan untuk provisi. |
| Proposal faktur proyek V2 (faktur) | 1.0.0.2 | Tidak diperlukan untuk provisi. |
| Aktual Integrasi Project Operations (msdyn_actuals) | 1.0.0.14 | Tidak diperlukan untuk provisi. |
| Baris kontrak integrasi Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Tidak diperlukan untuk provisi. |
| Entitas integrasi Project Operations untuk estimasi pengeluaran (msdyn_estimateslines) | 1.0.0.2 | Tidak diperlukan untuk provisi. |
| Entitas integrasi Project Operations untuk estimasi jam (msdyn_resourceassignments) | 1.0.0.5 | Tidak diperlukan untuk provisi. |
| Entitas ekspor kategori pengeluaran proyek integrasi Project Operations (msdyn_expensecategories) | 1.0.0.2 | Tidak diperlukan untuk provisi. |
| Entitas ekspor pengeluaran proyek integrasi Project Operations (msdyn_expenses) | 1.0.0.2 | Tidak diperlukan untuk provisi. |
| Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Tidak diperlukan untuk provisi. |
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Tidak diperlukan untuk provisi. |
| Peran sumber daya proyek untuk semua perusahaan (bookableresourcecategories) | 1.0.0.1 | Memerlukan sinkronisasi awal untuk peta tabel agar dapat mensinkronisasi peran sumber daya Manajer Proyek dan anggota Tim yang diisi di lingkungan Dynamics 365 Dataverse selama provisi. Dataverse adalah sumber utama untuk sinkronisasi awal. |
| Tugas proyek (msdyn_projecttasks) | 1.0.0.4 | Tidak diperlukan untuk provisi. |
| Kategori transaksi proyek (msdyn_transactioncategories) | 1.0.0.0 | Tidak diperlukan untuk provisi. |
| Project V2 (msdyn_projects) | 1.0.0.1 | Tidak diperlukan untuk provisi. |

Selesaikan langkah-langkah berikut untuk menjalankan peta yang terdaftar.

1. Aktifkan peran sumber daya proyek untuk **semua peta tabel perusahaan (bookableresourcecategories)** karena peta ini memerlukan sinkronisasi awal. Pada bidang **Master untuk sinkronisasi awal**, pilih **Common Data Service**. 

 ![Sinkronisasi peta tabel peran sumber daya](media/6ResourceInitialSync.jpg)

 Tunggu hingga status peta **berjalan** sebelum Anda beralih ke langkah berikutnya.

2. Pilih semua peta yang tersisa yang diperlukan. Anda dapat memfilternya dalam daftar peta penulisan ganda menggunakan kata kunci **Proyek** dalam pencarian di sudut kanan atas. Anda dapat memilih banyak semua peta, lalu menjalankannya. Untuk informasi lebih lanjut, lihat [Mengelola beberapa peta tabel](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Pastikan juga mengaktifkan dan menjalankan peta entitas terkait.

### <a name="project-operations-dual-write-map-versions"></a>Versi peta penulisan ganda Project Operations

Selalu jalankan versi terbaru peta di lingkungan Anda. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika salah satu kondisi berikut ada:

- Peta tidak diaktifkan.
- Versi terbaru peta tidak diaktifkan. 
- Peta tabel terkait tidak diaktifkan.

Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Anda dapat mengaktifkan versi baru peta dengan memilih **versi peta Tabel**, memilih versi terbaru, kemudian menyimpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, Anda harus menerapkan ulang perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).