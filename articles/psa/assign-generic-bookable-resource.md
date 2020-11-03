---
title: Tetapkan sumber daya yang dapat dipesan generik ke tim tugas dan proyek
description: Topik ini menyediakan informasi tentang pemesanan sumber daya umum untuk tugas dan tim proyek.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078499"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="d7ccf-103">Tetapkan sumber daya yang dapat dipesan generik ke tugas dan buat persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="d7ccf-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7ccf-104">Selain memesan dan menetapkan sumber daya bernama atau sumber daya nyata ke proyek Anda, Anda dapat menetapkan sumber daya umum untuk tugas proyek.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="d7ccf-105">Sumber daya ini dapat berfungsi sebagai placeholder untuk sumber daya bernama hingga Anda siap dengan staf proyek Anda dengan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="d7ccf-106">Di Project Service Automation (PSA), buka halaman **proyek** dan pada tab **jadwal** , masukkan nama posisi sumber daya generik di sel **sumber daya** jadwal.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="d7ccf-107">Atau, klik ikon **sumber daya** di sel untuk membuka pemilih sumber daya, lalu masukkan nama sumber daya umum yang ingin Anda buat.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Membuat dan menetapkan anggota tim Umum](media/RM-how-to-9.png)

<span data-ttu-id="d7ccf-109">Ini akan membuka panel **Buat Cepat: Anggota Tim Proyek**.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="d7ccf-110">Masukkan peran dan unit organisasi anggota tim sumber daya generik, lalu klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Buat cepat anggota tim generik](media/RM-how-to-10.png)

3. <span data-ttu-id="d7ccf-112">Setelah Anda membuat anggota tim sumber daya generik baru, maka ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="d7ccf-113">Anda dapat terus menetapkan sumber daya generik untuk tugas lain dalam jadwal tugas.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Menetapkan anggota tim generik yang ada ke tugas](media/RM-how-to-11.png)

4. <span data-ttu-id="d7ccf-115">Setelah Anda menetapkan sumber daya generik, Anda dapat membuat persyaratan sumber daya dan memenuhinya dengan langsung memesan atau mengajukan permintaan sumber daya ke manajer sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Menghasilkan persyaratan untuk anggota tim generik](media/RM-how-to-12.png)

<span data-ttu-id="d7ccf-117">Pada kisi anggota tim, selain dapat menggunakan pemilih sumber daya sebagaimana disebutkan di atas, Anda dapat menambahkan sumber daya generik secara langsung.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="d7ccf-118">Sumber daya ditambahkan dengan persyaratan sumber daya yang didasarkan pada tanggal mulai/akhir dan metode alokasi yang ditentukan dalam panel **Buat Cepat: Anggota Tim Proyek**.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="d7ccf-119">Anda dapat melihat perbedaan jika Anda menambahkan anggota tim umum secara langsung, lalu menetapkan lebih banyak tugas ke sumber daya umum daripada waktu yang diperlukan untuk menutupi.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="d7ccf-120">Klik **buat persyaratan** untuk membuat ulang persyaratan untuk menyeimbangkan jam kerja yang diperlukan terhadap tugas.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="d7ccf-121">Anda juga dapat mengeklik tautan **persyaratan sumber daya** di kisi tim untuk membuka persyaratan dan menambahkan keahlian, sumber daya pilihan, dll.</span><span class="sxs-lookup"><span data-stu-id="d7ccf-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Persyaratan Sumber Daya](media/RM-how-to-13.png)

