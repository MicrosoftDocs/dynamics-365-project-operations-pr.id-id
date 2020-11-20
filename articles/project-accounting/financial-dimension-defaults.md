---
title: Default dimensi keuangan
description: Topik ini memberikan informasi tentang cara mengatur default dimensi keuangan.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131887"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="75851-103">Default dimensi keuangan</span><span class="sxs-lookup"><span data-stu-id="75851-103">Financial dimension defaults</span></span>

<span data-ttu-id="75851-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="75851-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="75851-105">Dynamics 365 Project Operations menggunakan kerangka kerja [dimensi Keuangan](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) di Dynamics 365 Finance untuk memberikan wawasan tambahan tentang buku besar pembantu proyek dan transaksi buku besar umum.</span><span class="sxs-lookup"><span data-stu-id="75851-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="75851-106">Dimensi keuangan default dapat ditetapkan pada pelanggan, sumber pendanaan proyek, tonggak pencapaian, lini kontrak proyek, atau proyek.</span><span class="sxs-lookup"><span data-stu-id="75851-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="75851-107">Tentukan dimensi keuangan default untuk pelanggan</span><span class="sxs-lookup"><span data-stu-id="75851-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="75851-108">Default dimensi pelanggan ditentukan dalam Finance.</span><span class="sxs-lookup"><span data-stu-id="75851-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="75851-109">Selesaikan langkah berikut ini untuk mengatur default dimensi.</span><span class="sxs-lookup"><span data-stu-id="75851-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="75851-110">Buka **piutang dagang** > **Pelanggan** > **Semua pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="75851-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="75851-111">Pada halaman **Pelanggan**, pada tab **Dimensi keuangan**, tetapkan nilai dimensi keuangan untuk pelanggan tertentu.</span><span class="sxs-lookup"><span data-stu-id="75851-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="75851-112">Tentukan dimensi keuangan default untuk kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="75851-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="75851-113">Kontrak proyek dibuat dan dipertahankan di Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="75851-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="75851-114">Atribut akuntansi untuk kontrak proyek diatur dalam modul **manajemen Proyek dan akuntansi** di Finance.</span><span class="sxs-lookup"><span data-stu-id="75851-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="75851-115">Menetapkan dimensi keuangan untuk sumber pendanaan proyek</span><span class="sxs-lookup"><span data-stu-id="75851-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="75851-116">Buka **manajemen proyek dan akuntansi** > **Proyek** > **Kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="75851-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="75851-117">Pilih rekaman yang ingin Anda perbarui, dan pada tab **Kontrak proyek**, pilih **Perlihatkan akuntansi default**.</span><span class="sxs-lookup"><span data-stu-id="75851-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="75851-118">Perluas **Informasi terkait** dan pilih tab **Sumber pendanaan**.</span><span class="sxs-lookup"><span data-stu-id="75851-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="75851-119">Atur Default dimensi keuangan.</span><span class="sxs-lookup"><span data-stu-id="75851-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="75851-120">Perhatikan bahwa dimensi keuangan di-default dari akun pelanggan.</span><span class="sxs-lookup"><span data-stu-id="75851-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="75851-121">Menetapkan dimensi keuangan untuk baris kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="75851-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="75851-122">Buka **manajemen proyek dan akuntansi** > **Proyek** > **Kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="75851-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="75851-123">Pilih rekaman yang ingin Anda perbarui, dan pada tab **Kontrak proyek**, pilih **Perlihatkan akuntansi default**.</span><span class="sxs-lookup"><span data-stu-id="75851-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="75851-124">Perluas **Informasi terkait** dan pilih tab **baris kontrak**.</span><span class="sxs-lookup"><span data-stu-id="75851-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="75851-125">Atur Default dimensi keuangan.</span><span class="sxs-lookup"><span data-stu-id="75851-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="75851-126">Default dimensi keuangan berlaku dan hanya dapat digunakan dengan baris kontrak Harga Tetap (tonggak pencapaian).</span><span class="sxs-lookup"><span data-stu-id="75851-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="75851-127">Default ini digunakan pada transaksi pada akun proyek terkait dan baris faktur.</span><span class="sxs-lookup"><span data-stu-id="75851-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="75851-128">Tentukan dimensi keuangan default untuk proyek</span><span class="sxs-lookup"><span data-stu-id="75851-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="75851-129">Proyek dibuat dan dikelola di (CDS).</span><span class="sxs-lookup"><span data-stu-id="75851-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="75851-130">Atribut akuntansi untuk proyek diatur dalam modul **manajemen Proyek dan akuntansi** di Finance.</span><span class="sxs-lookup"><span data-stu-id="75851-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="75851-131">Buka **manajemen proyek dan akuntansi** > **proyek** > **Semua proyek**.</span><span class="sxs-lookup"><span data-stu-id="75851-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="75851-132">Pilih rekaman yang ingin Anda perbarui, dan pada tab **proyek**, pilih **Perlihatkan akuntansi default**.</span><span class="sxs-lookup"><span data-stu-id="75851-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="75851-133">Perluas **Informasi terkait** dan pilih tab **Konfigurasi**.</span><span class="sxs-lookup"><span data-stu-id="75851-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="75851-134">Atur Default dimensi keuangan.</span><span class="sxs-lookup"><span data-stu-id="75851-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="75851-135">Perhatikan bahwa dimensi keuangan di-default dari akun pelanggan.</span><span class="sxs-lookup"><span data-stu-id="75851-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="75851-136">Jika proyek dikaitkan dengan baris kontrak dengan beberapa pelanggan kontrak proyek, pelanggan utama digunakan untuk dimensi keuangan default.</span><span class="sxs-lookup"><span data-stu-id="75851-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="75851-137">Dimensi keuangan default proyek digunakan untuk menetapkan default baris jurnal untuk transaksi waktu, pengeluaran, dan biaya di **Jurnal Integrasi Project Operations,** dan pada baris faktur proyek terkait.</span><span class="sxs-lookup"><span data-stu-id="75851-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
