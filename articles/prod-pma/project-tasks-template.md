---
title: Menyinkronkan tugas proyek langsung dari Project Service Automation ke keuangan dan operasi
description: Artikel ini menjelaskan templat dan tugas mendasar yang digunakan untuk menyinkronkan tugas proyek langsung dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028365"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Menyinkronkan tugas proyek langsung dari Project Service Automation ke keuangan dan operasi

[!include[banner](../includes/banner.md)]

Artikel ini menjelaskan templat dan tugas mendasar yang digunakan untuk menyinkronkan tugas proyek langsung dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.

> [!NOTE]
> - Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.
> - Jika Anda menggunakan Enterprise Edition 7.3.0 setelah menginstal 4132657 KB dan 4132660 KB, Anda dapat menggunakan template untuk mengintegrasikan tugas proyek, kategori transaksi pengeluaran, perkiraan jam, perkiraan biaya, dan aktual, serta untuk mengkonfigurasi penguncian fungsionalitas. Jika Anda harus me-reset distribusi akuntansi, kami sarankan Anda juga menginstal 4131710 KB.
> - Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation ke Finance

Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance. Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang tugas proyek dari Project Service Automation ke Finance.

Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

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

Anda harus menggunakan Microsoft Power Query untuk Excel untuk memfilter data jika kondisi ini terpenuhi:

- Anda memiliki rekaman khusus sumber daya dalam tugas proyek.

Jika Anda harus menggunakan Power Query, ikuti pedoman ini:

- Template tugas proyek (PSA untuk Fin dan Ops) memiliki filter default yang mengecualikan rekaman khusus sumber daya dari tugas proyek dengan mengatur filter pada **islinetask** ke **false**. Jika Anda membuat template sendiri, Anda harus menambahkan filter ini.

## <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.

[![Pemetaan template.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]