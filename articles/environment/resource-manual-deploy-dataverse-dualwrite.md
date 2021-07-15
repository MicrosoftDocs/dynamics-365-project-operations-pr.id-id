---
title: Terapkan aplikasi Project Operations Dataverse secara manual dengan dukungan penulisan ganda
description: Topik ini menjelaskan cara menyebarkan aplikasi Project Operations Dataverse secara manual sehingga mendukung penulisan ganda.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274012"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="5515b-103">Terapkan aplikasi Project Operations Dataverse secara manual dengan dukungan penulisan ganda</span><span class="sxs-lookup"><span data-stu-id="5515b-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="5515b-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="5515b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5515b-105">Topik ini menjelaskan cara menyebarkan Microsoft Dynamics 365 Project Operations di Microsoft Dataverse secara manual sehingga mendukung penulisan ganda.</span><span class="sxs-lookup"><span data-stu-id="5515b-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="5515b-106">Project Operations mendeteksi konfigurasi lingkungan dan menambahkan dukungan tambahan untuk penulisan ganda jika prasyarat terpenuhi.</span><span class="sxs-lookup"><span data-stu-id="5515b-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="5515b-107">Selama penyebaran Microsoft Dynamics melalui Lifecycle Services (LCS), jika Anda telah mengikuti petunjuk di topik ini, Anda dapat melewatkan penyebaran integrasi Microsoft Power Platform (sebelumnya dikenal sebagai lingkungan Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="5515b-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="5515b-108">Proses penyebaran Project Operations di Dataverse sehingga mendukung penulisan ganda memiliki empat langkah utama:</span><span class="sxs-lookup"><span data-stu-id="5515b-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="5515b-109">[Membuat lingkungan baru di Dataverse yang mendukung penulisan ganda](#create).</span><span class="sxs-lookup"><span data-stu-id="5515b-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="5515b-110">[Menambahkan prasyarat penulisan ganda ke lingkungan](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="5515b-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="5515b-111">[Tambahkan aplikasi Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="5515b-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="5515b-112">[Tautkan lingkungan Anda](#link).</span><span class="sxs-lookup"><span data-stu-id="5515b-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="5515b-113">Membuat lingkungan baru di Dataverse yang mendukung penulisan ganda</span><span class="sxs-lookup"><span data-stu-id="5515b-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="5515b-114">Untuk menyelesaikan prosedur ini, Anda harus masuk sebagai administrator.</span><span class="sxs-lookup"><span data-stu-id="5515b-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="5515b-115">Buka [pusat admin Power Platform](https://admin.powerplatform.com), lalu masuk sebagai administrator.</span><span class="sxs-lookup"><span data-stu-id="5515b-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="5515b-116">Buat lingkungan baru dan beri nama.</span><span class="sxs-lookup"><span data-stu-id="5515b-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="5515b-117">Pilih jenis lingkungan.</span><span class="sxs-lookup"><span data-stu-id="5515b-117">Select the environment type.</span></span> <span data-ttu-id="5515b-118">Jika Anda mendaftar penawaran uji coba, pilih **Uji Coba (berbasis langganan)**.</span><span class="sxs-lookup"><span data-stu-id="5515b-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="5515b-119">Konfirmasikan kawasan penyebaran.</span><span class="sxs-lookup"><span data-stu-id="5515b-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="5515b-120">Aktifkan pilihan **Buat database untuk lingkungan ini**.</span><span class="sxs-lookup"><span data-stu-id="5515b-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="5515b-121">Konfirmasikan bahasa, lalu konfirmasikan bahwa mata uang sesuai dengan mata uang untuk aplikasi Finance and Operations Anda.</span><span class="sxs-lookup"><span data-stu-id="5515b-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="5515b-122">Aktifkan pilihan **aplikasi Dynamics 365**, dan konfirmasikan bahwa bidang **Terapkan aplikasi ini secara otomatis** diatur ke **Tidak Ada**.</span><span class="sxs-lookup"><span data-stu-id="5515b-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="5515b-123">Tambahkan grup keamanan, jika grup keamanan diperlukan.</span><span class="sxs-lookup"><span data-stu-id="5515b-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="5515b-124">Pilih **Simpan** untuk membuat lingkungan.</span><span class="sxs-lookup"><span data-stu-id="5515b-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="5515b-125">Tunggu selama penyebaran selesai dan lingkungan mencapai status **Siap**.</span><span class="sxs-lookup"><span data-stu-id="5515b-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="5515b-126">Menambahkan prasyarat penulisan ganda ke lingkungan</span><span class="sxs-lookup"><span data-stu-id="5515b-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="5515b-127">Dukungan penulisan ganda mencakup bidang tambahan yang ditambahkan ke entitas utama, seperti entitas **Perusahaan**.</span><span class="sxs-lookup"><span data-stu-id="5515b-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="5515b-128">Jika Anda menambahkan dukungan penulisan ganda ke lingkungan yang ada, Anda harus memperbarui data untuk mengaktifkan dukungan.</span><span class="sxs-lookup"><span data-stu-id="5515b-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="5515b-129">Untuk informasi tentang cara meng-klik data, lihat [data perusahaan Bootstrap](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="5515b-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="5515b-130">Untuk informasi lebih lanjut tentang penulisan ganda, lihat [persyaratan sistem Penulisan ganda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="5515b-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="5515b-131">Selesaikan prosedur ini untuk menambahkan prasyarat penulisan ganda ke lingkungan Anda.</span><span class="sxs-lookup"><span data-stu-id="5515b-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="5515b-132">Buka lingkungan yang baru saja Anda buat, lalu buka **Sumber daya** \> **aplikasi Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5515b-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="5515b-133">Pilih **solusi inti penulisan ganda** dalam daftar aplikasi, lalu instal.</span><span class="sxs-lookup"><span data-stu-id="5515b-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="5515b-134">Tunggu hingga penginstalan selesai.</span><span class="sxs-lookup"><span data-stu-id="5515b-134">Wait until the installation is completed.</span></span> <span data-ttu-id="5515b-135">Lalu Pilih **solusi orkestrasi aplikasi penulisan ganda** dalam daftar aplikasi, lalu instal.</span><span class="sxs-lookup"><span data-stu-id="5515b-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="5515b-136">Tambahkan aplikasi Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="5515b-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="5515b-137">Anda dapat menyelesaikan prosedur ini hanya jika Anda telah menyelesaikan prosedur sebelumnya sebelum menginstal Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5515b-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="5515b-138">Selama penginstalan, sistem akan menganalisis konfigurasi lingkungan dan menambahkan dukungan untuk penulisan ganda jika diperlukan.</span><span class="sxs-lookup"><span data-stu-id="5515b-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="5515b-139">Buka lingkungan yang Anda buat tadi, lalu buka **Sumber daya** \> **aplikasi Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5515b-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="5515b-140">Pilih **Microsoft Dynamics 365 Project Operations** dalam daftar aplikasi, lalu instal.</span><span class="sxs-lookup"><span data-stu-id="5515b-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="5515b-141">Tautkan lingkungan Anda</span><span class="sxs-lookup"><span data-stu-id="5515b-141">Link your environments</span></span>

<span data-ttu-id="5515b-142">Setelah lingkungan Dataverse disebarkan, Anda dapat mengkonfigurasi tautan di aplikasi Finance and Operations Anda.</span><span class="sxs-lookup"><span data-stu-id="5515b-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="5515b-143">Ikuti langkah-langkah dalam [Gunakan wizard penulisan ganda untuk menautkan lingkungan Anda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="5515b-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
