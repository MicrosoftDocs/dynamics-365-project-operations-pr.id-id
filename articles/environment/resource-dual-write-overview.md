---
title: Integrasi Penulisan Ganda Project Operations
description: Ringkasan topik ini memberikan ikhtisar integrasi penulisan ganda Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955662"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="38af2-103">Ikhtisar Integrasi Penulisan Ganda Project Operations</span><span class="sxs-lookup"><span data-stu-id="38af2-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="38af2-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="38af2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="38af2-105">Project Operations menggunakan [kemampuan penulisan ganda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) untuk mensinkronisasi data di seluruh Microsoft Dataverse dan Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="38af2-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="38af2-106">Ilustrasi berikut menunjukkan cara sinkronisasi data sebagai bagian dari integrasi antara Dataverse dan Finance.</span><span class="sxs-lookup"><span data-stu-id="38af2-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Ikhtisar alur data Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="38af2-108">Project Operations di Dataverse menyediakan antarmuka pengguna (UI) modern dan ekstensibilitas tanpa kode/kode rendah yang mudah menggunakan kemampuan Power Platform.</span><span class="sxs-lookup"><span data-stu-id="38af2-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="38af2-109">Manajer proyek, Manajer sumber daya, anggota tim proyek, dan staf kantor depan lainnya, melakukan aktivitas mereka di Project Operations di Dataverse.</span><span class="sxs-lookup"><span data-stu-id="38af2-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="38af2-110">Project Operations in Finance memberikan dukungan akuntansi proyek dan pengakuan pendapatan.</span><span class="sxs-lookup"><span data-stu-id="38af2-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="38af2-111">Project Operations terhubung dengan kerangka kerja keuangan di Finance untuk perhitungan pajak penjualan, nilai tukar mata uang, pelaporan dimensi keuangan, dan banyak lagi.</span><span class="sxs-lookup"><span data-stu-id="38af2-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="38af2-112">Pengalaman akuntan Proyek kebanyakan berbasis di Finance.</span><span class="sxs-lookup"><span data-stu-id="38af2-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="38af2-113">Integrasi Project Operations terdiri dari integrasi komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="38af2-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="38af2-114">Konfigurasi Project Operations dan integrasi data konfigurasi</span><span class="sxs-lookup"><span data-stu-id="38af2-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="38af2-115">Estimasi proyek dan aktual</span><span class="sxs-lookup"><span data-stu-id="38af2-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="38af2-116">Faktur Proyek</span><span class="sxs-lookup"><span data-stu-id="38af2-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="38af2-117">Manajemen pengeluaran</span><span class="sxs-lookup"><span data-stu-id="38af2-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="38af2-118">Faktur Vendor</span><span class="sxs-lookup"><span data-stu-id="38af2-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
