---
title: Sekilas persetujuan
description: Topik ini menyediakan informasi topik tentang bekerja dengan nilai persetujuan dalam Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368660"
---
# <a name="approvals-overview"></a><span data-ttu-id="db165-103">Sekilas persetujuan</span><span class="sxs-lookup"><span data-stu-id="db165-103">Approvals overview</span></span>

<span data-ttu-id="db165-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="db165-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="db165-105">Pengajuan penggunaan bahan, waktu, dan pengeluaran akan melalui alur kerja yang telah disetujui.</span><span class="sxs-lookup"><span data-stu-id="db165-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="db165-106">Setelah entri disetujui, transaksi dicatat dalam aktual atau waktu dipesan dalam jadwal.</span><span class="sxs-lookup"><span data-stu-id="db165-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="db165-107">Alur kerja persetujuan</span><span class="sxs-lookup"><span data-stu-id="db165-107">Approvals workflow</span></span>
<span data-ttu-id="db165-108">Saat Anda membuat dan mengajukan entri penggunaan bahan, waktu, atau pengeluaran, rekaman persetujuan dibuat.</span><span class="sxs-lookup"><span data-stu-id="db165-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="db165-109">Pemberi izin proyek atau manajer meninjau dan menyetujui entri.</span><span class="sxs-lookup"><span data-stu-id="db165-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="db165-110">Jika entrinya terkait dengan proyek, aktual akan dibuat saat disetujui.</span><span class="sxs-lookup"><span data-stu-id="db165-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="db165-111">Hal ini memungkinkan biaya dan penagihan dilacak.</span><span class="sxs-lookup"><span data-stu-id="db165-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="db165-112">Setujui entri</span><span class="sxs-lookup"><span data-stu-id="db165-112">Approve an entry</span></span>
<span data-ttu-id="db165-113">Halaman **Persetujuan** memungkinkan Anda beralih antara tampilan yang berbeda sehingga Anda dapat melihat berbagai jenis persetujuan.</span><span class="sxs-lookup"><span data-stu-id="db165-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="db165-114">Buka halaman **Persetujuan**, lalu pilih **Pengeluaran**, **Waktu**, **Penggunaan Bahan**, atau **Penarikan**.</span><span class="sxs-lookup"><span data-stu-id="db165-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="db165-115">Tinjau setiap persetujuan, dan pilih yang ingin Anda setujui.</span><span class="sxs-lookup"><span data-stu-id="db165-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="db165-116">Pilih **setujui** untuk menyetujui entri yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="db165-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="db165-117">Sistem memproses entri ini dan membuat aktual.</span><span class="sxs-lookup"><span data-stu-id="db165-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="db165-118">Menolak entri</span><span class="sxs-lookup"><span data-stu-id="db165-118">Reject an entry</span></span>
<span data-ttu-id="db165-119">Sebagai pemberi izin proyek, Anda mungkin harus mengirim entri kembali ke pengguna untuk koreksi.</span><span class="sxs-lookup"><span data-stu-id="db165-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="db165-120">Buka halaman **Persetujuan**, lalu pilih entri untuk ditolak.</span><span class="sxs-lookup"><span data-stu-id="db165-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="db165-121">Pilih **Tolak**.</span><span class="sxs-lookup"><span data-stu-id="db165-121">Select **Reject**.</span></span>
3. <span data-ttu-id="db165-122">Opsional, tambahkan komentar dalam kotak dialog **Komentar Penolakan** untuk memberitahukan pengguna alasan ditolaknya entri.</span><span class="sxs-lookup"><span data-stu-id="db165-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="db165-123">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="db165-123">Select **OK**.</span></span> <span data-ttu-id="db165-124">Entri akan dikembalikan kepada pengguna.</span><span class="sxs-lookup"><span data-stu-id="db165-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="db165-125">Batalkan Persetujuan</span><span class="sxs-lookup"><span data-stu-id="db165-125">Cancel approval</span></span>
<span data-ttu-id="db165-126">Dalam kasus tertentu, Anda mungkin harus membatalkan entri yang disetujui sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="db165-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="db165-127">Membatalkan entri yang disetujui sebelumnya akan memiliki dampak keuangan.</span><span class="sxs-lookup"><span data-stu-id="db165-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="db165-128">Menyetujui permintaan penarikan</span><span class="sxs-lookup"><span data-stu-id="db165-128">Approving recall requests</span></span>
<span data-ttu-id="db165-129">Dalam kasus tertentu, seorang konsultan mungkin harus menarik entri yang disetujui sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="db165-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="db165-130">Membatalkan entri yang disetujui sebelumnya akan memiliki dampak keuangan.</span><span class="sxs-lookup"><span data-stu-id="db165-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="db165-131">Pemberi izin proyek harus menyetujui penarikan untuk membatalkan transaksi dalam Aktual.</span><span class="sxs-lookup"><span data-stu-id="db165-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="db165-132">Menentukan Pemberi persetujuan proyek</span><span class="sxs-lookup"><span data-stu-id="db165-132">Specify Project approvers</span></span>
<span data-ttu-id="db165-133">Setiap proyek memiliki sejumlah anggota tim proyek.</span><span class="sxs-lookup"><span data-stu-id="db165-133">Each project has a number of project team members.</span></span> <span data-ttu-id="db165-134">Anda dapat menentukan anggota tim yang juga pemberi persetujuan proyek.</span><span class="sxs-lookup"><span data-stu-id="db165-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="db165-135">Buka halaman **Proyek**, lalu buka proyek dari daftar.</span><span class="sxs-lookup"><span data-stu-id="db165-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="db165-136">Pada tab **tim**, pilih anggota tim yang akan menjadi pemberi izin proyek dan kemudian pilih **Edit**.</span><span class="sxs-lookup"><span data-stu-id="db165-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="db165-137">Atur **bidang pemberi izin proyek** ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="db165-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="db165-138">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="db165-138">Select **Save**.</span></span>
5. <span data-ttu-id="db165-139">Ulangi langkah 2-4 untuk menambahkan pemberi izin proyek tambahan.</span><span class="sxs-lookup"><span data-stu-id="db165-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="db165-140">Mengkonfigurasi manajer pengguna</span><span class="sxs-lookup"><span data-stu-id="db165-140">Configure the user's manager</span></span>

1. <span data-ttu-id="db165-141">Buka **Pengaturan** > **Keamanan** > **Pengguna**.</span><span class="sxs-lookup"><span data-stu-id="db165-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="db165-142">Pilih pengguna yang akan Anda tetapkan manajer dan di area **informasi organisasi**, pilih manajer dari daftar.</span><span class="sxs-lookup"><span data-stu-id="db165-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="db165-143">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="db165-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
