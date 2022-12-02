---
title: Integrasi faktur proyek
description: Artikel ini mem informasi tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029028"
---
# <a name="project-invoice-integration"></a>Integrasi faktur proyek

Artikel ini mem informasi tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.

Dalam Project Operations, manajer proyek mengelola akumulasi penagihan proyek dan membuat faktur proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan faktur proforma ini, petugas piutang dagang atau akuntan Proyek membuat faktur untuk pelanggan. Integrasi penulisan ganda memastikan bahwa rincian faktur proforma disinkronisasikan ke aplikasi keuangan dan operasi. Setelah faktur pelanggan dikirim, sistem memperbarui aktual proyek yang relevan di Dataverse dengan rincian akuntansi. Grafis berikut memberikan ikhtisar konsep tingkat tinggi integrasi ini.

   ![Integrasi faktur proyek.](./media/DW5Invoicing.png)

Setelah Manajer proyek mengkonfirmasikan faktur proforma dalam Dataverse, informasi header faktur proforma disinkronisasikan ke aplikasi keuangan dan operasi menggunakan peta tabel penulisan ganda, **Proposal faktur proyek V2 (faktur)**. Ini adalah integrasi satu arah dari Dataverse ke aplikasi keuangan dan operasi. Membuat atau menghapus proposal faktur Proyek secara langsung di aplikasi keuangan dan operasi tidak didukung.

Konfirmasi faktur di Dataverse juga memicu logika bisnis untuk membuat rekaman terkait penagihan di entitas **Aktual**. Rekaman ini disinkronkan kekeuangan dan operasi menggunakan peta tabel dua ganda, **aktual integrasi Project Operations (msdyn\_actuals).** Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md). 

Baris proposal faktur proyek dibuat oleh proses periodik, **Impor penahapan formulir**. Proses ini didasarkan pada rincian aktual penjualan yang ditagihkan dalam tabel **penahapan Aktual**. Untuk informasi lebih lanjut, lihat [Mengelola proposal faktur proyek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
