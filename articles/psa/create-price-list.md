---
title: Membuat daftar harga
description: Bagaimana membuat daftar harga di Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290318"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="96698-103">Membuat daftar harga (Project Service)</span><span class="sxs-lookup"><span data-stu-id="96698-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="96698-104">Daftar harga menyediakan template yang dapat digunakan manajer account Anda untuk membuat kuotasi dan proyek, dan untuk menetapkan biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="96698-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="96698-105">Mereka menyediakan daftar item baris peran dan pengeluaran, dan harga yang Anda akan kenakan untuk masing-masing.</span><span class="sxs-lookup"><span data-stu-id="96698-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="96698-106">Anda dapat membuat beberapa daftar harga sehingga Anda dapat menjaga struktur harga terpisah untuk Anda menjual produk Anda di daerah yang berbeda atau saluran penjualan yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="96698-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="96698-107">Adalah ide yang baik untuk membuat setidaknya satu daftar harga untuk setiap mata uang yang Anda rencanakan untuk tagih pelanggan Anda.</span><span class="sxs-lookup"><span data-stu-id="96698-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="96698-108">Untuk membuat perkiraan keuangan untuk pekerjaan yang akan dilaksanakan, pastikan setiap proyek memiliki daftar harga biaya dan penjualan cadangan.</span><span class="sxs-lookup"><span data-stu-id="96698-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="96698-109">Atur standar daftar biaya dan harga penjualan yang berlaku untuk semua proyek-proyek yang dibuat di organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="96698-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="96698-110">Daftar harga bergantung pada peran dan kategori pengeluaran, jadi sebelum membuat daftar harga, pastikan Anda telah mengonfigurasi peran dan biaya kategori yang ingin Anda gunakan sewaktu membuat daftar harga.</span><span class="sxs-lookup"><span data-stu-id="96698-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="96698-111">Pergi ke **Project Service > Daftar harga**.</span><span class="sxs-lookup"><span data-stu-id="96698-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="96698-112">Klik **Baru**.</span><span class="sxs-lookup"><span data-stu-id="96698-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="96698-113">Dalam **konteks**, pilih apakah daftar harga ini untuk **biaya**, **pembelian**, atau **penjualan**.</span><span class="sxs-lookup"><span data-stu-id="96698-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="96698-114">Dalam **nama**, masukkan nama untuk daftar harga.</span><span class="sxs-lookup"><span data-stu-id="96698-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="96698-115">Dalam **mata uang**, pilih mata uang yang Anda akan gunakan untuk penagihan atau biaya.</span><span class="sxs-lookup"><span data-stu-id="96698-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="96698-116">Dalam **Unit waktu**, tentukan periode waktu Harga berlaku, seperti hari atau jam.</span><span class="sxs-lookup"><span data-stu-id="96698-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="96698-117">Isi **tanggal mulai**, **tanggal akhir**, dan **Deskripsi** yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="96698-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="96698-118">Klik **Simpan** untuk membuat rekaman sehingga Anda dapat terus mengedit.</span><span class="sxs-lookup"><span data-stu-id="96698-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="96698-119">Untuk menambahkan harga peran ke daftar harga, klik **+** di bawah **harga peran**.</span><span class="sxs-lookup"><span data-stu-id="96698-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="96698-120">Dalam panel **harga peran**, isi rincian, dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="96698-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96698-121">Terus tambahkan harga peran yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="96698-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="96698-122">Setelah selesai klik **Simpan** di sudut kanan bawah layar.</span><span class="sxs-lookup"><span data-stu-id="96698-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="96698-123">Untuk menambahkan harga kategori biaya ke daftar harga, klik **+** di bawah **harga Kategori**.</span><span class="sxs-lookup"><span data-stu-id="96698-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="96698-124">Dalam panel **harga Kategori Transaksi**, isi rincian, dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="96698-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96698-125">Terus tambahkan harga kategori yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="96698-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="96698-126">Setelah selesai klik **Simpan** di sudut kanan bawah layar.</span><span class="sxs-lookup"><span data-stu-id="96698-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="96698-127">Untuk menambahkan item daftar harga ke daftar harga, klik **+** di bawah **item daftar harga**.</span><span class="sxs-lookup"><span data-stu-id="96698-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="96698-128">Dalam panel **item daftar harga**, isi rincian, dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="96698-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96698-129">Terus tambahkan item daftar harga yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="96698-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="96698-130">Setelah selesai klik **Simpan** di sudut kanan bawah layar.</span><span class="sxs-lookup"><span data-stu-id="96698-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="96698-131">Untuk menambahkan hubungan wilayah ke daftar harga, klik **+** di bawah **hubungan wilayah**.</span><span class="sxs-lookup"><span data-stu-id="96698-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="96698-132">Dalam jendela **Koneksi Baru**, isi rincian, dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="96698-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96698-133">Terus menambahkan hubungan wilayah yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="96698-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="96698-134">Setelah selesai klik **Simpan** di sudut kanan bawah layar.</span><span class="sxs-lookup"><span data-stu-id="96698-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="96698-135">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="96698-135">See Also</span></span>  
 [<span data-ttu-id="96698-136">Konfigurasi Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="96698-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]