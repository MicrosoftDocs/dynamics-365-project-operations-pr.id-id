---
title: Mensinkronisasikan kategori pengeluaran proyek antara Finance and Operations dan Project Service Automation
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan kategori pengeluaran proyek antara Microsoft Dynamics 365 Finance dan Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289643"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Mensinkronisasikan kategori pengeluaran proyek antara Finance and Operations dan Project Service Automation

[!include[banner](../includes/banner.md)]

Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan kategori pengeluaran proyek antara Dynamics 365 Finance dan Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.
> - Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.
> - Jika Anda menggunakan Enterprise Edition 7.3.0 setelah menginstal 4132657 KB dan 4132660 KB, Anda dapat menggunakan template untuk mengintegrasikan tugas proyek, kategori transaksi pengeluaran, perkiraan jam, perkiraan biaya, dan aktual, serta untuk mengkonfigurasi penguncian fungsionalitas. Jika Anda harus me-reset distribusi akuntansi, kami sarankan Anda juga menginstal 4131710 KB.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Aliran data untuk Project Service Automation dan Finance

Solusi integrasi Project Service Automation dan Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance. Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang kategori transaksi pengeluaran proyek antara Finance dan Project Service Automation.

Jika kategori pengeluaran proyek memiliki induk dalam Finance, aliran integrasi adalah yang pertama dari Finance hingga Project Service Automation. Id integrasi dari kategori pengeluaran proyek kemudian diperbarui melalui sinkronisasi dari Project Service Automation ke Finance.

Jika kategori pengeluaran proyek memiliki induk dalam Project Service Automation, aliran integrasi adalah yang pertama dari Project Service ke Finance. Kategori proyek harus sudah dikonfigurasi di Finance sebelum sinkronisasi dari Project Service Automation. Kemudian sinkronisasikan dari Finance kembali ke Project Service Automation, lalu dari Project Service Automation ke Finance lagi. Dengan cara ini, Anda membantu menjamin bahwa kategori ditautkan, dan tidak ada duplikat yang dibuat.

> [!NOTE]
> Biasanya, kategori biaya proyek memiliki induk di Finance. Namun, jika tidak, atau jika kategori pengeluaran telah dibuat dalam Project Service Automation, Anda harus terlebih dulu mensinkronisasi menggunakan template kategori pengeluaran transaksi proyek (PSA ke Fin and Ops). Kemudian sinkronisasikan dengan menggunakan template kategori pengeluaran transaksi proyek (Fin and Ops ke PSA). Selanjutnya, Anda harus menjalankan sinkronisasi dari Project Service Automation ke Finance sekali lagi.
>
> Jika Anda mensinkronisasi pertama kali dari Project Service Automation, persyaratan berikut harus dipenuhi di Finance sebelum sinkronisasi dijalankan:
>
> - Kategori bersama yang cocok dengan kategori proyek yang diatur dalam Project Service Automation harus ada, dan harus diaktifkan untuk **proyek** dan **Pengeluaran**.
> - Untuk setiap entitas hukum Finance yang harus diintegrasikan dengannya, kategori proyek berikut harus ada:
>
>     - **Kategori proyek** ada. 
>     - **Penggunaan Pengeluaran** diaktifkan.
>     - **Aktif dalam jurnal** diaktifkan.
>     - **Jenis transaksi** diatur ke **pengeluaran**.

Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sinkronisasi kategori pengeluaran proyek dari Finance ke Project Service Automation

### <a name="template-and-task"></a>Template dan tugas

Untuk mengakses template, di Pusat admin Microsoft Power Apps, pilih **proyek**, lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan kategori pengeluaran proyek dari Finance ke Project Service Automation:

- **Nama template di integrasi data:** kategori transaksi pengeluaran proyek (Fin and Ops ke PSA)
- **Nama tugas dalam proyek:** sinkronisasi kategori ke PSA

### <a name="entity-set"></a>Rangkaian Entitas

| Keuangan                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entitas integrasi untuk kategori | Kategori Transaksi     |

### <a name="entity-flow"></a>Alur entitas

Kategori pengeluaran proyek dikelola dalam Finance, dan disinkronisasi ke Project Service Automation sebagai kategori transaksi.

### <a name="power-query"></a>Power Query

Bila anda mensinkronisasi ke Project Service Automation, anda harus menggunakan Microsoft Power Query untuk Excel guna mengatur jenis penagihan pada kategori transaksi. Template kategori transaksi pengeluaran proyek (Fin and Ops ke PSA) menyediakan kolom dan pemetaan default. Jika Anda membuat template sendiri, Anda harus menambahkan kolom kondisional di Power Query. ikuti langkah berikut.

1. Klik tanda panah untuk membuka pemetaan tugas kategori pengeluaran proyek dalam template kategori pengeluaran transaksi (Fin and Ops ke PSA).
2. Klik tautan **kueri lanjutan dan filter** untuk membuka Power query.
2. Pilih **Tambah kolom kondisional**.
3. Masukkan nama untuk kolom baru, seperti **billingtype**.
4. Masukkan kondisi berikut: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Klik **OK** pada kolom.
6. Pastikan untuk memetakan kolom baru ini pada halaman pemetaan.

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Finance ke Project Service Automation.

[![Pemetaan template kategori pengeluaran proyek ke Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sinkronisasi kategori pengeluaran proyek dari Project Service Automation ke Finance

### <a name="template-and-task"></a>Template dan tugas

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan kategori pengeluaran proyek dari Project Service Automation ke Finance:

- **Nama template di integrasi data:** kategori transaksi pengeluaran proyek (PSA ke Fin and Ops)
- **Nama tugas dalam proyek:** sinkronisasi kategori ke Fin Ops

### <a name="entity-set"></a>Rangkaian Entitas

| Project Service Automation | Keuangan                           |
|----------------------------|-----------------------------------|
| Kategori Transaksi     | Entitas integrasi untuk kategori |

### <a name="entity-flow"></a>Alur entitas

Kategori pengeluaran proyek dikelola dalam Finance, dan disinkronisasi ke Project Service Automation sebagai kategori transaksi. Sinkronisasi kembali ke Finance memperbarui kategori proyek di Finance dengan ID integrasi dari Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data.

> [!NOTE]
> Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.

[![Pemetaan template Project Service Automation ke Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]