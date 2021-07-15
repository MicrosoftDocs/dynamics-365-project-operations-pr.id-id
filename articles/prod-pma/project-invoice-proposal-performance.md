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
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="2f04c-103">Kinerja proposal faktur proyek</span><span class="sxs-lookup"><span data-stu-id="2f04c-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f04c-104">Saat membuat proposal faktur baru, Anda mungkin mengalami masalah performa saat jumlah proyek dan subkisi meningkat.</span><span class="sxs-lookup"><span data-stu-id="2f04c-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="2f04c-105">Untuk meningkatkan kinerja, fitur tersedia yang mengurangi waktu yang diperlukan untuk membuat proposal faktur baru untuk transaksi proyek yang diposting.</span><span class="sxs-lookup"><span data-stu-id="2f04c-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="2f04c-106">Aktifkan peningkatan Kinerja proposal faktur proyek</span><span class="sxs-lookup"><span data-stu-id="2f04c-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="2f04c-107">Untuk mengaktifkan fitur peningkatan performa proposal faktur proyek, selesaikan langkah-langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="2f04c-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="2f04c-108">Buka **manajemen Fitur** > **Semua**.</span><span class="sxs-lookup"><span data-stu-id="2f04c-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="2f04c-109">Dalam daftar fitur, cari **Peningkatan kinerja proposal faktur proyek**.</span><span class="sxs-lookup"><span data-stu-id="2f04c-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="2f04c-110">Klik **Aktifkan sekarang**.</span><span class="sxs-lookup"><span data-stu-id="2f04c-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="2f04c-111">Refresh browser Anda, lalu buat proposal faktur baru.</span><span class="sxs-lookup"><span data-stu-id="2f04c-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="2f04c-112">Nonaktifkan peningkatan Kinerja proposal faktur proyek</span><span class="sxs-lookup"><span data-stu-id="2f04c-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="2f04c-113">Selesaikan langkah berikut ini untuk menonaktifkan fitur peningkatan performa proposal faktur proyek.</span><span class="sxs-lookup"><span data-stu-id="2f04c-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="2f04c-114">Buka **manajemen Fitur** > **Semua**.</span><span class="sxs-lookup"><span data-stu-id="2f04c-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="2f04c-115">Dalam daftar fitur, cari **Peningkatan kinerja proposal faktur proyek**.</span><span class="sxs-lookup"><span data-stu-id="2f04c-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="2f04c-116">Klik **Nonaktifkan**.</span><span class="sxs-lookup"><span data-stu-id="2f04c-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="2f04c-117">Refresh browser Anda.</span><span class="sxs-lookup"><span data-stu-id="2f04c-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="2f04c-118">Performa proposal faktur tidak dapat diterapkan saat aturan penagihan diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="2f04c-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="2f04c-119">Selama proses kumpulan untuk membuat proposal faktur, jumlah subtugas akan memecah tugas menjadi jumlah maksimum berdasarkan jumlah kontrak dengan transaksi yang dapat ditagih, berapa pun yang telah Anda masukkan.</span><span class="sxs-lookup"><span data-stu-id="2f04c-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="2f04c-120">Contohnya, jika Anda memasukkan **3** untuk jumlah subtugas untuk pembuatan proposal faktur dalam kumpulan, dan hanya ada dua kontrak dengan transaksi yang dapat ditagih, hanya dua subtugas yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="2f04c-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
