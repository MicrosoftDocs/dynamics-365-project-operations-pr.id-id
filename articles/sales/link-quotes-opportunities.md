---
title: Membuat kuotasi proyek dari peluang
description: Topik ini menyediakan informasi tentang membuat kuotasi proyek dari peluang.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078396"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="3a7fc-103">Membuat kuotasi proyek dari peluang</span><span class="sxs-lookup"><span data-stu-id="3a7fc-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="3a7fc-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="3a7fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3a7fc-105">Kuotasi dapat dibuat dari peluang proyek dengan cara berikut:</span><span class="sxs-lookup"><span data-stu-id="3a7fc-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="3a7fc-106">Dari tab **kuotasi** pada halaman **peluang proyek**</span><span class="sxs-lookup"><span data-stu-id="3a7fc-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="3a7fc-107">Dari alur Proses Penjualan Peluang</span><span class="sxs-lookup"><span data-stu-id="3a7fc-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="3a7fc-108">Dengan memperbarui referensi peluang pada kuotasi yang ada</span><span class="sxs-lookup"><span data-stu-id="3a7fc-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="3a7fc-109">Dari tab kuotasi pada halaman peluang proyek</span><span class="sxs-lookup"><span data-stu-id="3a7fc-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="3a7fc-110">Untuk membuat kuotasi proyek dari peluang, selesaikan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="3a7fc-111">Buka halaman **peluang proyek** dan pilih tab **Kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="3a7fc-112">Pada subkisi **kuotasi** , pilih **+** untuk membuat kuotasi proyek baru berdasarkan peluang.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="3a7fc-113">Semua baris peluang dan daftar harga proyek terkait akan disalin ke kuotasi baru dari peluang.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="3a7fc-114">Dari alur Proses Penjualan Peluang</span><span class="sxs-lookup"><span data-stu-id="3a7fc-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="3a7fc-115">Untuk membuat kuotasi dari alur proses penjualan peluang, selesaikan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="3a7fc-116">Dari alur proses penjualan peluang, buka peluang.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="3a7fc-117">Pilih tahap **Kualifikasi**.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="3a7fc-118">Pilih **berikutnya,** lalu pilih **+ buat** untuk membuat kuotasi baru.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="3a7fc-119">Sebagian besar informasi pada tab **ringkasan** untuk kuotasi baru ini akan di-default dari peluang.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="3a7fc-120">Masukkan informasi diperlukan yang tidak ada, atau Perbarui nilai default yang diperlukan pada tab **ringkasan** ,</span><span class="sxs-lookup"><span data-stu-id="3a7fc-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="3a7fc-121">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-121">Select **Save**.</span></span> <span data-ttu-id="3a7fc-122">Kuotasi baru dibuat dan terkait dengan peluang.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="3a7fc-123">Anda sekarang dapat melihat informasi kuotasi pada tab **kuotasi** pada halaman **peluang**.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="3a7fc-124">Proses penjualan peluang bergerak ke tahap berikutnya, **mengusulkan**.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="3a7fc-125">Dengan memperbarui referensi peluang pada kuotasi yang ada</span><span class="sxs-lookup"><span data-stu-id="3a7fc-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="3a7fc-126">Kuotasi yang ada dapat ditautkan ke peluang.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="3a7fc-127">Selesaikan langkah-langkah berikut untuk memperbarui informasi peluang pada kuotasi yang ada.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="3a7fc-128">Buka halaman **Kuotasi** dan pilih tab **Ringkasan**.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="3a7fc-129">Di bidang **peluang** , pilih peluang yang akan ditautkan ke kuotasi.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="3a7fc-130">Anda dapat melihat kuotasi di kisi **kuotasi** peluang.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="3a7fc-131">Menggunakan proses penjualan peluang, peluang dapat dipindahkan ke tahap berikutnya, **mengusulkan**.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="3a7fc-132">Saat Anda memindahkan peluang ke tahapan ini, Anda dapat memilih kuotasi ini dari daftar kuotasi yang terkait dengan peluang ini.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="3a7fc-133">Memilih kuotasi ini menunjukkan bahwa Anda bergerak maju dengan itu.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="3a7fc-134">Semua tanda lainnya yang terkait dengan peluang akan tetap tersedia dan aktif hingga salah satunya dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="3a7fc-135">Anda dapat memindahkan proses penjualan kembali ke tahap sebelumnya yaitu **Kualifikasi** , dan memilih kuotasi lainnya untuk diteruskan.</span><span class="sxs-lookup"><span data-stu-id="3a7fc-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
