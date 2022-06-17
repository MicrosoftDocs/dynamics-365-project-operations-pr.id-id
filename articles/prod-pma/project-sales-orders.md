---
title: Pesanan penjualan proyek untuk proyek waktu dan material
description: Artikel ini menjelaskan cara membuat pesanan penjualan berbasis proyek untuk proyek waktu dan material.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3a040de6d22b626b9e3d462272f43c5763b5b90f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933818"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Pesanan penjualan proyek untuk proyek waktu dan material

[!include[banner](../includes/banner.md)]

Artikel ini menjelaskan cara membuat pesanan penjualan untuk proyek. Pesanan penjualan hanya dapat dibuat untuk proyek dengan jenis **waktu dan material**.

Jika proyek waktu dan material memiliki beberapa sumber pendanaan pada kontrak proyek, Anda harus mengaktifkan parameter **Izinkan pesanan penjualan untuk proyek dengan beberapa sumber pendanaan** pada halaman **manajemen proyek dan parameter akuntansi**. 

> [!NOTE]
> - Dukungan untuk pesanan penjualan proyek dengan beberapa sumber pendanaan tersedia mulai dari rilis aplikasi 10.0.2 dan lebih tinggi.
> - Parameter untuk mengaktifkan dukungan untuk pesanan penjualan proyek dengan beberapa sumber pendanaan akan dihapus di gelombang rilis 2020 April, setelah itu fungsi akan selalu diaktifkan.

Anda dapat membuat pesanan penjualan berbasis proyek dengan dua cara:

- Buka proyek itu sendiri. Pada panel tindakan, pilih **kelola > tugas Item > pesanan penjualan**. Informasi proyek akan default ke pesanan penjualan dari proyek. Jika kontrak proyek memiliki lebih dari satu sumber pendanaan, Anda harus memilih sumber dana untuk menetapkan pelanggan untuk pesanan penjualan. Jika hanya ada satu sumber pendanaan untuk proyek, pelanggan akan secara otomatis diatur.
- Buka halaman daftar **semua pesanan penjualan** dan buat pesanan penjualan baru. Anda harus memilih proyek untuk pesanan penjualan. Setelah proyek dipilih, pelanggan akan diatur dari sumber pendanaan atau Anda perlu memilih sumber pendanaan jika kontrak proyek memiliki beberapa sumber pendanaan.



[!INCLUDE[footer-include](../includes/footer-banner.md)]