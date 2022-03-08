---
title: Sinkronisasikan tugas proyek secara langsung dari Project Service Automation ke Finance and Operations
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan tugas proyek secara langsung dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288923"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sinkronisasikan tugas proyek secara langsung dari Project Service Automation ke Finance and Operations

[!include[banner](../includes/banner.md)]

Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan tugas proyek secara langsung dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.

> [!NOTE]
> - Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.
> - Jika Anda menggunakan Enterprise Edition 7.3.0 setelah menginstal 4132657 KB dan 4132660 KB, Anda dapat menggunakan template untuk mengintegrasikan tugas proyek, kategori transaksi pengeluaran, perkiraan jam, perkiraan biaya, dan aktual, serta untuk mengkonfigurasi penguncian fungsionalitas. Jika Anda harus me-reset distribusi akuntansi, kami sarankan Anda juga menginstal 4131710 KB.
> - Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation ke Finance

Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance. Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang tugas proyek dari Project Service Automation ke Finance.

Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Template dan tugas

Untuk mengakses template, di Pusat admin Microsoft Power Apps, pilih **proyek**, lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan tugas proyek dari Project Service Automation ke Finance:

- **Nama template di integrasi data:** tugas proyek (PSA ke Fin and Ops)
- **Nama tugas dalam proyek:** Tugas proyek

Sebelum sinkronisasi tugas proyek dapat terjadi, Anda harus mensinkronisasikan kontrak proyek dan proyek.

## <a name="entity-set"></a>Rangkaian Entitas

| Project Service Automation | Keuangan                             |
|----------------------------|-------------------------------------|
| Tugas Proyek              | Entitas integrasi untuk tugas proyek |

## <a name="entity-flow"></a>Alur entitas

Tugas proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai aktivitas proyek.

## <a name="prerequisites-and-mapping-setup"></a>Prasyarat dan konfigurasi pemetaan

Sebelum sinkronisasi tugas proyek dapat terjadi, Anda harus mensinkronisasikan kontrak proyek dan proyek.

## <a name="power-query"></a>Power Query

Anda harus menggunakan Microsoft Power Query untuk Excel untuk memfilter data jika ini terpenuhi:

- Anda memiliki rekaman khusus sumber daya dalam tugas proyek.

Jika anda harus menggunakan Power Query, ikuti panduan ini:

- Template tugas proyek (PSA untuk Fin dan Ops) memiliki filter default yang mengecualikan rekaman khusus sumber daya dari tugas proyek dengan mengatur filter pada **islinetask** ke **false**. Jika Anda membuat template sendiri, Anda harus menambahkan filter ini.

## <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.

[![Pemetaan template](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]