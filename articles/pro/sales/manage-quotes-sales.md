---
title: Mengelola kuotasi proyek
description: Topik ini menyediakan informasi tentang kuotasi proyek.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272932"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="b3be7-103">Mengelola kuotasi proyek</span><span class="sxs-lookup"><span data-stu-id="b3be7-103">Manage project quotes</span></span>

<span data-ttu-id="b3be7-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b3be7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b3be7-105">Di Dynamics 365 Project Operations, kuotasi proyek dirancang untuk membantu membangun proposal untuk pekerjaan proyek.</span><span class="sxs-lookup"><span data-stu-id="b3be7-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="b3be7-106">Struktur kuotasi proyek dalam Project Operations distrukturkan untuk proposal proyek dengan komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="b3be7-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="b3be7-107">Baris kuotasi yang mengidentifikasi komponen pekerjaan diskrit yang akan disajikan sebagai komponen tingkat tinggi.</span><span class="sxs-lookup"><span data-stu-id="b3be7-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="b3be7-108">Rincian baris kuotasi yang mengidentifikasi dan memperkirakan pekerjaan untuk setiap komponen tingkat tinggi atau baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b3be7-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="b3be7-109">Jadwal atau estimasi tanggal dan aspek keuangan untuk pekerjaan terkait ke baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b3be7-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="b3be7-110">Model kontrak dan komponen yang kena biaya diatur untuk setiap baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b3be7-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="b3be7-111">Penyiapan ini membantu memperkirakan penyebaran pendapatan, pembelanjaan, dan profitabilitas untuk setiap baris kuotasi dan kuotasi keseluruhan.</span><span class="sxs-lookup"><span data-stu-id="b3be7-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="b3be7-112">Lihat semua kuotasi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="b3be7-112">View all project-based quotes</span></span>

<span data-ttu-id="b3be7-113">Daftar semua kuotasi proyek dapat dilihat dari halaman daftar **Kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="b3be7-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="b3be7-114">Buka **Penjualan** > **Kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="b3be7-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="b3be7-115">Daftar semua kuotasi proyek Anda dalam sistem akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="b3be7-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="b3be7-116">Gunakan **Pengalih tampilan** untuk memilih tampilan terfilter lainnya dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b3be7-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="b3be7-117">Menggunakan kriteria filter kustom, Anda dapat mengkonfigurasi tampilan Anda sendiri dan pilihan navigasi.</span><span class="sxs-lookup"><span data-stu-id="b3be7-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="b3be7-118">Kuotasi dapat dibuat atau dihapus dari halaman daftar ini atau halaman detail.</span><span class="sxs-lookup"><span data-stu-id="b3be7-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]