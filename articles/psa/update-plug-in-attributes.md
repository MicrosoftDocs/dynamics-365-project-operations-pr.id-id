---
title: Perbarui atribut plug-in untuk menyertakan dimensi harga baru
description: Topik ini menyediakan informasi tentang memperbarui atribut plug-in untuk dimensi harga.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281797"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="97b0c-103">Perbarui atribut plug-in untuk menyertakan dimensi harga baru</span><span class="sxs-lookup"><span data-stu-id="97b0c-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="97b0c-104">Jika Anda tidak menggunakan fitur kuotasi dan kontrak Project Service Automation (PSA), Anda dapat melewati topik ini.</span><span class="sxs-lookup"><span data-stu-id="97b0c-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="97b0c-105">Topik ini mengasumsikan bahwa anda telah menyelesaikan prosedur dalam topik, [membuat bidang kustom dan entitas](create-custom-fields-entities.md), [menambahkan bidang kustom untuk penyiapan harga dan entitas transaksi](field-references.md) serta [Mengonfigurasikan bidang kustom sebagai dimensi harga](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="97b0c-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="97b0c-106">Jika anda belum menyelesaikan prosedur tersebut, kembali dan selesaikan dan kemudian kembali ke topik ini.</span><span class="sxs-lookup"><span data-stu-id="97b0c-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="97b0c-107">Bila detail baris kuotasi dibuat pada halaman **baris kuotasi** untuk baris kuotasi proyek, sistem membuat dua baris perkiraan di background--satu baris untuk sisi biaya perkiraan dan satu untuk sisi penjualan.</span><span class="sxs-lookup"><span data-stu-id="97b0c-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="97b0c-108">Ini sama untuk baris kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="97b0c-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="97b0c-109">Bila Anda membuat perubahan pada kuantitas atau bidang pada sisi biaya, perubahan tersebut disebarkan ke sisi penjualan.</span><span class="sxs-lookup"><span data-stu-id="97b0c-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="97b0c-110">Hal ini dimungkinkan karena plug-in berikut yang harus didaftarkan ulang setelah perubahan pada dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="97b0c-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="97b0c-111">PreOperationContractLineDetailUpdate - Pembaruan **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="97b0c-112">PreOperationQuoteLineDetailUpdate - Pembaruan **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="97b0c-113">Langkah-langkah berikut menjelaskan proses pendaftaran plug-in.</span><span class="sxs-lookup"><span data-stu-id="97b0c-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="97b0c-114">Buka **PluginRegistrationTool** dan Sambungkan ke instans online Anda.</span><span class="sxs-lookup"><span data-stu-id="97b0c-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="97b0c-115">Klik **pencarian**, dan Cari plug-in untuk diperbarui.</span><span class="sxs-lookup"><span data-stu-id="97b0c-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Tangkapan layar dari pohon pencarian](media/PRT-1.png)

3. <span data-ttu-id="97b0c-117">Setelah plug-in ditemukan, pilih dan kemudian klik **pilih formulir utama**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="97b0c-118">Pilih langkah plug-in untuk diperbarui, klik kanan, lalu pilih **Perbarui**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Tangkapan layar plug-in yang akan diperbarui](media/PRT-2.png)
 
5. <span data-ttu-id="97b0c-120">Di jendela pembaruan, klik elipsis (**...**) di atribut pemfilteran.</span><span class="sxs-lookup"><span data-stu-id="97b0c-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Tangkapan layar pembaruan informasi konfigurasi langkah yang ada](media/PRT-3.png)
 
6. <span data-ttu-id="97b0c-122">Pilih kotak centang atribut penetapan harga.</span><span class="sxs-lookup"><span data-stu-id="97b0c-122">Select the pricing attribute check boxes.</span></span>

 ![Screenshot menampilkan pemilihan kotak centang untuk atribut harga](media/PRT-4.png)

7. <span data-ttu-id="97b0c-124">Klik **OK** untuk menutup halaman, lalu pilih **Perbarui langkah**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Screenshot menampilkan tombol "Perbarui langkah"](media/PRT-5.png)
 
8. <span data-ttu-id="97b0c-126">Ulangi proses ini untuk plug-in kedua, **PreOperationQuoteLineDetail - Pembaruan msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="97b0c-127">Tutup alat registrasi plug-in.</span><span class="sxs-lookup"><span data-stu-id="97b0c-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]