---
title: Membuat faktur proforma manual
description: Topik ini memberikan informasi tentang membuat faktur proforma manual di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/20/2020
ms.locfileid: "4078713"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="be251-103">Membuat faktur proforma manual</span><span class="sxs-lookup"><span data-stu-id="be251-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="be251-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="be251-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be251-105">Di Dynamics 365 Project Operations, faktur proforma dapat dibuat secara manual sesuai kebutuhan.</span><span class="sxs-lookup"><span data-stu-id="be251-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="be251-106">Anda dapat secara manual membuat faktur proforma dari halaman daftar **kontrak proyek** atau dari halaman rincian **kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="be251-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="be251-107">Daftar Harga Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="be251-107">Project Contracts list page</span></span>

<span data-ttu-id="be251-108">Dari halaman daftar **kontrak proyek** , pilih satu atau beberapa kontrak proyek, dan buat faktur untuk semua rekaman yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="be251-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="be251-109">Sistem akan memeriksa untuk melihat yang mana dari kontrak proyek yang dipilih memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini.</span><span class="sxs-lookup"><span data-stu-id="be251-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="be251-110">Dari kontrak tersebut, sistem membuat faktur proforma draft.</span><span class="sxs-lookup"><span data-stu-id="be251-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="be251-111">Jika kontrak proyek memiliki beberapa pelanggan, mungkin ada satu faktur dibuat per pelanggan, dan beberapa faktur per kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="be251-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="be251-112">Semua faktur proyek yang dibuat tersedia pada halaman **faktur** di Bagian **tagihan** area **penjualan**.</span><span class="sxs-lookup"><span data-stu-id="be251-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="be251-113">Halaman Detail Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="be251-113">Project Contract details page</span></span>

<span data-ttu-id="be251-114">Faktur proforma juga dapat dibuat dari halaman rincian **kontrak proyek** , yang membuat faktur untuk kontrak proyek tertentu.</span><span class="sxs-lookup"><span data-stu-id="be251-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="be251-115">Sistem akan memverifikasi bahwa kontrak proyek memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini.</span><span class="sxs-lookup"><span data-stu-id="be251-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="be251-116">Dari kontrak ini, sistem membuat rancangan faktur proforma berdasarkan jumlah pelanggan pada setiap baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="be251-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="be251-117">Bila ada faktur proforma tunggal yang dibuat, halaman **faktur** akan terbuka.</span><span class="sxs-lookup"><span data-stu-id="be251-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="be251-118">Jika ada beberapa faktur yang dibuat untuk kontrak proyek tersebut, maka halaman daftar **faktur** akan terbuka untuk menampilkan semua faktur yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="be251-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
