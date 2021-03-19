---
title: Mengelola daftar harga proyek pada kontrak proyek
description: Topik ini menyediakan informasi tentang mengelola daftar harga proyek pada kontrak proyek.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278602"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="7ec07-103">Mengelola daftar harga proyek pada kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="7ec07-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="7ec07-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="7ec07-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7ec07-105">Kontrak proyek di Dynamics 365 Project Operations dirancang untuk mendukung beberapa daftar harga penjualan efektif tanggal pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="7ec07-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="7ec07-106">Dalam Project Operations, ada entitas baru yang terkait disebut **Daftar harga proyek**.</span><span class="sxs-lookup"><span data-stu-id="7ec07-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="7ec07-107">Entitas ini memiliki relasi satu ke banyak dengan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="7ec07-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="7ec07-108">Daftar harga proyek digunakan untuk transaksi waktu harga dan pengeluaran pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="7ec07-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="7ec07-109">Bila kontrak memiliki satu atau beberapa daftar harga proyek, daftar harga ini digunakan untuk harga untuk perkiraan waktu dan biaya dan aktual pada proyek yang terkait dengan kontrak melalui baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="7ec07-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="7ec07-110">Bila tidak ada daftar harga proyek pada kontrak proyek, Anda akan melihat pesan peringatan bahwa tidak ada daftar harga proyek dan estimasi, pekerjaan proyek yang sebenarnya, dan pengeluaran Anda tidak akan diberi harga.</span><span class="sxs-lookup"><span data-stu-id="7ec07-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="7ec07-111">Tidak akan ada harga untuk nilai penjualan.</span><span class="sxs-lookup"><span data-stu-id="7ec07-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="7ec07-112">Mengaitkan atau membatalkan kaitan daftar harga proyek pada kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="7ec07-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="7ec07-113">Membuat atau mengaitkan daftar harga tertentu untuk memperkirakan pekerjaan dan pengeluaran berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="7ec07-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="7ec07-114">Pada kontrak proyek, pilih tab **daftar harga proyek**.</span><span class="sxs-lookup"><span data-stu-id="7ec07-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="7ec07-115">Di subkisi, pilih **+ Tambah daftar harga proyek baru**.</span><span class="sxs-lookup"><span data-stu-id="7ec07-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="7ec07-116">Di slider **buat cepat**, pilih daftar harga.</span><span class="sxs-lookup"><span data-stu-id="7ec07-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="7ec07-117">Daftar drop-down menampilkan semua daftar harga yang memiliki konteks yang diatur ke **penjualan**, dengan mata uang pada daftar harga sesuai dengan mata uang pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="7ec07-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="7ec07-118">Masukkan Deskripsi untuk Asosiasi daftar harga proyek, pilih **Simpan**, lalu tutup penggeser **buat cepat**.</span><span class="sxs-lookup"><span data-stu-id="7ec07-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="7ec07-119">Asosiasi Daftar Harga Proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="7ec07-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="7ec07-120">Ulangi langkah 1-4 untuk mengaitkan lebih dari satu daftar harga proyek ke kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="7ec07-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="7ec07-121">Cukup buat beberapa daftar harga proyek jika Anda memiliki efektivitas tanggal yang berbeda pada setiap daftar harga proyek terkait.</span><span class="sxs-lookup"><span data-stu-id="7ec07-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="7ec07-122">Project Operations tidak mendukung tumpang tindih efektivitas tanggal daftar harga proyek.</span><span class="sxs-lookup"><span data-stu-id="7ec07-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="7ec07-123">Jika ada beberapa daftar harga proyek untuk transaksi dengan tanggal tertentu, harga pada transaksi tersebut akan default ke nol.</span><span class="sxs-lookup"><span data-stu-id="7ec07-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="7ec07-124">Hapus asosiasi daftar harga proyek</span><span class="sxs-lookup"><span data-stu-id="7ec07-124">Remove a project price list association</span></span>

- <span data-ttu-id="7ec07-125">Pilih daftar harga proyek, lalu pilih **Hapus daftar harga proyek kontrak** pada subkisi.</span><span class="sxs-lookup"><span data-stu-id="7ec07-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="7ec07-126">Daftar harga akan dihapus dari daftar harga proyek pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="7ec07-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="7ec07-127">Daftar harga itu sendiri tidak akan dihapus.</span><span class="sxs-lookup"><span data-stu-id="7ec07-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="7ec07-128">Hanya Asosiasi ke kontrak yang akan dihapus.</span><span class="sxs-lookup"><span data-stu-id="7ec07-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="7ec07-129">Mengkonfigurasi default otomatis daftar harga proyek pada kontrak</span><span class="sxs-lookup"><span data-stu-id="7ec07-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="7ec07-130">Daftar harga proyek dapat diatur sebagai daftar default pada kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="7ec07-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="7ec07-131">Konfigurasi ini dapat membantu memastikan bahwa semua kontrak di organisasi Anda selalu diawali dengan daftar harga standar untuk periode harga tersebut.</span><span class="sxs-lookup"><span data-stu-id="7ec07-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="7ec07-132">Mengkonfigurasi default organisasi untuk daftar harga proyek</span><span class="sxs-lookup"><span data-stu-id="7ec07-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="7ec07-133">Buka **Pengaturan** > **Umum** lalu pilih **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="7ec07-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="7ec07-134">Di halaman daftar **parameter aktif**, pilih dan klik dua kali rekaman untuk membukanya.</span><span class="sxs-lookup"><span data-stu-id="7ec07-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="7ec07-135">Sementara mengklik gand, pastikan bahwa Anda tidak mengklik nilai bidang yang merupakan hyperlink.</span><span class="sxs-lookup"><span data-stu-id="7ec07-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="7ec07-136">Pada halaman **parameter aktif**, pilih tab **daftar harga**. Subkisi menampilkan daftar daftar harga default.</span><span class="sxs-lookup"><span data-stu-id="7ec07-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="7ec07-137">Daftar ini adalah daftar harga standar dan daftar harga penjualan.</span><span class="sxs-lookup"><span data-stu-id="7ec07-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="7ec07-138">Memiliki Daftar harga **penjualan** yang terkait di sini untuk setiap mata uang yang Anda Jual memastikan bahwa daftar harga penjualan adalah default pada kontrak apa pun yang Anda buat untuk pelanggan yang bertransaksi dalam mata uang ini.</span><span class="sxs-lookup"><span data-stu-id="7ec07-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="7ec07-139">Mengkonfigurasi daftar harga proyek khusus pelanggan</span><span class="sxs-lookup"><span data-stu-id="7ec07-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="7ec07-140">Anda juga dapat mengkonfigurasi daftar harga proyek tertentu pelanggan saat Anda menegosiasikan perjanjian harga induk dengan pelanggan Anda.</span><span class="sxs-lookup"><span data-stu-id="7ec07-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="7ec07-141">Buka **Penjualan** > **Pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="7ec07-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="7ec07-142">Dari daftar akun aktif, pilih Pelanggan yang memiliki daftar harga khusus.</span><span class="sxs-lookup"><span data-stu-id="7ec07-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="7ec07-143">Pilih rekaman pelanggan untuk membukanya, lalu pilih tab **daftar harga proyek**. Subkisi menampilkan daftar daftar harga proyek yang spesifik untuk pelanggan ini.</span><span class="sxs-lookup"><span data-stu-id="7ec07-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="7ec07-144">Buat Asosiasi daftar harga baru di sini untuk memiliki daftar harga proyek khusus untuk pelanggan ini.</span><span class="sxs-lookup"><span data-stu-id="7ec07-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="7ec07-145">Harga kustom pada kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="7ec07-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="7ec07-146">Setelah Anda memiliki daftar harga proyek default organisasi dan spesifik pelanggan, kontrak proyek Anda akan dibuat dengan Asosiasi daftar harga proyek ini secara otomatis.</span><span class="sxs-lookup"><span data-stu-id="7ec07-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="7ec07-147">Namun, daftar harga proyek pada kontrak proyek selalu disalin dengan nama tanggal dan kontrak yang ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="7ec07-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="7ec07-148">Manajer akun dan proyek kemudian dapat mulai membuat pengeditan pada harga pada salinan ini.</span><span class="sxs-lookup"><span data-stu-id="7ec07-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="7ec07-149">Harga yang telah diubah ini akan berlaku hanya untuk kontrak proyek ini.</span><span class="sxs-lookup"><span data-stu-id="7ec07-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]