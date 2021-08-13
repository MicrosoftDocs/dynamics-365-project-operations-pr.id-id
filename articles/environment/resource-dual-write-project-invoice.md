---
title: Integrasi faktur proyek
description: Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993245"
---
# <a name="project-invoice-integration"></a>Integrasi faktur proyek

Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.

Dalam Project Operations, manajer proyek mengelola akumulasi penagihan proyek dan membuat faktur proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan faktur proforma ini, petugas piutang dagang atau akuntan Proyek membuat faktur untuk pelanggan. Integrasi penulisan ganda memastikan bahwa rincian faktur proforma disinkronisasikan ke aplikasi Finance and Operations. Setelah faktur pelanggan dikirim, sistem memperbarui aktual proyek yang relevan di Dataverse dengan rincian akuntansi. Grafis berikut memberikan ikhtisar konsep tingkat tinggi integrasi ini.

   ![Integrasi faktur proyek.](./media/DW5Invoicing.png)

Setelah Manajer proyek mengkonfirmasikan faktur proforma dalam Dataverse, informasi header faktur proforma disinkronisasikan ke aplikasi Finance and Operations menggunakan peta tabel penulisan ganda, **Proposal faktur proyek V2 (faktur)**. Ini adalah integrasi satu arah dari Dataverse ke aplikasi Finance and Operations. Membuat atau menghapus proposal faktur Proyek secara langsung di aplikasi Finance and Operations tidak didukung.

Konfirmasi faktur di Dataverse juga memicu logika bisnis untuk membuat rekaman terkait penagihan di entitas **Aktual**. Rekaman ini disinkronkan ke Finance and Operations menggunakan peta tabel dua ganda, **aktual integrasi Project Operations (msdyn\_actuals).** Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md). 

Baris proposal faktur proyek dibuat oleh proses periodik, **Impor penahapan formulir**. Proses ini didasarkan pada rincian aktual penjualan yang ditagihkan dalam tabel **penahapan Aktual**. Untuk informasi lebih lanjut, lihat [Mengelola proposal faktur proyek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
