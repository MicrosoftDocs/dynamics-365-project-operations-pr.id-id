---
title: Analisis kuotasi proyek
description: Topik ini menyediakan informasi tentang analisis kuotasi proyek.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078600"
---
# <a name="analysis-of-project-quotes"></a>Analisis kuotasi proyek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation menganalisis kuotasi proyek untuk memperkirakan profitabilitas. Juga menganalisis seberapa baik kuotasi selaras dengan ekspektasi pelanggan tentang tanggal pengiriman atau tanggal selesai, dan tentang anggaran.

## <a name="profitability-analysis"></a>Analisis Profitabilitas

Project Service Automation menganalisis profitabilitas menggunakan margin kotor dan margin kotor yang disesuaikan.

- Margin kotor dihitung menggunakan rumus berikut:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Margin kotor yang disesuaikan dihitung menggunakan rumus berikut:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Jika nilai margin kotor dan margin kotor yang disesuaikan berbeda dengan margin yang lebar, sebagian besar pekerjaan dalam kuotasi diklasifikasikan sebagai tidak dikenakan biaya.

## <a name="analysis-of-customer-expectations"></a>Analisis Harapan Pelanggan

Anda dapat menganalisis kuotasi dan membuat diagram untuk ekspektasi pelanggan tentang jadwal dan anggaran jika Anda memasukkan nilai untuk bidang berikut:

- Bidang **tanggal pengiriman diminta** pada header kuotasi.
- Bidang **anggaran pelanggan** untuk setiap baris kuotasi (untuk baris berbasis proyek dan baris berbasis produk).

Analisis ekspektasi pelanggan tentang jadwal dilakukan dengan membandingkan tanggal akhir terbaru detail baris kuotasi dengan tanggal pengiriman yang diminta di semua baris kuotasi dalam kuotasi.

Analisis ekspektasi pelanggan tentang anggaran dilakukan dengan membandingkan jumlah total anggaran pelanggan dengan jumlah yang dikutip di semua baris kuotasi.
