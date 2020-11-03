---
title: Mensinkronkan kapasitas sumber daya
description: Topik ini menyediakan informasi tentang cara mensinkronisasi kapasitas sumber daya di seluruh kalender dan proyek.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078462"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="4229d-103">Mensinkronkan kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="4229d-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4229d-104">Proses untuk sinkronisasi sumber daya membantu menjamin bahwa informasi untuk kalender dan kalender dasar menetes ke dalam penjadwalan sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="4229d-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="4229d-105">Jika kalender diubah, proses akan melakukan pembaruan yang diperlukan terhadap penjadwalan sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="4229d-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="4229d-106">Proses juga membantu meningkatkan kinerja, karena informasi sumber daya kalender disinkronisasikan terlebih dahulu.</span><span class="sxs-lookup"><span data-stu-id="4229d-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="4229d-107">Oleh karena itu, pembaruan untuk informasi penjadwalan sumber daya terjadi lebih cepat.</span><span class="sxs-lookup"><span data-stu-id="4229d-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="4229d-108">Sebaiknya jadwalkan proses sebagai kumpulan, bukan satu per satu.</span><span class="sxs-lookup"><span data-stu-id="4229d-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="4229d-109">Jika tidak, ada risiko bahwa seseorang akan melupakan tanggal inklusif saat informasi terakhir disinkronisasi.</span><span class="sxs-lookup"><span data-stu-id="4229d-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="4229d-110">Jika tanggal inklusif tidak digunakan, kesenjangan dapat terjadi selama sinkronisasi tanggal.</span><span class="sxs-lookup"><span data-stu-id="4229d-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sinkronisasi kalender](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="4229d-112">Sinkronisasikan akumulasi kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="4229d-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="4229d-113">Proses sinkronisasi dirancang untuk mensinkronisasi semua informasi kalender sumber daya.</span><span class="sxs-lookup"><span data-stu-id="4229d-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="4229d-114">Informasi ini mencakup informasi kalender dasar tentang perubahan pada tabel kapasitas kalender sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="4229d-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="4229d-115">Jika sumber daya baru ditambahkan dalam proyek, sinkronisasi akan membantu menjamin bahwa informasi kalender yang diperbarui tersedia.</span><span class="sxs-lookup"><span data-stu-id="4229d-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="4229d-116">Sinkronisasi ini dapat dilakukan kapan pun.</span><span class="sxs-lookup"><span data-stu-id="4229d-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="4229d-117">Sebaiknya Anda menggunakan kumpulan.</span><span class="sxs-lookup"><span data-stu-id="4229d-117">We recommend that you use a batch.</span></span> <span data-ttu-id="4229d-118">Pilihan tersedia selama sinkronisasi Pemesanan kapasitas.</span><span class="sxs-lookup"><span data-stu-id="4229d-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="4229d-119">Pilih **manajemen proyek dan akuntansi** &gt; **Periodik** &gt; **Sinkronisasi kapasitas** &gt; **Sinkronisasi akumulasi kapasitas sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="4229d-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="4229d-120">Atur pilihan dalam tabel berikut.</span><span class="sxs-lookup"><span data-stu-id="4229d-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="4229d-121">Opsi</span><span class="sxs-lookup"><span data-stu-id="4229d-121">Option</span></span>      | <span data-ttu-id="4229d-122">Deskripsi</span><span class="sxs-lookup"><span data-stu-id="4229d-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="4229d-123">Kode periode</span><span class="sxs-lookup"><span data-stu-id="4229d-123">Period code</span></span> | <span data-ttu-id="4229d-124">Atau pilih kode interval tanggal buku besar untuk mengatur tanggal mulai dan berakhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="4229d-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4229d-125">Tanggal mulai</span><span class="sxs-lookup"><span data-stu-id="4229d-125">Start date</span></span>  | <span data-ttu-id="4229d-126">Masukkan tanggal mulai untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="4229d-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4229d-127">Tanggal berakhir</span><span class="sxs-lookup"><span data-stu-id="4229d-127">End date</span></span>    | <span data-ttu-id="4229d-128">Masukkan tanggal akhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="4229d-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="4229d-129">[![Proses Sinkronisasi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="4229d-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
