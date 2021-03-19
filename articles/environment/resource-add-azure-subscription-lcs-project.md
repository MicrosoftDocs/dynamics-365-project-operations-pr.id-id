---
title: Menambahkan langganan Azure ke proyek LCS
description: Topik ini menyediakan informasi tentang cara menyambungkan langganan Azure ke proyek lcs.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289913"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="45d6c-103">Menambahkan langganan Azure ke proyek LCS</span><span class="sxs-lookup"><span data-stu-id="45d6c-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="45d6c-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="45d6c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="45d6c-105">Lingkungan host Cloud harus disebarkan menggunakan langganan Azure yang ada.</span><span class="sxs-lookup"><span data-stu-id="45d6c-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="45d6c-106">Topik ini menjelaskan cara menyambungkan langganan Azure yang ada ke proyek lcs.</span><span class="sxs-lookup"><span data-stu-id="45d6c-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="45d6c-107">Memberikan izin admin</span><span class="sxs-lookup"><span data-stu-id="45d6c-107">Grant admin consent</span></span>

1. <span data-ttu-id="45d6c-108">Di proyek LCS, di Bagian **lingkungan**, pilih **pengaturan Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Pengaturan Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="45d6c-110">Pada halaman **pengaturan proyek**, pada tab **konektor Azure**, pilih **otorisasi**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="45d6c-111">Hal ini memungkinkan lingkungan akan disebarkan ke proyek ini.</span><span class="sxs-lookup"><span data-stu-id="45d6c-111">This allows environments to be deployed to this project.</span></span>

![Azure Connectors](./media/2AzureConnectors.png)

3. <span data-ttu-id="45d6c-113">Pilih **otorisasi** lagi untuk memberikan izin admin.</span><span class="sxs-lookup"><span data-stu-id="45d6c-113">Select **Authorize** again to provide admin consent.</span></span>

![Memberikan izin admin](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="45d6c-115">Terima permintaan izin.</span><span class="sxs-lookup"><span data-stu-id="45d6c-115">Accept the permissions request.</span></span>

![Terima permintaan izin](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="45d6c-117">Otorisasi sekarang selesai.</span><span class="sxs-lookup"><span data-stu-id="45d6c-117">The authorization is now complete.</span></span> 

![Otorisasi berhasil](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="45d6c-119">Berikan akses layanan penyebaran Dynamics ke langganan Azure Anda</span><span class="sxs-lookup"><span data-stu-id="45d6c-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="45d6c-120">Pergi ke [penagihan Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) dan pilih langganan Anda.</span><span class="sxs-lookup"><span data-stu-id="45d6c-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="45d6c-121">Dynamics Deployment Services harus mengakses langganan ini agar dapat menerapkan lingkungan.</span><span class="sxs-lookup"><span data-stu-id="45d6c-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Rincian Langganan Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="45d6c-123">Pilih **kontrol akses (iam)** di panel navigasi, lalu pilih **Tambah penetapan peran**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="45d6c-124">Di penggeser di sisi kanan, pilih **kontributor peran**, dan di daftar yang tersedia, cari dan pilih **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="45d6c-125">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-125">Select **Save**.</span></span>

![Akses Langganan](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="45d6c-127">Menambahkan konektor langganan ke proyek LCS</span><span class="sxs-lookup"><span data-stu-id="45d6c-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="45d6c-128">Di proyek LCS, pada halaman **pengaturan Microsoft Azure**, pilih **Tambah** untuk menambahkan konektor baru.</span><span class="sxs-lookup"><span data-stu-id="45d6c-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="45d6c-129">Masukkan ID langganan Azure Anda.</span><span class="sxs-lookup"><span data-stu-id="45d6c-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="45d6c-130">Anda dapat menemukan ID langganan Azure di [portal Azure](https://ms.portal.azure.com/), dalam  **pengaturan**  di kiri bawah layar.</span><span class="sxs-lookup"><span data-stu-id="45d6c-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="45d6c-131">Di bidang **Konfigurasikan untuk menggunakan Azure Resource Manager**, pilih **ya**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="45d6c-132">Pastikan domain penyewa AAD langganan Azure cocok dengan langganan Azure pemilik domain yang Anda gunakan, lalu pilih **berikutnya**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="45d6c-133">Di layar **konfigurasi Microsoft Azure**, pilih **berikutnya** untuk mengonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="45d6c-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="45d6c-134">Jika Anda menerima kesalahan pada layar ini, kembali ke bagian [menyediakan akses Dynamics Deployment Services ke langganan Azure](#provide) di topik ini, dan pastikan Anda telah menyelesaikan semua langkah.</span><span class="sxs-lookup"><span data-stu-id="45d6c-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="45d6c-135">Unduh sertifikat Manajemen Azure ke folder lokal di komputer, lalu Unggah ke Portal Manajemen Azure dengan membuka **pengaturan** > **sertifikat Manajemen**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="45d6c-136">Sertifikat ini akan mengaktifkan LCS untuk berkomunikasi dengan Azure atas nama Anda.</span><span class="sxs-lookup"><span data-stu-id="45d6c-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="45d6c-137">Anda dapat melewatkan langkah ini jika pengguna Anda memiliki akses ke langganan.</span><span class="sxs-lookup"><span data-stu-id="45d6c-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="45d6c-138">Pilih  **Selanjutnya**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-138">Select  **Next**.</span></span>
8. <span data-ttu-id="45d6c-139">Pilih kawasan Azure untuk disebarkan, lalu pilih pusat data yang dekat dengan lokasi Anda berencana menggunakan sistem ini.</span><span class="sxs-lookup"><span data-stu-id="45d6c-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="45d6c-140">Pilih  **Sambungkan**.</span><span class="sxs-lookup"><span data-stu-id="45d6c-140">Select  **Connect**.</span></span>

<span data-ttu-id="45d6c-141">Anda telah berhasil terhubung langganan Azure Anda.</span><span class="sxs-lookup"><span data-stu-id="45d6c-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="45d6c-142">Anda sekarang dapat menyebarkan lingkungan host Cloud Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="45d6c-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]