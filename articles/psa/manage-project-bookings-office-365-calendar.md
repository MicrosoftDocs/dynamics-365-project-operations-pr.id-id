---
title: Mengelola Pemesanan dan proyek-proyek di kalender Office 365
description: Cara mengelola Pemesanan dan proyek-proyek di kalender Office 365
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: c575bd3deba5bcde2526ccfc598327917bf91642
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144462"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Mengelola proyek dan Pemesanan di kalender (Project Service)

> [!Note]
> DITOLAK: Fitur ini ini telah usang dan tidak lagi tersedia.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Lihat temu janji pribadi, Pemesanan pekerjaan proyek dan tugas perintah kerja field service dengan menggunakan kalender [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Dengan segala sesuatu ada di satu tempat, mudah untuk mengelola hari Anda. Pertemuan, janji temu, pemesanan, dan tugas tersedia di kalender [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Jika Anda menggunakan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], Anda juga dapat memasukkan janji pribadi Anda di tampilan catatan waktu Project service. Hal ini memungkinkan manajer proyek dan sumber daya tahu ketersediaan Anda untuk proyek-proyek. Ini juga menghemat waktu, karena Anda tidak perlu memasukkan info tentang janji pribadi Anda dua kali. Anda cukup mengimpor janji pribadi Anda dari kalender ke tampilan entri waktu Project service.  
  
 Kalender akan mensinkronkan proyek dan pemesanan perintah kerja dari hari ini untuk empat minggu mendatang. Pengaturan ini tidak dapat diubah.  
  
 Sinkronisasi hanya didukung satu arah, dari PSA ke kalender [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Anda. Anda dapat mensinkronisasi dalam urutan terbalik. 
  
 Untuk mempelajari cara menggunakan kalender [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], lihat [kalender di Outlook di web untuk bisnis](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Konfigurasi  
 Sebelum Anda dapat melihat dan mengelola pemesanan Anda di kalender [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], Anda perlu untuk mengatur beberapa hal.  
  
- Anda akan perlu untuk memiliki kredensial Global Administrator [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] atau Administrator sistem.  
  
- Admin Anda perlu mengkonfigurasi profil server email dan setiap pengguna akan perlu untuk mengkonfigurasi kotak pesan mereka. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Mengatur email agar memproses melalui sinkronisasi sisi server](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Aktifkan sinkronisasi untuk organisasi (tugas admin)  
  
1.  Dari menu utama, klik **Pengaturan** > **Administrasi**.  
  
2.  Klik **Pengaturan Sistem**.  
  
3.  Klik tab **sinkronisasi**.  
  
4.  Di bawah **pilih apakah akan mengaktifkan sinkronisasi Pemesanan sumber daya dengan**, periksa **sinkronisasikan pemesanan sumber daya dengan Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Aktifkan sinkronisasi untuk profil pengguna Anda (tugas pengguna)  
  
1.  Klik tombol **Pengaturan** di sudut kanan atas layar.  
  
2.  Klik **Pilihan**.  
  
3.  Klik tab **sinkronisasi**.  
  
4.  Di bawah **Sinkronisasi pemesanan sumber daya dengan Outlook**, periksa **sinkronisasi pemesanan sumber daya dengan Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Impor janji temu pribadi Anda (tugas pengguna)  
 Anda dapat mengimpor janji pribadi Anda dari kalender ke tampilan entri waktu Project service automation.  
  
1. Buka kalender [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] dan klik **impor Data**.  
  
2. Pada layar Filter, pilih **janji temu dari Exchange** dan kemudian klik **Terapkan**.  
  
3. Sistem akan menarik janji temu ke tampilan entri waktu sebagai entri yang disarankan dari minggu saat ini. Untuk menambahkan entri untuk satu minggu, klik **sebelumnya** atau **berikutnya**.  
  
4. Pilih janji temu yang ingin Anda tambahkan ke tampilan entri waktu Project Service Automation.  
  
5. Pada kotak popup **Entri waktu**, pilih opsi yang sesuai untuk mengubah janji temu ke tampilan entri waktu Project service automation.  
  
6. Klik **Simpan**.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan Waktu, biaya dan kolaborasi](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]