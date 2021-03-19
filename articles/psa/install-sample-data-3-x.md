---
title: Penginstalan data sampel
description: Aplikasi topik menyediakan informasi tentang menginstal data sampel di Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 377e50fc5772c4dc146ccee098bf2806bbc8c6b7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275092"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="498af-103">Instalasi data sampel untuk aplikasi Project Service</span><span class="sxs-lookup"><span data-stu-id="498af-103">Sample data installation for the Project Service application</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="498af-104">Untuk membantu Anda membangun lingkungan demo sendiri, Microsoft memberikan paket data sampel dapat diunduh yang menampilkan kemampuan aplikasi Anda.</span><span class="sxs-lookup"><span data-stu-id="498af-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="498af-105">Ada dua jenis paket data sampel:</span><span class="sxs-lookup"><span data-stu-id="498af-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="498af-106">Data konfigurasi/referensi</span><span class="sxs-lookup"><span data-stu-id="498af-106">reference/setup data</span></span>
- <span data-ttu-id="498af-107">Data demo (data referensi/konfigurasi dan transaksi seperti perintah kerja dan proyek)</span><span class="sxs-lookup"><span data-stu-id="498af-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="498af-108">Paket data **referensi** sampel dapat diunduh dalam tiga paket berbeda, sehingga Anda dapat menginstal data hanya untuk project service, atau hanya untuk Field Service, atau Anda dapat menginstal data sampel untuk kedua aplikasi sekaligus.</span><span class="sxs-lookup"><span data-stu-id="498af-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="498af-109">Paket Data konfigurasi/referensi sampel adalah:</span><span class="sxs-lookup"><span data-stu-id="498af-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="498af-110">**V902PSMasterData** - Project Service versi 3.x saja</span><span class="sxs-lookup"><span data-stu-id="498af-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="498af-111">**V902FSMasterData** - Field Service versi 8.x saja</span><span class="sxs-lookup"><span data-stu-id="498af-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="498af-112">**V902FPSMasterData** - Field Service 8.x dan Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="498af-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="498af-113">Paket data **demo** terbaru adalah:</span><span class="sxs-lookup"><span data-stu-id="498af-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="498af-114">**FPSDemoData** - Field Service 8.x dan Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="498af-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="498af-115">Petunjuk penginstalan sedikit berbeda dalam hal pengguna harus membuat dan mengkonfigurasikan bagian namun lainnya adalah sama seperti [**posting blog**](https://aka.ms/fpsdemodatablog)sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="498af-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="498af-116">Paket ini memiliki rangkaian data demo yang dikurangi dan memerlukan sekitar 3 jam untuk menginstal.</span><span class="sxs-lookup"><span data-stu-id="498af-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="498af-117">Paket data sampel ini tersedia dalam bahasa Inggris saja.</span><span class="sxs-lookup"><span data-stu-id="498af-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="498af-118">**Tidak ada cara untuk menghapus instalasi data sampel.**</span><span class="sxs-lookup"><span data-stu-id="498af-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="498af-119">Anda seharusnya hanya menginstal paket ini pada demonstrasi, evaluasi, pelatihan, dan menguji sistem.</span><span class="sxs-lookup"><span data-stu-id="498af-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="498af-120">Juga perhatikan bahwa menginstal paket individual, dan kemudian menginstal paket individual lainnya, tidak didukung.</span><span class="sxs-lookup"><span data-stu-id="498af-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="498af-121">(Dengan kata lain, Anda tidak dapat menginstal **FSMasterData** diikuti **PSMasterData**, atau sebaliknya.) Jika Anda merasa perlu data sampel untuk kedua aplikasi di setiap titik di masa mendatang, Anda harus menginstal paket **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="498af-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="498af-122">Saat Anda menginstal salah satu paket data sampel, proses instalasi melakukan tindakan berikut:</span><span class="sxs-lookup"><span data-stu-id="498af-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="498af-123">Membuat atau menetapkan parameter default untuk menggunakan project service, Field Service, atau kedua aplikasi (jika ada).</span><span class="sxs-lookup"><span data-stu-id="498af-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="498af-124">Impor sampel data untuk aplikasi, seperti sumber daya yang dapat dipesan, peran khusus aplikasi, penjualan dan daftar harga biaya, unit organisasi, rekaman proses penjualan, dan entitas lain untuk menunjukkan kemampuan utama.</span><span class="sxs-lookup"><span data-stu-id="498af-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="498af-125">Dengan paket **data demo**, Anda mendapatkan data transaksi di atas dan tambahan seperti perintah kerja dan proyek.</span><span class="sxs-lookup"><span data-stu-id="498af-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="498af-126">Ingin mengetahui kemampuan yang dapat Anda demonstrasikan dengan data sampel?</span><span class="sxs-lookup"><span data-stu-id="498af-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="498af-127">Lihat skenario fiktif Fabrikam Robotics dalam [catatan teknis](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="498af-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="498af-128">Jika Anda memiliki pertanyaan tentang cara menginstal paket data sampel ini, [kirim email di fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="498af-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="498af-129">Persyaratan</span><span class="sxs-lookup"><span data-stu-id="498af-129">Requirements</span></span>

<span data-ttu-id="498af-130">Protokol penginstalan mengasumsikan berikut tentang target instans (organisasi):</span><span class="sxs-lookup"><span data-stu-id="498af-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="498af-131">Bahasa dasar adalah bahasa Inggris dan mata uang dasar dolar AS (USD,$).</span><span class="sxs-lookup"><span data-stu-id="498af-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="498af-132">Organisasi belum memiliki data project service atau Field Service, atau hanya memiliki data default barebone yang disertakan dengan setiap organisasi baru.</span><span class="sxs-lookup"><span data-stu-id="498af-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="498af-133">Versi benar aplikasi bisnis sudah diinstal:</span><span class="sxs-lookup"><span data-stu-id="498af-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="498af-134">**Untuk FPSDemoData atau v902FPSMasterData:** organisasi memiliki Field Service versi 8.x dan project service versi 3.x diinstal.</span><span class="sxs-lookup"><span data-stu-id="498af-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="498af-135">**Untuk v902PSMasterData:** organisasi memiliki Project Service versi 3.x diinstal.</span><span class="sxs-lookup"><span data-stu-id="498af-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="498af-136">**Untuk v902FSMasterData:** organisasi memiliki Field Service versi 8.x diinstal.</span><span class="sxs-lookup"><span data-stu-id="498af-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="498af-137">Jika Anda harus menginstal data sampel di atas project service dan Field Service uji coba atau lingkungan demo yang ada yang sudah memiliki data (tidak disarankan), Anda harus menunda pra-pemeriksaan keamanan yang dilakukan oleh Penginstal.</span><span class="sxs-lookup"><span data-stu-id="498af-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="498af-138">Untuk informasi lebih lanjut, lihat catatan teknis di bawah ini.</span><span class="sxs-lookup"><span data-stu-id="498af-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="498af-139">Siapkan penginstalan</span><span class="sxs-lookup"><span data-stu-id="498af-139">Prepare for installation</span></span>

<span data-ttu-id="498af-140">Anda harus Jalankan Penginstal di komputer dengan versi terbaru dari Windows (Windows 10 lebih disukai).</span><span class="sxs-lookup"><span data-stu-id="498af-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="498af-141">Anda harus merencanakan untuk komputer untuk tetap tersambung ke jaringan, dan untuk penginstalan untuk menjalankan hingga **satu jam** untuk **data konfigurasi/referensi**.</span><span class="sxs-lookup"><span data-stu-id="498af-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="498af-142">(Biasanya penginstalan waktu sekitar 30 menit untuk **FPSMasterData**, yang mencakup data sampel untuk kedua aplikasi.) Untuk **FPSDemoData**, penginstalan akan memerlukan sekitar **3 jam**.</span><span class="sxs-lookup"><span data-stu-id="498af-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="498af-143">Fungsi screensaver komputer harus dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="498af-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="498af-144">Jika tidak, sesi kredensial untuk penginstalan mungkin akan hilang saat screensaver aktif (kecuali Anda menjaga sesi selalu aktif).</span><span class="sxs-lookup"><span data-stu-id="498af-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="498af-145">![Tangkapan layar pengaturan screensaver, dengan screensaver dinonaktifkan](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="498af-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="498af-146">Unduh dan ekstrak</span><span class="sxs-lookup"><span data-stu-id="498af-146">Download and unpack</span></span>

<span data-ttu-id="498af-147">Penginstal data sampel Project Service dan Field Service didistribusikan sebagai eksekusi yang terekstrak.</span><span class="sxs-lookup"><span data-stu-id="498af-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="498af-148">Nama file mungkin berbeda tergantung pada paket data sampel, namun jika tidak langkah-langkah tetap sama tidak peduli paket yang Anda instal.</span><span class="sxs-lookup"><span data-stu-id="498af-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="498af-149">Setelah mengunduh paket, jalankan file .exe, dan kemudian terima persyaratan dan ketentuan untuk mengekstrak file terkompresi zip.</span><span class="sxs-lookup"><span data-stu-id="498af-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="498af-150">Kemudian Anda perlu mengekstrak isi file itu ke folder di komputer.</span><span class="sxs-lookup"><span data-stu-id="498af-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="498af-151">Tergantung pada sistem operasi dan pengaturan keamanan, Anda mungkin harus melakukan langkah-langkah berikut setelah membuka Kemasan zip file:</span><span class="sxs-lookup"><span data-stu-id="498af-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="498af-152">Cari dan klik kanan **FPSDemoData.dll** file dalam folder **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="498af-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="498af-153">Pilih **buka blokir**.</span><span class="sxs-lookup"><span data-stu-id="498af-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="498af-154">Pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="498af-154">Select **Apply**.</span></span>

4. <span data-ttu-id="498af-155">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="498af-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="498af-156">Membuat atau mengkonfigurasi pengguna</span><span class="sxs-lookup"><span data-stu-id="498af-156">Create or configure users</span></span>

<span data-ttu-id="498af-157">Paket **FPSDemoData** memerlukan enam pengguna sedangkan paket **FPSMasterData** memerlukan satu pengguna.</span><span class="sxs-lookup"><span data-stu-id="498af-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="498af-158">Lihat yang benar untuk paket data sampel Anda.</span><span class="sxs-lookup"><span data-stu-id="498af-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="498af-159">Membuat atau mengkonfigurasi pengguna - paket data referensi/konfigurasi</span><span class="sxs-lookup"><span data-stu-id="498af-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="498af-160">Paket **FPSMasterData** dirancang untuk menginstal dengan satu pengguna bernama Spencer Low dengan pengaturan yang diuraikan di sini.</span><span class="sxs-lookup"><span data-stu-id="498af-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="498af-161">Untuk menginstal paket dengan benar, Anda harus membuat (atau sementara ganti nama) pengguna di lingkungan Anda dengan konfigurasi data sampel masuk.</span><span class="sxs-lookup"><span data-stu-id="498af-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="498af-162">Untuk membuat atau mengkonfigurasi pengguna, buka **pengaturan** > **Keamanan** > **pengguna**, dan melakukan hal berikut:</span><span class="sxs-lookup"><span data-stu-id="498af-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="498af-163">Atur UserFullname = "Spencer Low" dengan nama pengguna "spencerl" (**huruf kecil**) untuk peran manajer proyek dan manajer praktik.</span><span class="sxs-lookup"><span data-stu-id="498af-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="498af-164">Pilih pengguna **Spencer Low**, lalu pilih **Kelola peran**.</span><span class="sxs-lookup"><span data-stu-id="498af-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="498af-165">Cari dan pilih peran **Administrator sistem**, dan kemudian pilih **OK** untuk memberikan hak penuh admin ke Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="498af-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="498af-166">Langkah ini diperlukan untuk memastikan bahwa sampel rekaman dibuat dengan kepemilikan pengguna yang benar dan oleh karena itu mengisi tampilan dengan benar.</span><span class="sxs-lookup"><span data-stu-id="498af-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="498af-167">Dari paket yang diunduh, Anda harus memperbarui file pemetaan data dengan alamat email dari konteks pengguna default.</span><span class="sxs-lookup"><span data-stu-id="498af-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="498af-168">Untuk melakukannya, buka **PkgFolder**, lalu Cari dan membuka **ImportUserMapFile.xml** file di Notepad (atau Visual Studio atau editor XML lainnya).</span><span class="sxs-lookup"><span data-stu-id="498af-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="498af-169">Atur bidang **DefaultUserToMapTo=** ke alamat email pengguna Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="498af-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="498af-170">Jika Anda tidak menggunakan Spencer Low dengan nama pengguna **spencerl**, Anda harus memperbarui file tambahan.</span><span class="sxs-lookup"><span data-stu-id="498af-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="498af-171">Buka **DemoDataPreImportConfig.xml** file, dan kemudian menemukan **userstocreateandconfigure** tag.</span><span class="sxs-lookup"><span data-stu-id="498af-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="498af-172">Perbarui tag **\<login\>** dengan nama pengguna Anda pengguna Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="498af-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="498af-173">Untuk detail tambahan, lihat [catatan teknis](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="498af-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="498af-174">Membuat atau mengkonfigurasi pengguna - paket data demo</span><span class="sxs-lookup"><span data-stu-id="498af-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="498af-175">Paket data demo memerlukan enam pengguna.</span><span class="sxs-lookup"><span data-stu-id="498af-175">The demo data package requires six users.</span></span> <span data-ttu-id="498af-176">Agar paket terinstal dengan benar, lakukan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="498af-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="498af-177">Buat atau sementara ganti nama pengguna yang ada sesuai konfigurasi data sampel masuk dengan membuka **pengaturan** > **keamanan** > **pengguna**.</span><span class="sxs-lookup"><span data-stu-id="498af-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="498af-178">Peran ini hanya diperlukan untuk demo berbasis persona.</span><span class="sxs-lookup"><span data-stu-id="498af-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="498af-179">Nama Lengkap Pengguna = "David So" sebagai teknisi Field Service</span><span class="sxs-lookup"><span data-stu-id="498af-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="498af-180">Fullname Pengguna = "Jamie Reding" sebagai operator Customer Service & Field Service</span><span class="sxs-lookup"><span data-stu-id="498af-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="498af-181">Fullname Pengguna = "Molly Clark" sebagai manajer akun</span><span class="sxs-lookup"><span data-stu-id="498af-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="498af-182">Fullname Pengguna = "Spencer Low" sebagai manajer praktik dan proyek</span><span class="sxs-lookup"><span data-stu-id="498af-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="498af-183">Fullname Pengguna = "Veronica Quek" sebagai anggota tim</span><span class="sxs-lookup"><span data-stu-id="498af-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="498af-184">Fullname Pengguna = "William Contoso"</span><span class="sxs-lookup"><span data-stu-id="498af-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="498af-185">Untuk tujuan impor data demo, tetapkan enam pengguna atas Peran Administrator sehingga sampel rekaman diimpor dengan benar.</span><span class="sxs-lookup"><span data-stu-id="498af-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="498af-186">Buka **PkgFolder** lalu Cari dan membuka **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="498af-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="498af-187">Perbarui bidang **baru=** ke alamat email pengguna yang terkait di sistem.</span><span class="sxs-lookup"><span data-stu-id="498af-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="498af-188">![Screenshot UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="498af-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="498af-189">Jika nama lengkap pengguna "Spencer Low" Anda memiliki ID pengguna yang berbeda dari **"spencerl"**, maka Anda harus memperbarui file tambahan.</span><span class="sxs-lookup"><span data-stu-id="498af-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="498af-190">Buka **DemoDataPreImportConfig.xml** file, dan kemudian menemukan **userstocreateandconfigure** tag.</span><span class="sxs-lookup"><span data-stu-id="498af-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="498af-191">Pembaruan tag **\<login\>** dengan loginId (peka huruf besar/kecil).</span><span class="sxs-lookup"><span data-stu-id="498af-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="498af-192">Kalender pengguna pertama (di **userstocreateandconfigure** tag) digunakan untuk mengisi jam kerja untuk semua sumber daya yang dapat dipesan pada impor data demo.</span><span class="sxs-lookup"><span data-stu-id="498af-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="498af-193">Navigasikan ke **pengaturan** > **keamanan** > **pengguna**, Cari pengguna "Spencer Low" Anda, dan buka pilihan "Jam kerja".</span><span class="sxs-lookup"><span data-stu-id="498af-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="498af-194">Edit jam kerja yang ada, dengan memilih pilihan **seluruh jadwal mingguan berulang dari mulai hingga berakhir**.</span><span class="sxs-lookup"><span data-stu-id="498af-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="498af-195">Pastikan **jam kerja ditetapkan untuk 8 pagi - 5 sore (9 jam), Senin hingga Jumat dan dengan zona waktu yang diatur ke waktu Pasifik (AS & Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="498af-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="498af-196">Hal ini diperlukan untuk memastikan bahwa proyek dan papan jadwal menunjukkan sebagaimana mestinya.</span><span class="sxs-lookup"><span data-stu-id="498af-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="498af-197">**Rekomendasi:** pertimbangkan untuk membuat cadangan organisasi Anda sekarang, jika Anda perlu Kembalikan ke titik awal jika terjadi kesalahan selama penginstalan data sampel.</span><span class="sxs-lookup"><span data-stu-id="498af-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="498af-198">Untuk informasi lebih lanjut, lihat [instans pencadangan dan pemulihan](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="498af-198">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="498af-199">Jalankan Package Deployer</span><span class="sxs-lookup"><span data-stu-id="498af-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="498af-200">Cari dan jalankan **PackageDeployer.exe** di folder **v902FPSMasterData** atau **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="498af-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="498af-201">Terima syarat dan ketentuan.</span><span class="sxs-lookup"><span data-stu-id="498af-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="498af-202">Pada jendela berikutnya:</span><span class="sxs-lookup"><span data-stu-id="498af-202">On the next window:</span></span>

   <span data-ttu-id="498af-203">a.</span><span class="sxs-lookup"><span data-stu-id="498af-203">a.</span></span> <span data-ttu-id="498af-204">Pilih Jenis Penyebaran **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="498af-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="498af-205">b.</span><span class="sxs-lookup"><span data-stu-id="498af-205">b.</span></span> <span data-ttu-id="498af-206">Gunakan pengguna dan sandi pengguna administrator sistem yang dikonfigurasi dalam "Buat atau konfigurasi pengguna" ("Spencer Low" dengan nama pengguna "spencerl").</span><span class="sxs-lookup"><span data-stu-id="498af-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="498af-207">c.</span><span class="sxs-lookup"><span data-stu-id="498af-207">c.</span></span> <span data-ttu-id="498af-208">Pastikan **tampilan daftar organisasi-organisasi yang tersedia** dipilih.</span><span class="sxs-lookup"><span data-stu-id="498af-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="498af-209">![tangkapan layar jendela Package Deployer dengan "Tampilan daftar organisasi yang tersedia" dipilih](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="498af-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="498af-210">Pilih organisasi yang akan menginstal data sampel.</span><span class="sxs-lookup"><span data-stu-id="498af-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="498af-211">Pilih **berikutnya** hingga Anda melihat **konfigurasi Data Demo** dialog.</span><span class="sxs-lookup"><span data-stu-id="498af-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="498af-212">![Ambil Screenshot dari jendela status Penginstal data demo](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="498af-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="498af-213">Sebelum melanjutkan, perhatikan bahwa menginstal data sampel dapat memerlukan waktu hingga satu jam (biasanya ~ 10 menit).</span><span class="sxs-lookup"><span data-stu-id="498af-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="498af-214">Anda harus memastikan bahwa komputer tetap hidup dan tersambung ke jaringan selama seluruh proses penginstalan, dan bahwa sesi Anda tetap aktif.</span><span class="sxs-lookup"><span data-stu-id="498af-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="498af-215">Saat Anda siap, klik **berikutnya** untuk memulai proses penginstalan data sampel.</span><span class="sxs-lookup"><span data-stu-id="498af-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="498af-216">Setelah data sampel dimuat, klik **selesai**.</span><span class="sxs-lookup"><span data-stu-id="498af-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="498af-217">Memverifikasi penginstalan data sampel</span><span class="sxs-lookup"><span data-stu-id="498af-217">Verify the sample data installation</span></span>

<span data-ttu-id="498af-218">Untuk memeriksa kewajaran, pastikan bahwa jumlah rekaman dan jenis entitas yang tercantum di skenario fiktif Fabrikam Robotics muncul sebagaimana mestinya.</span><span class="sxs-lookup"><span data-stu-id="498af-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="498af-219">Setelah data sampel benar-benar terbuka, masuk sebagai pengguna Spencer Low dan konfirmasikan berikut:</span><span class="sxs-lookup"><span data-stu-id="498af-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="498af-220">Jika aplikasi Project Service diinstal, buka **Project Service** > **Pengaturan** > **Daftar harga**.</span><span class="sxs-lookup"><span data-stu-id="498af-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="498af-221">Konfirmasikan bahwa tingkat tagihan dan tingkat biaya ada dengan mata uang yang sesuai untuk setiap negara/kawasan dalam himpunan data.</span><span class="sxs-lookup"><span data-stu-id="498af-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="498af-222">Jika aplikasi Project Service diinstal, buka **Universal Resource Scheduling** > **Pengaturan** > **Unit Organisasi**.</span><span class="sxs-lookup"><span data-stu-id="498af-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="498af-223">Konfirmasikan bahwa daftar harga biaya dengan mata uang yang sesuai telah dikaitkan dengan masing-masing unit organisasi (termasuk entri kota).</span><span class="sxs-lookup"><span data-stu-id="498af-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="498af-224">Jika ada yang hilang, Cari dan kaitkan daftar harga biaya yang benar.</span><span class="sxs-lookup"><span data-stu-id="498af-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="498af-225">Jika aplikasi Field Service diinstal, buka **Project Service** > **Pengaturan** > **Daftar harga**.</span><span class="sxs-lookup"><span data-stu-id="498af-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="498af-226">Konfirmasikan bahwa tingkat tagihan dan tingkat biaya sudah ada.</span><span class="sxs-lookup"><span data-stu-id="498af-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="498af-227">Buka **Field Service** > **Pengaturan** > **Daftar harga** dan periksa bahwa tingkat tagihan dan biaya tingkat ada, dengan mata uang yang sesuai, untuk setiap negara/kawasan dalam himpunan data.</span><span class="sxs-lookup"><span data-stu-id="498af-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="498af-228">![Screenshot dari daftar harga aktif](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="498af-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="498af-229">![Screenshot unit organisasional aktif](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="498af-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="498af-230">Catatan teknis</span><span class="sxs-lookup"><span data-stu-id="498af-230">Technical notes</span></span>

<span data-ttu-id="498af-231">Lihat di bawah ini untuk lebih banyak rincian teknis tentang penginstalan data ini.</span><span class="sxs-lookup"><span data-stu-id="498af-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="498af-232">Menginstal data sampel di atas data yang ada (tidak disarankan)</span><span class="sxs-lookup"><span data-stu-id="498af-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="498af-233">Jika Anda harus menginstal data sampel di atas project service dan Field Service uji coba atau lingkungan demo yang ada yang sudah memiliki data, Anda harus menunda pra-pemeriksaan keamanan yang dilakukan oleh Penginstal.</span><span class="sxs-lookup"><span data-stu-id="498af-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="498af-234">Untuk melakukannya, buka **PkgFolder** folder untuk menemukan dan membuka **DemoDataPreImportConfig.xml** file dengan Notepad (atau editor XML lainnya).</span><span class="sxs-lookup"><span data-stu-id="498af-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="498af-235">Cari nilai berikut, dan kemudian mengubah pengaturan dari benar menjadi salah:</span><span class="sxs-lookup"><span data-stu-id="498af-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="498af-236">Perubahan ini menyebabkan Penginstal untuk memotong beberapa pemeriksaan penting keamanan, termasuk:</span><span class="sxs-lookup"><span data-stu-id="498af-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="498af-237">Mengkonfirmasikan bahwa tidak lebih dari satu rekaman **Unit organisasi** aktif, dan kemudian mengganti nama ke **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="498af-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="498af-238">Mengkonfirmasikan bahwa ada tidak lebih dari satu rekaman **Template kerja** aktif.</span><span class="sxs-lookup"><span data-stu-id="498af-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="498af-239">Mengkonfirmasikan bahwa tidak lebih dari satu rekaman **Parameter Proyek** aktif, dan kemudian mengganti nama entri itu ke **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="498af-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="498af-240">Komponen konfigurasi</span><span class="sxs-lookup"><span data-stu-id="498af-240">Configuration components</span></span>

<span data-ttu-id="498af-241">Ada beberapa komponen konfigurasi lain di file pra-impor konfigurasi ini.</span><span class="sxs-lookup"><span data-stu-id="498af-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="498af-242">Untuk pengguna teknis, sebagian di antaranya mencakup:</span><span class="sxs-lookup"><span data-stu-id="498af-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="498af-243">**\<RequiredSolutions\>** menentukan penginstalan solusi prasyarat dan nomor versi mereka.</span><span class="sxs-lookup"><span data-stu-id="498af-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="498af-244">**\<InstallSampleData\>** mengontrol apakah data sampel siap pakai untuk aplikasi diinstal.</span><span class="sxs-lookup"><span data-stu-id="498af-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="498af-245">false - melewati penginstalan data built-in ini (yang dapat dilepaskan)</span><span class="sxs-lookup"><span data-stu-id="498af-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="498af-246">True - menginstal data built-in bersamaan dengan penginstalan sampel data PSA dan FS</span><span class="sxs-lookup"><span data-stu-id="498af-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="498af-247">**\<PreImportDataCollection\>** menentukan peta Data file rata dan rekaman terkait yang akan diimpor sebelum instalasi data sampel utama.</span><span class="sxs-lookup"><span data-stu-id="498af-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="498af-248">**\<EntitiesToEnableScheduling\>** menentukan entitas yang harus diaktifkan untuk Pemesanan di Microsoft Dynamics Scheduling (alias Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="498af-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="498af-249">**\<UsersToCreateAndConfigure\>** menentukan sumber daya dipesan yang akan dibuat (jika belum ada) sebelum mengeksekusi impor data sampel.</span><span class="sxs-lookup"><span data-stu-id="498af-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="498af-250">Perlu diketahui bahwa data sampel sistem sumber daya dapat dipesan sesuai dengan target rekaman sumber daya sistem dapat dipesan pada FullName dan login setiap sumber daya.</span><span class="sxs-lookup"><span data-stu-id="498af-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="498af-251">Oleh karena itu, TIDAK mungkin mengubah nama dalam file pra-konfigurasi ini kecuali jika Anda mengimpor data sampel ke sistem target menggunakan nama ini, lalu mengganti nama sumber daya dapat dipesan untuk nama yang Anda inginkan yang ditetapkan bersama rekaman pengguna yang diaktifkan, dan kemudian mengekspor data lagi untuk impor ke sistem tujuan akhir (memperbarui entri baru dan lama **ImportUserMapFile.xml** sesuai dengan itu).</span><span class="sxs-lookup"><span data-stu-id="498af-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="498af-252">**\<PluginsToDisable\>** menentukan plug-in item baris yang sangat diskrit yang harus dinonaktifkan selama impor data sampel dan kemudian diaktifkan lagi setelahnya.</span><span class="sxs-lookup"><span data-stu-id="498af-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="498af-253">Skenario fiktif Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="498af-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="498af-254">Paket data referensi sampel Field Service dan Project Service menginstal **solusi Data induk Produksi Fabrikam (v3.0.0.0)**, bersama sekitar 4000 rekaman dan sekitar 40 entitas yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="498af-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="498af-255">Paket data sampel terpisah untuk Field Service atau project service berisi subset sampel data **v902FPSMasterData** untukaplikasi tersebut.</span><span class="sxs-lookup"><span data-stu-id="498af-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="498af-256">Paket **Data Demo** menginstal **solusi Data Demo Fabrikam Manufacturing (v3.0.0.7)** dengan sekitar 22.000 rekaman di seluruh 148 entitas.</span><span class="sxs-lookup"><span data-stu-id="498af-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="498af-257">Perusahaan fiktif, Fabrikam Robotics, adalah produsen robot lini perakitan perangkat elektronik dan dikenal untuk kualitas produk, inovasi, dan layanan pelanggan yang kuat, termasuk perencanaan penginstalan, pelaksanaan dan Layanan pemeliharaan berkelanjutan.</span><span class="sxs-lookup"><span data-stu-id="498af-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="498af-258">Fabrikam berkantor pusat di Amerika Serikat (Fabrikam U.S.), dan memiliki operasi layanan berbasis proyek di Prancis, India, Inggris, dan Swiss.</span><span class="sxs-lookup"><span data-stu-id="498af-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="498af-259">Operasi Field Service terpusat di Amerika Serikat, sebagian besar di area Seattle raya.</span><span class="sxs-lookup"><span data-stu-id="498af-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="498af-260">Perusahaan berfokus pada memanfaatkan konektivitas Internet of Things (IoT) untuk memantau kinerja aset pelanggan dan memberikan layanan di lokasi yang semakin proaktif.</span><span class="sxs-lookup"><span data-stu-id="498af-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="498af-261">Ikhtisar tingkat tinggi data sampel adalah sebagai berikut:</span><span class="sxs-lookup"><span data-stu-id="498af-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="498af-262">Elemen data sampel Umum (termasuk untuk kedua aplikasi)</span><span class="sxs-lookup"><span data-stu-id="498af-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="498af-263">1 Pengguna</span><span class="sxs-lookup"><span data-stu-id="498af-263">1 user</span></span>

    - <span data-ttu-id="498af-264">71 Akun</span><span class="sxs-lookup"><span data-stu-id="498af-264">71 accounts</span></span>

    - <span data-ttu-id="498af-265">137 Kontak</span><span class="sxs-lookup"><span data-stu-id="498af-265">137 contacts</span></span>

    - <span data-ttu-id="498af-266">Berbagai jenis transaksi dan kategori</span><span class="sxs-lookup"><span data-stu-id="498af-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="498af-267">50 Produk dengan 1 daftar harga produk</span><span class="sxs-lookup"><span data-stu-id="498af-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="498af-268">14 Daftar Harga/Biaya</span><span class="sxs-lookup"><span data-stu-id="498af-268">14 price/cost lists</span></span>

    - <span data-ttu-id="498af-269">31 karakteristik (keahlian sumber daya) dalam 2 model peringkat dengan 3 tingkat (nilai peringkat)</span><span class="sxs-lookup"><span data-stu-id="498af-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="498af-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="498af-270">Project Service</span></span>

    - <span data-ttu-id="498af-271">8 Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="498af-271">8 organizational units</span></span>

    - <span data-ttu-id="498af-272">6 tingkat pemanfaatan khusus peran</span><span class="sxs-lookup"><span data-stu-id="498af-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="498af-273">2,8 k+ spesifikasi peran-harga</span><span class="sxs-lookup"><span data-stu-id="498af-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="498af-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="498af-274">Field Service</span></span>

    - <span data-ttu-id="498af-275">4 Wilayah</span><span class="sxs-lookup"><span data-stu-id="498af-275">4 territories</span></span>

    - <span data-ttu-id="498af-276">5 Jenis Perintah Kerja</span><span class="sxs-lookup"><span data-stu-id="498af-276">5 work order types</span></span>

    - <span data-ttu-id="498af-277">22 Aset Pelanggan</span><span class="sxs-lookup"><span data-stu-id="498af-277">22 customer assets</span></span>

    - <span data-ttu-id="498af-278">9 jenis insiden dengan berbagai karakteristik sumber daya terkait (9), Layanan (13) dan tugas Layanan (13)</span><span class="sxs-lookup"><span data-stu-id="498af-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="498af-279">Paket **Data Demo** menginstal sekitar 179 perintah kerja, 12 proyek, dan data transaksi terkait.</span><span class="sxs-lookup"><span data-stu-id="498af-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="498af-280">Ubah jam kerja untuk sumber daya sampel</span><span class="sxs-lookup"><span data-stu-id="498af-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="498af-281">Secara default, semua sumber daya yang dapat dipesan memiliki kalender 24 jam kerja.</span><span class="sxs-lookup"><span data-stu-id="498af-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="498af-282">Jika Anda ingin mengubah jam kerja untuk sampel sumber daya dapat dipesan, buka **Universal Resource Scheduling** > **Scheduling** > **Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="498af-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="498af-283">Pilih pengguna (misalnya, Spencer Low) dan Ubah jam kerja dari Spencer ke jam yang akan diterapkan ke beberapa pengguna.</span><span class="sxs-lookup"><span data-stu-id="498af-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="498af-284">Buka **Universal Resource Scheduling** > **Pengaturan** > **Template Jam Kerja** dan edit rekaman **Template Kerja Default**.</span><span class="sxs-lookup"><span data-stu-id="498af-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="498af-285">Di bidang **sumber daya Template**, pilih pengguna dengan jam kerja yang akan diterapkan ke sumber daya lainnya.</span><span class="sxs-lookup"><span data-stu-id="498af-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="498af-286">Buka **Universal Resource Scheduling** > **Penjadwalan** > **Sumber daya** > **Sumber daya Dapat Dipesan Aktif**.</span><span class="sxs-lookup"><span data-stu-id="498af-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="498af-287">Pilih sumber daya yang akan diubah, dan kemudian pilih **Atur kalender**.</span><span class="sxs-lookup"><span data-stu-id="498af-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="498af-288">Pada **Template kerja** daftar drop-down, pilih **Default jam kerja** template atau template lain dengan sumber daya template yang benar.</span><span class="sxs-lookup"><span data-stu-id="498af-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="498af-289">Saat Anda membuka papan jadwal, Anda dapat melihat bahwa sumber daya sekarang telah memperbarui jam kerja.</span><span class="sxs-lookup"><span data-stu-id="498af-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="498af-290">![Tangkapan layar Sumber Daya yang Dapat Dipesan Aktif](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="498af-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]