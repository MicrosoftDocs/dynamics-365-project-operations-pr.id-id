---
title: Integrasi faktur proyek
description: Artikel ini menyediakan informasi tentang integrasi penulisan ganda Operasi Proyek untuk faktur pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912106"
---
# <a name="project-invoice-integration"></a>Integrasi faktur proyek

Artikel ini menyediakan informasi tentang integrasi penulisan ganda Operasi Proyek untuk faktur pelanggan.

Dalam Project Operations, manajer proyek mengelola akumulasi penagihan proyek dan membuat faktur proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan faktur proforma ini, petugas piutang dagang atau akuntan Proyek membuat faktur untuk pelanggan. Integrasi tulis ganda memastikan bahwa detail faktur proforma disinkronkan ke aplikasi Keuangan dan Operasi. Setelah faktur pelanggan dikirim, sistem memperbarui aktual proyek yang relevan di Dataverse dengan rincian akuntansi. Grafis berikut memberikan ikhtisar konsep tingkat tinggi integrasi ini.

   ![Integrasi faktur proyek.](./media/DW5Invoicing.png)

Setelah manajer Proyek mengonfirmasi faktur proforma di Dataverse, informasi header faktur proforma disinkronkan ke aplikasi Keuangan dan Operasi menggunakan peta tabel tulis ganda, **proposal faktur Proyek V2 (faktur)**. Ini adalah integrasi satu arah dari Dataverse ke aplikasi Keuangan dan Operasi. Membuat atau menghapus proposal faktur Project secara langsung di aplikasi Finance and Operations tidak didukung.

Konfirmasi faktur di Dataverse juga memicu logika bisnis untuk membuat rekaman terkait penagihan di entitas **Aktual**. Catatan ini disinkronkan ke Keuangan dan Operasi menggunakan peta tabel tulis ganda, **aktual integrasi Operasi Proyek (msdyn\_ actuals).** Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md). 

Baris proposal faktur proyek dibuat oleh proses periodik, **Impor penahapan formulir**. Proses ini didasarkan pada rincian aktual penjualan yang ditagihkan dalam tabel **penahapan Aktual**. Untuk informasi lebih lanjut, lihat [Mengelola proposal faktur proyek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
