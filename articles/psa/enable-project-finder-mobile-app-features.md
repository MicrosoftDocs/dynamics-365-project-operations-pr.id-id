---
title: Mengaktifkan fitur Project Finder Mobile
description: Bagaimana mengaktifkan fitur Project Finder Mobile untuk Project Service
author: JohnPBurrows
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f068c32ac957dc5921ccabc989b3b7a347585c19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007730"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="9d228-103">Mengaktifkan fitur Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9d228-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9d228-104">Sumber daya Anda dapat menggunakan app Project Finder Mobile di ponsel mereka dengan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk menemukan proyek-proyek baru untuk bekerja dan memperbarui set keterampilan mereka.</span><span class="sxs-lookup"><span data-stu-id="9d228-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skillsets.</span></span>  
  
 <span data-ttu-id="9d228-105">Aplikasi ini tersedia untuk [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telepon [!INCLUDE[tn_android](../includes/tn-android.md)], dan [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="9d228-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
    
 <span data-ttu-id="9d228-106">Anda perlu untuk memilih beberapa opsi dalam pengaturan parameter untuk unit organisasi Anda untuk memungkinkan pengguna untuk melihat kebutuhan sumber daya proyek dan memperbarui keterampilan mereka.</span><span class="sxs-lookup"><span data-stu-id="9d228-106">To allow users to view project resource requirements and update skills, options must be selected in the parameter settings for your organizational unit.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="9d228-107">Aplikasi Project Finder Mobile hanya berfungsi pada [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], tidak dengan instalasi lokal.</span><span class="sxs-lookup"><span data-stu-id="9d228-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="9d228-108">Lihat **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="9d228-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="9d228-109">Klik parameter pengaturan yang Anda ingin gunakan untuk memungkinkan fitur aplikasi Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="9d228-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="9d228-110">Dalam area **umum**, atur **kebutuhan sumber daya terlihat oleh sumber daya** ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="9d228-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="9d228-111">Atur **Izinkan pembaruan keahlian oleh sumber daya** ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="9d228-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="9d228-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="9d228-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="9d228-113">Ini adalah pengaturan global.</span><span class="sxs-lookup"><span data-stu-id="9d228-113">This is a global setting.</span></span> <span data-ttu-id="9d228-114">Manajer proyek dapat mengatur apakah proyek individu akan terlihat pada halaman **tim proyek** proyek itu.</span><span class="sxs-lookup"><span data-stu-id="9d228-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="9d228-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="9d228-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="9d228-116">Pemberitahuan email</span><span class="sxs-lookup"><span data-stu-id="9d228-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="9d228-117">mengirim email tentang permintaan sumber daya ke Penerima berikut pada waktu-waktu berikut:</span><span class="sxs-lookup"><span data-stu-id="9d228-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="9d228-118">Penerima</span><span class="sxs-lookup"><span data-stu-id="9d228-118">Recipient</span></span>|<span data-ttu-id="9d228-119">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="9d228-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="9d228-120">Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="9d228-120">Project manager</span></span>|<span data-ttu-id="9d228-121">- Sumber daya mendaftarkan diri ke sebuah proyek dengan aplikasi Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="9d228-121">- A resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="9d228-122">Sumber daya</span><span class="sxs-lookup"><span data-stu-id="9d228-122">Resource</span></span>|<span data-ttu-id="9d228-123">- Pekerjaan proyek di mana sumber daya telah mendaftar sudah diisi oleh sumber daya lain.</span><span class="sxs-lookup"><span data-stu-id="9d228-123">- The project work that the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="9d228-124">- Permintaan persetujuan keterampilan mereka disetujui atau ditolak.</span><span class="sxs-lookup"><span data-stu-id="9d228-124">- The skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="9d228-125">- Permintaan pendaftaran proyek disetujui atau ditolak.</span><span class="sxs-lookup"><span data-stu-id="9d228-125">- The project sign-up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="9d228-126">Pemberitahuan privasi</span><span class="sxs-lookup"><span data-stu-id="9d228-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="9d228-127">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="9d228-127">See Also</span></span>  
 [<span data-ttu-id="9d228-128">Konfigurasi Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="9d228-128">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]