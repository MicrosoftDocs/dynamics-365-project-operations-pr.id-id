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
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177335"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="d00d3-103">Mengelola kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="d00d3-103">Manage project contracts</span></span>

<span data-ttu-id="d00d3-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="d00d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d00d3-105">Kontrak proyek dalam Dynamics 365 Project Operations mencatat dan mengelola komitmen yang disetujui secara kontraktual dan rincian penagihan proyek.</span><span class="sxs-lookup"><span data-stu-id="d00d3-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="d00d3-106">Struktur kontrak proyek dalam Project Operations disesuaikan dengan pekerjaan berbasis proyek dengan komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="d00d3-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="d00d3-107">Baris kontrak yang mengidentifikasi komponen pekerjaan diskrit yang akan disajikan sebagai komponen tingkat tinggi pada faktur proyek.</span><span class="sxs-lookup"><span data-stu-id="d00d3-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="d00d3-108">Rincian baris kontrak yang mengidentifikasi dan memperkirakan pekerjaan untuk setiap komponen tingkat tinggi atau baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="d00d3-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="d00d3-109">Perkiraan mencakup jadwal dan aspek keuangan untuk pekerjaan yang terkait dengan baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="d00d3-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="d00d3-110">Model kontrak dan komponen yang kena biaya diatur untuk setiap baris kontrak yang memegang pengaturan penagihan untuk setiap baris kontrak dan kontrak secara keseluruhan.</span><span class="sxs-lookup"><span data-stu-id="d00d3-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="d00d3-111">Lihat semua kontrak berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="d00d3-111">View all project-based contracts</span></span>

<span data-ttu-id="d00d3-112">Daftar semua kontrak proyek dapat dilihat pada halaman daftar **kontrak**.</span><span class="sxs-lookup"><span data-stu-id="d00d3-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="d00d3-113">Buka **Penjualan** > **Kontak**.</span><span class="sxs-lookup"><span data-stu-id="d00d3-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="d00d3-114">Daftar semua kontrak proyek Anda dalam sistem akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="d00d3-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="d00d3-115">Pilih **pengalih tampilan** (panah drop-down di sebelah nama tampilan) untuk memilih tampilan terfilter lainnya.</span><span class="sxs-lookup"><span data-stu-id="d00d3-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="d00d3-116">Anda dapat membuat tampilan sendiri dengan kriteria filter kustom.</span><span class="sxs-lookup"><span data-stu-id="d00d3-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="d00d3-117">Kontrak dapat dibuat atau dihapus dari halaman daftar ini atau halaman detail.</span><span class="sxs-lookup"><span data-stu-id="d00d3-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
