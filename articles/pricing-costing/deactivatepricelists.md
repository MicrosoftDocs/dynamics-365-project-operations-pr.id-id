---
title: Menonaktifkan daftar harga
description: Informasi topik menjelaskan cara menonaktifkan atau menghilangkan daftar harga yang tidak digunakan atau lama.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701942"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="42e42-103">Menonaktifkan daftar harga</span><span class="sxs-lookup"><span data-stu-id="42e42-103">Deactivate price lists</span></span> 

<span data-ttu-id="42e42-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="42e42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="42e42-105">Untuk menghilangkan daftar harga lama atau yang tidak digunakan dari Dynamics 365 Project Operations, ada dua langkah yang harus diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="42e42-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="42e42-106">Hilangkan atau hapus daftar harga dari halaman tertentu.</span><span class="sxs-lookup"><span data-stu-id="42e42-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="42e42-107">Nonaktifkan atau hapus daftar harga dari daftar harga Aktif pada halaman **Daftar Harga**.</span><span class="sxs-lookup"><span data-stu-id="42e42-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="42e42-108">Anda harus menyelesaikan kedua langkah tersebut untuk sepenuhnya menghilangkan daftar harga.</span><span class="sxs-lookup"><span data-stu-id="42e42-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="42e42-109">Hanya melakukan langkah 2, yakni secara langsung menghapus atau menonaktifkan daftar harga dari tampilan Daftar Harga Aktif, tidak memadai.</span><span class="sxs-lookup"><span data-stu-id="42e42-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="42e42-110">Anda juga harus menghapus keterkaitan daftar harga ini dari semua tempat yang disebutkan pada langkah 1.</span><span class="sxs-lookup"><span data-stu-id="42e42-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="42e42-111">Hapus daftar harga dari halaman tertentu</span><span class="sxs-lookup"><span data-stu-id="42e42-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="42e42-112">Untuk menghapus daftar harga dari Project Operations, buka halaman berikut:</span><span class="sxs-lookup"><span data-stu-id="42e42-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="42e42-113">Halaman **Parameter Proyek** > tab **Daftar harga**</span><span class="sxs-lookup"><span data-stu-id="42e42-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="42e42-114">Halaman **Unit Organisasional** > kisi **Daftar Harga**</span><span class="sxs-lookup"><span data-stu-id="42e42-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="42e42-115">Halaman **Akun** > kisi **Daftar Harga Proyek**</span><span class="sxs-lookup"><span data-stu-id="42e42-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="42e42-116">Halaman **Kuotasi Proyek** > kisi **Daftar Harga Proyek**: Berlaku untuk semua kuotasi proyek aktif.</span><span class="sxs-lookup"><span data-stu-id="42e42-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="42e42-117">Halaman **Kontrak Proyek** > kisi **Daftar Harga Proyek**: Berlaku untuk semua kontrak proyek aktif.</span><span class="sxs-lookup"><span data-stu-id="42e42-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="42e42-118">Untuk setiap halaman, Anda harus memilih daftar harga yang akan dihapus, kemudian memilih **Hapus**.</span><span class="sxs-lookup"><span data-stu-id="42e42-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="42e42-119">Hapus atau nonaktifkan daftar harga dari halaman Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="42e42-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="42e42-120">Untuk menghapus daftar harga dari daftar harga aktif, buka **Penjualan** > **Pelanggan** > **Daftar Harga**.</span><span class="sxs-lookup"><span data-stu-id="42e42-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="42e42-121">Pilih daftar harga yang akan dihapus, lalu pilih **hapus**.</span><span class="sxs-lookup"><span data-stu-id="42e42-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="42e42-122">Jika daftar harga direferensikan pada transaksi yang ada, Anda tidak akan dapat menghapusnya.</span><span class="sxs-lookup"><span data-stu-id="42e42-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="42e42-123">Jika hal ini terjadi, Anda dapat menonaktifkan daftar harga sehingga tidak muncul dalam tampilan apa pun.</span><span class="sxs-lookup"><span data-stu-id="42e42-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="42e42-124">Untuk menonaktifkan daftar harga, pilih kembali daftar harga, lalu pilih **Nonaktifkan**.</span><span class="sxs-lookup"><span data-stu-id="42e42-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   