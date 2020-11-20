---
title: Buat Template Proyek
description: Bagaimana membuat template proyek di Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 78d25183aad8d86593d3f2582295db59eb84cf14
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133192"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="a0a0b-103">Buat Template proyek (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a0a0b-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a0a0b-104">Template proyek menghemat waktu Anda jika perusahaan Anda secara teratur mengajukan penawaran pada jenis proyek yang serupa.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="a0a0b-105">Mereka memberikan set standar peran dan perkiraan jam untuk jenis proyek.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="a0a0b-106">Manajer akun dan manajer proyek dapat membuat proyek-proyek berdasarkan template proyek, atau mereka dapat menyalin template dan membuatnya sendiri.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="a0a0b-107">Komponen template proyek</span><span class="sxs-lookup"><span data-stu-id="a0a0b-107">Components of project template</span></span>
 <span data-ttu-id="a0a0b-108">Template proyek terdiri dari tiga komponen:</span><span class="sxs-lookup"><span data-stu-id="a0a0b-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="a0a0b-109">**Struktur rincian kerja**: struktur rincian kerja dalam sebuah template proyek memiliki serangkaian elemen yang sama seperti dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="a0a0b-110">Anda dapat membuat hierarki tugas, mengaitkan peran untuk tugas, menetapkan atribut jadwal, mengatur dependensi dan melihat semua data di Gantt.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="a0a0b-111">Struktur rincian kerja dalam template proyek juga mendukung mode tugas untuk setiap tugas.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="a0a0b-112">Tidak ada perbedaan antara template proyek dan sebuah proyek ketika membuat jadwal kerja.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="a0a0b-113">**Perkiraan proyek**: Perkiraan proyek dalam template berfungsi dengan cara yang sama seperti yang mereka lakukan dalam proyek-proyek, kecuali daftar harga untuk default biaya dan harga penjualan selalu merupakan default biaya dan daftar harga penjualan yang didefinisikan dalam parameter [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a0a0b-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="a0a0b-114">Fungsi lainnya adalah sama seperti dalam sebuah proyek.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="a0a0b-115">**Pembentukan tim proyek**: ketika membentuk sebuah tim proyek untuk template proyek, Anda tidak dapat memesan sumber daya bernama dalam sebuah template.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="a0a0b-116">Anda dapat menggunakan **Buat tim proyek** dalam struktur rincian kerja untuk menghasilkan set sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="a0a0b-117">Anda juga dapat menentukan keterampilan dan penguasaan yang diperlukan untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="a0a0b-118">Anda tidak dapat menggantikan sumber daya generik dengan sumber daya yang dapat dipesan dalam template proyek.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="a0a0b-119">Buat Proyek dari Template</span><span class="sxs-lookup"><span data-stu-id="a0a0b-119">Create a project from a template</span></span>  
 <span data-ttu-id="a0a0b-120">Anda dapat membuat sebuah proyek dari template dengan cara berikut ini:</span><span class="sxs-lookup"><span data-stu-id="a0a0b-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="a0a0b-121">Ketika membuat sebuah proyek dari kuotasi, Anda dapat memilih template proyek dalam formulir membuat cepat proyek.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="a0a0b-122">Ketika membuat sebuah proyek dengan mengklik **Proyek baru**, formulir proyek ditampilkan sebelum menyimpan rekaman.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="a0a0b-123">Dari sini, Anda dapat mengklik bidang **pilih template** untuk memilih dari daftar template proyek yang telah ditetapkan di organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="a0a0b-124">Klik **buat proyek dari template** di halaman **Template proyek** untuk membuat sebuah proyek dari template.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="a0a0b-125">Menyalin komponen template ke proyek</span><span class="sxs-lookup"><span data-stu-id="a0a0b-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="a0a0b-126">Bila Anda menyalin komponen template menjadi proyek, ada beberapa hal yang harus Anda ketahui.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="a0a0b-127">**Menyalin struktur rincian kerja**: ketika Anda menyalin struktur rincian kerja dari template proyek, jika proyek memiliki kalender proyek yang berbeda dari template, jam kerja dari kalender proyek akan diterapkan ke jadwal tugas.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="a0a0b-128">Ini menyesuaikan jadwal untuk kalendar proyek dukungan.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="a0a0b-129">Demikian pula, tugas pertama pada struktur rincian kerja mengambil tanggal mulai proyek, sehingga sisa jadwal hirarki tugas diperbarui berdasarkan durasi dan dependensi yang ditentukan dalam struktur rincian kerja template.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="a0a0b-130">**Menyalin perkiraan proyek**: ketika Anda menyalin seluruh baris perkiraan proyek, daftar harga diperbarui berdasarkan unit penanggung jawab proyek untuk daftar harga biaya dan pelanggan untuk daftar harga penjualan.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="a0a0b-131">Unit biaya dan harga penjualan ditentukan dari daftar harga ini pada proyek-proyek yang terkait ke entitas penjualan.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="a0a0b-132">**Menyalin tim proyek**: bila Anda menyalin tim proyek dari template untuk sebuah proyek, sumber daya generik akan disalin di seluruhnya, bersama dengan keterampilan dan penguasaan yang didefinisikan dalam template.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="a0a0b-133">Tugas sumber generik juga dikelola seperti template proyek.</span><span class="sxs-lookup"><span data-stu-id="a0a0b-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a0a0b-134">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="a0a0b-134">See Also</span></span>  
 [<span data-ttu-id="a0a0b-135">Panduan Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="a0a0b-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
