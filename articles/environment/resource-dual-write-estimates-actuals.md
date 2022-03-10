---
title: Estimasi proyek dan integrasi aktual
description: Pembaruan topik menyediakan informasi tentang integrasi penulisan ganda Project Operations untuk estimasi proyek dan aktual.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006295"
---
# <a name="project-estimates-and-actuals-integration"></a>Estimasi proyek dan integrasi aktual

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Pembaruan topik menyediakan informasi tentang integrasi penulisan ganda Project Operations untuk estimasi proyek dan aktual.

## <a name="project-estimates"></a>Perkiraan proyek

Estimasi tenaga kerja, pengeluaran, dan bahan proyek dibuat dan dikelola di Microsoft Dataverse serta disinkronisasikan ke aplikasi Finance and Operations untuk tujuan akuntansi. Operasi buat, perbarui, dan hapus tidak didukung melalui aplikasi Finance and Operations.

Membuat estimasi memerlukan konfigurasi akuntansi yang valid untuk proyek. Proyek yang terkait dengan baris kontrak harus memiliki biaya proyek dan profil pendapatan yang valid yang ditentukan dalam aturan biaya proyek dan profil pendapatan. Untuk informasi lebih lanjut, lihat [Mengkonfigurasi akuntansi untuk proyek yang dapat ditagih](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimasi tenaga kerja

Estimasi tenaga kerja dibuat oleh Manajer Proyek atau Manajer Sumber Daya yang juga menetapkan sumber daya generik atau bernama ke tugas proyek. Rekaman penetapan sumber daya dapat ditinjau pada tab **Penugasan Sumber Daya** pada halaman **Rincian Proyek** di Dataverse. Rekaman penetapan sumber daya di Dataverse membuat rekaman perkiraan jam di aplikasi Finance and Operations menggunakan **entitas integrasi Project Operations untuk estimasi jam (msdyn\_resourceassignments)**.

   ![Integrasi estimasi tenaga kerja.](./Media/DW4LaborEstimates.png)

Penulisan ganda mensinkronisasi rekaman penetapan sumber daya ke tabel penahapan (**ProjCDSEstimateHoursImport**), lalu menggunakan logika bisnis untuk membuat dan memperbarui rekaman perkiraan jam (**ProjForecastEmpl**).

Akuntan proyek akan melihat rekaman jam perkiraan yang dibuat di aplikasi Finance and Operations dengan masuk ke **manajemen proyek dan akuntansi** > **Semua proyek** > **Rencana** > **Perkiraan Jam**.

## <a name="expense-estimates"></a>Perkiraan pengeluaran

Estimasi pengeluaran dibuat oleh manajer proyek pada tab **Estimasi Pengeluaran** pada halaman **Rincian Proyek** di Dataverse. Rekaman estimasi pengeluaran disimpan dalam entitas **Baris Perkiraan** di Dataverse. Rekaman perkiraan ini memiliki kelas transaksi, **Pengeluaran** dan disinkronisasikan ke rekaman perkiraan pengeluaran di aplikasi Finance and Operations menggunakan **entitas integrasi Project Operations untuk estimasi pengeluaran (msdyn\_estimatelines)**.

   ![Integrasi estimasi pengeluaran.](./Media/DW4ExpenseEstimates.png)

Penulisan ganda mensinkronisasi rekaman estimasi pengeluaran ke tabel penahapan, **ProjCDSEstimateExpenseImport**, lalu menggunakan logika bisnis untuk membuat dan memperbarui rekaman perkiraan pengeluaran (**ProjForecastCost**). Baris estimasi menyimpan rekaman estimasi penjualan dan estimasi biaya secara terpisah. Logika bisnis dalam aplikasi Finance and Operations mengisi satu rekaman perkiraan Pengeluaran menggunakan rincian ini dalam tabel penahapan.

Akuntan dapat meninjau rekaman jam perkiraan pengeluaran di aplikasi Finance and Operations dengan masuk ke **manajemen proyek dan akuntansi** > **Semua proyek** > **Rencana** > **Perkiraan Pengeluaran**.

## <a name="material-estimates"></a>estimasi bahan

Estimasi bahan dibuat oleh manajer proyek pada tab **Estimasi bahan** pada halaman **Rincian Proyek** di Dataverse. Rekaman estimasi bahan disimpan dalam entitas **Baris Perkiraan** di Dataverse. Rekaman perkiraan ini memiliki kelas transaksi, **bahan** dan disinkronisasikan ke rekaman perkiraan item di aplikasi Finance and Operations menggunakan **tabel integrasi Project Operations untuk estimasi bahan (msdyn\_estimatelines)**.

   ![Integrasi estimasi bahan.](./Media/DW4MaterialEstimates.png)

Penulisan ganda mensinkronisasi rekaman estimasi bahan ke tabel penahapan, **ProjForecastSalesImpor**, lalu menggunakan logika bisnis untuk membuat dan memperbarui rekaman perkiraan item (**ForecastSales**). Baris estimasi menyimpan rekaman estimasi penjualan dan estimasi biaya secara terpisah. Logika bisnis dalam aplikasi Finance and Operations mengisi satu rekaman perkiraan item menggunakan rincian ini dalam tabel penahapan.

Akuntan dapat meninjau rekaman jam perkiraan item di aplikasi Finance and Operations dengan masuk ke **manajemen proyek dan akuntansi** > **Semua proyek** > **Rencana** > **Perkiraan item**.

## <a name="project-actuals"></a>Aktual proyek

Aktual proyek dibuat dalam Dataverse, berdasarkan waktu, pengeluaran, bahan, dan aktivitas penagihan. Semua atribut operasional dari transaksi ini termasuk kuantitas, harga biaya, harga penjualan, dan proyek diambil dalam entitas Dataverse ini. Untuk informasi lebih lanjut, lihat [Aktual](../actuals/actuals-overview.md). Rekaman aktual disinkronisasi ke aplikasi Finance and Operations menggunakan **aktual integrasi project Operations (msdyn\_actuals)** peta tabel penulisan ganda untuk akuntansi hilir.

   ![Integrasi aktual.](./Media/DW4Actuals.png)

Peta tabel **aktual integrasi Project Operations** mensinkronisasikan semua rekaman dari entitas **Aktual** di Dataverse, dengan atribut **Lewati Sinkronisasi (hanya penggunaan internal)** yang diatur ke **Salah**. Nilai atribut ini diatur di Dataverse secara otomatis saat rekaman dibuat. Contoh lokasi atribut ini diatur ke **Benar** adalah:

  - Aktual biaya proyek untuk transaksi antarperusahaan. Untuk informasi lebih lanjut, lihat [Membuat transaksi antarperusahaan](../project-accounting/create-intercompany-transactions.md). Rekaman ini diabaikan karena sistem membuat ulang biaya proyek yang sebenarnya di aplikasi Finance and Operations saat faktur vendor antarperusahaan diposting.
  - Rekaman penjualan tidak tertagih negatif yang dibuat saat faktur proforma dikonfirmasi. Rekaman ini diabaikan karena buku besar pembantu proyek dalam aplikasi Finance and Operations tidak membalik rekaman penjualan yang belum ditagihkan pada faktur, namun mengubah status menjadi sepenuhnya ditagih.

Peta tabel penulisan ganda mensinkronisasikan rekaman aktual dengan tabel penahapan, **ProjCDSActualsImport**. Rekaman ini diproses oleh proses periodik **Impor dari tabel penahapan** saat membuat baris jurnal integrasi Project Operations dan baris proposal faktur proyek. Untuk informasi lebih lanjut, lihat [integrasi jurnal di Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse juga menangkap tautan antara transaksi aktual proyek di entitas **sambungan Transaksi**. Untuk informasi lebih lanjut, lihat [Menautkan aktual ke rekaman asli](../actuals/linkingactuals.md). Tautan antara transaksi aktual juga disinkronisasi ke aplikasi Finance and Operations menggunakan peta tabel penulisan ganda, **Entitas integrasi untuk relasi transaksi proyek (msdyn\_transactionconnections)**. Rekaman ini digunakan oleh proses periodik **Impor dari tabel penahapan** saat membuat baris jurnal integrasi Project Operations dan baris proposal faktur proyek.

Memposting jurnal integrasi Project Operations dan proposal faktur proyek memicu pembaruan di rekaman masing-masing dalam tabel penahapan, **ProjCDSActualsImport**. Sistem mengambil dan merekam atribut akuntansi berikut untuk transaksi aktual:

- Jumlah mata uang akuntansi
- Kurs
- Nomor Voucher
- Jumlah pajak penjualan

Peta tabel **aktual integrasi Project Operations** memperbarui rekaman aktual masing-masing di Dataverse dengan informasi ini.
