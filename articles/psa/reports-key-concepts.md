---
title: Konsep kunci
description: Topik ini memberikan informasi tentang konsep utama untuk manajemen sumber daya dalam Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 8e56523a9a2fbe8bc07e6d46062f4e1c20e6d2fa2244b32ff53e96d898b0086c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995090"
---
# <a name="key-concepts"></a>Konsep kunci

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tabel berikut mendefinisikan konsep utama yang digunakan di aplikasi Dynamics 365 Project Service Automation.

| Konsep                    | Definisi |
|----------------------------|------------|
| Anggota Tim Proyek        | Sebagai bagian dari tim proyek, anggota tim proyek dapat berupa sumber daya bernama yang memiliki Pemesanan, sumber daya bernama yang tidak memiliki Pemesanan, atau sumber daya generik. Sumber daya generik tidak memiliki Pemesanan, bersifat lokal untuk proyek, dan tidak memiliki kendala kapasitas di seluruh proyek. |
| Sumber Daya generik proyek   | placeholder sumber daya yang memungkinkan Anda membentuk rencana proyek tim dan staf tanpa harus mengetahui sumber daya bernama. Kalender Proyek digunakan sebagai kalender sumber daya generik. Sumber daya generik dapat ditambahkan ke tim proyek dan ditetapkan ke tugas. |
| Jam yang dipesan               | Jam operasional dipesan secara definitif terhadap proyek untuk membantu menjamin bahwa pekerjaan proyek selesai. Jam pesanan dikonsumsi dari kapasitas keseluruhan sumber daya. Pemesanan hanya didasarkan pada sumber daya bernama, bukan terhadap sumber daya generik. |
| Jam yang Ditetapkan             | Jam sumber daya ditetapkan ke tugas dalam jadwal proyek. Penetapan dapat bertentangan dengan sumber daya bernama atau sumber daya generik. Penetapan dapat terlepas dari pemesanan. |
| Jam yang Diperlukan             | Kapasitas yang diperlukan, namun yang belum dipenuhi oleh sumber daya bernama. Jam yang diperlukan hanya relevan untuk anggota tim generik yang telah membuat persyaratan sumber. |
| Permintaan                     | Beban kerja saat ini dan masuk. Di Project Service Automation, permintaan ditampilkan sebagai persyaratan sumber daya, atau permintaan sumber daya. |
| Persyaratan Sumber Daya       | Entitas yang digunakan untuk mengambil waktu jam, tanggal mulai dan berakhir, keterampilan, geografi, dan dimensi harga lainnya untuk sumber daya yang diperlukan. Persyaratan sumber daya dihasilkan dari anggota tim proyek maupun dibuat secara individual. |
| Permintaan Sumber Daya           | Entitas yang digunakan sebagai 'lingkup" untuk menampung persyaratan yang harus dipenuhi oleh Manajer sumber daya. |
| Peran default sumber daya      | Peran pengelompokan sumber daya untuk perhitungan pemanfaatan. Sumber daya diasumsikan memiliki keterampilan yang diperlukan untuk peran dan untuk memenuhi pemanfaatan target untuk peran tersebut. |
| unit organisasi sumber daya | Unit organisasi yang ditetapkan suatu sumber daya. |
| Kontur                    | Tugas, persyaratan, atau jam penugasan saat dibagi ke dalam distribusi harian. Misalnya, tugas selama lima hari, 40 jam dapat berkontur menjadi delapan jam per hari selama lima hari. |
| Tampilan Rekonsiliasi        | Tampilan yang menampilkan Pemesanan dan tugas untuk setiap anggota tim proyek. Tampilan ini memungkinkan manajer proyek mencari ketidakcocokan antara Pemesanan dan tugas, dan melakukan tindakan perbaikan jika terjadi ketidakcocokan. |
| Jam kerja                 | Entitas yang digunakan untuk mengidentifikasi kapasitas sumber daya, serta jam kerja dan non-kerja. Entitas ini juga disebut sebagai kalender sumber daya. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]