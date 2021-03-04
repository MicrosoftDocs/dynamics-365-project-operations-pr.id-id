---
title: Gambaran Umum Project Service Automation
description: Topik ini menyediakan informasi tentang solusi integrasi Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642457"
---
# <a name="project-service-automation-overview"></a>Gambaran Umum Project Service Automation

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans Dynamics 365 Finance dan Dynamics 365 Project Service Automation melalui Common Data Service. Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran proyek, kontrak proyek, baris kontrak proyek, tonggak pencapaian baris kontrak proyek, tugas proyek, kategori transaksi pengeluaran, estimasi jam, dan estimasi pengeluaran dari Project Service Automation ke Finance.

> [!NOTE]
> - Jika Anda menggunakan versi 7.3.0, Anda harus menginstal KB 4074835. Anda kemudian akan dapat mengintegrasikan proyek harga tetap.
> - Jika Anda menggunakan versi 7.3.0, dan Anda membawa transaksi biaya melalui dari Project Service Automation, Anda harus menginstal 4345320 KB agar dapat mencakup biaya tersebut dalam faktur proyek.
> - Jika Anda menggunakan versi 8.0, Anda akan dapat menggunakan Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi.
> - Jika Anda menggunakan versi 8.0.1 atau yang lebih baru, Anda akan dapat mensinkronisasi aktual.

Sebelum Anda dapat mengintegrasikan Project Service Automation Finance, Anda harus mengkonfigurasikan parameter integrasi Project Service Automation. Untuk Informasi lebih lanjut, lihat [mengintegrasikan parameter integrasi Project Service Automation](PSA-parameters.md).

Solusi integrasi ini memungkinkan sinkronisasi langsung dalam skenario berikut:

- Kelola kontrak proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.
- Buat proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.
- Kelola baris kontrak proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.
- Kelola tonggak pencapaian baris kontrak proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.
- Kelola tugas proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.
- Kelola kategori transaksi pengeluaran di Finance, dan sinkronisasikan secara langsung dari Finance ke Project Service Automation.
- Buat estimasi jam proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.
- Buat estimasi pengeluaran proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.
- Buat waktu proyek, pengeluaran, dan aktual ongkos dalam Project Service Automation, dan buat transaksi proyek dalam jurnal integrasi Project Service Automation sehingga dapat diposting di Finance.

## <a name="data-synchronization"></a>Sinkronisasi data

Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan sebagai bagian integrasi antara Project Service Automation dan Finance.

> [!NOTE]
> Tidak semua template tersedia saat ini. Template akan dirilis saat selesai.

[![Integrasi Project Service Automation dengan Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Persyaratan sistem untuk Finance

Untuk menggunakan solusi integrasi Project Service Automation ke Finance, Anda harus menginstal Enterprise Edition 7.3 dengan pembaruan platform 12, atau yang lebih baru.

## <a name="system-requirements-for-project-service-automation"></a>Persyaratan sistem untuk Project Service Automation

Untuk menggunakan solusi integrasi Project Service Automation ke Finance, Anda harus menginstal komponen berikut:

- Dynamics 365 Project Service Automation versi 9.0.0.0 atau lebih baru
- Solusi Prospek ke kas untuk Dynamics 365 Sales, versi 1.14.0.0 (V14) atau versi lebih baru
- Solusi Project Service Automation ke Finance untuk Dynamics 365 Project Service Automation versi 1.0.0.0 atau lebih baru

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instal solusi integrasi Project Service Automation ke Finance di instans Project Service Automation Anda

Unduh solusi integrasi Project Service Automation ke Finance dari [pusat Unduh Microsoft](https://www.microsoft.com/download/details.aspx?id=57016), dan ikuti petunjuk yang disertakan dengan solusi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]