---
title: Mengonfigurasi integrasi kartu kredit
description: Topik ini menjelaskan cara mengimpor dan mengelola transaksi kartu kredit terkait pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276172"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="c39b0-103">Mengonfigurasi integrasi kartu kredit</span><span class="sxs-lookup"><span data-stu-id="c39b0-103">Set up credit card integration</span></span>

<span data-ttu-id="c39b0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="c39b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c39b0-105">Transaksi kartu kredit terkait dengan pengeluaran dapat diatur sehingga mereka secara otomatis diimpor pada jadwal yang berulang.</span><span class="sxs-lookup"><span data-stu-id="c39b0-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="c39b0-106">Atau, transaksi dapat diimpor secara manual sebagaimana diperlukan.</span><span class="sxs-lookup"><span data-stu-id="c39b0-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="c39b0-107">Transaksi kartu kredit diimpor melalui entitas data transaksi kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="c39b0-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="c39b0-108">Mengimpor transaksi kartu kredit</span><span class="sxs-lookup"><span data-stu-id="c39b0-108">Import credit card transactions</span></span>

1. <span data-ttu-id="c39b0-109">Pada halaman **transaksi kartu kredit**, pilih **impor transaksi**.</span><span class="sxs-lookup"><span data-stu-id="c39b0-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="c39b0-110">Jika Anda membuka manajemen data untuk pertama kalinya, sistem harus memperbarui daftar entitas data agar dapat melanjutkan.</span><span class="sxs-lookup"><span data-stu-id="c39b0-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="c39b0-111">Di bidang **Nama**, masukkan deskripsi unik untuk pekerjaan impor.</span><span class="sxs-lookup"><span data-stu-id="c39b0-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="c39b0-112">Di bidang **format data sumber**, pilih format file yang berisi transaksi kartu kredit yang akan diimpor.</span><span class="sxs-lookup"><span data-stu-id="c39b0-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="c39b0-113">Pilih **Unggah**, lalu Cari dan pilih file yang akan diimpor.</span><span class="sxs-lookup"><span data-stu-id="c39b0-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="c39b0-114">Setelah file diunggah, validasi pemetaan file transaksi kartu kredit dan kolom entitas data transaksi kartu kredit dengan memilih tautan **Lihat peta** pada ubin.</span><span class="sxs-lookup"><span data-stu-id="c39b0-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="c39b0-115">Jika terjadi kesalahan pemetaan, atau jika Anda harus mengubah pemetaan, buat perubahan pemetaan dari tab **visualisasi pemetaan** atau tab **rincian pemetaan**.</span><span class="sxs-lookup"><span data-stu-id="c39b0-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="c39b0-116">Untuk mengotomatisasi transaksi kartu kredit, pilih **buat pekerjaan data yang berulang**.</span><span class="sxs-lookup"><span data-stu-id="c39b0-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="c39b0-117">Selanjutnya Anda dapat mengatur pengulangan yang menentukan seberapa sering transaksi kartu kredit harus diimpor.</span><span class="sxs-lookup"><span data-stu-id="c39b0-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="c39b0-118">Setelah selesai, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="c39b0-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="c39b0-119">Untuk mengimpor file yang dipilih sekarang, pilih **impor**.</span><span class="sxs-lookup"><span data-stu-id="c39b0-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="c39b0-120">Jika kesalahan terjadi selama impor, Anda dapat melihat log eksekusi atau data penahapan untuk melihat kesalahan yang harus Anda Perbaiki untuk membantu menjamin impor yang berhasil.</span><span class="sxs-lookup"><span data-stu-id="c39b0-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="c39b0-121">Jika Anda harus mengimpor lebih dari satu format file, Anda harus membuat tugas impor terpisah untuk setiap jenis format.</span><span class="sxs-lookup"><span data-stu-id="c39b0-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="c39b0-122">Tetapkan ulang transaksi kartu kredit untuk karyawan yang dihentikan</span><span class="sxs-lookup"><span data-stu-id="c39b0-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="c39b0-123">Setelah rekaman karyawan dihentikan, akun Active Directory Domain Services (AD DS) karyawan dinonaktifkan.</span><span class="sxs-lookup"><span data-stu-id="c39b0-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="c39b0-124">Namun, mungkin ada transaksi kartu kredit aktif yang harus tetap dikeluarkan dan diganti.</span><span class="sxs-lookup"><span data-stu-id="c39b0-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="c39b0-125">Dari halaman **transaksi kartu kredit**, Anda dapat menetapkan ulang karyawan untuk setiap transaksi kartu kredit dengan karyawan yang terkait telah dihentikan.</span><span class="sxs-lookup"><span data-stu-id="c39b0-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="c39b0-126">Pilih satu atau beberapa transaksi kartu kredit, lalu pilih **tetapkan ulang transaksi**.</span><span class="sxs-lookup"><span data-stu-id="c39b0-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="c39b0-127">Selanjutnya Anda dapat memilih karyawan lain untuk ditetapkan transaksi kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="c39b0-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="c39b0-128">Setelah transaksi kartu kredit telah dipindahkan, mereka dapat dipilih untuk laporan pengeluaran dan dibayar melalui proses biasa untuk penggantian laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="c39b0-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]