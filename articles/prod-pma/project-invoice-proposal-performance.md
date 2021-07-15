---
title: Kinerja proposal faktur proyek
description: Laporan topik ini berisi informasi tentang peningkatan performa pada proposal faktur proyek.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269794"
---
# <a name="project-invoice-proposal-performance"></a>Kinerja proposal faktur proyek

[!include [banner](../includes/banner.md)]

Saat membuat proposal faktur baru, Anda mungkin mengalami masalah performa saat jumlah proyek dan subkisi meningkat. Untuk meningkatkan kinerja, fitur tersedia yang mengurangi waktu yang diperlukan untuk membuat proposal faktur baru untuk transaksi proyek yang diposting.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Aktifkan peningkatan Kinerja proposal faktur proyek
Untuk mengaktifkan fitur peningkatan performa proposal faktur proyek, selesaikan langkah-langkah berikut.

1.  Buka **manajemen Fitur** > **Semua**. Dalam daftar fitur, cari **Peningkatan kinerja proposal faktur proyek**.
2.  Klik **Aktifkan sekarang**.
3.  Refresh browser Anda, lalu buat proposal faktur baru.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Nonaktifkan peningkatan Kinerja proposal faktur proyek
Selesaikan langkah berikut ini untuk menonaktifkan fitur peningkatan performa proposal faktur proyek.

1.  Buka **manajemen Fitur** > **Semua**. Dalam daftar fitur, cari **Peningkatan kinerja proposal faktur proyek**.
2.  Klik **Nonaktifkan**.
3.  Refresh browser Anda.

> [!NOTE]
> Performa proposal faktur tidak dapat diterapkan saat aturan penagihan diaktifkan.
> 
> Selama proses kumpulan untuk membuat proposal faktur, jumlah subtugas akan memecah tugas menjadi jumlah maksimum berdasarkan jumlah kontrak dengan transaksi yang dapat ditagih, berapa pun yang telah Anda masukkan. Contohnya, jika Anda memasukkan **3** untuk jumlah subtugas untuk pembuatan proposal faktur dalam kumpulan, dan hanya ada dua kontrak dengan transaksi yang dapat ditagih, hanya dua subtugas yang dibuat.
