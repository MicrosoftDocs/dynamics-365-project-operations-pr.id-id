---
title: Mengelola kuotasi proyek
description: Topik ini menyediakan informasi tentang kuotasi proyek.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8e0b20d4780a14edc3c242e261e22d4905f783a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994815"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="94405-103">Mengelola kuotasi proyek</span><span class="sxs-lookup"><span data-stu-id="94405-103">Manage project quotes</span></span>

<span data-ttu-id="94405-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="94405-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94405-105">Di Dynamics 365 Project Operations, kuotasi proyek dirancang untuk membantu membangun proposal untuk pekerjaan proyek.</span><span class="sxs-lookup"><span data-stu-id="94405-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="94405-106">Struktur kuotasi proyek dalam Project Operations distrukturkan untuk proposal proyek dengan komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="94405-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="94405-107">Baris kuotasi yang mengidentifikasi komponen pekerjaan diskrit yang akan disajikan sebagai komponen tingkat tinggi.</span><span class="sxs-lookup"><span data-stu-id="94405-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="94405-108">Rincian baris kuotasi yang mengidentifikasi dan memperkirakan pekerjaan untuk setiap komponen tingkat tinggi atau baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="94405-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="94405-109">Jadwal atau estimasi tanggal dan aspek keuangan untuk pekerjaan terkait ke baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="94405-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="94405-110">Model kontrak dan komponen yang kena biaya diatur untuk setiap baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="94405-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="94405-111">Penyiapan ini membantu memperkirakan penyebaran pendapatan, pembelanjaan, dan profitabilitas untuk setiap baris kuotasi dan kuotasi keseluruhan.</span><span class="sxs-lookup"><span data-stu-id="94405-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="94405-112">Lihat semua kuotasi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="94405-112">View all project-based quotes</span></span>

<span data-ttu-id="94405-113">Daftar semua kuotasi proyek dapat dilihat dari halaman daftar **Kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="94405-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="94405-114">Buka **Penjualan** > **Kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="94405-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="94405-115">Daftar semua kuotasi proyek Anda dalam sistem akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="94405-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="94405-116">Gunakan **Pengalih tampilan** untuk memilih tampilan terfilter lainnya dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="94405-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="94405-117">Menggunakan kriteria filter kustom, Anda dapat mengkonfigurasi tampilan Anda sendiri dan pilihan navigasi.</span><span class="sxs-lookup"><span data-stu-id="94405-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="94405-118">Kuotasi dapat dibuat atau dihapus dari halaman daftar ini atau halaman detail.</span><span class="sxs-lookup"><span data-stu-id="94405-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]