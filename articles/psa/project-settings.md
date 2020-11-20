---
title: pengaturan proyek
description: Topik ini menyediakan informasi tentang pengaturan manajemen proyek.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123112"
---
# <a name="project-settings"></a><span data-ttu-id="2c17b-103">pengaturan proyek</span><span class="sxs-lookup"><span data-stu-id="2c17b-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2c17b-104">Gunakan pengaturan berikut untuk mengakses fitur Perencanaan proyek.</span><span class="sxs-lookup"><span data-stu-id="2c17b-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="2c17b-105">Template kerja</span><span class="sxs-lookup"><span data-stu-id="2c17b-105">Work template</span></span>

<span data-ttu-id="2c17b-106">Untuk membuat jadwal proyek, Anda membuat template kalender proyek yang mendefinisikan jumlah jam kerja setiap hari dan penutupan bisnis apapun.</span><span class="sxs-lookup"><span data-stu-id="2c17b-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="2c17b-107">Untuk membuat template kalender proyek, Anda mengaitkan template kerja dengan bidang **template kalender** untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="2c17b-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="2c17b-108">Ikuti langkah berikut untuk membuat template kerja.</span><span class="sxs-lookup"><span data-stu-id="2c17b-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="2c17b-109">Dalam PSA, di panel navigasi kiri, klik **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="2c17b-110">Di halaman daftar **sumber daya**, buka rekaman pengguna, lalu pilih **Tampilkan Jam Kerja**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2c17b-111">Pastikan Anda mengizinkan pop-up di halaman browser.</span><span class="sxs-lookup"><span data-stu-id="2c17b-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="2c17b-112">Dengan demikian, Anda dapat melihat jam kerja yang ditetapkan untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="2c17b-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="2c17b-113">Pada tab **tampilan bulanan**, klik **Atur**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="2c17b-114">Daftar tiga pilihan muncul:</span><span class="sxs-lookup"><span data-stu-id="2c17b-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="2c17b-115">Jadwal Mingguan Baru</span><span class="sxs-lookup"><span data-stu-id="2c17b-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="2c17b-116">Jadwal Kerja untuk Satu Hari</span><span class="sxs-lookup"><span data-stu-id="2c17b-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="2c17b-117">Waktu Nonaktif</span><span class="sxs-lookup"><span data-stu-id="2c17b-117">Time Off</span></span>

> ![Pilihan konfigurasi](media/project-13.png)

4. <span data-ttu-id="2c17b-119">Pilih **jadwal mingguan baru**, lalu Atur pilihan untuk jadwal sumber daya ini.</span><span class="sxs-lookup"><span data-stu-id="2c17b-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="2c17b-120">Anda dapat mengatur jadwal mingguan yang berulang, parameter jam harian, penutupan bisnis, dan banyak lagi.</span><span class="sxs-lookup"><span data-stu-id="2c17b-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="2c17b-121">Atur rentang tanggal, pilih **Simpan**, lalu klik **tutup**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="2c17b-122">Kembali ke halaman daftar **sumber daya**, dan pilih sumber daya yang Anda tetapkan jam kerja.</span><span class="sxs-lookup"><span data-stu-id="2c17b-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="2c17b-123">Pilih **Atur kalender sebagai** untuk mengatur template kerja.</span><span class="sxs-lookup"><span data-stu-id="2c17b-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="2c17b-124">Di kotak dialog **template kerja**, masukkan nama untuk template kerja, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="2c17b-125">Sekarang Anda dapat mengaitkan template kerja dengan template kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="2c17b-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="2c17b-126">Peran Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="2c17b-126">Resource roles</span></span>

<span data-ttu-id="2c17b-127">Istilah *peran sumber daya* merujuk pada seperangkat keterampilan, kompetensi, dan sertifikasi yang harus dimiliki oleh seseorang untuk melakukan serangkaian tugas tertentu pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="2c17b-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="2c17b-128">PSA memungkinkan Anda mata uang biaya dan tagihan waktu sumber daya berdasarkan peran yang terkait dengan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="2c17b-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="2c17b-129">Setiap organisasi harus mengkonfigurasi peran ini dengan menggunakan navigasi kiri pada menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="2c17b-130">Setiap organisasi harus mengkonfigurasi peran ini di halaman **kategori sumber daya aktif**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="2c17b-131">Untuk membuka Halaman ini, di panel navigasi kiri, pilih **peran sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="2c17b-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="2c17b-132">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="2c17b-132">Price lists</span></span>

<span data-ttu-id="2c17b-133">Daftar harga memungkinkan Anda menetapkan biaya dan harga penjualan untuk peran sumber, kategori pengeluaran, produk, dan elemen lain dalam organisasi.</span><span class="sxs-lookup"><span data-stu-id="2c17b-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="2c17b-134">Sebelum Anda membuat perkiraan keuangan untuk pekerjaan yang harus dilaksanakan untuk proyek, Anda harus membuat daftar harga biaya dan penjualan cadangan.</span><span class="sxs-lookup"><span data-stu-id="2c17b-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="2c17b-135">Di bagian parameter, Anda juga harus mengkonfigurasi daftar harga dan harga penjualan default yang berlaku untuk semua proyek yang dibuat di organisasi.</span><span class="sxs-lookup"><span data-stu-id="2c17b-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="2c17b-136">Pada halaman **parameter proyek aktif**, pastikan Anda mengkonfigurasi daftar biaya dan harga penjualan default.</span><span class="sxs-lookup"><span data-stu-id="2c17b-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
