---
title: Integrasi Penulisan Ganda Project Operations
description: Ringkasan topik ini memberikan ikhtisar integrasi penulisan ganda Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955662"
---
# <a name="project-operations-dual-write-integration-overview"></a>Ikhtisar Integrasi Penulisan Ganda Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Project Operations menggunakan [kemampuan penulisan ganda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) untuk mensinkronisasi data di seluruh Microsoft Dataverse dan Dynamics 365 Finance.

Ilustrasi berikut menunjukkan cara sinkronisasi data sebagai bagian dari integrasi antara Dataverse dan Finance.

![Ikhtisar alur data Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations di Dataverse menyediakan antarmuka pengguna (UI) modern dan ekstensibilitas tanpa kode/kode rendah yang mudah menggunakan kemampuan Power Platform. Manajer proyek, Manajer sumber daya, anggota tim proyek, dan staf kantor depan lainnya, melakukan aktivitas mereka di Project Operations di Dataverse.

Project Operations in Finance memberikan dukungan akuntansi proyek dan pengakuan pendapatan. Project Operations terhubung dengan kerangka kerja keuangan di Finance untuk perhitungan pajak penjualan, nilai tukar mata uang, pelaporan dimensi keuangan, dan banyak lagi. Pengalaman akuntan Proyek kebanyakan berbasis di Finance.

Integrasi Project Operations terdiri dari integrasi komponen berikut:


- [Konfigurasi Project Operations dan integrasi data konfigurasi](resource-dual-write-setup-integration.md) 
- [Estimasi proyek dan aktual](resource-dual-write-estimates-actuals.md)
- [Faktur Proyek](resource-dual-write-project-invoice.md)
- [Manajemen pengeluaran](resource-dual-write-expense.md)
- [Faktur Vendor](resource-dual-write-vendor-invoice.md)
