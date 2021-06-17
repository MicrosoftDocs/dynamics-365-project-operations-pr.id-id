---
title: Beli bahan non-stok dengan faktur vendor tertunda
description: Laporan topik menjelaskan cara mencatat faktur vendor yang tertunda.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993801"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="0fa7a-103">Beli bahan non-stok dengan faktur vendor tertunda</span><span class="sxs-lookup"><span data-stu-id="0fa7a-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="0fa7a-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="0fa7a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0fa7a-105">Sebagai perusahaan yang mendapatkan bahan non-stok untuk proyek, biayanya dapat dengan segera dicatat terhadap proyek.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="0fa7a-106">Contohnya, Contoso Robotics US sedang melakukan proyek pembaruan perlengkapan dan memerlukan lisensi perangkat lunak.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="0fa7a-107">Lisensi ini diperoleh dari vendor pihak ketiga.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="0fa7a-108">Menggunakan Dynamics 365 Finance, petugas utang dagang mencatat dokumen faktur vendor yang tertunda dan mengaitkan biaya lisensi secara langsung terhadap proyek pembaruan perlengkapan.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="0fa7a-109">Sebelum Anda menggunakan fungsi yang dijelaskan di topik ini, lihat dan terapkan konfigurasi yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="0fa7a-110">Untuk informasi lebih lanjut, lihat [Mengaktifkan materi non-stok dan faktur vendor yang tertunda](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="0fa7a-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="0fa7a-111">Posting faktur vendor tertunda terkait proyek</span><span class="sxs-lookup"><span data-stu-id="0fa7a-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="0fa7a-112">Faktur vendor yang tertunda dapat direkam pada halaman **faktur vendor tertunda** (**utang dagang** > **Faktur** > **Faktur vendor tertunda**).</span><span class="sxs-lookup"><span data-stu-id="0fa7a-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="0fa7a-113">Selesaikan langkah-langkah berikut untuk memposting faktur vendor tertunda terkait proyek:</span><span class="sxs-lookup"><span data-stu-id="0fa7a-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="0fa7a-114">Buka **utang dagang** > **Faktur**, lalu pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="0fa7a-115">Pada bidang **Akun faktur**, pilih vendor dan pada bidang **Nomor**, masukkan identifikasi faktur vendor.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="0fa7a-116">Tambahkan baris ke faktur vendor dan di bidang **Nomor Item**, pilih item non-stok yang dibeli dari vendor.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0fa7a-117">Baris faktur vendor yang didasarkan pada kategori pengadaan tidak dapat dicatat terhadap proyek.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="0fa7a-118">Tambahkan kuantitas yang dibeli.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-118">Add the quantity purchased.</span></span> <span data-ttu-id="0fa7a-119">Sistem akan mengisi harga per unit berdasarkan konfigurasi harga item yang tidak distok.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="0fa7a-120">Verifikasikan jumlah total dan rincian lainnya yang diperlukan di baris.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="0fa7a-121">Pada detail baris, pada tab **Proyek**, pilih ID proyek untuk mencatat item ini.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="0fa7a-122">Atau pilih nomor aktivitas, lalu perbarui kategori proyek dan properti baris.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="0fa7a-123">Posting faktur vendor yang tertunda.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-123">Post pending vendor invoice.</span></span> <span data-ttu-id="0fa7a-124">Saat faktur diposting, sistem mencatat:</span><span class="sxs-lookup"><span data-stu-id="0fa7a-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="0fa7a-125">Jumlah saldo vendor.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="0fa7a-126">Jumlah Pajak Penjualan.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-126">The sales tax amount.</span></span>
    - <span data-ttu-id="0fa7a-127">Biaya terhadap proyek dicatat ke akun integrasi pengadaan.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="0fa7a-128">Transaksi aktual proyek di Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="0fa7a-129">Transaksi ini diproses lebih lanjut menggunakan [jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="0fa7a-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="0fa7a-130">Mem-posting jurnal ini akan memindahkan jumlah tersebut dari akun integrasi pengadaan ke akun biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="0fa7a-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
