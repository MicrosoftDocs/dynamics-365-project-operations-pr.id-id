---
title: Mengaktifkan fitur Project Finder Mobile
description: Bagaimana mengaktifkan fitur Project Finder Mobile untuk Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752370"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="71e34-103">Mengaktifkan fitur Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="71e34-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="71e34-104">Sumber daya Anda dapat menggunakan app Project Finder Mobile di ponsel mereka dengan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk menemukan proyek-proyek baru untuk bekerja dan memperbarui set keterampilan mereka.</span><span class="sxs-lookup"><span data-stu-id="71e34-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="71e34-105">Aplikasi ini tersedia untuk [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telepon [!INCLUDE[tn_android](../includes/tn-android.md)], dan [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="71e34-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="71e34-106">Anda perlu untuk mengatur beberapa opsi dalam pengaturan parameter untuk unit organisasi Anda untuk memungkinkan pengguna untuk melihat kebutuhan sumber daya proyek dan memperbarui keterampilan mereka.</span><span class="sxs-lookup"><span data-stu-id="71e34-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="71e34-107">Aplikasi Project Finder Mobile hanya berfungsi pada [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], tidak dengan instalasi lokal.</span><span class="sxs-lookup"><span data-stu-id="71e34-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="71e34-108">Lihat **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="71e34-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="71e34-109">Klik parameter pengaturan yang Anda ingin gunakan untuk memungkinkan fitur aplikasi Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="71e34-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="71e34-110">Dalam area **umum**, atur **kebutuhan sumber daya terlihat oleh sumber daya** ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="71e34-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="71e34-111">Atur **Izinkan pembaruan keahlian oleh sumber daya** ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="71e34-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="71e34-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="71e34-112">![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="71e34-113">Ini adalah pengaturan global.</span><span class="sxs-lookup"><span data-stu-id="71e34-113">This is a global setting.</span></span> <span data-ttu-id="71e34-114">Manajer proyek dapat mengatur apakah proyek individu akan terlihat pada halaman **tim proyek** proyek itu.</span><span class="sxs-lookup"><span data-stu-id="71e34-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="71e34-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="71e34-115">![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="71e34-116">Pemberitahuan email</span><span class="sxs-lookup"><span data-stu-id="71e34-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="71e34-117">mengirim email tentang permintaan sumber daya ke Penerima berikut pada waktu-waktu berikut:</span><span class="sxs-lookup"><span data-stu-id="71e34-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="71e34-118">Penerima</span><span class="sxs-lookup"><span data-stu-id="71e34-118">Recipient</span></span>|<span data-ttu-id="71e34-119">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="71e34-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="71e34-120">Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="71e34-120">Project manager</span></span>|<span data-ttu-id="71e34-121">-   Ketika sumber daya mendaftarkan diri ke sebuah proyek dengan app Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="71e34-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="71e34-122">Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="71e34-122">Resource</span></span>|<span data-ttu-id="71e34-123">-   Ketika pekerjaan proyek di mana sumber daya telah mendaftar sudah diisi oleh sumber daya lain.</span><span class="sxs-lookup"><span data-stu-id="71e34-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="71e34-124">-   Ketika permintaan persetujuan keterampilan mereka disetujui atau ditolak.</span><span class="sxs-lookup"><span data-stu-id="71e34-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="71e34-125">-   Ketika permintaan pendaftaran proyek disetujui atau ditolak.</span><span class="sxs-lookup"><span data-stu-id="71e34-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="71e34-126">Pemberitahuan privasi</span><span class="sxs-lookup"><span data-stu-id="71e34-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="71e34-127">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="71e34-127">See Also</span></span>  
 [<span data-ttu-id="71e34-128">Konfigurasi Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="71e34-128">Set up resources</span></span>](../project-service/set-up-resources.md)
