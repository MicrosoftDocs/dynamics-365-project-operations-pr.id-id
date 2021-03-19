---
title: Kelola sumber daya
description: Topik ini menyediakan informasi tentang cara Anda mengelola sumber daya.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 1d47be6c11ced70b94b7497dfbc0c67d1a3f631b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275002"
---
# <a name="manage-resources"></a><span data-ttu-id="da6ed-103">Kelola sumber daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="da6ed-104">Dynamics 365 Project Service Automation mencakup dasbor manajer sumber daya yang memberikan ikhtisar visual mengenai permintaan dan pemanfaatan sumber daya di seluruh organisasi.</span><span class="sxs-lookup"><span data-stu-id="da6ed-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="da6ed-105">Anda dapat menggunakan diagram di dasbor ini untuk memvisualisasikan informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="da6ed-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="da6ed-106">**Permintaan sumber daya**- diagram **permintaan sumber daya aktif** menampilkan sumber daya yang telah diajukan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="da6ed-107">Sumber daya dikumpulkan baik oleh peran maupun proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="da6ed-108">**Permintaan sumber daya yang belum diajukan** – diagram **permintaan sumber daya yang belum ditetapkan** menampilkan semua persyaratan sumber daya yang belum diajukan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="da6ed-109">Hal ini membantu manajer sumber daya melihat permintaan yang tidak tegas dan dapat diajukan melalui permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="da6ed-110">**Pemanfaatan yang dapat ditagih selama seminggu terakhir** – diagram **pemanfaatan berdasarkan peran** menunjukkan persentase pemanfaatan aktual yang dilakukan organisasi berdasarkan target yang dapat ditagih berdasarkan peran.</span><span class="sxs-lookup"><span data-stu-id="da6ed-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da6ed-111">Untuk membuat diagram **pemanfaatan berdasarkan peran** tersedia, buat pekerjaan yang menjalankan alur kerja UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="da6ed-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="da6ed-112">Pekerjaan rutin ini berjalan setiap tujuh hari untuk menghitung pemanfaatan yang dapat ditagih selama tujuh hari sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="da6ed-113">Hasil akan digabungkan berdasarkan peran.</span><span class="sxs-lookup"><span data-stu-id="da6ed-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="da6ed-114">Kelola Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="da6ed-114">Manage project team members</span></span>

<span data-ttu-id="da6ed-115">Manajer proyek dapat menggunakan dasbor manajer sumber daya untuk mengelola sumber daya pada proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="da6ed-116">Misalnya, mereka dapat menambahkan anggota tim secara langsung ke proyek dan memesan anggota tim untuk memenuhi persyaratan sumber daya yang ditangkap oleh sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="da6ed-117">Tambahkan anggota tim langsung ke proyek</span><span class="sxs-lookup"><span data-stu-id="da6ed-117">Add a team member directly to a project</span></span>

<span data-ttu-id="da6ed-118">Untuk menambahkan anggota tim secara langsung ke proyek, pada halaman **proyek**, pada tab **tim**, pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="da6ed-119">Kotak dialog **buat cepat: anggota tim proyek** akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="da6ed-120">Di kotak dialog ini, Anda dapat melakukan tugas berikut:</span><span class="sxs-lookup"><span data-stu-id="da6ed-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="da6ed-121">**Memesan sumber daya bernama**-di bidang **sumber daya dapat dipesan**, pilih nama sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="da6ed-122">Kemudian pilih peran, atur periode, dan pilih metode alokasi.</span><span class="sxs-lookup"><span data-stu-id="da6ed-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="da6ed-123">Sumber daya bernama yang Anda pilih ditambahkan ke proyek menggunakan metode alokasi yang dipilih dan kalender sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="da6ed-124">**Menambahkan sumber daya generik** – biarkan bidang **sumber daya dapat dipesan** kosong, lalu pilih peran, atur periode, dan pilih metode alokasi yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="da6ed-125">Sumber daya generik ditambahkan ke tim sebagai placeholder untuk menyimpan pola permintaan yang digunakan untuk memesan sumber daya pada tim.</span><span class="sxs-lookup"><span data-stu-id="da6ed-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="da6ed-126">Persyaratan dibuat sesuai dengan kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="da6ed-127">**Tambahkan sumber daya bernama ke tim tanpa menggunakan kapasitas sumber daya**-di bidang **sumber daya dapat dipesan**, pilih sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="da6ed-128">Kemudian pilih periode, dan pilih metode alokasi **Tidak ada**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="da6ed-129">Sumber daya ditambahkan ke tim, namun kapasitas sumber daya tidak dihabiskan melalui pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="da6ed-130">Pesan anggota tim untuk memenuhi persyaratan sumber daya untuk sumber daya generik</span><span class="sxs-lookup"><span data-stu-id="da6ed-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="da6ed-131">Dalam PSA, Anda dapat memesan sumber daya generik pada tim proyek, dan dapat menentukan peran, kapasitas yang diperlukan, dan bagaimana kapasitas tersebut didistribusikan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="da6ed-132">Pada persyaratan sumber daya, Anda dapat menentukan atribut yang terkait dengan sumber daya generik .</span><span class="sxs-lookup"><span data-stu-id="da6ed-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="da6ed-133">Atribut ini mencakup keterampilan yang diperlukan, unit organisasi yang disukai, dan sumber daya pilihan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="da6ed-134">Ikuti langkah berikut untuk menentukan keterampilan yang diperlukan pada sumber daya generik untuk pengembang.</span><span class="sxs-lookup"><span data-stu-id="da6ed-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="da6ed-135">Pada halaman **proyek**, pada tab **tim**, pilih **baru** untuk memesan sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Sumber daya generik yang dipesan pada tim](media/Resource-Management-image9.png)

2. <span data-ttu-id="da6ed-137">Di tampilan **semua anggota tim**, di kolom **persyaratan sumber daya**, pilih tautan untuk menambahkan keterampilan yang diperlukan untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Tautan persyaratan](media/Resource-Management-image10.png)

3. <span data-ttu-id="da6ed-139">Pada halaman **persyaratan sumber daya** yang muncul, di kisi **keahlian**, pilih elipsis (**...**) kemudian pilih **Tambah karakteristik kebutuhan baru** untuk menambahkan keterampilan yang diperlukan untuk pengembang Anda.</span><span class="sxs-lookup"><span data-stu-id="da6ed-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Perintah Tambahkan Karakteristik Persyaratan Baru](media/Resource-Management-image11.png)

4. <span data-ttu-id="da6ed-141">Di kotak dialog **buat cepat: karakteristik persyaratan** yang muncul, di bidang **karakteristik**, pilih keahlian yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="da6ed-142">Selanjutnya, di bidang **nilai peringkat**, pilih tingkat kemahiran untuk keahlian tersebut.</span><span class="sxs-lookup"><span data-stu-id="da6ed-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="da6ed-143">Terakhir, di bidang **persyaratan sumber daya**, atur persyaratan sumber daya sumber dari unit organisasi atau bahkan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="da6ed-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="da6ed-144">Setelah selesai, pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-144">When you've finished, select **Save**.</span></span>

    ![Kotak dialog buat cepat: karakteristik persyaratan](media/Resource-Management-image12.png)

5. <span data-ttu-id="da6ed-146">Pada halaman **persyaratan sumber daya**, pilih **Pesan** untuk memenuhi persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Tombol pesan di halaman persyaratan sumber daya](media/Resource-Management-image13.png)

    <span data-ttu-id="da6ed-148">Anda juga dapat memilih sumber daya generik di kisi **semua anggota tim**, lalu pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Tombol pesan di atas kisi semua anggota tim](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="da6ed-150">Dalam contoh ini, ada 40 jam yang diperlukan namun tidak ada jam Pemesanan aktual, karena sumber daya generik tidak memiliki Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="da6ed-151">Selain itu, tidak ada jam yang ditetapkan, karena sumber daya generik ditambahkan langsung ke tim.</span><span class="sxs-lookup"><span data-stu-id="da6ed-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="da6ed-152">Tidak ditambahkan menggunakan penetapan tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="da6ed-153">Pada halaman **asisten penjadwalan**, Anda dapat memfilter sumber daya yang tersedia berdasarkan persyaratan yang ditentukan pada persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="da6ed-154">Sumber daya diurutkan berdasarkan parameter pengurutan yang ditentukan di papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="da6ed-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Halaman Asisten Penjadwalan](media/Resource-Management-image15.png)

    <span data-ttu-id="da6ed-156">Berikut adalah beberapa filter yang sering digunakan:</span><span class="sxs-lookup"><span data-stu-id="da6ed-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="da6ed-157">**Karakteristik bersama dengan peringkat** -filter berdasarkan keterampilan, sertifikasi, dan kualitas sumber daya lainnya, selain peringkat kemahiran.</span><span class="sxs-lookup"><span data-stu-id="da6ed-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="da6ed-158">**Peran** – filter berdasarkan peran default yang ditetapkan ke sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="da6ed-159">**Unit organisasi** – memfilter sumber daya yang dapat dipesan berdasarkan unit organisasi yang ditetapkan untuknya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="da6ed-160">Jika Anda tidak puas dengan hasil pencarian persyaratan awal, Anda dapat mengubah kriteria filter.</span><span class="sxs-lookup"><span data-stu-id="da6ed-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="da6ed-161">Perluas panel **tampilan filter** di sebelah kiri, lalu pilih **pencarian** untuk menemukan sumber daya tambahan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Panel Tampilan Filter](media/Resource-Management-image16.png)

7. <span data-ttu-id="da6ed-163">Untuk mengubah cara pengurutan, **Urutkan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Perintah Urutkan](media/Resource-Management-image17.png)

8. <span data-ttu-id="da6ed-165">Pilih sumber daya sesuai permintaan yang ditentukan pada persyaratan, seperti ditunjukkan di bagian atas kisi.</span><span class="sxs-lookup"><span data-stu-id="da6ed-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="da6ed-166">Anda dapat menghapus pilihan sel di kisi dan membiarkan kapasitas sumber daya terbuka.</span><span class="sxs-lookup"><span data-stu-id="da6ed-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="da6ed-167">Hanya satu sumber daya setiap kalinya yang dapat dipilih sebagai dipesan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="da6ed-168">Pilih **Pesan** untuk memesan sumber daya yang dipilih dan biarkan papan jadwal terbuka, sehingga Anda dapat memilih sumber daya tambahan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="da6ed-169">Atau, pilih **Pesan & keluar** untuk memesan sumber daya yang dipilih dan tutup papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="da6ed-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Sumber Daya untuk dipesan](media/Resource-Management-image19.png)

    <span data-ttu-id="da6ed-171">Anda akan menerima pemberitahuan tentang jam dipesan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="da6ed-172">Indikator permintaan menunjukkan seberapa besar persyaratan Pemesanan terpenuhi dan berapa banyak yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="da6ed-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="da6ed-173">Anda juga dapat mengetahui jumlah kapasitas sumber daya yang dihabiskan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="da6ed-174">Pilih **Perluas** untuk melihat rincian lebih lanjut tentang Pemesanan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="da6ed-175">Kembali ke tampilan **semua anggota tim**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="da6ed-176">Di kisi, perhatikan bahwa sumber daya umum telah digantikan oleh sumber daya bernama, dan 40 jam terdaftar sebagai dipesan untuk sumber daya tersebut.</span><span class="sxs-lookup"><span data-stu-id="da6ed-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Diperbarui kisi semua anggota tim](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="da6ed-178">Tidak ada jam yang ditetapkan ditampilkan, karena mereka dipesan langsung pada tim.</span><span class="sxs-lookup"><span data-stu-id="da6ed-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="da6ed-179">Mereka tidak dipesan menggunakan penetapan tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="da6ed-180">Tetapkan sumber daya generik ke tugas dan buat persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="da6ed-181">Dalam PSA, Anda dapat membuat tugas, lalu menetapkan sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="da6ed-182">Dengan cara ini, permintaan sumber daya dapat diwakili oleh placeholder saat Anda memperkirakan jadwal dan angka keuangan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="da6ed-183">Selanjutnya Anda dapat membuat persyaratan sumber daya untuk sumber daya generik dan memenuhinya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="da6ed-184">Pada halaman **proyek**, pada tab **jadwal**, pilih **Tambah** untuk membuat tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Tugas Baru dibuat](media/Resource-Management-image21.png)

2. <span data-ttu-id="da6ed-186">Di bidang **sumber daya**, pilih simbol **pemilih sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="da6ed-187">Pemilih sumber daya muncul dan menampilkan anggota tim yang ada untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Pemilih sumber daya](media/Resource-Management-image22.png)

3. <span data-ttu-id="da6ed-189">Masukkan nama sumber daya generik baru, lalu pilih **buat**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Nama sumber daya generik baru yang dimasukkan](media/Resource-Management-image23.png)

4. <span data-ttu-id="da6ed-191">Di kotak dialog **buat cepat: anggota tim proyek** yang muncul, di bidang **Peran**, pilih peran untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="da6ed-192">Di bidang **unit sumber daya**, pilih unit organisasi untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="da6ed-193">Kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-193">Then select **Save**.</span></span>

    ![Kotak dialog buat cepat: anggota tim proyek](media/Resource-Management-image24.png)

    <span data-ttu-id="da6ed-195">Anggota tim generik kini ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-195">The generic team member is now assigned to the task.</span></span>

    ![Anggota tim generik ditetapkan ke tugas](media/Resource-Management-image25.png)

    <span data-ttu-id="da6ed-197">Pada tab **tim**, Anda akan melihat anggota tim generik baru.</span><span class="sxs-lookup"><span data-stu-id="da6ed-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="da6ed-198">Perhatikan bahwa hanya jam yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="da6ed-199">Jam tersebut adalah jumlah semua tugas yang ditetapkan ke anggota tim generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="da6ed-200">Anggota tim generik belum memerlukan persyaratan jam atau sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Anggota tim persyaratan pada tab tim](media/Resource-Management-image26.png)

5. <span data-ttu-id="da6ed-202">Anda sekarang dapat menetapkan anggota tim umum untuk tugas lain menggunakan pemilih sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Anggota tim persyaratan dalam pemilih sumber daya](media/Resource-Management-image27.png)

    <span data-ttu-id="da6ed-204">Setelah selesai menetapkan sumber daya generik untuk tugas, Anda dapat membuat persyaratan sumber daya untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="da6ed-205">Pada tab **tim**, pilih sumber daya generik, lalu pilih **buat persyaratan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Perintah Buat Persyaratan](media/Resource-Management-image28.png)

    <span data-ttu-id="da6ed-207">Bila persyaratan dibuat, anggota tim generik akan memiliki jam wajib dan tautan untuk persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Tautan Persyaratan Sumber Daya](media/Resource-Management-image29.png)

    <span data-ttu-id="da6ed-209">Setelah Anda memesan sumber daya bernama, sumber daya generik dihapus dari tim dan digantikan dengan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="da6ed-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Sumber daya generik digantikan oleh sumber daya bernama](media/Resource-Management-image30.png)

    <span data-ttu-id="da6ed-211">Pada tab **jadwal**, tugas sumber daya generik akan dihapus dan digantikan oleh sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="da6ed-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Pada tab jadwal, tugas sumber daya generik digantikan oleh sumber daya bernama](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="da6ed-213">Perilaku ini hanya terjadi bila sumber daya bernama sepenuhnya dipesan untuk persyaratan sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="da6ed-214">Bila sumber daya bernama sebagian menggantikan persyaratan sumber daya generik atau beberapa sumber daya bernama menggantikan persyaratan sumber daya generik, sumber daya generik tetap ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="da6ed-215">Dalam ilustrasi berikut, tugas 80 jam telah direncanakan selama lima hari (16 jam per hari selama lima hari) dan ditetapkan ke sumber daya generik yang dinamai **fungsional**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-jam, tugas lima hari yang ditetapkan ke sumber daya generik fungsional](media/Resource-Management-image32.png)

    <span data-ttu-id="da6ed-217">Bila Anda membuat persyaratan, maka untuk 80 jam selama lima hari.</span><span class="sxs-lookup"><span data-stu-id="da6ed-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Persyaratan dihasilkan untuk 80 jam selama lima hari](media/Resource-Management-image33.png)

    <span data-ttu-id="da6ed-219">Karena sumber daya yang tersedia hanya berfungsi selama delapan jam per hari, dua sumber daya diperlukan untuk memenuhi persyaratan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Sumber daya kedua](media/Resource-Management-image35.png)

    <span data-ttu-id="da6ed-221">Pada tab **tim**, Anda sekarang dapat melihat bahwa sumber daya generik tidak memiliki jam yang diperlukan, namun jam yang ditetapkan tetap ditampilkan bersama dengan dua sumber daya bernama yang membentuk pemenuhan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dua sumber daya bernama di tab tim](media/Resource-Management-image36.png)

    <span data-ttu-id="da6ed-223">Pada tab **jadwal**, sumber daya generik tetap ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Sumber daya generik pada tab jadwal](media/Resource-Management-image37.png)

<span data-ttu-id="da6ed-225">PSA tidak menetapkan sumber daya ke tugas, karena perilaku tersebut akan menghasilkan jadwal yang kurang dapat diprediksi.</span><span class="sxs-lookup"><span data-stu-id="da6ed-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="da6ed-226">Dalam contoh sederhana ini, mudah untuk membagi jam secara merata antara dua sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="da6ed-227">Namun, dalam skenario yang lebih kompleks yang melibatkan beberapa tugas dan beberapa sumber daya, PSA harus membuat asumsi tentang cara mengalokasikan Pemesanan yang diterima untuk beberapa sumber daya di beberapa tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="da6ed-228">Oleh karena itu, dalam skenario ini, manajer proyek bertanggung jawab untuk menguraikan beberapa Pemesanan dan menetapkannya sesuai kebutuhan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="da6ed-229">Untuk mengalokasikan Pemesanan, manajer proyek menetapkan tugas dari sumber daya generik ke sumber daya bernama dan kemudian menggunakan tampilan **rekonsiliasi** untuk memastikan bahwa alokasi berfungsi dengan pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="da6ed-230">Edit Persyaratan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-230">Edit a resource requirement</span></span>

<span data-ttu-id="da6ed-231">Setelah persyaratan sumber daya dibuat, manajer proyek atau manajer sumber daya mungkin ingin mengedit rincian untuk menyempurnakan kriteria pencarian bila papan jadwal digunakan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="da6ed-232">Untuk mengedit persyaratan sumber daya, ikuti langkah-langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="da6ed-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="da6ed-233">Pada halaman **proyek**, pada tab **tim**, pilih tautan ke persyaratan apa pun di sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="da6ed-234">Di halaman **persyaratan sumber daya** yang muncul, Anda dapat memperbarui beberapa atribut.</span><span class="sxs-lookup"><span data-stu-id="da6ed-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="da6ed-235">Berikut adalah beberapa contoh:</span><span class="sxs-lookup"><span data-stu-id="da6ed-235">Here are some examples:</span></span>

    - <span data-ttu-id="da6ed-236">Nama</span><span class="sxs-lookup"><span data-stu-id="da6ed-236">Name</span></span>
    - <span data-ttu-id="da6ed-237">Tanggal Mulai</span><span class="sxs-lookup"><span data-stu-id="da6ed-237">From Date</span></span>
    - <span data-ttu-id="da6ed-238">Tanggal Selesai</span><span class="sxs-lookup"><span data-stu-id="da6ed-238">To Date</span></span>
    - <span data-ttu-id="da6ed-239">Durasi</span><span class="sxs-lookup"><span data-stu-id="da6ed-239">Duration</span></span>
    - <span data-ttu-id="da6ed-240">Jenis Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-240">Resource Type</span></span>

<span data-ttu-id="da6ed-241">Pada halaman **persyaratan sumber daya**, manajer proyek atau manajer sumber daya juga dapat menentukan informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="da6ed-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="da6ed-242">Keterampilan</span><span class="sxs-lookup"><span data-stu-id="da6ed-242">Skills</span></span>
- <span data-ttu-id="da6ed-243">Peran</span><span class="sxs-lookup"><span data-stu-id="da6ed-243">Roles</span></span>
- <span data-ttu-id="da6ed-244">Preferensi Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-244">Resource preferences</span></span>
- <span data-ttu-id="da6ed-245">Unit Organisasi Pilihan</span><span class="sxs-lookup"><span data-stu-id="da6ed-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="da6ed-246">Perbarui Pemesanan sumber daya setelah mereka dipesan pada proyek</span><span class="sxs-lookup"><span data-stu-id="da6ed-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="da6ed-247">Setelah menambahkan sumber daya generik atau bernama ke tim proyek, Anda dapat mengubah Pemesanan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="da6ed-248">Pada halaman **proyek**, pada tab **tim**, pilih anggota tim, lalu pilih **Kelola Pemesanan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Papan jadwal dibuka untuk anggota tim yang dipilih](media/Resource-Management-image40.png)

    <span data-ttu-id="da6ed-250">Papan jadwal akan ditampilkan dan menampilkan Pemesanan anggota tim proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="da6ed-251">Perluas rekaman anggota tim untuk melihat jam yang telah dipesan terhadap proyek ini dan proyek lainnya yang memakan kapasitas anggota tim.</span><span class="sxs-lookup"><span data-stu-id="da6ed-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="da6ed-252">Pilih dan tarik Pemesanan untuk memperluas atau mempersingkat.</span><span class="sxs-lookup"><span data-stu-id="da6ed-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="da6ed-253">Kotak dialog **buat Pemesanan sumber daya** muncul yang memungkinkan Anda menyesuaikan Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Kotak dialog Buat Pemesanan Sumber Daya](media/Resource-Management-image41.png)

3. <span data-ttu-id="da6ed-255">Klik kanan Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-255">Right-click the booking.</span></span> <span data-ttu-id="da6ed-256">Anda kemudian dapat menggunakan menu pintasan untuk menyelesaikan tindakan berikut:</span><span class="sxs-lookup"><span data-stu-id="da6ed-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="da6ed-257">Ubah Status Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-257">Change the booking status.</span></span>
    - <span data-ttu-id="da6ed-258">Edit Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-258">Edit the booking.</span></span>
    - <span data-ttu-id="da6ed-259">Gantikan sumber daya pada tim proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="da6ed-260">Ubah Status Pemesanan</span><span class="sxs-lookup"><span data-stu-id="da6ed-260">Change the booking status</span></span>

<span data-ttu-id="da6ed-261">Anda dapat mengubah status pemesanan default atau kustom.</span><span class="sxs-lookup"><span data-stu-id="da6ed-261">You can change any default or custom booking status.</span></span>

![Perintah Ubah Status](media/Resource-Management-image42.png)

<span data-ttu-id="da6ed-263">Status berikut termasuk dalam PSA:</span><span class="sxs-lookup"><span data-stu-id="da6ed-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="da6ed-264">**Dibatalkan** -status ini membatalkan pemesanan sumber daya dan membebaskan kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="da6ed-265">**Pemesanan definitif** -status ini mengkonsumsi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="da6ed-266">Pemesanan biasanya memiliki status ini saat Anda membuka **Kelola Pemesanan** dari kisi **semua anggota tim** di halaman **proyek**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="da6ed-267">**Pemesanan tentatif** – status ini menambahkan sumber daya ke tim namun tidak mengkonsumsi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="da6ed-268">Ini menunjukkan bahwa sumber daya telah dicadangkan untuk pekerjaan potensial namun masih memiliki kapasitas jika diperlukan pada pekerjaan lain.</span><span class="sxs-lookup"><span data-stu-id="da6ed-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="da6ed-269">Di tampilan ketersediaan sumber daya secara keseluruhan, Pemesanan tentatif memiliki status yang berbeda dengan Pemesanan definitif.</span><span class="sxs-lookup"><span data-stu-id="da6ed-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="da6ed-270">**Diusulkan** -status ini mewakili usulan manajer sumber daya atau manajer proyek untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="da6ed-271">Proposal tidak mengkonsumsi kapasitas sumber daya, dan sumber daya tidak ditambahkan ke tim proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="da6ed-272">Untuk pemesanan definitif sumber daya pada tim, manajer proyek harus menerima proposal.</span><span class="sxs-lookup"><span data-stu-id="da6ed-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="da6ed-273">Kirim permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-273">Submit resource requests</span></span>

<span data-ttu-id="da6ed-274">Permintaan sumber daya digunakan untuk melakukan permintaan (persyaratan sumber daya) yang harus dipenuhi oleh Manajer sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="da6ed-275">Untuk sumber daya generik yang sudah ada di tim, Anda dapat mengajukan permintaan sumber daya secara langsung.</span><span class="sxs-lookup"><span data-stu-id="da6ed-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="da6ed-276">Permintaan sumber daya dapat dipenuhi dengan dua cara:</span><span class="sxs-lookup"><span data-stu-id="da6ed-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="da6ed-277">Manajer sumber daya langsung memenuhi permintaan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="da6ed-278">Dalam kasus ini, sumber daya umum digantikan dengan pemesanan definitif yang memiliki sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="da6ed-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="da6ed-279">Manajer sumber daya mengusulkan sumber daya untuk manajer proyek, dan manajer proyek menyetujui atau menolak sumber daya yang diusulkan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="da6ed-280">Pemenuhan langsung permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="da6ed-281">Bila persyaratan sumber daya dihasilkan, manajer proyek dapat mengajukan permintaan sumber daya umum dengan memilih sumber daya, lalu memilih **Ajukan permintaan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Tombol Ajukan permintaan](media/Resource-Management-image45.png)

<span data-ttu-id="da6ed-283">Komentar tentang sumber daya dapat diberikan kepada manajer sumber daya yang memenuhi permintaan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="da6ed-284">Setelah permintaan diajukan, bidang **status** untuk anggota tim akan diubah ke **Diajukan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Memasukkan Komentar opsional](media/Resource-Management-image46.png)

<span data-ttu-id="da6ed-286">Ketika manajer sumber daya memenuhi permintaan, anggota tim generik digantikan dengan sumber daya bernama di kisi **semua anggota tim**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Anggota tim generik digantikan oleh sumber daya bernama di kisi semua anggota tim](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="da6ed-288">Menggunakan proposal sumber daya untuk permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="da6ed-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="da6ed-289">Alih-alih langsung memesan sumber daya pada permintaan sumber daya, manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="da6ed-290">Manajer sumber daya dapat menggunakan pilihan ini bila pencocokan yang tepat dengan persyaratan tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="da6ed-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="da6ed-291">Bila manajer sumber daya mengusulkan suatu sumber daya, manajer proyek melihat bahwa bidang **status** untuk anggota tim generik diubah ke **perlu ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Status anggota tim generik diubah ke perlu ditinjau](media/Resource-Management-image48.png)

<span data-ttu-id="da6ed-293">Untuk melihat sumber daya yang diusulkan bersama dengan visualisasi dari efek dari Pemesanan proposal, klik dua kali anggota tim yang memiliki status **Perlu ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="da6ed-294">Kemudian pilih tab **sumber daya yang diusulkan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-294">Then select the **Proposed Resources** tab.</span></span>

![Tab Sumber Daya yang Diusulkan](media/Resource-Management-image49.png)

<span data-ttu-id="da6ed-296">Pilih **terima semua proposal** untuk menerima semua sumber daya yang diusulkan atau **Tolak semua proposal** untuk menolaknya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="da6ed-297">Jika Anda menerima sumber daya yang diusulkan, mereka dipesan secara definitif pada proyek sebagai anggota tim dan mengganti sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="da6ed-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="da6ed-298">Anda harus menerima atau menolak semua sumber daya yang diusulkan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="da6ed-299">Anda tidak dapat menerima atau menolaknya secara parsial.</span><span class="sxs-lookup"><span data-stu-id="da6ed-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="da6ed-300">Gantikan sumber daya pada tim proyek</span><span class="sxs-lookup"><span data-stu-id="da6ed-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="da6ed-301">Terkadang, manajer proyek harus mengganti anggota tim yang dipesan pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="da6ed-302">Pada halaman **proyek**, pada tab **tim**, pilih sumber daya yang memerlukan pengganti, lalu pilih **Kelola Pemesanan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="da6ed-303">Perluas sumber daya untuk melihat proyek yang ditetapkan untuknya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Sumber daya diperluas untuk menampilkan proyek yang ditugaskan](media/Resource-Management-image50.png)

3. <span data-ttu-id="da6ed-305">Klik kanan proyek, lalu pilih **ganti sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="da6ed-306">Jika Anda mengetahui sumber daya yang ingin Anda ganti untuk sumber daya saat ini, pilih atau ketik nama, lalu pilih **tetapkan ulang**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Menentukan sumber daya pengganti](media/Resource-Management-image51.png)

    <span data-ttu-id="da6ed-308">Atau, ikuti langkah berikut untuk mencari sumber daya:</span><span class="sxs-lookup"><span data-stu-id="da6ed-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="da6ed-309">Pilih **Cari Pengganti**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-309">Select **Find Substitution**.</span></span>

        ![Mencari sumber daya pengganti](media/Resource-Management-image52.png)

        <span data-ttu-id="da6ed-311">Asisten jadwal akan menampilkan daftar pengganti yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="da6ed-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="da6ed-312">Di asisten jadwal, Anda dapat memfilter lebih lanjut sumber daya yang tersedia untuk menemukan pengganti yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="da6ed-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Daftar pengganti yang tersedia](media/Resource-Management-image53.png)

    2. <span data-ttu-id="da6ed-314">Untuk mengganti sumber daya, pilih sumber daya yang diinginkan, lalu pilih **Ganti**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Sumber Daya Pengganti dipilih](media/Resource-Management-image54.png)

    <span data-ttu-id="da6ed-316">Pemesanan dan penugasan digantikan dengan sumber daya baru.</span><span class="sxs-lookup"><span data-stu-id="da6ed-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Pemesanan dan penugasan digantikan dengan sumber daya baru](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="da6ed-318">Rekonsiliasi pemesanan dan penugasan Anggota tim</span><span class="sxs-lookup"><span data-stu-id="da6ed-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="da6ed-319">Untuk anggota tim, Pemesanan dan tugas secara longgar digabungkan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="da6ed-320">Dengan kata lain, sumber daya dapat memiliki tugas namun tidak ada pemesanan, atau mereka dapat memiliki Pemesanan namun tidak ada tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="da6ed-321">Idealnya, Pemesanan dan penetapan harus selaras, sehingga sumber daya memiliki kapasitas untuk melakukan tugas tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="da6ed-322">Namun, Pemesanan mungkin didasarkan pada ketersediaan, dan waktu tugas dapat berubah saat proyek berlanjut.</span><span class="sxs-lookup"><span data-stu-id="da6ed-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="da6ed-323">Oleh karena itu, pasangan longgar Pemesanan dan penugasan memberikan fleksibilitas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="da6ed-324">PSA memiliki tab **rekonsiliasi** yang memungkinkan manajer proyek merekonsiliasi Pemesanan anggota tim dan tugas mereka untuk tim proyek.</span><span class="sxs-lookup"><span data-stu-id="da6ed-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Tab Rekonsiliasi](media/Resource-Management-image56.png)

<span data-ttu-id="da6ed-326">Tab **rekonsiliasi** menampilkan Pemesanan dan tugas hingga tingkat penetapan tugas individual untuk setiap anggota tim.</span><span class="sxs-lookup"><span data-stu-id="da6ed-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="da6ed-327">Ini menunjukkan jam di sel yang menunjukkan periode waktu dari bulan ke hari.</span><span class="sxs-lookup"><span data-stu-id="da6ed-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="da6ed-328">Tab juga menampilkan Total keseluruhan bersih untuk proyek, bersama dengan kolom total.</span><span class="sxs-lookup"><span data-stu-id="da6ed-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="da6ed-329">Untuk setiap sumber daya, tab akan menghitung perbedaan antara Pemesanan anggota tim dan Rollup tugas anggota tim.</span><span class="sxs-lookup"><span data-stu-id="da6ed-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="da6ed-330">Idealnya, perbedaan ini harus 0 (nol).</span><span class="sxs-lookup"><span data-stu-id="da6ed-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="da6ed-331">Dengan kata lain, tidak ada perbedaan antara Pemesanan dan tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="da6ed-332">Perbedaan berwarna dan berarsir untuk menarik perhatian ke dua kondisi:</span><span class="sxs-lookup"><span data-stu-id="da6ed-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="da6ed-333">**Kekurangan Pemesanan** – kekurangan Pemesanan terjadi bila sumber daya memiliki lebih banyak tugas daripada Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="da6ed-334">Karena kapasitas ini belum dicadangkan, manajer proyek mungkin ingin memperbaiki kondisi ini dengan memperluas Pemesanan sumber daya untuk mengatasi defisit.</span><span class="sxs-lookup"><span data-stu-id="da6ed-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="da6ed-335">**Pemesanan berlebih** – kelebihan Pemesanan terjadi saat sumber daya telah dipesan ke proyek namun belum ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="da6ed-336">Kondisi ini mungkin dapat diterima dalam kasus saat sumber daya dipesan ke proyek sebelum penetapan tugas terjadi.</span><span class="sxs-lookup"><span data-stu-id="da6ed-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="da6ed-337">Namun, dalam kasus lain, sumber daya tidak direncanakan untuk ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="da6ed-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="da6ed-338">Dalam kasus ini, manajer proyek harus mempertimbangkan membatalkan pemesanan sumber daya, sehingga kapasitas dapat digunakan untuk proyek lain.</span><span class="sxs-lookup"><span data-stu-id="da6ed-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="da6ed-339">Dalam kasus tertentu, bila Anda melihat waktu pada tingkat yang lebih tinggi daripada tingkat hari (misalnya, tingkat bulan), Anda mungkin melihat perbedaan bersih nol untuk sumber daya (dengan kata lain, Pemesanan = penetapan).</span><span class="sxs-lookup"><span data-stu-id="da6ed-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="da6ed-340">Namun, jika Anda melihat waktu di tingkat minggu, Anda mungkin melihat bahwa ada tugas yang dilakukan nol jam dan Pemesanan 40 jam di minggu pertama, namun penetapan 40 jam dan Pemesanan dalam nol jam di minggu kedua.</span><span class="sxs-lookup"><span data-stu-id="da6ed-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="da6ed-341">Secara keseluruhan, Pemesanan dan penugasan akan didamaikan, namun berbeda dari satu minggu ke hari berikutnya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="da6ed-342">Bila Anda melihat waktu di tingkat yang lebih tinggi, sel dalam tab **rekonsiliasi** memiliki indikator untuk menginformasikan bahwa ada perbedaan pada tingkat yang lebih rendah.</span><span class="sxs-lookup"><span data-stu-id="da6ed-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="da6ed-343">Dengan mengklik dua kali di sel, Anda dapat memperbesar untuk melihat perbedaannya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="da6ed-344">Anda kemudian dapat klik kanan untuk memperkecil. Dengan memilih sumber daya, lalu menggunakan kontrol **perbedaan berikutnya** pada Toolbar kisi, Anda dapat membuka perbedaan berikutnya antara Pemesanan dan tugas untuk sumber daya tersebut.</span><span class="sxs-lookup"><span data-stu-id="da6ed-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="da6ed-345">Selanjutnya Anda dapat menggunakan kontrol **perbedaan sebelumnya** untuk kembali.</span><span class="sxs-lookup"><span data-stu-id="da6ed-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="da6ed-346">Anda juga dapat menonaktifkan indikator perbedaan dan perilaku navigasi dalam **pengaturan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Indikator perbedaan](media/Resource-Management-image57.png)

<span data-ttu-id="da6ed-348">Jika Anda memiliki penetapan tugas untuk sumber daya, namun tidak ada pemesanan, pada halaman **proyek**, pada tab **rekonsiliasi**, pilih kekurangan Pemesanan, lalu pilih **Perluas Pemesanan**.</span><span class="sxs-lookup"><span data-stu-id="da6ed-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="da6ed-349">Kotak dialog **Perluas Pemesanan** muncul dan menunjukkan Pemesanan yang diperlukan untuk mengatasi kekurangan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="da6ed-350">Juga menampilkan Pemesanan sumber daya yang ada di seluruh proyek atau entitas yang dapat dijadwalkan lainnya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="da6ed-351">Jika Anda memilih **OK** untuk membuat pemesanan untuk sumber daya, terlepas dari ketersediaan sumber daya tersebut, Anda dapat menyebabkan pemesanan berlebihan.</span><span class="sxs-lookup"><span data-stu-id="da6ed-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Kotak dialog Perluas Pemesanan](media/Resource-Management-image58.png)

<span data-ttu-id="da6ed-353">Manajer proyek atau manajer sumber daya kemudian dapat menggunakan papan jadwal untuk mengelola setiap situasi dengan sumber daya yang dipesan berlebihan di luar kapasitasnya.</span><span class="sxs-lookup"><span data-stu-id="da6ed-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]