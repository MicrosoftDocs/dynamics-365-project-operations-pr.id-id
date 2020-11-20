---
title: Mengonfigurasikan integrasi Project Operations per entitas hukum
description: Topik ini menyediakan informasi tentang mengonfigurasikan integrasi per entitas hukum di Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122887"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="f0952-103">Mengonfigurasikan integrasi Project Operations per entitas hukum</span><span class="sxs-lookup"><span data-stu-id="f0952-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="f0952-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="f0952-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f0952-105">Ini topik memandu Anda melakukan langkah-langkah yang diperlukan untuk mengkonfigurasi Dynamics 365 Project Operations per entitas hukum.</span><span class="sxs-lookup"><span data-stu-id="f0952-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="f0952-106">Aktifkan kunci target di Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f0952-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="f0952-107">Selesaikan langkah-langkah berikut untuk mengaktifkan fitur yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="f0952-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="f0952-108">Di Dynamics 365 Finance, buka ruang kerja **manajemen fitur**.</span><span class="sxs-lookup"><span data-stu-id="f0952-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="f0952-109">Dalam **Daftar fitur**, Cari dan Aktifkan fitur berikut:</span><span class="sxs-lookup"><span data-stu-id="f0952-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="f0952-110">**Aktifkan beberapa baris kontrak untuk proyek**</span><span class="sxs-lookup"><span data-stu-id="f0952-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="f0952-111">**Aktifkan Project Operations di Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="f0952-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="f0952-112">Jika Anda tidak melihat **tombol fitur** yang tercantum, Verifikasikan bahwa versi keuangan Anda memenuhi persyaratan versi minimum (versi aplikasi 10.0.13 dengan semua pembaruan kualitas yang diterapkan atau lebih tinggi).</span><span class="sxs-lookup"><span data-stu-id="f0952-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="f0952-113">Pilih **Periksa pembaruan** untuk me-refresh daftar fitur.</span><span class="sxs-lookup"><span data-stu-id="f0952-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="f0952-114">Menentukan skenario penyebaran Project Operations untuk entitas hukum</span><span class="sxs-lookup"><span data-stu-id="f0952-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="f0952-115">Anda dapat mengaktifkan Project Operations pada Dynamics 365 Customer Engagement di tingkat entitas hukum.</span><span class="sxs-lookup"><span data-stu-id="f0952-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="f0952-116">Anda dapat memiliki satu entitas hukum menggunakan Project Operations di Dynamics 365 Customer Engagement untuk skenario berbasis sumber daya/non-stok.</span><span class="sxs-lookup"><span data-stu-id="f0952-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="f0952-117">Di lingkungan yang sama, Anda dapat memiliki entitas hukum lain menggunakan Project Operations untuk skenario pesanan produksi/di-stok.</span><span class="sxs-lookup"><span data-stu-id="f0952-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="f0952-118">Di Dynamics 365 Finance, buka **manajemen proyek dan akuntansi** > **konfigurasi** > **parameter manajemen proyek dan akuntansi global**.</span><span class="sxs-lookup"><span data-stu-id="f0952-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="f0952-119">Dalam daftar entitas hukum yang tersedia, pilih entitas di mana beberapa baris kontrak dan Project Operations pada fitur Dynamics 365 Customer Engagement akan diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="f0952-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="f0952-120">Biarkan entitas hukum yang akan menggunakan Project Operations untuk skenario pesanan distok/produksi tidak dipilih.</span><span class="sxs-lookup"><span data-stu-id="f0952-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="f0952-121">Entitas hukum dapat dipilih hanya jika tidak memiliki proyek saat ini.</span><span class="sxs-lookup"><span data-stu-id="f0952-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="f0952-122">Konfigurasikan parameter akuntansi dan manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="f0952-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="f0952-123">Setiap entitas hukum yang menggunakan Project Operations pada Dynamics 365 Customer Engagement memerlukan seperangkat parameter default.</span><span class="sxs-lookup"><span data-stu-id="f0952-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="f0952-124">Parameter ini dikonfigurasi pada tab **Project Operations** pada halaman **parameter manajemen proyek dan akuntansi**.</span><span class="sxs-lookup"><span data-stu-id="f0952-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="f0952-125">Parameter itu adalah:</span><span class="sxs-lookup"><span data-stu-id="f0952-125">The parameters are:</span></span>

  - <span data-ttu-id="f0952-126">**Jenis penagihan default**: Project Operations menggunakan rangkaian tetap default jenis penagihan yang harus dipetakan ke properti baris Finance.</span><span class="sxs-lookup"><span data-stu-id="f0952-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="f0952-127">Buat rekaman untuk setiap jenis penagihan: **tidak ditentukan**, **Dikenakan biaya**, **Tidak dikenakan biaya**, **gratis**, dan **tidak tersedia**.</span><span class="sxs-lookup"><span data-stu-id="f0952-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="f0952-128">**Default kategori proyek**: Pilih kategori proyek default yang akan digunakan untuk setiap jenis transaksi.</span><span class="sxs-lookup"><span data-stu-id="f0952-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="f0952-129">Default ini akan digunakan dalam **jurnal integrasi Project Operations** dan di perkiraan yang mana tidak ada kategori transaksi yang ditentukan untuk aktual proyek.</span><span class="sxs-lookup"><span data-stu-id="f0952-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="f0952-130">**Perkiraan**: Pilih model perkiraan yang akan digunakan untuk perkiraan waktu dan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f0952-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>
