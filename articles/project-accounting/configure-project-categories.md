---
title: Mengonfigurasikan kategori proyek
description: Topik ini menyediakan informasi tentang pengaturan kategori proyek.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078380"
---
# <a name="configure-project-categories"></a><span data-ttu-id="7d1d6-103">Mengonfigurasikan kategori proyek</span><span class="sxs-lookup"><span data-stu-id="7d1d6-103">Configure project categories</span></span>

<span data-ttu-id="7d1d6-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="7d1d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7d1d6-105">Project Operations menawarkan kemampuan kuat untuk mengkategorikan pendapatan dan pengeluaran dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="7d1d6-106">Kategori memberikan kemampuan untuk melaporkan dan menganalisis transaksi proyek, dan mendorong posting ke buku besar.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="7d1d6-107">Diagram berikut mengilustrasikan korelasi antara kategori transaksi, kategori bersama, dan kategori proyek.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="7d1d6-108">Kategori transaksi adalah pengelompokan dasar untuk transaksi proyek.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="7d1d6-109">Dalam pengelompokan tersebut, ada seperangkat kategori bersama yang dapat dibagikan di seluruh aplikasi dan modul.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="7d1d6-110">Menyelami lebih jauh ke yang spesifik, kategori proyek adalah tingkat kategori yang paling rinci.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="7d1d6-111">Kategori proyek dikhususkan untuk badan hukum, modul, dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelasi antara kategori transaksi, kategori bersama, dan kategori proyek](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="7d1d6-113">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="7d1d6-113">Transaction categories</span></span>

<span data-ttu-id="7d1d6-114">Kategori transaksi mewakili pengelompokan dasar untuk transaksi proyek dan bukan spesifik perusahaan atau jenis transaksi.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="7d1d6-115">Misalnya, Aswono Robotics menggunakan kategori Desain, perjalanan, penginstalan, dan transaksi layanan untuk mengelompokkan transaksi proyek.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="7d1d6-116">Kategori transaksi ditentukan dalam modul Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="7d1d6-117">Buka **pengaturan** \> **Kategori Transaksi** untuk membuka formulir.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="7d1d6-118">Buat kategori transaksi baru baik dengan memilih **baru** atau dengan memilih **impor dari Excel**.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="7d1d6-119">Kategori bersama</span><span class="sxs-lookup"><span data-stu-id="7d1d6-119">Shared categories</span></span>

<span data-ttu-id="7d1d6-120">Dynamics 365 menggunakan konsep kategori bersama untuk mengkategorikan pengeluaran dalam aplikasi yang berbeda, seperti Dynamics 365 Finance, Dynamics 365 Supply Chain, dan Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="7d1d6-121">Untuk setiap kategori transaksi yang dibuat, Project Operations secara otomatis membuat empat kategori bersama terkait: jam, pengeluaran, ongkos, dan item.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="7d1d6-122">Anda dapat meninjau dan menyesuaikan kategori bersama dengan membuka kategori **manajemen proyek dan akuntansi** \> **penataan** \> **kategori** \> **Kategori bersama**.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="7d1d6-123">Kategori proyek</span><span class="sxs-lookup"><span data-stu-id="7d1d6-123">Project categories</span></span>

<span data-ttu-id="7d1d6-124">Kategori proyek mewakili tingkat konfigurasi kategori yang paling rinci dan harus dikonfigurasi secara terpisah, dan untuk setiap perusahaan, oleh akuntan proyek.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="7d1d6-125">Buka **manajemen Proyek dan Akuntansi** \> **Penyiapan** \> **kategori** \> **Kategori proyek**.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="7d1d6-126">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-126">Select **New**.</span></span>
3. <span data-ttu-id="7d1d6-127">Pilih **id kategori** dari kategori bersama yang Anda buat di bagian sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="7d1d6-128">Project Operations hanya memungkinkan menggunakan kategori bersama yang terkait dengan kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="7d1d6-129">Pilih grup kategori.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="7d1d6-130">Grup kategori</span><span class="sxs-lookup"><span data-stu-id="7d1d6-130">Category groups</span></span>

<span data-ttu-id="7d1d6-131">Grup kategori digunakan untuk berbagi properti, terutama profil posting, antara kategori proyek terkait.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="7d1d6-132">Harus ada minimal satu grup kategori untuk setiap jenis transaksi dan setiap kategori proyek diberi grup.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="7d1d6-133">Spesifikasi posting dalam Project Operations ditentukan berdasarkan aturan profil biaya proyek dan pendapatan, kategori proyek, dan grup kategori.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="7d1d6-134">Anda dapat mengkonfigurasi grup kategori dengan membuka **manajemen proyek dan akuntansi** \> **Penyiapan** \> **Kategori** \> **Grup kategori**.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
