---
title: Metode biaya penyelesaian
description: Topik ini berisi informasi tentang metode yang digunakan untuk menghitung biaya penyelesaian satu proyek.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 837cb3abe33e6e74087b8aae8b072bf4a21dc933
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279052"
---
# <a name="cost-to-complete-methods"></a><span data-ttu-id="6f956-103">Metode biaya penyelesaian</span><span class="sxs-lookup"><span data-stu-id="6f956-103">Cost to complete methods</span></span>

<span data-ttu-id="6f956-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="6f956-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6f956-105">Topik ini berisi informasi tentang metode yang digunakan untuk menghitung biaya penyelesaian satu proyek.</span><span class="sxs-lookup"><span data-stu-id="6f956-105">This topic provides information about the methods used to calculate the cost to complete a project.</span></span> <span data-ttu-id="6f956-106">Ada beberapa metode yang dapat Anda gunakan untuk menghitung biaya penyelesaian satu proyek.</span><span class="sxs-lookup"><span data-stu-id="6f956-106">There are multiple methods you can use to calculate the cost to complete a project.</span></span> 

<span data-ttu-id="6f956-107">Saat Anda membuat perkiraan untuk proyek, di halaman **Buat perkiraan**, di bidang **Metode biaya penyelesaian**, Anda dapat memilih salah satu biaya berikut untuk menyelesaikan metode.</span><span class="sxs-lookup"><span data-stu-id="6f956-107">When you create an estimate for a project, on the **Create estimate** page, in the **Cost to complete method** field, you can select one of the following cost to complete methods.</span></span>

| <span data-ttu-id="6f956-108">Metode biaya penyelesaian</span><span class="sxs-lookup"><span data-stu-id="6f956-108">Cost to complete method</span></span>    | <span data-ttu-id="6f956-109">KETERANGAN</span><span class="sxs-lookup"><span data-stu-id="6f956-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f956-110">Biaya total - aktual</span><span class="sxs-lookup"><span data-stu-id="6f956-110">Total cost-actual</span></span>            | <span data-ttu-id="6f956-111">Masukkan biaya estimasi secara manual di bidang **Biaya total** atau **Jumlah total** menggunakan tombol **Perkiraan biaya** pada halaman **Perkiraan**.</span><span class="sxs-lookup"><span data-stu-id="6f956-111">Enter estimate costs manually in the **Total cost** or **Total quantity** fields using the **Cost estimate** button on the **Estimate page**.</span></span> <span data-ttu-id="6f956-112">Sistem akan mengurangi biaya aktual dari total yang Anda masukkan.</span><span class="sxs-lookup"><span data-stu-id="6f956-112">The system subtracts the actual costs from the totals you entered.</span></span> <span data-ttu-id="6f956-113">Total adalah biaya untuk menyelesaikan proyek.</span><span class="sxs-lookup"><span data-stu-id="6f956-113">The total is the cost to complete the project.</span></span> <span data-ttu-id="6f956-114">Metode ini tidak menggunakan perkiraan pengeluaran dan penugasan sumber daya yang dimasukkan di Project Operations yang dibuat di dalam Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6f956-114">This method doesn't use the expense estimates and resources assignments entered in Project Operations built within Microsoft Dataverse.</span></span> <span data-ttu-id="6f956-115">Total biaya atau jumlah total dapat diperbarui secara manual sesuai kebutuhan.</span><span class="sxs-lookup"><span data-stu-id="6f956-115">The total cost or total quantity can be updated manually as needed.</span></span>  |
| <span data-ttu-id="6f956-116">Total prakiraan - aktual</span><span class="sxs-lookup"><span data-stu-id="6f956-116">Total forecast-actual</span></span>        | <span data-ttu-id="6f956-117">Penetapan sumber daya dan perkiraan biaya digunakan untuk menentukan total jumlah prakiraan proyek.</span><span class="sxs-lookup"><span data-stu-id="6f956-117">Resource assignments and expense estimates are used to determine the total project forecast amount.</span></span> <span data-ttu-id="6f956-118">Biaya aktual dibandingkan dengan prakiraan ini untuk menghitung biaya penyelesaian.</span><span class="sxs-lookup"><span data-stu-id="6f956-118">Actual costs are compared against this forecast to calculate the cost to complete.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6f956-119">Seperti estimasi sebelumnya</span><span class="sxs-lookup"><span data-stu-id="6f956-119">As previous estimate</span></span>         | <span data-ttu-id="6f956-120">Metode estimasi yang sama yang digunakan pada periode sebelumnya digunakan di sini.</span><span class="sxs-lookup"><span data-stu-id="6f956-120">The same estimate methods that was used in the previous period is used here.</span></span> <span data-ttu-id="6f956-121">Metode ini memerlukan model perkiraan jika periode sebelumnya memerlukan model perkiraan.</span><span class="sxs-lookup"><span data-stu-id="6f956-121">This method requires a forecast model if the previous period required a forecast model.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6f956-122">Atur biaya penyelesaian ke nol</span><span class="sxs-lookup"><span data-stu-id="6f956-122">Set cost to complete to zero</span></span> | <span data-ttu-id="6f956-123">Biasanya digunakan sebelum proyek estimasi dihilangkan, metode ini sesuai dengan estimasi total dengan transaksi aktual yang diposting dan menghapus **Biaya penyelesaian**.</span><span class="sxs-lookup"><span data-stu-id="6f956-123">Typically used before the estimate project is eliminated, this method matches total estimates with posted actual transactions and clears the **Cost to complete** column.</span></span> <span data-ttu-id="6f956-124">Setelah selesai, hasilnya selalu bernilai 100 persen.</span><span class="sxs-lookup"><span data-stu-id="6f956-124">When complete, the result is always 100 percent.</span></span> <span data-ttu-id="6f956-125">Untuk setiap lini biaya yang Anda buat, kotak centang **Prakiraan** dikosongkan dan estimasi total disalin dari estimasi biaya sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="6f956-125">For each cost line that you create, the **Forecasting** check box is cleared and the total estimate is copied from the previous cost estimate.</span></span> <span data-ttu-id="6f956-126">Konsumsi aktual untuk periode estimasi dikurangi dari biaya untuk menyelesaikan proyek.</span><span class="sxs-lookup"><span data-stu-id="6f956-126">The actual consumption for the estimate period is deducted from the cost to complete the project.</span></span>              |
| <span data-ttu-id="6f956-127">Dari template biaya</span><span class="sxs-lookup"><span data-stu-id="6f956-127">From cost template</span></span>           | <span data-ttu-id="6f956-128">Metode biaya penyelesaian yang diatur dalam template biaya yang terkait dengan proyek estimasi yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="6f956-128">The cost to complete method that is set up in the cost template that's associated with the selected estimate project.</span></span>                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]