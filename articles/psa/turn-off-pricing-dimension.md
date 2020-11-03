---
title: Menonaktifkan dimensi harga
description: Topik ini menunjukkan cara mengkonfigurasi dimensi harga dalam solusi Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078569"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="db145-103">Menonaktifkan dimensi harga</span><span class="sxs-lookup"><span data-stu-id="db145-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="db145-104">Anda mungkin harus meninjau dan memperbarui strategi harga setiap beberapa tahun.</span><span class="sxs-lookup"><span data-stu-id="db145-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="db145-105">Pembaruan apa pun yang Anda buat mungkin mengharuskan Anda menonaktifkan dimensi harga yang ada dan membuat yang baru.</span><span class="sxs-lookup"><span data-stu-id="db145-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="db145-106">Misalnya, Anda mungkin sebelumnya menetapkan harga berdasarkan **peran** , tapi sekarang Anda telah memutuskan harga dengan **pengalaman kerja**.</span><span class="sxs-lookup"><span data-stu-id="db145-106">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="db145-107">Ini mungkin mengharuskan Anda menonaktifkan **peran** sebagai dimensi harga dan membuat **pengalaman kerja** sebagai dimensi harga baru.</span><span class="sxs-lookup"><span data-stu-id="db145-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="db145-108">Menonaktifkan dimensi harga, tidak peduli apakah itu bawaan atau kustom, dapat dilakukan dengan mengatur bidang **berlaku untuk biaya** dan **berlaku untuk penjualan** pada dimensi harga ke **tidak**.</span><span class="sxs-lookup"><span data-stu-id="db145-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="db145-109">Namun, bila Anda melakukannya, Anda mungkin menerima pesan kesalahan berikut.</span><span class="sxs-lookup"><span data-stu-id="db145-109">However, when you do this, you might receive the following error message.</span></span>

![Kesalahan proses bisnis cenderung terjadi saat mematikan dimensi harga](media/Business-Process-Error.png)


<span data-ttu-id="db145-111">Pesan kesalahan ini menunjukkan bahwa ada rekaman harga yang diatur sebelumnya untuk dimensi yang dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="db145-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="db145-112">Semua rekaman **harga peran** dan **markup harga peran** yang merujuk ke dimensi harus dihapus sebelum penerapan dimensi dapat diatur ke **tidak**.</span><span class="sxs-lookup"><span data-stu-id="db145-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="db145-113">Aturan ini berlaku untuk dimensi harga Bawaan dan dimensi harga kustom apa pun yang mungkin telah Anda buat.</span><span class="sxs-lookup"><span data-stu-id="db145-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="db145-114">Alasan untuk validasi ini adalah karena Project Service memiliki batasan bahwa setiap rekaman **harga peran** harus memiliki kombinasi dimensi yang unik.</span><span class="sxs-lookup"><span data-stu-id="db145-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="db145-115">Misalnya, pada daftar harga yang disebut **Tarif Biaya AS 2018** , Anda memiliki baris **harga peran** berikut.</span><span class="sxs-lookup"><span data-stu-id="db145-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="db145-116">Jabatan standar</span><span class="sxs-lookup"><span data-stu-id="db145-116">Standard Title</span></span>         | <span data-ttu-id="db145-117">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="db145-117">Org Unit</span></span>    |<span data-ttu-id="db145-118">Unit</span><span class="sxs-lookup"><span data-stu-id="db145-118">Unit</span></span>   |<span data-ttu-id="db145-119">Harga</span><span class="sxs-lookup"><span data-stu-id="db145-119">Price</span></span>  |<span data-ttu-id="db145-120">Mata Uang</span><span class="sxs-lookup"><span data-stu-id="db145-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="db145-121">Insinyur sistem</span><span class="sxs-lookup"><span data-stu-id="db145-121">Systems Engineer</span></span>|<span data-ttu-id="db145-122">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="db145-122">Contoso US</span></span>|<span data-ttu-id="db145-123">Hour</span><span class="sxs-lookup"><span data-stu-id="db145-123">Hour</span></span>| <span data-ttu-id="db145-124">100</span><span class="sxs-lookup"><span data-stu-id="db145-124">100</span></span>|<span data-ttu-id="db145-125">USD</span><span class="sxs-lookup"><span data-stu-id="db145-125">USD</span></span>|
| <span data-ttu-id="db145-126">Insinyur sistem senior</span><span class="sxs-lookup"><span data-stu-id="db145-126">Senior Systems Engineer</span></span>|<span data-ttu-id="db145-127">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="db145-127">Contoso US</span></span>|<span data-ttu-id="db145-128">Hour</span><span class="sxs-lookup"><span data-stu-id="db145-128">Hour</span></span>| <span data-ttu-id="db145-129">150</span><span class="sxs-lookup"><span data-stu-id="db145-129">150</span></span>| <span data-ttu-id="db145-130">USD</span><span class="sxs-lookup"><span data-stu-id="db145-130">USD</span></span>|


<span data-ttu-id="db145-131">Bila Anda menonaktifkan **jabatan standar** sebagai dimensi harga, dan mesin harga Project Service mencari harga, ia hanya akan menggunakan nilai **unit organisasi** dari konteks input.</span><span class="sxs-lookup"><span data-stu-id="db145-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="db145-132">Jika **unit organisasi** konteks input adalah "Aswono US", hasilnya akan non-deterministik karena kedua baris akan cocok.</span><span class="sxs-lookup"><span data-stu-id="db145-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="db145-133">Untuk menghindari skenario ini, saat Anda membuat rekaman **harga peran** , Project Service memvalidasi bahwa kombinasi dimensi itu adalah unik.</span><span class="sxs-lookup"><span data-stu-id="db145-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="db145-134">Jika dimensi dinonaktifkan setelah rekaman **harga peran** dibuat, kendala ini dapat dilanggar.</span><span class="sxs-lookup"><span data-stu-id="db145-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="db145-135">Oleh karena itu, diperlukan bahwa sebelum Anda menonaktifkan dimensi, Anda menghapus semua baris **harga peran** dan **markup harga peran** yang diisi nilai dimensi tersebut.</span><span class="sxs-lookup"><span data-stu-id="db145-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

