---
title: Halaman beranda pelaporan
description: Topik ini memberikan informasi tentang pelaporan di Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 32b504a862f98dac4b1d9b54289476026d988c13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951483"
---
# <a name="reporting-home-page"></a><span data-ttu-id="8da4b-103">Laman beranda pelaporan</span><span class="sxs-lookup"><span data-stu-id="8da4b-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8da4b-104">Microsoft Dynamics 365 Project Service Automation memungkinkan organisasi berbasis proyek secara efisien mengelola operasi bisnis mereka.</span><span class="sxs-lookup"><span data-stu-id="8da4b-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="8da4b-105">Pada setiap proyek, anggota tim harus mengelola peluang, kuotasi, dan merencanakan pekerjaan, sumber daya proyek, mengelola pekerjaan sesuai rencana, menagih pekerjaan, dan kemudian melakukan pekerjaan untuk menyelesaikan proyek.</span><span class="sxs-lookup"><span data-stu-id="8da4b-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="8da4b-106">Kemampuan untuk melaporkan operasi adalah kunci untuk menentukan kesehatan organisasi dan melakukan tindakan perbaikan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="8da4b-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="8da4b-107">PSA menggunakan metode pelaporan dan teknologi Microsoft Dynamics 365 untuk semua pelaporan.</span><span class="sxs-lookup"><span data-stu-id="8da4b-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="8da4b-108">Untuk informasi lebih lanjut tentang pilihan pelaporan, lihat [panduan penulisan laporan untuk Dynamics 365 Customer Engagement (on-premises), versi 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="8da4b-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="8da4b-109">Wizard Laporan</span><span class="sxs-lookup"><span data-stu-id="8da4b-109">Report Wizard</span></span>

<span data-ttu-id="8da4b-110">Wizard laporan memungkinkan non-pengembang membuat laporan sederhana.</span><span class="sxs-lookup"><span data-stu-id="8da4b-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="8da4b-111">Karena aplikasi ini dibuat di platform yang ada, pengalaman sama dengan pengalaman yang didokumentasikan di [membuat atau mengedit laporan menggunakan wizard laporan](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="8da4b-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="8da4b-112">Namun, Anda akan menggunakan entitas khusus Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8da4b-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="8da4b-113">Laporan SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="8da4b-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="8da4b-114">Jika bisnis Anda memerlukan laporan tertentu yang tidak dapat dibuat dengan menggunakan wizard laporan, Anda dapat membuat laporan kustom.</span><span class="sxs-lookup"><span data-stu-id="8da4b-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="8da4b-115">Anda harus menginstal Microsoft Visual Studio, bersama dengan Microsoft SQL Server Data Tools yang sesuai dan ekstensi penulisan laporan.</span><span class="sxs-lookup"><span data-stu-id="8da4b-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="8da4b-116">Untuk informasi lebih lanjut tentang alat dan versi, Lihat [lingkungan penulisan laporan menggunakan SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="8da4b-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="8da4b-117">Untuk informasi tentang cara membuat laporan kustom, lihat [membuat laporan baru menggunakan SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="8da4b-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="8da4b-118">aplikasi wawasan Power BI</span><span class="sxs-lookup"><span data-stu-id="8da4b-118">Power BI insights apps</span></span>

<span data-ttu-id="8da4b-119">Bersama-sama, Microsoft Power BI dan Dynamics 365 memberikan cara ampuh untuk bekerja dengan data Anda, dalam bentuk aplikasi wawasan.</span><span class="sxs-lookup"><span data-stu-id="8da4b-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="8da4b-120">Untuk informasi tentang ketersediaan aplikasi wawasan, lihat halaman [aplikasi Power BI insights](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="8da4b-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8da4b-121">Sumber daya tambahan</span><span class="sxs-lookup"><span data-stu-id="8da4b-121">Additional resources</span></span>
<span data-ttu-id="8da4b-122">Untuk informasi lebih lanjut tentang pelaporan di PSA, lihat topik berikut ini:</span><span class="sxs-lookup"><span data-stu-id="8da4b-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="8da4b-123">Bekerja dengan model data Project Service</span><span class="sxs-lookup"><span data-stu-id="8da4b-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="8da4b-124">Dasbor</span><span class="sxs-lookup"><span data-stu-id="8da4b-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]