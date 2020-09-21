---
title: Template Proyek
description: Topik ini menyediakan informasi tentang cara menggunakan template proyek untuk konfigurasi proyek cepat.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f0161bf9-af4c-4a21-b767-ac20a8e30688
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5a3112c2eef9525946314bdb587c44904557fa52
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752409"
---
# <a name="project-templates"></a><span data-ttu-id="e7385-103">Template Proyek</span><span class="sxs-lookup"><span data-stu-id="e7385-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e7385-104">Template proyek adalah kerangka kerja standar yang membantu Anda dengan cepat dan mudah memulai proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="e7385-105">Anda dapat menggunakan template yang telah ditetapkan untuk membuat proyek baru dengan sekali klik.</span><span class="sxs-lookup"><span data-stu-id="e7385-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="e7385-106">Untuk proyek, Anda harus menentukan prasyarat untuk template proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="e7385-107">Anda harus menentukan kalender proyek untuk setiap template proyek, dan peran dan daftar harga harus ditentukan dalam organisasi, sehingga komponen template memiliki data yang berguna.</span><span class="sxs-lookup"><span data-stu-id="e7385-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="e7385-108">Template proyek terdiri dari tiga komponen: jadwal, perkiraan proyek, dan anggota tim proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="e7385-109">Jadwal</span><span class="sxs-lookup"><span data-stu-id="e7385-109">Schedule</span></span>

<span data-ttu-id="e7385-110">Jadwal dalam template proyek memiliki rangkaian elemen yang sama dengan jadwal di proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="e7385-111">Anda dapat membuat hierarki tugas, mengaitkan peran dengan tugas, menetapkan atribut jadwal, dan mengatur dependensi.</span><span class="sxs-lookup"><span data-stu-id="e7385-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="e7385-112">Jadwal dalam template proyek juga mendukung mode tugas untuk setiap tugas.</span><span class="sxs-lookup"><span data-stu-id="e7385-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="e7385-113">Oleh karena itu, alat ini mendukung mesin penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="e7385-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="e7385-114">Anda harus mengaitkan kalender proyek dengan proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="e7385-115">Tidak ada perbedaan antara template proyek dan sebuah proyek ketika membuat jadwal kerja.</span><span class="sxs-lookup"><span data-stu-id="e7385-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="e7385-116">Perkiraan proyek</span><span class="sxs-lookup"><span data-stu-id="e7385-116">Project estimates</span></span>

<span data-ttu-id="e7385-117">Perkiraan proyek dalam template proyek berfungsi sama seperti perkiraan proyek dalam suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="e7385-118">Namun, harga dan harga penjualan ditarik dari daftar harga penjualan dan biaya default yang ditentukan dalam parameter.</span><span class="sxs-lookup"><span data-stu-id="e7385-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="e7385-119">Membuat Proyek dari Template</span><span class="sxs-lookup"><span data-stu-id="e7385-119">Creating a project from a template</span></span>
 
<span data-ttu-id="e7385-120">Ada beberapa cara membuat proyek dari template proyek:</span><span class="sxs-lookup"><span data-stu-id="e7385-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="e7385-121">Ketika Anda membuat proyek dari kuotasi, Anda dapat memilih template proyek dalam kotak dialog **Buat cepat: proyek**.</span><span class="sxs-lookup"><span data-stu-id="e7385-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Kotak dialog buat cepat: proyek](media/project-11.png)

- <span data-ttu-id="e7385-123">Saat membuat proyek dengan memilih **proyek baru**, halaman **proyek** akan ditampilkan sebelum rekaman disimpan.</span><span class="sxs-lookup"><span data-stu-id="e7385-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="e7385-124">Di bidang **pilih template**, pilih salah satu template proyek yang telah ditetapkan dalam organisasi.</span><span class="sxs-lookup"><span data-stu-id="e7385-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="e7385-125">Gunakan **buat proyek dari template** di halaman **entitas template**.</span><span class="sxs-lookup"><span data-stu-id="e7385-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="e7385-126">Menyalin komponen template ke proyek</span><span class="sxs-lookup"><span data-stu-id="e7385-126">Copying components of template to project</span></span>

<span data-ttu-id="e7385-127">Bila Anda menyalin komponen template proyek ke proyek, beberapa penimpaan dapat terjadi, tergantung pada pengaturan dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="e7385-128">Menyalin jadwal</span><span class="sxs-lookup"><span data-stu-id="e7385-128">Copying the schedule</span></span>

<span data-ttu-id="e7385-129">Ketika Anda menyalin jadwal dari template proyek, jika proyek memiliki kalender proyek yang berbeda dari template, jam kerja dari kalender proyek akan diterapkan ke jadwal tugas.</span><span class="sxs-lookup"><span data-stu-id="e7385-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="e7385-130">Dengan demikian, jadwal disesuaikan agar cocok dengan kalendar proyek cadangan.</span><span class="sxs-lookup"><span data-stu-id="e7385-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="e7385-131">Demikian pula, tugas pertama pada jadwal mengambil tanggal mulai proyek, dan jadwal sisa jadwal hierarki tugas diperbarui berdasarkan durasi dan dependensi yang ditentukan dalam struktur rincian kerja template.</span><span class="sxs-lookup"><span data-stu-id="e7385-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="e7385-132">Menyalin Perkiraan proyek</span><span class="sxs-lookup"><span data-stu-id="e7385-132">Copying project estimates</span></span> 

<span data-ttu-id="e7385-133">Bila Anda menyalin seluruh baris perkiraan proyek, daftar harga akan diperbarui.</span><span class="sxs-lookup"><span data-stu-id="e7385-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="e7385-134">Untuk daftar harga biaya, pembaruan ini didasarkan pada unit kepemilikan proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="e7385-135">Untuk daftar harga penjualan, mereka didasarkan pada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="e7385-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="e7385-136">Unit biaya dan harga penjualan ditentukan dari daftar harga ini pada proyek-proyek yang terkait ke entitas penjualan.</span><span class="sxs-lookup"><span data-stu-id="e7385-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="e7385-137">Menyalin tim proyek</span><span class="sxs-lookup"><span data-stu-id="e7385-137">Copying a project team</span></span>

<span data-ttu-id="e7385-138">Bila Anda menyalin tim proyek dari template proyek untuk sebuah proyek, sumber daya generik akan disalin di seluruhnya, bersama dengan keterampilan dan penguasaan yang didefinisikan dalam template.</span><span class="sxs-lookup"><span data-stu-id="e7385-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="e7385-139">Tugas sumber generik juga dikelola seperti template proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="e7385-140">Sumber daya bernama tidak didukung dalam template proyek.</span><span class="sxs-lookup"><span data-stu-id="e7385-140">Named resources aren't supported in project templates.</span></span>
