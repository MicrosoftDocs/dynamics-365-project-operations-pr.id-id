---
title: Membuat faktur proforma manual - lite
description: Topik ini memberikan informasi tentang membuat faktur proforma manual di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764507"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="c17d1-103">Membuat faktur proforma manual - lite</span><span class="sxs-lookup"><span data-stu-id="c17d1-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="c17d1-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="c17d1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c17d1-105">Di Dynamics 365 Project Operations, faktur proforma dapat dibuat secara manual jika diperlukan.</span><span class="sxs-lookup"><span data-stu-id="c17d1-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="c17d1-106">Anda dapat secara manual membuat faktur proforma dari halaman daftar **kontrak proyek** atau dari halaman rincian **kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="c17d1-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="c17d1-107">Daftar Harga Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="c17d1-107">Project Contracts list page</span></span>

<span data-ttu-id="c17d1-108">Dari halaman daftar **kontrak proyek**, pilih satu atau beberapa kontrak proyek, dan buat faktur untuk semua rekaman yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="c17d1-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="c17d1-109">Sistem akan memeriksa untuk melihat yang mana dari kontrak proyek yang dipilih memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini.</span><span class="sxs-lookup"><span data-stu-id="c17d1-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="c17d1-110">Dari kontrak tersebut, sistem membuat faktur proforma draft.</span><span class="sxs-lookup"><span data-stu-id="c17d1-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="c17d1-111">Jika kontrak proyek memiliki beberapa pelanggan, mungkin ada satu faktur dibuat per pelanggan, dan beberapa faktur per kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="c17d1-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="c17d1-112">Semua faktur proyek yang dibuat tersedia pada halaman **faktur** di Bagian **tagihan** area **penjualan**.</span><span class="sxs-lookup"><span data-stu-id="c17d1-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="c17d1-113">Halaman Detail Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="c17d1-113">Project Contract details page</span></span>

<span data-ttu-id="c17d1-114">Faktur proforma juga dapat dibuat dari halaman rincian **Kontrak Proyek**.</span><span class="sxs-lookup"><span data-stu-id="c17d1-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="c17d1-115">Sistem akan memverifikasi apakah kontrak proyek memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini.</span><span class="sxs-lookup"><span data-stu-id="c17d1-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="c17d1-116">Dari kontrak ini, sistem membuat rancangan faktur proforma berdasarkan jumlah pelanggan pada setiap baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="c17d1-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="c17d1-117">Bila ada faktur proforma tunggal yang dibuat, halaman **faktur** akan terbuka.</span><span class="sxs-lookup"><span data-stu-id="c17d1-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="c17d1-118">Jika beberapa faktur dibuat untuk kontrak proyek tersebut, halaman daftar **Faktur** akan terbuka untuk menampilkan semua faktur yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="c17d1-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
