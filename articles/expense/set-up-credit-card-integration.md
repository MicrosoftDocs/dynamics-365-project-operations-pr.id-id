---
title: Mengonfigurasi integrasi kartu kredit
description: Laporan topik menjelaskan cara bekerja dengan transaksi kartu kredit yang terkait dengan pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866687"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="c4c6a-103">Mengonfigurasi integrasi kartu kredit</span><span class="sxs-lookup"><span data-stu-id="c4c6a-103">Set up credit card integration</span></span>

<span data-ttu-id="c4c6a-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="c4c6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c4c6a-105">Transaksi kartu kredit terkait dengan pengeluaran dapat diatur sehingga mereka secara otomatis diimpor pada jadwal yang berulang.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="c4c6a-106">Atau, transaksi dapat diimpor secara manual sebagaimana diperlukan.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="c4c6a-107">Transaksi kartu kredit diimpor melalui entitas data transaksi kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="c4c6a-108">Mengimpor transaksi kartu kredit</span><span class="sxs-lookup"><span data-stu-id="c4c6a-108">Import credit card transactions</span></span>

<span data-ttu-id="c4c6a-109">Untuk mengimpor transaksi kartu kredit, ikuti langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="c4c6a-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="c4c6a-110">Pada halaman **transaksi kartu kredit**, pilih **impor transaksi**.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="c4c6a-111">Jika Anda membuka manajemen data untuk pertama kalinya, sistem harus memperbarui daftar entitas data agar dapat melanjutkan.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="c4c6a-112">Di bidang **Nama**, masukkan deskripsi unik untuk pekerjaan impor.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="c4c6a-113">Di bidang **format data sumber**, pilih format file yang berisi transaksi kartu kredit yang akan diimpor.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="c4c6a-114">Pilih **Unggah**, lalu Cari dan pilih file yang akan diimpor.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="c4c6a-115">Setelah file diunggah, validasi pemetaan file transaksi kartu kredit dan kolom entitas data transaksi kartu kredit dengan memilih tautan **Lihat peta** pada ubin.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="c4c6a-116">Jika terjadi kesalahan pemetaan, atau jika Anda harus mengubah pemetaan, buat perubahan pemetaan dari tab **visualisasi pemetaan** atau tab **rincian pemetaan**.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="c4c6a-117">Untuk mengotomatisasi transaksi kartu kredit, pilih **buat pekerjaan data yang berulang**.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="c4c6a-118">Selanjutnya Anda dapat mengatur pengulangan yang menentukan seberapa sering transaksi kartu kredit harus diimpor.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="c4c6a-119">Setelah selesai, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="c4c6a-120">Untuk mengimpor file yang dipilih sekarang, pilih **impor**.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="c4c6a-121">Jika kesalahan terjadi selama impor, Anda dapat melihat log eksekusi atau data penahapan untuk melihat kesalahan yang harus Anda perbaiki untuk membantu memastikan keberhasilan impor.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="c4c6a-122">Jika Anda ingin mengimpor lebih dari satu format file, Anda harus membuat pekerjaan impor terpisah untuk setiap jenis format.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="c4c6a-123">Tetapkan ulang transaksi kartu kredit untuk karyawan yang dihentikan</span><span class="sxs-lookup"><span data-stu-id="c4c6a-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="c4c6a-124">Setelah rekaman karyawan dihentikan, akun Active Directory Domain Services (AD DS) karyawan dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="c4c6a-125">Namun, mungkin ada transaksi kartu kredit aktif yang harus tetap dikeluarkan dan diganti.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="c4c6a-126">Pada halaman **transaksi kartu kredit**, Anda dapat melakukan penetapan ulang karyawan untuk setiap transaksi kartu kredit jika karyawan telah diberhentikan.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="c4c6a-127">Pilih satu atau beberapa transaksi kartu kredit, lalu pilih **tetapkan ulang transaksi**.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="c4c6a-128">Selanjutnya Anda dapat memilih karyawan lain untuk ditetapkan transaksi kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="c4c6a-129">Setelah transaksi kartu kredit telah dipindahkan, mereka dapat dipilih untuk laporan pengeluaran dan dibayar melalui proses biasa untuk penggantian laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="c4c6a-130">Menghapus transaksi kartu kredit</span><span class="sxs-lookup"><span data-stu-id="c4c6a-130">Delete credit card transactions</span></span> 

<span data-ttu-id="c4c6a-131">Terkadang, setelah transaksi kartu kredit diimpor, transaksi tertentu mungkin harus dihapus.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="c4c6a-132">Hal ini dapat dikarenakan transaksi merupakan duplikat atau karena data mungkin tidak akurat.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="c4c6a-133">Admin dapat menggunakan fitur **"Hapus transaksi kartu kredit"** untuk memilih dan menghapus transaksi kartu kredit yang **tidak dilampirkan** ke laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="c4c6a-134">Buka **tugas Periodik** > **hapus transaksi kartu kredit**.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="c4c6a-135">Pilih **Filter** dan berikan informasi untuk mengidentifikasi rekaman yang akan disertakan.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="c4c6a-136">Pilih **OK** untuk menghapus rekaman.</span><span class="sxs-lookup"><span data-stu-id="c4c6a-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
