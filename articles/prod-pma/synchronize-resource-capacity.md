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
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288564"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="41620-103">Mensinkronkan kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="41620-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41620-104">Proses untuk sinkronisasi sumber daya membantu menjamin bahwa informasi untuk kalender dan kalender dasar menetes ke dalam penjadwalan sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="41620-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="41620-105">Jika kalender diubah, proses akan melakukan pembaruan yang diperlukan terhadap penjadwalan sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="41620-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="41620-106">Proses juga membantu meningkatkan kinerja, karena informasi sumber daya kalender disinkronisasikan terlebih dahulu.</span><span class="sxs-lookup"><span data-stu-id="41620-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="41620-107">Oleh karena itu, pembaruan untuk informasi penjadwalan sumber daya terjadi lebih cepat.</span><span class="sxs-lookup"><span data-stu-id="41620-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="41620-108">Sebaiknya jadwalkan proses sebagai kumpulan, bukan satu per satu.</span><span class="sxs-lookup"><span data-stu-id="41620-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="41620-109">Jika tidak, ada risiko bahwa seseorang akan melupakan tanggal inklusif saat informasi terakhir disinkronisasi.</span><span class="sxs-lookup"><span data-stu-id="41620-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="41620-110">Jika tanggal inklusif tidak digunakan, kesenjangan dapat terjadi selama sinkronisasi tanggal.</span><span class="sxs-lookup"><span data-stu-id="41620-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sinkronisasi kalender](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="41620-112">Sinkronisasikan akumulasi kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="41620-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="41620-113">Proses sinkronisasi dirancang untuk mensinkronisasi semua informasi kalender sumber daya.</span><span class="sxs-lookup"><span data-stu-id="41620-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="41620-114">Informasi ini mencakup informasi kalender dasar tentang perubahan pada tabel kapasitas kalender sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="41620-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="41620-115">Jika sumber daya baru ditambahkan dalam proyek, sinkronisasi akan membantu menjamin bahwa informasi kalender yang diperbarui tersedia.</span><span class="sxs-lookup"><span data-stu-id="41620-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="41620-116">Sinkronisasi ini dapat dilakukan kapan pun.</span><span class="sxs-lookup"><span data-stu-id="41620-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="41620-117">Sebaiknya Anda menggunakan kumpulan.</span><span class="sxs-lookup"><span data-stu-id="41620-117">We recommend that you use a batch.</span></span> <span data-ttu-id="41620-118">Pilihan tersedia selama sinkronisasi Pemesanan kapasitas.</span><span class="sxs-lookup"><span data-stu-id="41620-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="41620-119">Pilih **manajemen proyek dan akuntansi** &gt; **Periodik** &gt; **Sinkronisasi kapasitas** &gt; **Sinkronisasi akumulasi kapasitas sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="41620-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="41620-120">Atur pilihan dalam tabel berikut.</span><span class="sxs-lookup"><span data-stu-id="41620-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="41620-121">Opsi</span><span class="sxs-lookup"><span data-stu-id="41620-121">Option</span></span>      | <span data-ttu-id="41620-122">Deskripsi</span><span class="sxs-lookup"><span data-stu-id="41620-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="41620-123">Kode periode</span><span class="sxs-lookup"><span data-stu-id="41620-123">Period code</span></span> | <span data-ttu-id="41620-124">Atau pilih kode interval tanggal buku besar untuk mengatur tanggal mulai dan berakhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="41620-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="41620-125">Tanggal mulai</span><span class="sxs-lookup"><span data-stu-id="41620-125">Start date</span></span>  | <span data-ttu-id="41620-126">Masukkan tanggal mulai untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="41620-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="41620-127">Tanggal berakhir</span><span class="sxs-lookup"><span data-stu-id="41620-127">End date</span></span>    | <span data-ttu-id="41620-128">Masukkan tanggal akhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="41620-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="41620-129">[![Proses Sinkronisasi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="41620-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]