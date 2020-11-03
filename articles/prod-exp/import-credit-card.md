---
title: Mengimpor dan mengelola transaksi kartu kredit
description: Topik ini menjelaskan cara mengimpor dan mengelola transaksi kartu kredit terkait pengeluaran. Transaksi ini dapat diatur sehingga mereka secara otomatis diimpor pada jadwal berulang, atau mereka dapat secara manual diimpor sebagaimana diperlukan.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078637"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="276f5-104">Mengimpor dan mengelola transaksi kartu kredit</span><span class="sxs-lookup"><span data-stu-id="276f5-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="276f5-105">Transaksi kartu kredit terkait dengan pengeluaran dapat diatur sehingga mereka secara otomatis diimpor pada jadwal yang berulang.</span><span class="sxs-lookup"><span data-stu-id="276f5-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="276f5-106">Atau, transaksi dapat diimpor secara manual sebagaimana diperlukan.</span><span class="sxs-lookup"><span data-stu-id="276f5-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="276f5-107">Transaksi kartu kredit diimpor melalui entitas data transaksi kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="276f5-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="276f5-108">Untuk informasi lebih lanjut tentang entitas data, lihat [entitas data](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="276f5-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="276f5-109">Mengimpor transaksi kartu kredit</span><span class="sxs-lookup"><span data-stu-id="276f5-109">Import credit card transactions</span></span>

1. <span data-ttu-id="276f5-110">Pada halaman **transaksi kartu kredit** , pilih **impor transaksi**.</span><span class="sxs-lookup"><span data-stu-id="276f5-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="276f5-111">Jika Anda membuka manajemen data untuk pertama kalinya, sistem harus memperbarui daftar entitas data agar dapat melanjutkan.</span><span class="sxs-lookup"><span data-stu-id="276f5-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="276f5-112">Di bidang **Nama** , masukkan deskripsi unik untuk pekerjaan impor.</span><span class="sxs-lookup"><span data-stu-id="276f5-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="276f5-113">Di bidang **format data sumber** , pilih format file yang berisi transaksi kartu kredit yang akan diimpor.</span><span class="sxs-lookup"><span data-stu-id="276f5-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="276f5-114">Pilih **Unggah** , lalu Cari dan pilih file yang akan diimpor.</span><span class="sxs-lookup"><span data-stu-id="276f5-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="276f5-115">Setelah file diunggah, validasi pemetaan file transaksi kartu kredit dan kolom entitas data transaksi kartu kredit dengan memilih tautan **Lihat peta** pada ubin.</span><span class="sxs-lookup"><span data-stu-id="276f5-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="276f5-116">Jika terjadi kesalahan pemetaan, atau jika Anda harus mengubah pemetaan, buat perubahan pemetaan dari tab **visualisasi pemetaan** atau tab **rincian pemetaan**.</span><span class="sxs-lookup"><span data-stu-id="276f5-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="276f5-117">Untuk mengotomatisasi transaksi kartu kredit, pilih **buat pekerjaan data yang berulang**.</span><span class="sxs-lookup"><span data-stu-id="276f5-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="276f5-118">Selanjutnya Anda dapat mengatur pengulangan yang menentukan seberapa sering transaksi kartu kredit harus diimpor.</span><span class="sxs-lookup"><span data-stu-id="276f5-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="276f5-119">Setelah selesai, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="276f5-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="276f5-120">Untuk mengimpor file yang dipilih sekarang, pilih **impor**.</span><span class="sxs-lookup"><span data-stu-id="276f5-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="276f5-121">Jika kesalahan terjadi selama impor, Anda dapat melihat log eksekusi atau data penahapan untuk melihat kesalahan yang harus Anda Perbaiki untuk membantu menjamin impor yang berhasil.</span><span class="sxs-lookup"><span data-stu-id="276f5-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="276f5-122">Jika Anda harus mengimpor lebih dari satu format file, Anda harus membuat tugas impor terpisah untuk setiap jenis format.</span><span class="sxs-lookup"><span data-stu-id="276f5-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="276f5-123">Tetapkan ulang transaksi kartu kredit untuk karyawan yang dihentikan</span><span class="sxs-lookup"><span data-stu-id="276f5-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="276f5-124">Setelah rekaman karyawan dihentikan, akun Active Directory Domain Services (AD DS) karyawan dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="276f5-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="276f5-125">Namun, mungkin ada transaksi kartu kredit aktif yang harus tetap dikeluarkan dan diganti.</span><span class="sxs-lookup"><span data-stu-id="276f5-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="276f5-126">Dari halaman **transaksi kartu kredit** , Anda dapat menetapkan ulang karyawan untuk setiap transaksi kartu kredit dengan karyawan yang terkait telah dihentikan.</span><span class="sxs-lookup"><span data-stu-id="276f5-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="276f5-127">Pilih satu atau beberapa transaksi kartu kredit, lalu pilih **tetapkan ulang transaksi**.</span><span class="sxs-lookup"><span data-stu-id="276f5-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="276f5-128">Selanjutnya Anda dapat memilih karyawan lain untuk ditetapkan transaksi kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="276f5-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="276f5-129">Setelah transaksi kartu kredit telah dipindahkan, mereka dapat dipilih untuk laporan pengeluaran dan dibayar melalui proses biasa untuk penggantian laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="276f5-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
