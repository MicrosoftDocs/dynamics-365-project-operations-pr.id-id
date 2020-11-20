---
title: Menimpa daftar harga penjualan proyek
description: Topik ini menyediakan informasi tentang pembuatan daftar harga penjualan kustom.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130852"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="b94b1-103">Menimpa daftar harga penjualan proyek</span><span class="sxs-lookup"><span data-stu-id="b94b1-103">Override project sales price lists</span></span>

<span data-ttu-id="b94b1-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b94b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="b94b1-105">Daftar harga proyek khusus pelanggan</span><span class="sxs-lookup"><span data-stu-id="b94b1-105">Customer-specific project price lists</span></span>

<span data-ttu-id="b94b1-106">Perjanjian harga spesifik pelanggan dapat diatur sebagai daftar harga proyek pada rekaman akun di Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b94b1-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="b94b1-107">Untuk membuat daftar harga proyek khusus pelanggan, di area **penjualan**, navigasi ke rekaman akun.</span><span class="sxs-lookup"><span data-stu-id="b94b1-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="b94b1-108">Buka halaman daftar **akun**.</span><span class="sxs-lookup"><span data-stu-id="b94b1-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="b94b1-109">Cari dan klik dua kali rekaman pelanggan untuk membuka halaman rincian **akun**.</span><span class="sxs-lookup"><span data-stu-id="b94b1-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="b94b1-110">Pada tab **daftar harga proyek**, pilih \*\*+ daftar harga proyek baru^^.</span><span class="sxs-lookup"><span data-stu-id="b94b1-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="b94b1-111">Pada halaman **daftar harga proyek baru**, pilih daftar harga dari drop-down.</span><span class="sxs-lookup"><span data-stu-id="b94b1-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="b94b1-112">Hanya daftar harga yang konteksnya diatur ke **penjualan** dan yang mata uangnya sesuai dengan mata uang akun yang disertakan.</span><span class="sxs-lookup"><span data-stu-id="b94b1-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="b94b1-113">Namai asosiasi tersebut, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="b94b1-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="b94b1-114">Daftar harga proyek khusus pelanggan dibuat.</span><span class="sxs-lookup"><span data-stu-id="b94b1-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="b94b1-115">Daftar harga ini akan digunakan untuk harga proyek default pada kuotasi proyek atau kontrak yang dibuat untuk pelanggan ini saat tanggal pembuatan kuotasi atau kontrak proyek jatuh dalam efektivitas tanggal dari daftar harga.</span><span class="sxs-lookup"><span data-stu-id="b94b1-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="b94b1-116">Harga kustom pada kuotasi proyek</span><span class="sxs-lookup"><span data-stu-id="b94b1-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="b94b1-117">Pada kuotasi proyek, Anda dapat memiliki harga proyek yang diawali dengan daftar harga standar default yang di-default dari pelanggan atau dari parameter proyek.</span><span class="sxs-lookup"><span data-stu-id="b94b1-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="b94b1-118">Bila Anda memerlukan harga kustom untuk pekerjaan yang terkait dengan proyek pada kuotasi tertentu, Anda dapat mendapatkannya dari daftar harga proyek yang terkait dengan entitas.</span><span class="sxs-lookup"><span data-stu-id="b94b1-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="b94b1-119">Selesaikan langkah-langkah berikut untuk mengkonfigurasi harga proyek khusus kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b94b1-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="b94b1-120">Buka kuotasi proyek, dan pilih tab **daftar harga proyek**.</span><span class="sxs-lookup"><span data-stu-id="b94b1-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="b94b1-121">Dalam subgrid, pilih **Buat harga kustom**.</span><span class="sxs-lookup"><span data-stu-id="b94b1-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="b94b1-122">Semua daftar harga proyek yang dilampirkan ke kuotasi akan disalin ke daftar harga baru.</span><span class="sxs-lookup"><span data-stu-id="b94b1-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="b94b1-123">Nama dari daftar harga baru menunjukkan nama kuotasi dengan stempel waktu tanggal saat daftar harga ini dibuat.</span><span class="sxs-lookup"><span data-stu-id="b94b1-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="b94b1-124">Anda dapat menggunakan masing-masing daftar harga dan melakukan pembaruan terhadap harga tenaga kerja (harga peran) dan pengeluaran (harga kategori).</span><span class="sxs-lookup"><span data-stu-id="b94b1-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="b94b1-125">Harga ini akan berlaku hanya untuk kuotasi proyek ini.</span><span class="sxs-lookup"><span data-stu-id="b94b1-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="b94b1-126">Daftar Harga pada Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="b94b1-126">Price lists on a project contract</span></span>

<span data-ttu-id="b94b1-127">Pada kontrak proyek, harga proyek selalu default sebagai daftar harga kustom dengan nama kontrak dan stempel waktu tanggal dibuat yang ditambahkan ke nama.</span><span class="sxs-lookup"><span data-stu-id="b94b1-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="b94b1-128">Hal ini berlaku apakah kontrak dibuat saat kuotasi dimenangkan atau jika kontrak dibuat dari awal.</span><span class="sxs-lookup"><span data-stu-id="b94b1-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="b94b1-129">Jika diperlukan, Anda dapat menghapus Asosiasi ini ke daftar harga kustom dan mengaitkan daftar harga standar ke kontrak proyek sebagai gantinya.</span><span class="sxs-lookup"><span data-stu-id="b94b1-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="b94b1-130">Bila Anda mengaitkan daftar harga standar ke daftar harga proyek pada kuotasi atau kontrak, setiap perubahan yang dibuat pada harga dalam daftar harga akan mempengaruhi semua kuotasi dan kontrak yang menggunakan daftar harga.</span><span class="sxs-lookup"><span data-stu-id="b94b1-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
