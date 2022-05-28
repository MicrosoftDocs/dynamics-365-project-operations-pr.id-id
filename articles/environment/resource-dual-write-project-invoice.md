---
title: Integrasi faktur proyek
description: Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581242"
---
# <a name="project-invoice-integration"></a>Integrasi faktur proyek

Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.

Dalam Project Operations, manajer proyek mengelola akumulasi penagihan proyek dan membuat faktur proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan faktur proforma ini, petugas piutang dagang atau akuntan Proyek membuat faktur untuk pelanggan. Integrasi dual-write memastikan bahwa detail faktur proforma disinkronkan ke aplikasi Keuangan dan Operasi. Setelah faktur pelanggan dikirim, sistem memperbarui aktual proyek yang relevan di Dataverse dengan rincian akuntansi. Grafis berikut memberikan ikhtisar konsep tingkat tinggi integrasi ini.

   ![Integrasi faktur proyek.](./media/DW5Invoicing.png)

Setelah manajer Proyek mengonfirmasi faktur proforma pada Dataverse tahun 2010, informasi header faktur proforma disinkronkan ke aplikasi Keuangan dan Operasi menggunakan peta tabel tulis ganda, **Proposal faktur proyek V2 (faktur)**. Ini adalah integrasi satu arah dari Dataverse aplikasi Keuangan dan Operasi. Membuat atau menghapus proposal faktur Proyek secara langsung di aplikasi Keuangan dan Operasi tidak didukung.

Konfirmasi faktur di Dataverse juga memicu logika bisnis untuk membuat rekaman terkait penagihan di entitas **Aktual**. Catatan-catatan ini disinkronkan dengan Keuangan dan Operasi menggunakan peta tabel dual-write, **aktual integrasi Operasi Proyek (aktual msdyn\_).** Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md). 

Baris proposal faktur proyek dibuat oleh proses periodik, **Impor penahapan formulir**. Proses ini didasarkan pada rincian aktual penjualan yang ditagihkan dalam tabel **penahapan Aktual**. Untuk informasi lebih lanjut, lihat [Mengelola proposal faktur proyek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
