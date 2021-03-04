---
title: Tinjau akumulasi faktur pada proyek dan kontrak proyek
description: Topik ini menyediakan informasi tentang cara meninjau waktu, pengeluaran, dan akumulasi produk, serta cara menandainya sebagai siap digunakan untuk faktur.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150492"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="fe840-103">Tinjau akumulasi faktur pada proyek dan kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="fe840-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fe840-104">Bila transaksi siap untuk membuat dan memproses faktur, transaksi harus ditandai **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="fe840-105">Topik ini menjelaskan jenis transaksi yang dapat dibuat.</span><span class="sxs-lookup"><span data-stu-id="fe840-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="fe840-106">Tinjau akumulasi penagihan waktu dan material</span><span class="sxs-lookup"><span data-stu-id="fe840-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="fe840-107">Bila entri waktu atau biaya diajukan dan disetujui untuk proyek, PSA membuat aktual proyek.</span><span class="sxs-lookup"><span data-stu-id="fe840-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="fe840-108">Jika kombinasi proyek dan kelas transaksi dipetakan ke baris kontrak untuk proyek waktu dan bahan, dua aktual dibuat saat entri disetujui:</span><span class="sxs-lookup"><span data-stu-id="fe840-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="fe840-109">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="fe840-109">Cost actual</span></span> 
- <span data-ttu-id="fe840-110">Aktual Penjualan Belum Tertagih</span><span class="sxs-lookup"><span data-stu-id="fe840-110">Unbilled sales actual</span></span>

<span data-ttu-id="fe840-111">Aktual penjualan yang tidak ditagihkan menunjukkan akumulasi tagihan, dan status penagihan mereka harus diatur ke **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="fe840-112">Saat faktur proyek dibuat, aktual penjualan yang tidak ditagih yang ditandai **siap untuk faktur** disalin sebagai rincian baris faktur.</span><span class="sxs-lookup"><span data-stu-id="fe840-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="fe840-113">Untuk meninjau akumulasi tagihan untuk waktu dan material, buka **Sales** \> **penagihan** \> **Akumulasi penagihan waktu dan material**.</span><span class="sxs-lookup"><span data-stu-id="fe840-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="fe840-114">Pilih Semua aktual penjualan yang tidak ditagih yang siap ditagih, lalu pilih **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="fe840-115">Status tagihan aktual ini diubah ke **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Akumulasi Penagihan Waktu dan Material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="fe840-117">Tinjau Akumulasi Penagihan Produk</span><span class="sxs-lookup"><span data-stu-id="fe840-117">Review the product billing backlog</span></span>

<span data-ttu-id="fe840-118">Dalam PSA, ketika kontrak proyek memiliki baris kontrak berbasis produk, baris tersebut dipertimbangkan untuk faktur setiap kali faktur dibuat untuk kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="fe840-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="fe840-119">Setiap produk yang memiliki baris kontrak yang ditandai **siap untuk faktur** disalin ke faktur proyek sebagai baris faktur proyek.</span><span class="sxs-lookup"><span data-stu-id="fe840-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="fe840-120">Untuk meninjau jaminan akumulasi produk, buka **penjualan** \> **tagihan** \> **Akumulasi tagihan produk**.</span><span class="sxs-lookup"><span data-stu-id="fe840-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="fe840-121">Pilih Semua baris kontrak berbasis produk yang siap ditagih, lalu pilih **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="fe840-122">Status tagihan baris ini diubah ke **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Akumulasi Penagihan Produk](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="fe840-124">Meninjau tonggak waktu penagihan pada kontrak harga tetap</span><span class="sxs-lookup"><span data-stu-id="fe840-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="fe840-125">Setiap baris kontrak proyek yang memiliki metode penagihan harga tetap harus menentukan tonggak waktu kontrak.</span><span class="sxs-lookup"><span data-stu-id="fe840-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="fe840-126">tonggak waktu waktu kontrak ini dapat ditagih hanya jika ditAndai siap **untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="fe840-127">Untuk meninjau tonggak waktu penagihan, buka **Sales** \> **tagihan** \> **tonggak waktu harga tetap**.</span><span class="sxs-lookup"><span data-stu-id="fe840-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="fe840-128">Pilih tonggak waktu yang siap ditagih yang siap ditagih, lalu pilih **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="fe840-129">Status tagihan tonggak waktu ini diubah ke **siap untuk faktur**.</span><span class="sxs-lookup"><span data-stu-id="fe840-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Tonggak waktu Harga Tetap](media/FPBacklog.png)
