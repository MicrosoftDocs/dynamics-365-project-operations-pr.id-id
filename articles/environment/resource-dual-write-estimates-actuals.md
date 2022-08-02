---
title: Estimasi proyek dan integrasi aktual
description: Artikel ini menyediakan informasi tentang integrasi penulisan ganda Operasi Proyek untuk perkiraan dan aktual proyek.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029084"
---
# <a name="project-estimates-and-actuals-integration"></a>Estimasi proyek dan integrasi aktual

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini menyediakan informasi tentang integrasi penulisan ganda Operasi Proyek untuk perkiraan dan aktual proyek.

## <a name="project-estimates"></a>Perkiraan proyek

Perkiraan tenaga kerja, pengeluaran, dan material proyek dibuat dan dipelihara dalam Microsoft Dataverse dan disinkronkan ke aplikasi keuangan dan operasi untuk tujuan akuntansi. Operasi buat, perbarui, dan hapus tidak didukung melalui aplikasi keuangan dan operasi.

Membuat estimasi memerlukan konfigurasi akuntansi yang valid untuk proyek. Proyek yang terkait dengan baris kontrak harus memiliki biaya proyek dan profil pendapatan yang valid yang ditentukan dalam aturan biaya proyek dan profil pendapatan. Untuk informasi lebih lanjut, lihat [Mengkonfigurasi akuntansi untuk proyek yang dapat ditagih](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimasi tenaga kerja

Estimasi tenaga kerja dibuat oleh Manajer Proyek atau Manajer Sumber Daya yang juga menetapkan sumber daya generik atau bernama ke tugas proyek. Rekaman penetapan sumber daya dapat ditinjau pada tab **Penugasan Sumber Daya** pada halaman **Rincian Proyek** di Dataverse. Rekaman penugasan sumber daya dalam Dataverse membuat catatan perkiraan jam di aplikasi keuangan dan operasi menggunakan **entitas integrasi Operasi Proyek untuk perkiraan jam (msdyn\_ resourceassignments)**.

   ![Integrasi estimasi tenaga kerja.](./Media/DW4LaborEstimates.png)

Penulisan ganda mensinkronisasi rekaman penetapan sumber daya ke tabel penahapan (**ProjCDSEstimateHoursImport**), lalu menggunakan logika bisnis untuk membuat dan memperbarui rekaman perkiraan jam (**ProjForecastEmpl**).

Akuntan Proyek meninjau catatan jam perkiraan yang dibuat di aplikasi keuangan dan operasi dengan **membuka Manajemen proyek dan akuntansi** > **Semua perkiraan** > **Jam Rencana** > **proyek**.

## <a name="expense-estimates"></a>Perkiraan pengeluaran

Estimasi pengeluaran dibuat oleh manajer proyek pada tab **Estimasi Pengeluaran** pada halaman **Rincian Proyek** di Dataverse. Rekaman estimasi pengeluaran disimpan dalam entitas **Baris Perkiraan** di Dataverse. Catatan perkiraan ini memiliki kelas transaksi, **Pengeluaran** dan disinkronkan ke catatan perkiraan pengeluaran di aplikasi keuangan dan operasi menggunakan **entitas integrasi Operasi Proyek untuk perkiraan biaya (perkiraan msdyn\_)**.

   ![Integrasi estimasi pengeluaran.](./Media/DW4ExpenseEstimates.png)

Penulisan ganda mensinkronisasi rekaman estimasi pengeluaran ke tabel penahapan, **ProjCDSEstimateExpenseImport**, lalu menggunakan logika bisnis untuk membuat dan memperbarui rekaman perkiraan pengeluaran (**ProjForecastCost**). Baris estimasi menyimpan rekaman estimasi penjualan dan estimasi biaya secara terpisah. Logika bisnis dalam aplikasi keuangan dan operasi mengisi satu catatan perkiraan Biaya menggunakan detail ini dalam tabel pementasan.

Akuntan Proyek dapat meninjau catatan perkiraan pengeluaran di aplikasi keuangan dan operasi dengan membuka **Manajemen proyek dan akuntansi** > **Semua proyek** > **Rencanakan** > **Perkiraan** biaya.

## <a name="material-estimates"></a>estimasi bahan

Estimasi bahan dibuat oleh manajer proyek pada tab **Estimasi bahan** pada halaman **Rincian Proyek** di Dataverse. Rekaman estimasi bahan disimpan dalam entitas **Baris Perkiraan** di Dataverse. Catatan perkiraan ini memiliki kelas transaksi, **Material** dan disinkronkan ke catatan perkiraan item di aplikasi keuangan dan operasi menggunakan **tabel integrasi Project untuk estimasi material (msdyn\_ estimatelines)**.

   ![Integrasi estimasi bahan.](./Media/DW4MaterialEstimates.png)

Penulisan ganda mensinkronisasi rekaman estimasi bahan ke tabel penahapan, **ProjForecastSalesImpor**, lalu menggunakan logika bisnis untuk membuat dan memperbarui rekaman perkiraan item (**ForecastSales**). Baris estimasi menyimpan rekaman estimasi penjualan dan estimasi biaya secara terpisah. Logika bisnis dalam aplikasi keuangan dan operasi mengisi satu catatan perkiraan Item menggunakan detail ini dalam tabel pementasan.

Akuntan Proyek dapat meninjau catatan perkiraan item di aplikasi keuangan dan operasi dengan membuka **Manajemen proyek dan akuntansi** > **Semua perkiraan** > **Item Rencana** > **proyek**.

## <a name="project-actuals"></a>Aktual proyek

Aktual proyek dibuat dalam Dataverse, berdasarkan waktu, pengeluaran, bahan, dan aktivitas penagihan. Semua atribut operasional dari transaksi ini termasuk kuantitas, harga biaya, harga penjualan, dan proyek diambil dalam entitas Dataverse ini. Untuk informasi lebih lanjut, lihat [Aktual](../actuals/actuals-overview.md). Catatan aktual disinkronkan ke aplikasi keuangan dan operasi menggunakan peta tabel tulis ganda Aktual **integrasi Operasi Proyek (msdyn\_ actuals)** untuk akuntansi hilir.

   ![Integrasi aktual.](./Media/DW4Actuals.png)

Peta tabel **aktual integrasi Project Operations** mensinkronisasikan semua rekaman dari entitas **Aktual** di Dataverse, dengan atribut **Lewati Sinkronisasi (hanya penggunaan internal)** yang diatur ke **Salah**. Nilai atribut ini diatur di Dataverse secara otomatis saat rekaman dibuat. Contoh lokasi atribut ini diatur ke **Benar** adalah:

  - Aktual biaya proyek untuk transaksi antarperusahaan. Untuk informasi lebih lanjut, lihat [Membuat transaksi antarperusahaan](../project-accounting/create-intercompany-transactions.md). Catatan ini dilewati karena sistem membuat ulang biaya proyek aktual dalam aplikasi keuangan dan operasi ketika faktur vendor antar perusahaan diposting.
  - Rekaman penjualan tidak tertagih negatif yang dibuat saat faktur proforma dikonfirmasi. Catatan ini dilewati karena subledger proyek di aplikasi keuangan dan operasi tidak membalikkan catatan penjualan yang tidak ditagih saat faktur tetapi mengubah status menjadi ditagih penuh.

Peta tabel penulisan ganda mensinkronisasikan rekaman aktual dengan tabel penahapan, **ProjCDSActualsImport**. Rekaman ini diproses oleh proses periodik **Impor dari tabel penahapan** saat membuat baris jurnal integrasi Project Operations dan baris proposal faktur proyek. Untuk informasi lebih lanjut, lihat [integrasi jurnal di Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse juga menangkap tautan antara transaksi aktual proyek di entitas **sambungan Transaksi**. Untuk informasi lebih lanjut, lihat [Menautkan aktual ke rekaman asli](../actuals/linkingactuals.md). Tautan antara transaksi aktual juga disinkronkan ke aplikasi keuangan dan operasi menggunakan peta tabel tulis ganda, **entitas Integrasi untuk transaksi proyek Relasi (koneksi transaksi msdyn\_)**. Rekaman ini digunakan oleh proses periodik **Impor dari tabel penahapan** saat membuat baris jurnal integrasi Project Operations dan baris proposal faktur proyek.

Memposting jurnal integrasi Project Operations dan proposal faktur proyek memicu pembaruan di rekaman masing-masing dalam tabel penahapan, **ProjCDSActualsImport**. Sistem mengambil dan merekam atribut akuntansi berikut untuk transaksi aktual:

- Jumlah mata uang akuntansi
- Kurs
- Nomor Voucher
- Jumlah pajak penjualan

Peta tabel **aktual integrasi Project Operations** memperbarui rekaman aktual masing-masing di Dataverse dengan informasi ini.
