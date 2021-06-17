---
title: Integrasi faktur proyek
description: Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996570"
---
# <a name="project-invoice-integration"></a>Integrasi faktur proyek

Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.

Dalam Project Operations, manajer proyek mengelola akumulasi penagihan proyek dan membuat faktur proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan faktur proforma ini, petugas piutang dagang atau akuntan Proyek membuat faktur untuk pelanggan. Integrasi penulisan ganda memastikan bahwa rincian faktur proforma disinkronisasikan ke aplikasi Finance and Operations. Setelah faktur pelanggan dikirim, sistem memperbarui aktual proyek yang relevan di Dataverse dengan rincian akuntansi. Grafis berikut memberikan ikhtisar konsep tingkat tinggi integrasi ini.

   ![Integrasi faktur proyek](./media/DW5Invoicing.png)

Setelah Manajer proyek mengkonfirmasikan faktur proforma dalam Dataverse, informasi header faktur proforma disinkronisasikan ke aplikasi Finance and Operations menggunakan peta tabel penulisan ganda, **Proposal faktur proyek V2 (faktur)**. Ini adalah integrasi satu arah dari Dataverse ke aplikasi Finance and Operations. Membuat atau menghapus proposal faktur Proyek secara langsung di aplikasi Finance and Operations tidak didukung.

Konfirmasi faktur di Dataverse juga memicu logika bisnis untuk membuat rekaman terkait penagihan di entitas **Aktual**. Rekaman ini disinkronkan ke Finance and Operations menggunakan peta tabel dua ganda, **aktual integrasi Project Operations (msdyn\_actuals).** Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md). 

Baris proposal faktur proyek dibuat oleh proses periodik, **Impor penahapan formulir**. Proses ini didasarkan pada rincian aktual penjualan yang ditagihkan dalam tabel **penahapan Aktual**. Untuk informasi lebih lanjut, lihat [Mengelola proposal faktur proyek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
