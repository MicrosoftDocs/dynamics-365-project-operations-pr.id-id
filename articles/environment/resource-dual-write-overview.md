---
title: Integrasi Penulisan Ganda Project Operations
description: Artikel ini memberikan gambaran umum tentang integrasi penulisan ganda Operasi Proyek.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927976"
---
# <a name="project-operations-dual-write-integration-overview"></a>Ikhtisar Integrasi Penulisan Ganda Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Operasi Proyek menggunakan [kemampuan](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) tulis ganda untuk menyinkronkan data di seluruh Microsoft Dataverse dan Dynamics 365 Finance.

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
