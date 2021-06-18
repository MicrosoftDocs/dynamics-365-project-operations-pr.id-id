---
title: Menghapus estimasi proyek
description: Ini topik menyediakan informasi tentang menghapus estimasi proyek setelah selesai.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006920"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="3c22b-103">Menghapus estimasi proyek</span><span class="sxs-lookup"><span data-stu-id="3c22b-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c22b-104">Perkiraan proyek memberikan tampilan keuangan untuk pekerjaan yang diperkirakan dan dijadwalkan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="3c22b-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="3c22b-105">Untuk bekerja dengan estimasi untuk proyek, Anda harus melampirkan proyek ke proyek estimasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="3c22b-106">Proyek estimasi selalu didasarkan pada proyek yang ada, namun beberapa proyek dapat merujuk ke satu proyek estimasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="3c22b-107">Hanya proyek harga tetap dan investasi yang dapat dilampirkan untuk mengestimasi proyek, dan proyek-proyek tersebut harus termasuk dalam kelompok proyek yang sama dengan proyek estimasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="3c22b-108">Untuk menghapus estimasi proyek, itu harus diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="3c22b-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="3c22b-109">Langkah-langkah berikut menjelaskan cara menghapus estimasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="3c22b-110">Buka **manajemen proyek dan akuntansi** > **Semua proyek** dan buka proyek.</span><span class="sxs-lookup"><span data-stu-id="3c22b-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="3c22b-111">Pada tab **Kelola**, pilih **Estimasi**, dan pada halaman **Estimasi** pilih **Hapus**.</span><span class="sxs-lookup"><span data-stu-id="3c22b-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="3c22b-112">Pada halaman **Hapus estimasi** pada tab **Umum**, atur opsi berikut ini:</span><span class="sxs-lookup"><span data-stu-id="3c22b-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="3c22b-113">**Kode periode**: Pilih kode periode untuk memilih estimasi proyek yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="3c22b-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="3c22b-114">**Tanggal estimasi**: Pilih tanggal estimasi yang sesuai untuk eliminasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="3c22b-115">**Hapus dengan peringatan WIP**: Aktifkan opsi ini untuk memberikan pemberitahuan ketika perkiraan yang terkait dengan pekerjaan yang sedang berlangsung (WIP) akan dihilangkan.</span><span class="sxs-lookup"><span data-stu-id="3c22b-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="3c22b-116">Ketika opsi ini tidak diaktifkan, eliminasi tidak dapat dilanjutkan jika ada transaksi yang tidak diestimasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="3c22b-117">Opsi ini hanya tersedia saat eliminasi diterapkan ke proyek estimasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="3c22b-118">Ini tidak tersedia jika Anda menggunakan posting berkala.</span><span class="sxs-lookup"><span data-stu-id="3c22b-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="3c22b-119">Pengaturan ini berfungsi dengan pengaturan pada tab **Estimasi** pada halaman **Parameter proyek**, di grup bidang **Perbolehkan penghapusan saat transaksi yang tidak diestimasi ada**.</span><span class="sxs-lookup"><span data-stu-id="3c22b-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="3c22b-120">**Atur tahap ke Selesai**: Aktifkan opsi ini untuk mengatur tahap estimasi proyek ke **Selesai** setelah Anda menjalankan eliminasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="3c22b-121">**Cetak Daftar estimasi**: Pilih informasi yang akan disertakan ketika daftar estimasi dicetak.</span><span class="sxs-lookup"><span data-stu-id="3c22b-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="3c22b-122">**Tampilkan Infolog** : Aktifkan opsi ini untuk menampilkan Infolog.</span><span class="sxs-lookup"><span data-stu-id="3c22b-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="3c22b-123">**Tanggal posting** : Pilih tanggal posting buku besar dari estimasi.</span><span class="sxs-lookup"><span data-stu-id="3c22b-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="3c22b-124">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c22b-124">Select **OK**.</span></span>
5. <span data-ttu-id="3c22b-125">Setelah proses eliminasi selesai, proyek estimasi yang dihapus ditampilkan dengan nilai negatif.</span><span class="sxs-lookup"><span data-stu-id="3c22b-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="3c22b-126">Jika Anda tidak bermaksud menghapus estimasi, Anda dapat memilih estimasi yang dihapus dan memilih **Balikkan eliminasi**.</span><span class="sxs-lookup"><span data-stu-id="3c22b-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]