---
title: Membuat model perkiraan untuk anggaran proyek
description: Topik ini menjelaskan cara membuat model perkiraan untuk anggaran yang tersisa.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078620"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="0838e-103">Membuat model perkiraan untuk anggaran proyek</span><span class="sxs-lookup"><span data-stu-id="0838e-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0838e-104">Topik ini menjelaskan cara membuat model perkiraan untuk anggaran yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="0838e-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="0838e-105">Proyek yang terkait dengan kontrol anggaran menggunakan dua jenis anggaran: asli dan tersisa.</span><span class="sxs-lookup"><span data-stu-id="0838e-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="0838e-106">Saat membuat anggaran proyek, Anda harus menentukan model perkiraan anggaran asli dan yang tersisa yang dibuat di halaman **model perkiraan**.</span><span class="sxs-lookup"><span data-stu-id="0838e-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="0838e-107">Anggaran proyek berdasarkan model tertentu dibuat saat Anda menerapkan anggaran proyek.</span><span class="sxs-lookup"><span data-stu-id="0838e-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="0838e-108">Model perkiraan yang digunakan untuk kontrol anggaran tidak dapat memiliki submodel atau digunakan sebagai submodel.</span><span class="sxs-lookup"><span data-stu-id="0838e-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="0838e-109">Pilih **manajemen proyek dan akuntansi** > **pengaturan** > **perkiraan**  > **model perkiraan**.</span><span class="sxs-lookup"><span data-stu-id="0838e-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="0838e-110">Pilih **baru** untuk membuat model perkiraan baru, lalu masukkan nomor id model dan nama untuk model baru.</span><span class="sxs-lookup"><span data-stu-id="0838e-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="0838e-111">Atur pilihan **berhenti** ke **ya** untuk mencegah perubahan pada baris perkiraan untuk model perkiraan.</span><span class="sxs-lookup"><span data-stu-id="0838e-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="0838e-112">Jika baris perkiraan yang terkait dengan model harus menghasilkan perkiraan arus kas di buku besar, atur **sertakan dalam perkiraan arus kas** ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="0838e-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="0838e-113">Untuk menggunakan tanggal proyek sebagai tanggal faktur, atur **tanggal faktur perkiraan** menjadi **ya**.</span><span class="sxs-lookup"><span data-stu-id="0838e-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="0838e-114">Di bidang **Jenis anggaran** , pilih salah satu jenis model berikut:</span><span class="sxs-lookup"><span data-stu-id="0838e-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="0838e-115">**Anggaran asli** : menggunakan jumlah anggaran asli yang diterapkan saat anggaran awal dibuat dan disetujui.</span><span class="sxs-lookup"><span data-stu-id="0838e-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="0838e-116">**Anggaran tersisa** : Gunakan jumlah anggaran yang tersisa selama masa pakai proyek.</span><span class="sxs-lookup"><span data-stu-id="0838e-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="0838e-117">Saldo dalam model perkiraan ini dikurangi dengan transaksi aktual dan ditingkatkan atau dikurangi dengan revisi anggaran.</span><span class="sxs-lookup"><span data-stu-id="0838e-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="0838e-118">**Penerusan** : Gunakan jumlah anggaran penerusan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="0838e-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="0838e-119">Penerusan adalah proses opsional yang dapat dijalankan untuk mentransfer jumlah anggaran yang tidak terpakai dari satu tahun fiskal ke yang lain.</span><span class="sxs-lookup"><span data-stu-id="0838e-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="0838e-120">Atur pilihan berikut bila diperlukan:</span><span class="sxs-lookup"><span data-stu-id="0838e-120">Set the following options as required:</span></span>

   - <span data-ttu-id="0838e-121">Aktifkan **Tanggal faktur perkiraan** untuk menggunakan tanggal proyek sebagai tanggal faktur.</span><span class="sxs-lookup"><span data-stu-id="0838e-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="0838e-122">Aktifkan **perkiraan dengan WIP** untuk perkiraan berdasarkan pekerjaan yang sedang berlangsung (WIP), lalu pilih jenis WIP.</span><span class="sxs-lookup"><span data-stu-id="0838e-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="0838e-123">Anda dapat menyimpan **jenis anggaran** default sebagai **tidak ada** atau memasukkan jenis baru.</span><span class="sxs-lookup"><span data-stu-id="0838e-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="0838e-124">Jenis anggaran tidak dapat diubah setelah Anda mengubah rekaman.</span><span class="sxs-lookup"><span data-stu-id="0838e-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="0838e-125">Jika Anda mengubah jenis anggaran default, Semua pilihan lain tidak akan tersedia untuk pembaruan, dan Anda tidak dapat menggunakan kembali model perkiraan ini.</span><span class="sxs-lookup"><span data-stu-id="0838e-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

