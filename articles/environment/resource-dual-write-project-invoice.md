---
title: Integrasi faktur proyek
description: Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955771"
---
# <a name="project-invoice-integration"></a><span data-ttu-id="1d2f8-103">Integrasi faktur proyek</span><span class="sxs-lookup"><span data-stu-id="1d2f8-103">Project invoice integration</span></span>

<span data-ttu-id="1d2f8-104">Informasi topik tentang integrasi penulisan ganda Project Operations untuk faktur pelanggan.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-104">This topic provides information about Project Operations dual-write integration for customer invoicing.</span></span>

<span data-ttu-id="1d2f8-105">Dalam Project Operations, manajer proyek mengelola akumulasi penagihan proyek dan membuat faktur proforma untuk pelanggan dalam Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-105">In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse.</span></span> <span data-ttu-id="1d2f8-106">Berdasarkan faktur proforma ini, petugas piutang dagang atau akuntan Proyek membuat faktur untuk pelanggan.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-106">Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice.</span></span> <span data-ttu-id="1d2f8-107">Integrasi penulisan ganda memastikan bahwa rincian faktur proforma disinkronisasikan ke aplikasi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-107">Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps.</span></span> <span data-ttu-id="1d2f8-108">Setelah faktur pelanggan dikirim, sistem memperbarui aktual proyek yang relevan di Dataverse dengan rincian akuntansi.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-108">After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail.</span></span> <span data-ttu-id="1d2f8-109">Grafis berikut memberikan ikhtisar konsep tingkat tinggi integrasi ini.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-109">The following graphic provides a high-level conceptual overview of this integration.</span></span>

   ![Integrasi faktur proyek](./media/DW5Invoicing.png)

<span data-ttu-id="1d2f8-111">Setelah Manajer proyek mengkonfirmasikan faktur proforma dalam Dataverse, informasi header faktur proforma disinkronisasikan ke aplikasi Finance and Operations menggunakan peta tabel penulisan ganda, **Proposal faktur proyek V2 (faktur)**.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-111">After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**.</span></span> <span data-ttu-id="1d2f8-112">Ini adalah integrasi satu arah dari Dataverse ke aplikasi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-112">This is a one-way integration from Dataverse to Finance and Operations apps.</span></span> <span data-ttu-id="1d2f8-113">Membuat atau menghapus proposal faktur Proyek secara langsung di aplikasi Finance and Operations tidak didukung.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-113">Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.</span></span>

<span data-ttu-id="1d2f8-114">Konfirmasi faktur di Dataverse juga memicu logika bisnis untuk membuat rekaman terkait penagihan di entitas **Aktual**.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-114">Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity.</span></span> <span data-ttu-id="1d2f8-115">Rekaman ini disinkronkan ke Finance and Operations menggunakan peta tabel dua ganda, **aktual integrasi Project Operations (msdyn\_actuals).**</span><span class="sxs-lookup"><span data-stu-id="1d2f8-115">These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).**</span></span> <span data-ttu-id="1d2f8-116">Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md).</span><span class="sxs-lookup"><span data-stu-id="1d2f8-116">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span> 

<span data-ttu-id="1d2f8-117">Baris proposal faktur proyek dibuat oleh proses periodik, **Impor penahapan formulir**.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-117">Project invoice proposal lines are created by the periodic process, **Import form staging**.</span></span> <span data-ttu-id="1d2f8-118">Proses ini didasarkan pada rincian aktual penjualan yang ditagihkan dalam tabel **penahapan Aktual**.</span><span class="sxs-lookup"><span data-stu-id="1d2f8-118">This process is based on the billed sales actuals details in the **Actuals staging** table.</span></span> <span data-ttu-id="1d2f8-119">Untuk informasi lebih lanjut, lihat [Mengelola proposal faktur proyek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span><span class="sxs-lookup"><span data-stu-id="1d2f8-119">For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span></span> 
