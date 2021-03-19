---
title: Parameter Integrasi Project Service Automation
description: Topik ini menjelaskan cara mengonfigurasi data default yang dimasukkan saat anda mengintegrasikan Microsoft Dynamics 365 for Project Service Automation dengan Microsoft Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b8faba1d799e360e58d47a02dc8b46e09fa0d393
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270907"
---
# <a name="project-service-automation-integration-parameters"></a>Parameter Integrasi Project Service Automation

[!include[banner](../includes/banner.md)]

Di halaman **parameter integrasi Project Service Automation**, Anda dapat mengonfigurasi cara data default dimasukkan saat mengintegrasikan Dynamics 365 Project Service Automation dengan Dynamics 365 Finance. Agar proyek berhasil disinkronisasi dari Project Service Automation ke Finance, Anda harus mengkonfigurasi bidang berikut.

Untuk membuka halaman **parameter integrasi Project Service Automation**, buka **manajemen proyek dan parameter akuntansi** \> **Konfigurasi** \> **parameter integrasi Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.
> - Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.


| Tab                    | Bidang                | Deskripsi |
|------------------------|----------------------|-------------|
| Umum                | Jenis proyek default | Pilih jenis proyek default. Bila proyek disinkronisasi dari Project Service Automation, nilai ini digunakan jika Anda tidak memberikan nilai default dalam template integrasi. Selama sinkronisasi, bidang **jenis proyek** proyek baru diatur ke nilai ini. Namun, nilai mungkin diperbarui saat baris kontrak proyek disinkronisasi dari Project Service Automation. |
|                        | Kategori waktu        | Pilih kategori waktu default. Nilai ini digunakan saat estimasi jam disinkronisasi dari Project Service Automation. Bila estimasi jam dan aktual jam disinkronisasi dari Project Service Automation, bidang **kategori** dalam perkiraan jam proyek baru di Finance diatur ke nilai ini. |
|                        | Kategori ongkos         | Pilih kategori ongkos default. Nilai ini digunakan saat aktual ongkos disinkronisasi dari Project Service Automation. Bila aktual ongkos disinkronisasi dari Project Service Automation, bidang **kategori** dalam transaksi ongkos baru di Finance diatur ke nilai ini. |
| Default grup proyek | Jenis proyek         | Klik **baru** untuk menambahkan baris di mana Anda dapat memilih jenis proyek untuk mengatur grup proyek default. Jenis proyek tertentu dapat dipilih hanya satu kali di konfigurasi. |
|                        | Grup proyek        | Pilih grup proyek default untuk jenis proyek yang dipilih. Bila proyek baru disinkronisasi dari Project Service Automation, bidang **grup proyek** diatur ke nilai default untuk jenis proyek jika Anda tidak memberikan nilai default dalam template integrasi. |
| Default jenis penagihan  | Jenis Penagihan         | Klik **baru** untuk menambahkan baris di mana Anda dapat memilih jenis penagihan untuk mengatur properti baris default-nya. Jenis penagihan tertentu dapat dipilih hanya satu kali di konfigurasi. |
|                        | Properti baris        | Pilih properti baris default untuk jenis penagihan yang dipilih. Bila perkiraan jam baru, perkiraan pengeluaran baru, atau aktual baru akan disinkronisasi dari Project Service Automation, bidang **properti baris** diatur ke nilai default untuk jenis penagihan. |
| Penguncian fungsi  | Tidak berlaku       | Pilih fungsi yang akan dinonaktifkan di Finance untuk proyek dan kontrak yang berasal dari Project Service Automation. Misalnya, Anda dapat menonaktifkan kemampuan untuk mengedit kontrak dan proyek, membuat struktur rincian kerja, dan memasukkan lembar waktu di Finance. Bidang yang terkait dengan akuntansi akan terus diaktifkan, meskipun dibuat tidak tersedia oleh pengaturan parameter. Secara default, Semua fungsi diaktifkan. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]