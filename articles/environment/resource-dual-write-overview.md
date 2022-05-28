---
title: Integrasi Penulisan Ganda Project Operations
description: Ringkasan topik ini memberikan ikhtisar integrasi penulisan ganda Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582760"
---
# <a name="project-operations-dual-write-integration-overview"></a>Ikhtisar Integrasi Penulisan Ganda Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Operasi Proyek menggunakan [kemampuan](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) dual-write untuk menyinkronkan data di seluruh Microsoft Dataverse dan Dynamics 365 Finance.

Ilustrasi berikut menunjukkan cara sinkronisasi data sebagai bagian dari integrasi antara Dataverse dan Finance.

![Ikhtisar alur data Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations di Dataverse menyediakan antarmuka pengguna (UI) modern dan ekstensibilitas tanpa kode/kode rendah yang mudah menggunakan kemampuan Power Platform. Manajer proyek, Manajer sumber daya, anggota tim proyek, dan staf kantor depan lainnya, melakukan aktivitas mereka di Project Operations di Dataverse.

Project Operations in Finance memberikan dukungan akuntansi proyek dan pengakuan pendapatan. Project Operations terhubung dengan kerangka kerja keuangan di Finance untuk perhitungan pajak penjualan, nilai tukar mata uang, pelaporan dimensi keuangan, dan banyak lagi. Pengalaman akuntan Proyek kebanyakan berbasis di Finance.

Integrasi Project Operations terdiri dari integrasi komponen berikut:


- [Konfigurasi Project Operations dan integrasi data konfigurasi](resource-dual-write-setup-integration.md) 
- [Estimasi proyek dan aktual](resource-dual-write-estimates-actuals.md)
- [Faktur Proyek](resource-dual-write-project-invoice.md)
- [Manajemen pengeluaran](resource-dual-write-expense.md)
- [Faktur Vendor](resource-dual-write-vendor-invoice.md)
