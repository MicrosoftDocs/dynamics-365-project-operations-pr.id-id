---
title: Mengaktifkan fitur Project Finder Mobile
description: Bagaimana mengaktifkan fitur Project Finder Mobile untuk Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132967"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Mengaktifkan fitur Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sumber daya Anda dapat menggunakan app Project Finder Mobile di ponsel mereka dengan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk menemukan proyek-proyek baru untuk bekerja dan memperbarui set keterampilan mereka.  
  
 Aplikasi ini tersedia untuk [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telepon [!INCLUDE[tn_android](../includes/tn-android.md)], dan [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Anda perlu untuk mengatur beberapa opsi dalam pengaturan parameter untuk unit organisasi Anda untuk memungkinkan pengguna untuk melihat kebutuhan sumber daya proyek dan memperbarui keterampilan mereka.  
  
> [!NOTE]
>  Aplikasi Project Finder Mobile hanya berfungsi pada [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], tidak dengan instalasi lokal.  
  
1. Lihat **Project Service > Parameter**.  
  
2. Klik parameter pengaturan yang Anda ingin gunakan untuk memungkinkan fitur aplikasi Project Finder Mobile.  
  
3. Dalam area **umum**, atur **kebutuhan sumber daya terlihat oleh sumber daya** ke **ya**.  
  
4. Atur **Izinkan pembaruan keahlian oleh sumber daya** ke **Ya**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ini adalah pengaturan global. Manajer proyek dapat mengatur apakah proyek individu akan terlihat pada halaman **tim proyek** proyek itu.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Pemberitahuan email  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] mengirim email tentang permintaan sumber daya ke Penerima berikut pada waktu-waktu berikut:  
  
|Penerima|Aktivitas|  
|---------------|-----------|  
|Manajer Proyek|-   Ketika sumber daya mendaftarkan diri ke sebuah proyek dengan app Project Finder Mobile.|  
|Sumber Daya|-   Ketika pekerjaan proyek di mana sumber daya telah mendaftar sudah diisi oleh sumber daya lain.<br />-   Ketika permintaan persetujuan keterampilan mereka disetujui atau ditolak.<br />-   Ketika permintaan pendaftaran proyek disetujui atau ditolak.|  
  
## <a name="privacy-notice"></a>Pemberitahuan privasi  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Lihat Juga  
 [Konfigurasi Sumber Daya](../psa/set-up-resources.md)
