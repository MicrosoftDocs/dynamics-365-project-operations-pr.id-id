---
title: Memperbarui atribut plug-in dengan menyertakan dimensi harga baru
description: Topik ini berisi informasi tentang cara memperbarui atribut plug-in untuk dimensi harga.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274687"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="f2ba9-103">Memperbarui atribut plug-in dengan menyertakan dimensi harga baru</span><span class="sxs-lookup"><span data-stu-id="f2ba9-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="f2ba9-104">Topik ini berisi informasi tentang cara memperbarui atribut plug-in untuk dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="f2ba9-105">Topik ini hanya berlaku untuk fitur kuotasi dan kontrak di Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2ba9-106">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="f2ba9-106">Prerequisites</span></span>
<span data-ttu-id="f2ba9-107">Sebelum Anda menyelesaikan langkah-langkah dalam topik ini, Anda harus menyelesaikan prosedur dalam topik berikut:</span><span class="sxs-lookup"><span data-stu-id="f2ba9-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="f2ba9-108">Membuat bidang dan entitas kustom</span><span class="sxs-lookup"><span data-stu-id="f2ba9-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="f2ba9-109">Menambahkan bidang kustom ke pengaturan harga dan entitas transaksi </span><span class="sxs-lookup"><span data-stu-id="f2ba9-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="f2ba9-110">[Mengonfigurasikan bidang kustom sebagai dimensi harga](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="f2ba9-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="f2ba9-111">Jika Anda belum menyelesaikan prosedur tersebut, selesaikan dan kemudian kembali ke topik ini.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="f2ba9-112">Mendaftarkan plug-in</span><span class="sxs-lookup"><span data-stu-id="f2ba9-112">Register a plug-in</span></span>
<span data-ttu-id="f2ba9-113">Apabila rincian baris kuotasi dibuat pada halaman **Baris Kuotasi** untuk baris kuotasi proyek, sistem membuat dua baris estimasi.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="f2ba9-114">Satu baris adalah untuk sisi biaya estimasi dan baris lainnya adalah untuk sisi penjualan.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="f2ba9-115">Ini sama untuk baris kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="f2ba9-116">Apabila Anda membuat perubahan pada kuantitas atau bidang pada sisi biaya, perubahan tersebut juga dilakukan sisi penjualan.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="f2ba9-117">Hal ini dimungkinkan karena plug-in PreOperation di entitas Quotelinedetail dan rincian contractline menghubungkan atribut tertentu di sisi biaya ke sisi penjualan pada transaksi.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="f2ba9-118">Jika Anda memerlukan perubahan yang dibuat pada nilai dimensi harga di sisi penjualan untuk juga dibuat pada sisi biaya, plug-in berikut harus didaftarkan ulang setelah membuat perubahan pada dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="f2ba9-119">Berikut adalah plug-in untuk memperbarui dan mendaftar ulang:</span><span class="sxs-lookup"><span data-stu-id="f2ba9-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="f2ba9-120">PreOperationContractLineDetailUpdate - **Pembaruan msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="f2ba9-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="f2ba9-121">PreOperationQuoteLineDetailUpdate - **Pembaruan msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="f2ba9-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="f2ba9-122">Lakukan langkah-langkah berikut untuk memperbarui dan mendaftarkan ulang plug-in.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="f2ba9-123">Buka **PluginRegistrationTool** dan sambungkan ke lingkungan Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="f2ba9-124">Pilih **Cari**, dan ketik beberapa huruf pertama plug-in yang akan diperbarui.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="f2ba9-125">Setelah plug-in ditemukan, pilih dan kemudian pilih **Pilih Formulir Utama**.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="f2ba9-126">Pilih langkah **Perbarui msdyn_orderlinetransaction**, klik kanan dan kemudian pilih **Perbarui**.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="f2ba9-127">Di halaman dialog **Perbarui**, pilih elipsis (**...**) di atribut pemfilteran.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="f2ba9-128">Jendela atribut filter akan terbuka dan menyediakan daftar semua atribut di entitas dan dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="f2ba9-129">Pilih kotak centang untuk atribut dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="f2ba9-130">Pilih **OK** untuk menutup halaman, lalu pilih **Perbarui Langkah**.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="f2ba9-131">Ulangi langkah 2-7 untuk plug-in kedua, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="f2ba9-132">Untuk plug-in ini, Anda harus memperbarui langkah **Pembaruan msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="f2ba9-133">Tutup **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]