---
title: Unit dan grup unit
description: Topik ini memberikan informasi tentang cara membuat unit dan grup unit di Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996075"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="41bbe-103">Unit dan grup unit</span><span class="sxs-lookup"><span data-stu-id="41bbe-103">Units and unit groups</span></span>

<span data-ttu-id="41bbe-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="41bbe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="41bbe-105">Unit adalah kuantitas atau pengukuran tempat Anda menjual produk atau layanan.</span><span class="sxs-lookup"><span data-stu-id="41bbe-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="41bbe-106">Misalnya, jika Anda menjual perlengkapan berkebun, Anda mungkin menjual benih dalam satuan paket, kotak, dan palet.</span><span class="sxs-lookup"><span data-stu-id="41bbe-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="41bbe-107">Grup unit adalah kumpulan unit berbeda ini.</span><span class="sxs-lookup"><span data-stu-id="41bbe-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="41bbe-108">Untuk menyelesaikan langkah-langkah dalam topik ini, pastikan Anda telah ditetapkan ke peran Administrator sistem, atau manajer Sales Professional, atau memiliki izin yang setara.</span><span class="sxs-lookup"><span data-stu-id="41bbe-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="41bbe-109">Membuat grup unit</span><span class="sxs-lookup"><span data-stu-id="41bbe-109">Create a unit group</span></span>

1. <span data-ttu-id="41bbe-110">Di peta situs, pilih **Unit**.</span><span class="sxs-lookup"><span data-stu-id="41bbe-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="41bbe-111">Pilih **baru**, dan di kotak dialog **Buat grup unit**, masukkan nama unit.</span><span class="sxs-lookup"><span data-stu-id="41bbe-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="41bbe-112">Di bidang **unit primer**, Masukkan satuan pengukuran umum terendah yang dari sana produk akan dijual.</span><span class="sxs-lookup"><span data-stu-id="41bbe-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="41bbe-113">Misalnya, Anda dapat memasukkan "buah" atau "ounce".</span><span class="sxs-lookup"><span data-stu-id="41bbe-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="41bbe-114">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="41bbe-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="41bbe-115">Tambahkan unit ke grup unit</span><span class="sxs-lookup"><span data-stu-id="41bbe-115">Add units to a unit group</span></span>

1. <span data-ttu-id="41bbe-116">Buka grup unit, dan di tab **terkait**, pilih **unit**.</span><span class="sxs-lookup"><span data-stu-id="41bbe-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="41bbe-117">Anda akan melihat bahwa unit utama telah ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="41bbe-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="41bbe-118">Pilih **Tambah unit baru**, dan di halaman **Buat cepat: unit**, di bidang **nama**, masukkan nama unit.</span><span class="sxs-lookup"><span data-stu-id="41bbe-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="41bbe-119">Di bidang **kuantitas**, masukkan kuantitas unit.</span><span class="sxs-lookup"><span data-stu-id="41bbe-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="41bbe-120">Sebagai contoh, jika sebuah kotak berisi 2 buah, ketik "2".</span><span class="sxs-lookup"><span data-stu-id="41bbe-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="41bbe-121">Di bidang **satuan dasar**, pilih satuan dasar untuk menetapkan satuan pengukuran terendah untuk unit.</span><span class="sxs-lookup"><span data-stu-id="41bbe-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="41bbe-122">Misalnya, Anda dapat memilih "Buah".</span><span class="sxs-lookup"><span data-stu-id="41bbe-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="41bbe-123">Pilih **Simpan**:</span><span class="sxs-lookup"><span data-stu-id="41bbe-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]