---
title: Laman beranda peningkatan
description: Topik ini menunjukkan lokasi untuk menemukan informasi penting tentang fitur baru dan yang diubah di Dynamics 365 Project Service Automation, serta proses peningkatan ke versi terbaru.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752471"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="c5542-103">Laman beranda peningkatan</span><span class="sxs-lookup"><span data-stu-id="c5542-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="c5542-104">Tingkatkan dari PSA versi 2.x atau 1.x ke versi 3.x</span><span class="sxs-lookup"><span data-stu-id="c5542-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="c5542-105">Instans baru</span><span class="sxs-lookup"><span data-stu-id="c5542-105">New instances</span></span>

<span data-ttu-id="c5542-106">Per tanggal 17 Mei 2019, ketika Project Service Automation dipilih selama penyediaan instans baru, versi 3. x diinstal secara default.</span><span class="sxs-lookup"><span data-stu-id="c5542-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="c5542-107">Instans yang Ada</span><span class="sxs-lookup"><span data-stu-id="c5542-107">Existing instances</span></span>

<span data-ttu-id="c5542-108">Sebelumnya, pelanggan yang memiliki instans PSA versi 2. x dan perlu meng-upgrade ke versi 3. x, yang merupakan versi berbasis antarmuka klien terpadu (UCI) PSA, harus menghubungi dukungan Microsoft, dan memberikan rincian instans mereka, sehingga dukungan dapat mengaktifkan instans untuk ditingkatkan ke versi 3.x.</span><span class="sxs-lookup"><span data-stu-id="c5542-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="c5542-109">Per 1 Maret 2020, pelanggan yang memiliki contoh PSA versi 2. x dan perlu meng-upgrade ke versi 3. x, akan dapat meningkatkan instance mereka langsung dari portal admin tanpa harus menghubungi dukungan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5542-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="c5542-110">PSA versi 3. x mencakup perubahan signifikan.</span><span class="sxs-lookup"><span data-stu-id="c5542-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="c5542-111">Telah dibangun di atas kerangka kerja Antarmuka Terpadu untuk membantu memberikan pengalaman pengguna yang lebih baik.</span><span class="sxs-lookup"><span data-stu-id="c5542-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="c5542-112">Aplikasi yang didesain ulang memberikan antarmuka pengguna yang konsisten dan seragam (UI), dan mengikuti prinsip desain responsif untuk tampilan optimal pada ukuran layar atau perangkat apa pun.</span><span class="sxs-lookup"><span data-stu-id="c5542-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="c5542-113">Ada perubahan lain di seluruh aplikasi.</span><span class="sxs-lookup"><span data-stu-id="c5542-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="c5542-114">Beberapa area yang telah diubah mencakup harga, pemesanan, dan penetapan sumber daya, waktu, pengeluaran, dan persetujuan.</span><span class="sxs-lookup"><span data-stu-id="c5542-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="c5542-115">Sebelum memulai proses peningkatan, sebaiknya selesaikan tugas berikut:</span><span class="sxs-lookup"><span data-stu-id="c5542-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="c5542-116">Verifikasikan Apakah baik Dynamics 365 Field Service maupun Project Service Automation diinstal pada instans yang teridentifikasi.</span><span class="sxs-lookup"><span data-stu-id="c5542-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="c5542-117">Jika solusi kedua terinstal, Anda harus merencanakan untuk meng-upgrade keduanya sebelum Anda melanjutkan penggunaan instans secara teratur.</span><span class="sxs-lookup"><span data-stu-id="c5542-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="c5542-118">Tinjau topik berikut dengan cermat.</span><span class="sxs-lookup"><span data-stu-id="c5542-118">Carefully review the following topics.</span></span> <span data-ttu-id="c5542-119">Kesadaran dan pemahaman tentang perubahan antara versi akan membantu Anda dengan proses peningkatan.</span><span class="sxs-lookup"><span data-stu-id="c5542-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="c5542-120">Topik ini memberikan informasi tentang perubahan besar dalam PSA, bersama dengan pertimbangan dan rekomendasi untuk merencanakan peningkatan Anda ke versi 3. x.</span><span class="sxs-lookup"><span data-stu-id="c5542-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="c5542-121">Yang baru atau yang diubah di Project Service Automation versi 3</span><span class="sxs-lookup"><span data-stu-id="c5542-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="c5542-122">Pertimbangan peningkatan – Project Service Automation versi 2.x atau 1.x ke versi 3.x</span><span class="sxs-lookup"><span data-stu-id="c5542-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="c5542-123">Tingkatkan instans sandbox anda untuk mengevaluasi perubahan dalam penerapan sebelum meningkatkan instans produksi.</span><span class="sxs-lookup"><span data-stu-id="c5542-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="c5542-124">Setelah Anda meninjau topik yang telah disebutkan sebelumnya dan siap mengupgrade ke versi PSA 3. x atau versi berbasis UCI, Kirim permintaan ke dukungan Microsoft untuk membuat peningkatan tersedia dari Pusat admin.</span><span class="sxs-lookup"><span data-stu-id="c5542-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="c5542-125">Dalam permintaan Anda, berikan rincian instans Anda.</span><span class="sxs-lookup"><span data-stu-id="c5542-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="c5542-126">Versi lama PSA (PSA versi 2. x) di instans yang baru dibuat</span><span class="sxs-lookup"><span data-stu-id="c5542-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="c5542-127">Pada tanggal 17 Mei 2019, Semua instance baru akan memiliki UCI sebagai klien default.</span><span class="sxs-lookup"><span data-stu-id="c5542-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="c5542-128">Untuk penyelarasan dengan perubahan ini, versi PSA 3. x dan Field Service 8. x akan ditetapkan secara default, karena versi ini dirancang untuk bekerja dengan klien UCI.</span><span class="sxs-lookup"><span data-stu-id="c5542-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="c5542-129">Mulai tanggal 1 Maret 2020, pelanggan Dynamics PSA tidak akan lagi dapat membuat lingkungan baru dengan versi PSA yang lebih lama, misalnya PSA versi 2.x atau lebih rendah.</span><span class="sxs-lookup"><span data-stu-id="c5542-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="c5542-130">Lingkungan baru hanya mendapatkan versi 3.x dari PSA.</span><span class="sxs-lookup"><span data-stu-id="c5542-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="c5542-131">Untuk pengalaman terbaik saat Anda menggunakan versi lama dari aplikasi Field Service dan PSA, buka halaman **pengaturan sistem**, dan untuk bidang, bidang **gunakan Antarmuka Terpadu baru saja (disarankan)**, pilih **tidak** karena versi ini tidak dirancang untuk dimuat dengan benar di UCI.</span><span class="sxs-lookup"><span data-stu-id="c5542-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="c5542-132">Setelah Anda telah menonaktifkan UCI, Anda dapat membuka dan menjalankan versi Field Service dan PSA menggunakan klien web lama.</span><span class="sxs-lookup"><span data-stu-id="c5542-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="c5542-133">Untuk petunjuk tentang cara menonaktifkan klien UCI, lihat [mengaktifkan Antarmuka Terpadu saja](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="c5542-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>
