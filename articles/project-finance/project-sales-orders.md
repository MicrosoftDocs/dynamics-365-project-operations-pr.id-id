---
title: Pesanan penjualan proyek untuk proyek waktu dan material
description: Topik ini menjelaskan cara membuat pesanan penjualan berbasis proyek untuk proyek waktu dan material.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752390"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Pesanan penjualan proyek untuk proyek waktu dan material

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Topik ini menjelaskan cara membuat pesanan penjualan untuk proyek. Pesanan penjualan hanya dapat dibuat untuk proyek dengan jenis **waktu dan material**.

Jika proyek waktu dan material memiliki beberapa sumber pendanaan pada kontrak proyek, Anda harus mengaktifkan parameter **Izinkan pesanan penjualan untuk proyek dengan beberapa sumber pendanaan** pada halaman **manajemen proyek dan parameter akuntansi**. 

> [!NOTE]
> - Dukungan untuk pesanan penjualan proyek dengan beberapa sumber pendanaan tersedia mulai dari rilis aplikasi 10.0.2 dan lebih tinggi.
> - Parameter untuk mengaktifkan dukungan untuk pesanan penjualan proyek dengan beberapa sumber pendanaan akan dihapus di gelombang rilis 2020 April, setelah itu fungsi akan selalu diaktifkan.

Anda dapat membuat pesanan penjualan berbasis proyek dengan dua cara:

- Buka proyek itu sendiri. Pada panel tindakan, pilih **kelola > tugas Item > pesanan penjualan**. Informasi proyek akan default ke pesanan penjualan dari proyek. Jika kontrak proyek memiliki lebih dari satu sumber pendanaan, Anda harus memilih sumber dana untuk menetapkan pelanggan untuk pesanan penjualan. Jika hanya ada satu sumber pendanaan untuk proyek, pelanggan akan secara otomatis diatur.
- Buka halaman daftar **semua pesanan penjualan** dan buat pesanan penjualan baru. Anda harus memilih proyek untuk pesanan penjualan. Setelah proyek dipilih, pelanggan akan diatur dari sumber pendanaan atau Anda perlu memilih sumber pendanaan jika kontrak proyek memiliki beberapa sumber pendanaan.

