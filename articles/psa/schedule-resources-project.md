---
title: Jadwalkan sumber daya untuk sebuah proyek
description: Cara menjadwalkan sumber daya di Project Service
author: JohnPBurrows
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
ms.openlocfilehash: c67633960bb448d2190ec1bfde4e964f4fcb7969
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008495"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Jadwalkan sumber daya untuk proyek (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Anda dapat memeriksa ketersediaan sumber untuk mendapatkan pandangan yang menyeluruh tentang sepadat apa tingkat pemesanan sumber daya Anda, atau Anda dapat menyaring tampilan menurut keterampilan, tim, lokasi, dan pilihan lainnya.  
  
Papan jadwal menunjukkan daftar sumber daya dan ketersediaan mereka. Pilih mode tampilan untuk menunjukkan ketersediaan menurut **jam**, **hari**, **minggu**, atau **bulan**.  
  
Sebelum Anda menggunakan papan jadwal, sangat penting untuk mengatur itu. Untuk informasi lebih lanjut, lihat [Mengkonfigurasi papan jadwal (Field Service atau Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Jika Anda menggunakan versi yang lebih tua, untuk ketersediaan sumber daya, lihat [Lihat ketersediaan sumber daya](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Untuk menggunakan fungsionalitas pemesanan papan jadwal, geocoding, dan Layanan lokasi, Anda perlu mengaktifkan peta.  
> 
> 1. Di menu utama, pilih **Penjadwalan Sumber daya** > **Administrasi**.  
> 2. Klik **Parameter Penjadwalan**.  
> 3. Buka rekaman dan gulir ke bawah ke bagian **Resource Scheduling Optimization**.  
> 4. Pada bidang **Sambung ke Maps**, pilih **ya**.  
> 5. Tnerima persyaratan dan simpan rekaman.  
> 6. Di menu utama, pilih **Project Service** > **papan jadwal**. Dari sini, ada beberapa cara untuk secara manual menjadwalkan persyaratan pemesanan. Pilih metode yang sesuai untuk Anda.
  
## <a name="find-available-resources"></a>Cari sumber daya tersedia

1.  Dari daftar **persyaratan pemesanan**, klik kanan pada Pemesanan tak terjadwal dan pilih salah satu dari berikut:  
  
- Pilih **Temukan ketersediaan-sumber daya saat ini** untuk menemukan sumber daya yang tersedia dari daftar sumber daya di papan jadwal.  
- Pilih **Temukan ketersediaan - semua sumber daya** untuk menemukan sumber daya yang tersedia dari sumber daya di sistem.  
   > [!NOTE]
   >  Ketika Anda melakukan ini, filter akan menampilkan pilihan untuk persyaratan pemesanan yang dipilih.  
  
2. Ketika Anda melihat slot yang tersedia, klik kanan pada slot waktu pada papan jadwal dan pilih **Pesan di sini**. Atau, tarik dan lepaskan persyaratan pemesanan ke slot waktu yang tersedia.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Pesan sumber daya menggunakan tampilan harian dan temukan mana yang pesanannya di bawah target
  
1.  Pada papan jadwal, pilih **Mode Tampilan** dan pilih **hari**.  
  
    Ini menunjukkan tampilan grid berapa jam sumber daya dipesan per hari dan hari-hari yang mereka bebas.  
  
2.  Klik nama sumber daya yang ingin Anda pesan, dan kemudian pilih **Pesan**.  
  
3.  Pada kotak dialog **Pemesanan sumber daya (membuat)**, pilih proyek yang Anda ingin pesan sumber dayanya bersama dengan metode pemesanan serta waktu mulai dan selesai.  
  
4.  Setelah selesai, pilih **Pesan**.  
  
## <a name="view-to-the-schedule-board"></a>Lihat papan Jadwal
  
1.  Pilih persyaratan pemesanan tak terjadwal dari daftar di bagian bawah.  
  
2.  Tarik persyaratan pemesanan ke slot sumber daya/waktu yang tersedia di papan jadwal.  
  
3.  Setelah selesai, pilih **Pesan**.  
  
### <a name="additional-resources"></a>Sumber daya tambahan  
 [Panduan Manajer Sumber Daya](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]