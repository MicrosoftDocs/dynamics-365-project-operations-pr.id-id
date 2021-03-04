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
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147297"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="8bfdc-103">Menonaktifkan dimensi harga</span><span class="sxs-lookup"><span data-stu-id="8bfdc-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8bfdc-104">Anda mungkin harus meninjau dan memperbarui strategi harga setiap beberapa tahun.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="8bfdc-105">Pembaruan apa pun yang Anda buat mungkin mengharuskan Anda menonaktifkan dimensi harga yang ada dan membuat yang baru.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="8bfdc-106">Misalnya, Anda mungkin sebelumnya menetapkan harga berdasarkan **peran**, tapi sekarang Anda telah memutuskan harga dengan **pengalaman kerja**.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="8bfdc-107">Ini mungkin mengharuskan Anda menonaktifkan **peran** sebagai dimensi harga dan membuat **pengalaman kerja** sebagai dimensi harga baru.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="8bfdc-108">Menonaktifkan dimensi harga, tidak peduli apakah itu bawaan atau kustom, dapat dilakukan dengan mengatur bidang **berlaku untuk biaya** dan **berlaku untuk penjualan** pada dimensi harga ke **tidak**.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="8bfdc-109">Namun, bila Anda melakukannya, Anda mungkin menerima pesan kesalahan berikut.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-109">However, when you do this, you might receive the following error message.</span></span>

![Kesalahan proses bisnis cenderung terjadi saat mematikan dimensi harga](media/Business-Process-Error.png)


<span data-ttu-id="8bfdc-111">Pesan kesalahan ini menunjukkan bahwa ada rekaman harga yang diatur sebelumnya untuk dimensi yang dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="8bfdc-112">Semua rekaman **harga peran** dan **markup harga peran** yang merujuk ke dimensi harus dihapus sebelum penerapan dimensi dapat diatur ke **tidak**.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="8bfdc-113">Aturan ini berlaku untuk dimensi harga Bawaan dan dimensi harga kustom apa pun yang mungkin telah Anda buat.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="8bfdc-114">Alasan untuk validasi ini adalah karena Project Service memiliki batasan bahwa setiap rekaman **harga peran** harus memiliki kombinasi dimensi yang unik.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="8bfdc-115">Misalnya, pada daftar harga yang disebut **Tarif Biaya AS 2018**, Anda memiliki baris **harga peran** berikut.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="8bfdc-116">Jabatan standar</span><span class="sxs-lookup"><span data-stu-id="8bfdc-116">Standard Title</span></span>         | <span data-ttu-id="8bfdc-117">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="8bfdc-117">Org Unit</span></span>    |<span data-ttu-id="8bfdc-118">Unit</span><span class="sxs-lookup"><span data-stu-id="8bfdc-118">Unit</span></span>   |<span data-ttu-id="8bfdc-119">Harga</span><span class="sxs-lookup"><span data-stu-id="8bfdc-119">Price</span></span>  |<span data-ttu-id="8bfdc-120">Mata Uang</span><span class="sxs-lookup"><span data-stu-id="8bfdc-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="8bfdc-121">Insinyur sistem</span><span class="sxs-lookup"><span data-stu-id="8bfdc-121">Systems Engineer</span></span>|<span data-ttu-id="8bfdc-122">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="8bfdc-122">Contoso US</span></span>|<span data-ttu-id="8bfdc-123">Hour</span><span class="sxs-lookup"><span data-stu-id="8bfdc-123">Hour</span></span>| <span data-ttu-id="8bfdc-124">100</span><span class="sxs-lookup"><span data-stu-id="8bfdc-124">100</span></span>|<span data-ttu-id="8bfdc-125">USD</span><span class="sxs-lookup"><span data-stu-id="8bfdc-125">USD</span></span>|
| <span data-ttu-id="8bfdc-126">Insinyur sistem senior</span><span class="sxs-lookup"><span data-stu-id="8bfdc-126">Senior Systems Engineer</span></span>|<span data-ttu-id="8bfdc-127">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="8bfdc-127">Contoso US</span></span>|<span data-ttu-id="8bfdc-128">Hour</span><span class="sxs-lookup"><span data-stu-id="8bfdc-128">Hour</span></span>| <span data-ttu-id="8bfdc-129">150</span><span class="sxs-lookup"><span data-stu-id="8bfdc-129">150</span></span>| <span data-ttu-id="8bfdc-130">USD</span><span class="sxs-lookup"><span data-stu-id="8bfdc-130">USD</span></span>|


<span data-ttu-id="8bfdc-131">Bila Anda menonaktifkan **jabatan standar** sebagai dimensi harga, dan mesin harga Project Service mencari harga, ia hanya akan menggunakan nilai **unit organisasi** dari konteks input.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="8bfdc-132">Jika **unit organisasi** konteks input adalah "Aswono US", hasilnya akan non-deterministik karena kedua baris akan cocok.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="8bfdc-133">Untuk menghindari skenario ini, saat Anda membuat rekaman **harga peran**, Project Service memvalidasi bahwa kombinasi dimensi itu adalah unik.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="8bfdc-134">Jika dimensi dinonaktifkan setelah rekaman **harga peran** dibuat, kendala ini dapat dilanggar.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="8bfdc-135">Oleh karena itu, diperlukan bahwa sebelum Anda menonaktifkan dimensi, Anda menghapus semua baris **harga peran** dan **markup harga peran** yang diisi nilai dimensi tersebut.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

