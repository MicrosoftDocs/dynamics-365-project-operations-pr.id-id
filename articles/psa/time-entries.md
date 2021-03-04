---
title: Buat Entri Waktu
description: Topik ini menyediakan informasi tentang cara membuat entri waktu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149682"
---
# <a name="create-time-entries"></a><span data-ttu-id="43975-103">Buat Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="43975-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="43975-104">Di versi sebelumnya Dynamics 365 Project Service Automation, entri waktu dimasukkan secara mingguan.</span><span class="sxs-lookup"><span data-stu-id="43975-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="43975-105">Di versi 3 dari Project Service Automation, entri waktu dimasukkan setiap hari.</span><span class="sxs-lookup"><span data-stu-id="43975-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="43975-106">Namun, setelah beberapa entri waktu dibuat, Anda dapat massal membuat atau menyalinnya.</span><span class="sxs-lookup"><span data-stu-id="43975-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="43975-107">Buat Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="43975-107">Create a time entry</span></span>

<span data-ttu-id="43975-108">Ikuti langkah berikut untuk membuat entri waktu.</span><span class="sxs-lookup"><span data-stu-id="43975-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="43975-109">Pada halaman **Entri waktu**, pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="43975-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="43975-110">Di kotak dialog **buat cepat: entri waktu**, masukkan durasi entri waktu dalam menit, jam, atau hari.</span><span class="sxs-lookup"><span data-stu-id="43975-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="43975-111">Durasi harus dimasukkan dalam format berikut: *x* menit, *x* jam, atau *x* hari.</span><span class="sxs-lookup"><span data-stu-id="43975-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="43975-112">Jam dan hari juga dapat dimasukkan dalam nilai desimal, misalnya, *x,x* jam atau *x,x* hari.</span><span class="sxs-lookup"><span data-stu-id="43975-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="43975-113">Pilih jenis entri waktu dan proyek yang Anda masukkan entri waktunya.</span><span class="sxs-lookup"><span data-stu-id="43975-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="43975-114">Di bidang **tugas proyek**, Cari tugas untuk entri waktu ini.</span><span class="sxs-lookup"><span data-stu-id="43975-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43975-115">Jika Anda membuat entri waktu untuk tugas yang tidak ditetapkan ke pengguna, di bidang **tugas proyek**, pilih tombol **pencarian**, pilih **Ubah tampilan**, lalu pilih **semua tugas proyek yang aktif** untuk mencantumkan semua tugas.</span><span class="sxs-lookup"><span data-stu-id="43975-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="43975-116">Masukkan deskripsi, jika Deskripsi diperlukan, lalu pilih **Simpan dan tutup**.</span><span class="sxs-lookup"><span data-stu-id="43975-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="43975-117">Setelah entri waktu dibuat dan disimpan, Anda dapat mengeditnya di kisi entri waktu .</span><span class="sxs-lookup"><span data-stu-id="43975-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="43975-118">Kisi entri waktu mendukung dua format:</span><span class="sxs-lookup"><span data-stu-id="43975-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="43975-119">Anda dapat memasukkan entri waktu dalam Format **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="43975-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="43975-120">Format ini kemudian dikonversi ke jam dan pecahan.</span><span class="sxs-lookup"><span data-stu-id="43975-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="43975-121">Anda dapat memasukkan jam dan pecahan secara langsung.</span><span class="sxs-lookup"><span data-stu-id="43975-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="43975-122">Perhatikan bahwa pecahan jam bukan menit.</span><span class="sxs-lookup"><span data-stu-id="43975-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="43975-123">Oleh karena itu, 1,5 jam mewakili 1 jam 30 menit.</span><span class="sxs-lookup"><span data-stu-id="43975-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="43975-124">Aturan yang sama berlaku untuk pecahan sehari.</span><span class="sxs-lookup"><span data-stu-id="43975-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="43975-125">Satu hari adalah 24 Jam, dan 0,5 hari menunjukkan 12 jam.</span><span class="sxs-lookup"><span data-stu-id="43975-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="43975-126">Buat Entri Waktu secara massal</span><span class="sxs-lookup"><span data-stu-id="43975-126">Bulk create time entries</span></span>

<span data-ttu-id="43975-127">Setelah beberapa entri waktu dibuat, Anda dapat menyalinnya untuk membuat entri waktu tambahan secara massal.</span><span class="sxs-lookup"><span data-stu-id="43975-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="43975-128">Pada halaman **Entri waktu**, pilih **Salin Pekan**.</span><span class="sxs-lookup"><span data-stu-id="43975-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="43975-129">Di grup bidang **dari periode** di bidang **tanggal mulai** dan **tanggal berakhir**, tentukan rentang tanggal untuk menyalin entri waktu.</span><span class="sxs-lookup"><span data-stu-id="43975-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="43975-130">Di grup bidang **hingga periode**, di bidang **tanggal mulai**, tentukan tanggal untuk membuat entri waktu.</span><span class="sxs-lookup"><span data-stu-id="43975-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="43975-131">Pilih **salin** untuk membuat salinan entri waktu yang sesuai dengan hari dalam minggu yang ditentukan dalam grup bidang **hingga periode**.</span><span class="sxs-lookup"><span data-stu-id="43975-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="43975-132">Misalnya, entri waktu untuk hari Senin pekan lalu disalin ke hari Senin dalam pekan yang ditentukan dalam grup bidang **hingga periode**.</span><span class="sxs-lookup"><span data-stu-id="43975-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="43975-133">Impor data untuk Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="43975-133">Import data for time entries</span></span>

<span data-ttu-id="43975-134">Anda dapat mengimpor data dari Pemesanan dan tugas proyek.</span><span class="sxs-lookup"><span data-stu-id="43975-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="43975-135">Saat mengimpor data, Anda dapat menentukan rentang tanggal Pemesanan untuk diimpor, lalu secara eksplisit memilih Pemesanan yang harus dibuat sebagai entri waktu **draf**.</span><span class="sxs-lookup"><span data-stu-id="43975-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="43975-136">Kemampuan Kelompokkan berdasarkan, Urutkan, pencarian, dan filter</span><span class="sxs-lookup"><span data-stu-id="43975-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="43975-137">Anda dapat mengelompokkan dan memfilter entri waktu berdasarkan dimensi yang ditentukan di kolom.</span><span class="sxs-lookup"><span data-stu-id="43975-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="43975-138">Di bidang **Kelompokkan berdasarkan**, pilih dimensi yang akan digunakan untuk memfilter entri waktu.</span><span class="sxs-lookup"><span data-stu-id="43975-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="43975-139">Anda juga dapat mengurutkan rekaman entri waktu dalam urutan naik atau turun menggunakan panah urut pada heading kolom.</span><span class="sxs-lookup"><span data-stu-id="43975-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="43975-140">Selain itu, Anda dapat menampilkan atau menyembunyikan entri dengan memilih tombol **filter** pada heading kolom, lalu, di kotak **pencarian**, memasukkan teks yang akan digunakan untuk mencari entri waktu berdasarkan nama proyek, tugas proyek, waktu entri, atau sumber daya.</span><span class="sxs-lookup"><span data-stu-id="43975-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
