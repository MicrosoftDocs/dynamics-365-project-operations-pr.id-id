---
title: Mengelola kontrak proyek
description: Topik ini menyediakan informasi tentang melihat kontrak berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273203"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="90bf9-103">Mengelola kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="90bf9-103">Manage project contracts</span></span>

<span data-ttu-id="90bf9-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="90bf9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90bf9-105">Kontrak proyek dalam Dynamics 365 Project Operations mencatat dan mengelola komitmen yang disetujui secara kontraktual dan rincian penagihan proyek.</span><span class="sxs-lookup"><span data-stu-id="90bf9-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="90bf9-106">Struktur kontrak proyek dalam Project Operations disesuaikan dengan pekerjaan berbasis proyek dengan komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="90bf9-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="90bf9-107">Baris kontrak yang mengidentifikasi komponen pekerjaan diskrit yang akan disajikan sebagai komponen tingkat tinggi pada faktur proyek.</span><span class="sxs-lookup"><span data-stu-id="90bf9-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="90bf9-108">Rincian baris kontrak yang mengidentifikasi dan memperkirakan pekerjaan untuk setiap komponen tingkat tinggi atau baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="90bf9-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="90bf9-109">Perkiraan mencakup jadwal dan aspek keuangan untuk pekerjaan yang terkait dengan baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="90bf9-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="90bf9-110">Model kontrak dan komponen yang kena biaya diatur untuk setiap baris kontrak yang memegang pengaturan penagihan untuk setiap baris kontrak dan kontrak secara keseluruhan.</span><span class="sxs-lookup"><span data-stu-id="90bf9-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="90bf9-111">Lihat semua kontrak berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="90bf9-111">View all project-based contracts</span></span>

<span data-ttu-id="90bf9-112">Daftar semua kontrak proyek dapat dilihat pada halaman daftar **kontrak**.</span><span class="sxs-lookup"><span data-stu-id="90bf9-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="90bf9-113">Buka **Penjualan** > **Kontak**.</span><span class="sxs-lookup"><span data-stu-id="90bf9-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="90bf9-114">Daftar semua kontrak proyek Anda dalam sistem akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="90bf9-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="90bf9-115">Pilih **pengalih tampilan** (panah drop-down di sebelah nama tampilan) untuk memilih tampilan terfilter lainnya.</span><span class="sxs-lookup"><span data-stu-id="90bf9-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="90bf9-116">Anda dapat membuat tampilan sendiri dengan kriteria filter kustom.</span><span class="sxs-lookup"><span data-stu-id="90bf9-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="90bf9-117">Kontrak dapat dibuat atau dihapus dari halaman daftar ini atau halaman detail.</span><span class="sxs-lookup"><span data-stu-id="90bf9-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]