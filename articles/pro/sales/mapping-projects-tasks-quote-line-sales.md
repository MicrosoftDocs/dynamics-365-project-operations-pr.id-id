---
title: Memetakan proyek dan tugas ke baris kuotasi berbasis proyek
description: Topik ini menyediakan informasi tentang cara memetakan proyek dan tugas ke baris tugas berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964911"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="2fb9e-103">Memetakan proyek dan tugas ke baris kuotasi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="2fb9e-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="2fb9e-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="2fb9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2fb9e-105">Pada baris kuotasi berbasis proyek, Anda dapat memetakan tugas spesifik proyek yang sudah terkait dengan baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="2fb9e-106">Bila Anda memetakan tugas ke baris kuotasi, item berikut yang ditentukan pada baris kuotasi hanya akan berlaku untuk tugas tersebut:</span><span class="sxs-lookup"><span data-stu-id="2fb9e-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="2fb9e-107">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="2fb9e-107">Billing method</span></span>
- <span data-ttu-id="2fb9e-108">Opsi ketertagihan</span><span class="sxs-lookup"><span data-stu-id="2fb9e-108">Chargeability options</span></span>
- <span data-ttu-id="2fb9e-109">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="2fb9e-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="2fb9e-110">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="2fb9e-110">Customers</span></span>

<span data-ttu-id="2fb9e-111">Misalnya, Anda mungkin memiliki proyek dengan satu fase adalah harga tetap dan semua fase lainnya adalah waktu dan bahan.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="2fb9e-112">Dalam kasus ini, Anda dapat mengaitkan tahap pertama, dan semua tugas anak, ke baris kuotasi untuk fase tersebut dengan metode penagihan harga tetap.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="2fb9e-113">Anda kemudian dapat mengaitkan Semua tahapan lain ke baris kuotasi berbasis waktu dan bahan.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="2fb9e-114">Kaitkan tugas ke Baris Kuotasi berbasis Proyek</span><span class="sxs-lookup"><span data-stu-id="2fb9e-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="2fb9e-115">Anda dapat mengaitkan tugas dengan baris kuotasi dari lokasi berikut:</span><span class="sxs-lookup"><span data-stu-id="2fb9e-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="2fb9e-116">Halaman **proyek** > tab **Penagihan tugas** (optimal)</span><span class="sxs-lookup"><span data-stu-id="2fb9e-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="2fb9e-117">Halaman **baris kuotasi** > tab **tugas yang ditagih**</span><span class="sxs-lookup"><span data-stu-id="2fb9e-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="2fb9e-118">Dari halaman proyek</span><span class="sxs-lookup"><span data-stu-id="2fb9e-118">From the Project page</span></span>

<span data-ttu-id="2fb9e-119">Halaman **proyek** memberikan pengalaman optimal untuk mengaitkan tugas ke baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="2fb9e-120">Anda dapat menggunakan Halaman ini untuk memilih beberapa tugas dan mengaitkan semuanya, serta tugas anak mereka, ke baris kuotasi yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="2fb9e-121">Pada tab **Umum** baris kuotasi berbasis proyek, Verifikasikan bidang **proyek** diisi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="2fb9e-122">Di bidang **tugas yang disertakan**, pilih **tugas yang dipilih saja**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="2fb9e-123">Simpan Baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-123">Save the project-based quote line.</span></span> <span data-ttu-id="2fb9e-124">Saat formulir disegarkan, tab **tugas yang bisa ditagih** akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="2fb9e-125">Pada tab **Umum**, pilih tautan untuk proyek dari bidang **proyek**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="2fb9e-126">Pada halaman **proyek**, pilih tab **Penagihan tugas**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="2fb9e-127">Di kisi kedua, yang berlaku untuk penyiapan penagihan khusus tugas, pilih satu atau beberapa tugas, lalu pilih **Kaitkan baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="2fb9e-128">Di halaman dialog yang muncul, pilih baris kuotasi yang menampilkan baris kuotasi berbasis proyek pada kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="2fb9e-129">Di bidang **jenis penagihan**, tentukan Apakah tugas ini dibebankan atau tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="2fb9e-130">Pilih kotak centang untuk menunjukkan apakah Asosiasi harus mencakup tugas anak dari tugas yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="2fb9e-131">Mencentang kotak akan mengaitkan tugas anak dari tugas yang dipilih ke baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="2fb9e-132">Pilih **OK** untuk menutup dialog.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="2fb9e-133">Dari halaman baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="2fb9e-133">From the Quote line page</span></span>

<span data-ttu-id="2fb9e-134">Anda dapat mengaitkan tugas proyek ke baris kuotasi dari tab **tugas yang dapat ditagih** pada halaman **baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="2fb9e-135">Tempat optimal untuk mengaitkan tugas proyek ke baris kuotasi adalah tab **Penagihan tugas** pada halaman **proyek**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="2fb9e-136">Jika Anda mengaitkan tugas dari tab **tugas dapat ditagih** pada halaman **baris kuotasi**, Anda harus mengkaitkan setiap proyek secara manual.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="2fb9e-137">Pada tab **Umum** baris kuotasi berbasis proyek, Verifikasikan bahwa ada proyek yang dipilih di bidang **proyek**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="2fb9e-138">Di bidang **tugas yang disertakan**, pilih **tugas yang dipilih saja**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="2fb9e-139">Simpan Baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-139">Save the project-based quote line.</span></span> <span data-ttu-id="2fb9e-140">Saat formulir disegarkan, tab **tugas yang bisa ditagih** akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="2fb9e-141">Pada tab **tugas dapat ditagih**, pilih **Tambah tugas baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="2fb9e-142">Pada halaman **tugas baris kuotasi**, di bidang **tugas**, pilih tugas dan di bidang **jenis penagihan**, pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="2fb9e-143">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-143">Close the page.</span></span> <span data-ttu-id="2fb9e-144">Tugas yang dipilih sekarang terkait dengan baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="2fb9e-145">Hapus kaitan tugas dari Baris Kuotasi berbasis Proyek</span><span class="sxs-lookup"><span data-stu-id="2fb9e-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="2fb9e-146">Dari halaman proyek</span><span class="sxs-lookup"><span data-stu-id="2fb9e-146">From the Project page</span></span>

<span data-ttu-id="2fb9e-147">Metode ini memberikan pengalaman paling optimal untuk menghapus kaitan tugas dari baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="2fb9e-148">Anda dapat menggunakan beberapa tugas dan menghapus kaitan semuanya, serta tugas anak mereka, dari baris kuotasi yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="2fb9e-149">Pada tab **Umum** baris kuotasi berbasis proyek, di bidang **proyek**, pilih tautan proyek.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="2fb9e-150">Pada halaman **proyek**, pilih tab **Penagihan tugas**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="2fb9e-151">Di kisi kedua, yang berlaku untuk penyiapan penagihan khusus tugas, pilih satu atau beberapa tugas, lalu pilih **Hapus kaitan baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="2fb9e-152">Di halaman dialog yang muncul, pilih baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="2fb9e-153">Pilih kotak centang untuk menunjukkan apakah Asosiasi juga harus dihapus dari tugas anak dari tugas yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="2fb9e-154">Mencentang kotak juga akan menghapus kaitan tugas anak dari tugas yang dipilih ke baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="2fb9e-155">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-155">Select **OK**.</span></span> <span data-ttu-id="2fb9e-156">Pesan peringatan akan menginformasikan bahwa jika Anda menghapus Asosiasi ini, setiap aktual yang sebelumnya dicatat pada tugas tersebut dapat dibalik.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="2fb9e-157">Pilih **OK** untuk melanjutkan dan menghapus keterkaitan antara tugas dan baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="2fb9e-158">Dari halaman baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="2fb9e-158">From the Quote line page</span></span>

<span data-ttu-id="2fb9e-159">Anda juga dapat menghapus kaitan tugas proyek ke baris kuotasi dari tab **tugas yang dapat ditagih** pada halaman **baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="2fb9e-160">Pada tab **tugas dapat ditagih**, pilih **Hapus tugas baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="2fb9e-161">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-161">Select **OK**.</span></span> <span data-ttu-id="2fb9e-162">Pesan peringatan akan menginformasikan bahwa jika Anda menghapus Asosiasi ini, setiap aktual yang sebelumnya dicatat pada tugas tersebut dapat dibalik.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="2fb9e-163">Pilih **OK** untuk melanjutkan dan menghapus keterkaitan antara tugas dan baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="2fb9e-164">Prosedur ini tidak menghapus tugas dari proyek.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="2fb9e-165">Ini hanya akan menghapus asosiasi tugas dari baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="2fb9e-165">It only removes the task association from the project-based quote line.</span></span>
