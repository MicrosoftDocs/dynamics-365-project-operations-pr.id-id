---
title: Perkiraan Penjualan dan Proyek
description: Topik ini menyediakan informasi tentang cara memanfaatkan jadwal dan perkiraan dalam proses penjualan.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148377"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="0dffe-103">Perkiraan Penjualan dan Proyek</span><span class="sxs-lookup"><span data-stu-id="0dffe-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0dffe-104">Selama proses penjualan, Anda dapat membuat perkiraan penjualan dengan menautkan proyek ke kuotasi penjualan.</span><span class="sxs-lookup"><span data-stu-id="0dffe-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="0dffe-105">Dengan cara ini, perkiraan deterministik dapat terjadi selama proses penjualan, untuk memanfaatkan kemampuan penjadwalan dan estimasi proyek.</span><span class="sxs-lookup"><span data-stu-id="0dffe-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="0dffe-106">Jika penjualan disetujui, jadwal yang digunakan untuk perkiraan penjualan dapat digunakan sebagai dasar untuk penyempurnaan lebih lanjut dari rencana proyek.</span><span class="sxs-lookup"><span data-stu-id="0dffe-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="0dffe-107">Menautkan proyek ke baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="0dffe-107">Linking a project to a quote line</span></span>

<span data-ttu-id="0dffe-108">Saat membuat baris kuotasi berbasis proyek, Anda dapat membuat proyek baru atau mengaitkannya proyek yang ada di halaman **baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="0dffe-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulir Baris kuotasi](media/project-8.png)
 
<span data-ttu-id="0dffe-110">Bila Anda membuat proyek baru dari rincian baris kuotasi, Anda dapat memanfaatkan template proyek.</span><span class="sxs-lookup"><span data-stu-id="0dffe-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="0dffe-111">Template proyek adalah proyek model yang menunjukkan rencana proyek standar dan perkiraan keuangan yang tipikal dalam suatu organisasi.</span><span class="sxs-lookup"><span data-stu-id="0dffe-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="0dffe-112">Mereka juga dapat menunjukkan salinan rencana proyek dan perkiraan dari proyek sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="0dffe-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Rincian Baris Kuotasi](media/project-9.png)
  
<span data-ttu-id="0dffe-114">Ketika Anda membuat proyek Anda dari kuotasi, proyek ini otomatis dikaitkan dengan baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="0dffe-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="0dffe-115">Komponen perkiraan dalam proyek</span><span class="sxs-lookup"><span data-stu-id="0dffe-115">Components of estimates in a project</span></span>

<span data-ttu-id="0dffe-116">Jadwal memungkinkan Anda membagi pekerjaan ke dalam tugas, mengelola hierarki tugas, menentukan sumber daya yang diperlukan untuk menyelesaikan tugas, dan menetapkan perkiraan upaya yang diperlukan untuk menyelesaikan tugas.</span><span class="sxs-lookup"><span data-stu-id="0dffe-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="0dffe-117">Anda dapat menentukan perkiraan upaya kerja dan jadwal dengan menggunakan bidang pada tab **jadwal** halaman **proyek**.</span><span class="sxs-lookup"><span data-stu-id="0dffe-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="0dffe-118">Karena daftar harga terkait dengan proyek, perkiraan keuangan dihitung menggunakan harga dan harga penjualan yang ditentukan dalam daftar harga.</span><span class="sxs-lookup"><span data-stu-id="0dffe-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="0dffe-119">Mengimpor perkiraan dari sebuah proyek ke kuotasi</span><span class="sxs-lookup"><span data-stu-id="0dffe-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="0dffe-120">Setelah menentukan perkiraan proyek, Anda dapat mengimpornya ke baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="0dffe-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="0dffe-121">Pada halaman **detail baris kuotasi**, pilih **impor dari perkiraan** pada pita untuk meringkas perkiraan proyek berdasarkan jenis transaksi, peran, atau tingkat tugas.</span><span class="sxs-lookup"><span data-stu-id="0dffe-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
