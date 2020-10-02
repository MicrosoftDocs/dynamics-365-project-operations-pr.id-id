---
title: Mengonfigurasi pembuatan faktur otomatis
description: Topik ini menyediakan informasi tentang mengkonfigurasi sistem untuk menghasilkan faktur secara otomatis.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898130"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="07ac4-103">Mengonfigurasi pembuatan faktur otomatis</span><span class="sxs-lookup"><span data-stu-id="07ac4-103">Configure automated invoice creation</span></span>

<span data-ttu-id="07ac4-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="07ac4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="07ac4-105">Selesaikan langkah-langkah berikut untuk mengkonfigurasi faktur otomatis berjalan dalam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="07ac4-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="07ac4-106">Buka **Pengaturan** \> **Pekerjaan bets**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="07ac4-107">Membuat batch pekerjaan, dan namai **Project operations buat faktur**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="07ac4-108">Nama pekerjaan batch harus mencakup istilah "Buat faktur".</span><span class="sxs-lookup"><span data-stu-id="07ac4-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="07ac4-109">Di bidang **jenis pekerjaan**, pilih **tidak ada**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="07ac4-110">Secara default, **frekuensi harian** dan opsi **aktif** diatur ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="07ac4-111">Pilih **Jalankan alur kerja**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-111">Select **Run Workflow**.</span></span> <span data-ttu-id="07ac4-112">Di kotak dialog **mencari rekaman**, Anda akan melihat tiga alur kerja:</span><span class="sxs-lookup"><span data-stu-id="07ac4-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="07ac4-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="07ac4-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="07ac4-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="07ac4-114">ProcessRunner</span></span>
    - <span data-ttu-id="07ac4-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="07ac4-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="07ac4-116">Pilih **ProcessRunCaller** dan kemudian pilih **Tambahkan**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="07ac4-117">Pilih **OK** di kotak dialog berikutnya.</span><span class="sxs-lookup"><span data-stu-id="07ac4-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="07ac4-118">Alur kerja **tidur** diikuti dengan alur kerja **proses**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="07ac4-119">Anda juga dapat memilih **ProcessRunner** di langkah 5.</span><span class="sxs-lookup"><span data-stu-id="07ac4-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="07ac4-120">Kemudian, bila Anda memilih **OK**, alur kerja **proses** diikuti dengan alur kerja **tidur**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="07ac4-121">Alur kerja **ProcessRunCaller** dan **ProcessRunner** membuat faktur.</span><span class="sxs-lookup"><span data-stu-id="07ac4-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="07ac4-122">**ProcessRunCaller** memanggil **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="07ac4-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="07ac4-123">**ProcessRunner** adalah alur kerja yang benar-benar membuat faktur.</span><span class="sxs-lookup"><span data-stu-id="07ac4-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="07ac4-124">Ia melalui semua baris kontrak pembuatan faktur, dan membuat faktur untuk baris tersebut.</span><span class="sxs-lookup"><span data-stu-id="07ac4-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="07ac4-125">Untuk menentukan baris kontrak yang harus dibuat faktur, pekerjaan akan melihat tanggal faktur berjalan untuk baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="07ac4-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="07ac4-126">Jika baris kontrak milik satu kontrak memiliki tanggal yang sama saat menjalankan faktur, transaksi digabungkan menjadi satu faktur yang memiliki dua baris faktur.</span><span class="sxs-lookup"><span data-stu-id="07ac4-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="07ac4-127">Jika tidak ada transaksi untuk membuat faktur, pekerjaan akan melompati pembuatan faktur.</span><span class="sxs-lookup"><span data-stu-id="07ac4-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="07ac4-128">Setelah **ProcessRunner** selesai berjalan, maka ia memanggil **ProcessRunCaller**, menyediakan waktu berakhir, dan ditutup.</span><span class="sxs-lookup"><span data-stu-id="07ac4-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="07ac4-129">**ProcessRunCaller** kemudian memulai timer yang berjalan selama 24 jam dari waktu berakhir yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="07ac4-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="07ac4-130">Di akhir timer, **ProcessRunCaller** ditutup.</span><span class="sxs-lookup"><span data-stu-id="07ac4-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="07ac4-131">Pekerjaan proses batch untuk membuat faktur adalah pekerjaan berulang.</span><span class="sxs-lookup"><span data-stu-id="07ac4-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="07ac4-132">Jika proses batch ini dijalankan berkali-kali, beberapa instans pekerjaan dibuat dan menyebabkan kesalahan.</span><span class="sxs-lookup"><span data-stu-id="07ac4-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="07ac4-133">Oleh karena itu, Anda harus memulai proses batch hanya satu kali, dan Anda harus me-restart hanya jika berhenti berjalan.</span><span class="sxs-lookup"><span data-stu-id="07ac4-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="07ac4-134">Faktur bets hanya berjalan untuk baris kontrak proyek yang dikonfigurasi dengan jadwal faktur.</span><span class="sxs-lookup"><span data-stu-id="07ac4-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="07ac4-135">Baris kontrak dengan metode penagihan harga tetap harus mengonfigurasikan tonggak waktu.</span><span class="sxs-lookup"><span data-stu-id="07ac4-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="07ac4-136">Baris kontrak proyek dengan metode waktu dan materi penagihan akan memerlukan pengaturan jadwal faktur berdasarkan tanggal.</span><span class="sxs-lookup"><span data-stu-id="07ac4-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="07ac4-137">Hal yang sama berlaku untuk baris kontrak berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="07ac4-137">The same applies to a project-based contract line.</span></span>     
