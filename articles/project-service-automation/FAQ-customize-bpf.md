---
title: Bagaimana cara menyesuaikan alur proses bisnis tahapan proyek?
description: Ikhtisar cara menyesuaikan alur proses bisnis Tahapan Proyek.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752391"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="750c0-103">Bagaimana cara menyesuaikan alur proses bisnis tahapan proyek?</span><span class="sxs-lookup"><span data-stu-id="750c0-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="750c0-104">Ada batasan umum di versi sebelumnya dari aplikasi Project Service bahwa nama tahapan di alur proses bisnis tahapan proyek harus sama persis dengan nama bahasa Inggris yang diharapkan (**kuotasi**, **merencanakan**, **Tutup**).</span><span class="sxs-lookup"><span data-stu-id="750c0-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="750c0-105">Jika tidak, logika bisnis, yang mengandalkan nama bahasa Inggris tahapan, tidak berfungsi sebagaimana yang diharapkan.</span><span class="sxs-lookup"><span data-stu-id="750c0-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="750c0-106">Karena itu Anda tidak akrab dengan tindakan seperti **beralih proses** atau **Edit proses** yang tersedia di formulir proyek, dan menyesuaikan alur proses bisnis tidak didukung.</span><span class="sxs-lookup"><span data-stu-id="750c0-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="750c0-107">Keterbatasan ini telah diatasi di versi 2.4.5.48 dan kemudian.</span><span class="sxs-lookup"><span data-stu-id="750c0-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="750c0-108">Artikel ini memberikan solusi yang disarankan jika Anda harus menyesuaikan alur proses bisnis default untuk versi sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="750c0-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="750c0-109">Logika bisnis memerlukan pencocokan sama persis dengan nama bahasa Inggris tahapan</span><span class="sxs-lookup"><span data-stu-id="750c0-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="750c0-110">Alur proses bisnis tahapan proyek mencakup logika bisnis yang menggerakkan perilaku berikut dalam aplikasi:</span><span class="sxs-lookup"><span data-stu-id="750c0-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="750c0-111">Bila proyek terkait dengan kuotasi, kode mengatur alur proses bisnis untuk **Quote** tahapan.</span><span class="sxs-lookup"><span data-stu-id="750c0-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="750c0-112">Bila proyek terkait dengan kontrak, kode mengatur alur proses bisnis untuk tahapan **Plan**.</span><span class="sxs-lookup"><span data-stu-id="750c0-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="750c0-113">Bila alur proses bisnis dilanjutkan ke tahapan **Close**, rekaman proyek akan dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="750c0-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="750c0-114">Bila proyek dinonaktifkan, formulir proyek dan struktur rincian kerja (WBS) diatur ke hanya baca, Pemesanan sumber daya bernama dirilis, dan daftar harga terkait apa pun dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="750c0-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="750c0-115">Logika bisnis ini mengandalkan nama bahasa Inggris tahapan proyek.</span><span class="sxs-lookup"><span data-stu-id="750c0-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="750c0-116">Dependensi pada nama tahapan bahasa Inggris ini adalah alasan utama mengapa penyesuaian alur proses bisnis tahapan proyek tidak didukung, serta mengapa Anda tidak melihat alur proses bisnis umum seperti **beralih proses** atau **Mengedit proses** di entitas proyek.</span><span class="sxs-lookup"><span data-stu-id="750c0-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="750c0-117">Apa yang terjadi jika nama tahapan tidak cocok dengan nama bahasa Inggris?</span><span class="sxs-lookup"><span data-stu-id="750c0-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="750c0-118">Di versi aplikasi Project Service 1.x platform 8,2, ketika nama tahapan dalam alur proses bisnis tidak cocok nama bahasa Inggris dengan sama persis, logika bisnis yang mengatur kuotasi atau kontrak, atau yang menyelesaikan proyek, diabaikan.</span><span class="sxs-lookup"><span data-stu-id="750c0-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="750c0-119">Tidak ada pesan kesalahan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="750c0-119">No error messages are displayed.</span></span> <span data-ttu-id="750c0-120">Oleh karena itu sepertinya Anda dapat menyesuaikan alur proses bisnis tahapan proyek.</span><span class="sxs-lookup"><span data-stu-id="750c0-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="750c0-121">Padahal, Anda tidak akan melihat proses otomatis yang berfungsi untuk kuotasi, kontrak, dan tutup proyek.</span><span class="sxs-lookup"><span data-stu-id="750c0-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="750c0-122">Di versi aplikasi Project Service 2.4.4.30 atau sebelumnya di 9.0 platform, ada perubahan arsitektural yang signifikan untuk alur proses bisnis yang mengharuskan penulisan ulang logika bisnis alur proses bisnis.</span><span class="sxs-lookup"><span data-stu-id="750c0-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="750c0-123">Oleh karena itu, jika nama tahapan proses tidak cocok dengan nama bahasa Inggris yang diharapkan, Anda menerima pesan kesalahan.</span><span class="sxs-lookup"><span data-stu-id="750c0-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="750c0-124">Oleh karena itu, jika Anda ingin menyesuaikan alur proses bisnis tahapan proyek untuk entitas proyek, Anda hanya dapat menambahkan tahapan baru untuk alur proses bisnis default untuk entitas proyek, sambil menjaga tahap **kuotasi**, **merencanakan**, dan **tutup** sebagaimana adanya.</span><span class="sxs-lookup"><span data-stu-id="750c0-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="750c0-125">Batasan ini memastikan bahwa Anda tidak mendapatkan kesalahan dari logika bisnis yang mengharapkan nama bahasa Inggris tahapan di alur proses bisnis.</span><span class="sxs-lookup"><span data-stu-id="750c0-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="750c0-126">Di versi 2.4.5.48 atau lebih baru, logika bisnis yang dijelaskan di artikel ini telah dihapus dari alur proses bisnis default untuk entitas proyek.</span><span class="sxs-lookup"><span data-stu-id="750c0-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="750c0-127">Meningkatkan ke versi tersebut atau nanti akan memungkinkan Anda menyesuaikan atau mengganti alur proses bisnis default dengan punya Anda sendiri.</span><span class="sxs-lookup"><span data-stu-id="750c0-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="750c0-128">Solusi untuk versi sebelumnya</span><span class="sxs-lookup"><span data-stu-id="750c0-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="750c0-129">Jika meningkatkan bukan pilihan, Anda dapat menyesuaikan alur proses bisnis tahapan proyek untuk entitas proyek dengan salah satu dari dua cara berikut:</span><span class="sxs-lookup"><span data-stu-id="750c0-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="750c0-130">Menambahkan tahapan tambahan untuk konfigurasi default, sementara tetap mempertahankan nama bahasa Inggris tahapan untuk **kuotasi**, **merencanakan**, dan **tutup**.</span><span class="sxs-lookup"><span data-stu-id="750c0-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-131">![Tangkapan layar menambahkan tahapan ke konfigurasi default](media/FAQ-Customize-BPF-1.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-131">![Screenshot of adding stages to default configuration](media/FAQ-Customize-BPF-1.png)</span></span>
 
2. <span data-ttu-id="750c0-132">Buat alur proses bisnis Anda sendiri dan jadikan itu alur proses bisnis utama untuk entitas proyek, yang memungkinkan Anda memiliki nama tahapan apa pun yang Anda inginkan.</span><span class="sxs-lookup"><span data-stu-id="750c0-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="750c0-133">Namun, jika Anda ingin menggunakan tahapan standar proyek yang sama **kuotasi**, **merencanakan**, dan **tutup**, Anda harus melakukan beberapa penyesuaian yang didorong oleh nama tahapan kustom Anda.</span><span class="sxs-lookup"><span data-stu-id="750c0-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="750c0-134">Logika yang lebih kompleks adalah penutup proyek, yang mana Anda tetap dapat memicu dengan hanya menonaktifkan rekaman proyek.</span><span class="sxs-lookup"><span data-stu-id="750c0-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-135">![Potret layar Penyesuaian BPF](media/FAQ-Customize-BPF-2.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-135">![Screenshot of BPF customization](media/FAQ-Customize-BPF-2.png)</span></span>

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="750c0-136">Pertimbangan tambahan untuk Project Service aplikasi versi 2.4.4.30 atau sebelumnya di platform 9.0</span><span class="sxs-lookup"><span data-stu-id="750c0-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="750c0-137">Project Service 2.4.4.30 atau sebelumnya di platform 9.0, dengan alur proses bisnis kustom, bidang **nama tahapan** di entitas proyek yang digunakan dalam bagan **proyek menurut tahapan**, dan tampilan daftar proyek tidak akan diperbarui, karena digabungkan ke default alur proses bisnis tahapan proyek.</span><span class="sxs-lookup"><span data-stu-id="750c0-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="750c0-138">Anda dapat mengatasi masalah ini dengan langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="750c0-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="750c0-139">Tambahkan bidang kustom untuk mengambil tahapan alur proses bisnis saat ini yang akan diperbarui saat pengguna melalui alur proses bisnis kustom.</span><span class="sxs-lookup"><span data-stu-id="750c0-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="750c0-140">Modifikasikan diagram **proyek menurut tahapan** untuk berfungsi pada bidang kustom Anda, bukan konfigurasi default.</span><span class="sxs-lookup"><span data-stu-id="750c0-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="750c0-141">Langkah-langkah untuk membuat bisnis alur proses bisnis Anda sendiri untuk entitas proyek</span><span class="sxs-lookup"><span data-stu-id="750c0-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="750c0-142">Untuk membuat bisnis alur proses bisnis Anda sendiri untuk entitas proyek, lakukan yang berikut ini:</span><span class="sxs-lookup"><span data-stu-id="750c0-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="750c0-143">Buka **Pengaturan** > **Pusat Proses**.</span><span class="sxs-lookup"><span data-stu-id="750c0-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="750c0-144">Jangan menyalin alur proses bisnis tahapan proyek karena juga menyalin logika bisnis Project Service.</span><span class="sxs-lookup"><span data-stu-id="750c0-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-145">![Potret layar Penyesuaian BPF](media/FAQ-Customize-BPF-3.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-145">![Screenshot of BPF customization](media/FAQ-Customize-BPF-3.png)</span></span>

2. <span data-ttu-id="750c0-146">Gunakan desainer proses untuk membuat nama tahapan yang Anda inginkan.</span><span class="sxs-lookup"><span data-stu-id="750c0-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="750c0-147">Jika Anda ingin fungsi yang sama seperti tahapan default untuk **kuotasi**, **merencanakan**, dan **tutup**, Anda harus membuatnya berdasarkan nama tahapan alur proses bisnis kustom Anda.</span><span class="sxs-lookup"><span data-stu-id="750c0-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-148">![Gambar layar desainer proses yang digunakan untuk menyesuaikan BPF](media/FAQ-Customize-BPF-4.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-148">![Screenshot of Process Designer used to customize BPF](media/FAQ-Customize-BPF-4.png)</span></span> 

3. <span data-ttu-id="750c0-149">Dalam desainer proses, klik **alur proses pesanan** untuk membuat proses bisnis kustom sebagai alur proses bisnis utama untuk entitas proyek dengan memindahkannya di alur proses bisnis tahapan proyek ke atas daftar.</span><span class="sxs-lookup"><span data-stu-id="750c0-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-150">![Tangkapan layar menggunakan alur proses pesanan](media/FAQ-Customize-BPF-5-720.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-150">![Screenshot of using Order Process Flow](media/FAQ-Customize-BPF-5-720.png)</span></span>

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="750c0-151">Langkah-langkah berikut berlaku untuk aplikasi Project Service 2.4.4.30 atau sebelumnya di 9.0 platform</span><span class="sxs-lookup"><span data-stu-id="750c0-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="750c0-152">Tambahkan bidang kustom baru untuk entitas proyek untuk mengambil tahapan kustom di alur proses bisnis kustom Anda.</span><span class="sxs-lookup"><span data-stu-id="750c0-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="750c0-153">Anda harus menambahkan logika bisnis (plugin/alur kerja) untuk memperbarui bidang ini saat tahapan pada alur proses bisnis kustom diperbarui.</span><span class="sxs-lookup"><span data-stu-id="750c0-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-154">![Tangkapan layar penyesuaian entitas proyek](media/FAQ-Customize-BPF-6-720.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-154">![Screenshot of customizing Project entity](media/FAQ-Customize-BPF-6-720.png)</span></span>

5. <span data-ttu-id="750c0-155">Modifikasikan **proyek menurut tahapan** diagram untuk menggunakan bidang kustom baru untuk tahapan.</span><span class="sxs-lookup"><span data-stu-id="750c0-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-156">![Tangkapan layar menggunakan diagram proyek menurut tahapan](media/FAQ-Customize-BPF-7-720.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-156">![Screenshot of using the Project By Stage chart](media/FAQ-Customize-BPF-7-720.png)</span></span>

6. <span data-ttu-id="750c0-157">Modifikasikan apa pun tampilan untuk entitas proyek untuk memasukkan bidang kustom baru untuk tahapan.</span><span class="sxs-lookup"><span data-stu-id="750c0-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="750c0-158">![Tangkapan layar memodifikasi tampilan di entitas proyek](media/FAQ-Customize-BPF-8-720.png)</span><span class="sxs-lookup"><span data-stu-id="750c0-158">![Screenshot of modifying views on the Project entity](media/FAQ-Customize-BPF-8-720.png)</span></span>

