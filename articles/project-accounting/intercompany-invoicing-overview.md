---
title: Sekilas faktur antarperusahaan
description: Topik ini berisi informasi dan contoh tentang membuat faktur antarperusahaan untuk berbagai proyek.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287332"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="711c0-103">Sekilas faktur antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="711c0-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="711c0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="711c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="711c0-105">Organisasi Anda mungkin memiliki beberapa divisi, anak perusahaan, dan entitas hukum lainnya yang mentransfer produk dan layanan satu sama lain untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="711c0-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="711c0-106">Entitas hukum yang menyediakan layanan atau produk disebut *entitas hukum pemberi pinjaman*.</span><span class="sxs-lookup"><span data-stu-id="711c0-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="711c0-107">Entitas hukum yang menerima layanan atau produk disebut *entitas hukum peminjam*.</span><span class="sxs-lookup"><span data-stu-id="711c0-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="711c0-108">Ilustrasi berikut menunjukkan skenario umum di mana dua entitas hukum, Contoso Robotics USA (entitas hukum peminjam) dan Contoso Robotics UK (entitas hukum pemberi pinjaman) berbagi sumber daya untuk menyediakan proyek bagi pelanggan, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="711c0-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="711c0-109">Untuk skenario ini, Contoso Robotics USA dikontrak untuk memberikan pekerjaan kepada Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="711c0-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Faktur antarperusahaan](./media/IntercompanyScenario.png) 

<span data-ttu-id="711c0-111">Dynamics 365 Project Operations menggunakan aliran berikut ini untuk memproses transaksi antarperusahaan:</span><span class="sxs-lookup"><span data-stu-id="711c0-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="711c0-112">Sumber daya dari record entitas hukum pemberi pinjaman untuk transaksi pengeluaran atau waktu antarperusahaan berdasarkan waktu dan biaya pemesanan proyek di entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="711c0-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="711c0-113">Biaya waktu dan pengeluaran dicatat di perusahaan pemberi pinjaman dengan menggunakan daftar harga biaya unit perusahaan peminjam.</span><span class="sxs-lookup"><span data-stu-id="711c0-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="711c0-114">Transaksi penjualan antarperusahaan yang belum ditagihkan dicatat di perusahaan pemberi pinjaman dengan menggunakan daftar harga biaya unit perusahaan peminjam.</span><span class="sxs-lookup"><span data-stu-id="711c0-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="711c0-115">Pendapatan yang belum ditagih tercatat di perusahaan peminjam menggunakan daftar harga penjualan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="711c0-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="711c0-116">Pelanggan dapat ditagih apabila pendapatan yang belum ditagih tercatat.</span><span class="sxs-lookup"><span data-stu-id="711c0-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="711c0-117">Pelanggan tidak perlu menunggu hingga pemrosesan faktur antarperusahaan selesai.</span><span class="sxs-lookup"><span data-stu-id="711c0-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="711c0-118">Faktur pelanggan antarperusahaan dibuat secara berkala di perusahaan pemberi pinjaman.</span><span class="sxs-lookup"><span data-stu-id="711c0-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="711c0-119">Faktur dibuat secara manual atau dengan menggunakan proses otomatis berkala.</span><span class="sxs-lookup"><span data-stu-id="711c0-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="711c0-120">Faktur tunggal dapat dibuat untuk setiap entitas hukum peminjam atau faktur terpisah dapat dibuat berdasarkan proyek.</span><span class="sxs-lookup"><span data-stu-id="711c0-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="711c0-121">Saat faktur pelanggan antarperusahaan diposting di entitas hukum pemberi pinjaman, faktur tertunda vendor yang terkait dibuat di entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="711c0-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="711c0-122">Biaya di faktur tertunda vendor akan dicatat di subbuku besar proyek saat faktur diposting.</span><span class="sxs-lookup"><span data-stu-id="711c0-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="711c0-123">Diagram berikut menunjukkan faktur antarperusahaan yang terkait dengan aktivitas akuntansi dan posting yang diharapkan ke buku besar.</span><span class="sxs-lookup"><span data-stu-id="711c0-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Alur antarperusahaan](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="711c0-125">Sumber daya tambahan</span><span class="sxs-lookup"><span data-stu-id="711c0-125">Additional resources</span></span>

- [<span data-ttu-id="711c0-126">Mengonfigurasikan faktur antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="711c0-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="711c0-127">Mencatat transaksi antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="711c0-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="711c0-128">Membuat faktur vendor dan pelanggan antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="711c0-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]