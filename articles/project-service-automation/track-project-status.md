---
title: Lacak status proyek
description: Cara melacak status proyek di Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752507"
---
# <a name="track-a-projects-status-project-service"></a>Melacak status proyek (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Gunakan [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] untuk melacak kemajuan proyek klien.  

Seiring perkembangan keterlibatan, tahap proyek diperbarui untuk mencerminkan tahap keterlibatan:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Baru**    | Bila Anda membuat sebuah proyek, tahapan diatur ke **Baru**. Jika Anda membuat proyek dari template, pada tahap ini proyek mungkin memiliki jadwal, perkiraan dan data tim. Jika tidak, itu akan menjadi garis besar proyek dan Anda harus secara manual memasukkan seluruh komponen proyek. |
|  **Kuotasi**   |      Ketika Anda menghubungkan sebuah proyek dengan kuotasi atau membuatnya dari kuotasi, tahapan proyek diatur ke **kuotasi**, dan perkiraan awal dan akhir tanggal juga diperbarui. Ketika proyek pada tahapan kuotasi, rincian pada kuotasi ditampilkan pada tab **Sales** pada halaman **proyek**.      |
|   **Rencana**   |                                     Ketika Anda memenangkan kuotasi yang berkaitan dengan proyek, dan ketika keterlibatan berkembang ke tahapan kontrak, tahapan proyek diperbarui ke **rencana**. Rincian kontrak ditampilkan pada tab **Sales** pada halaman **proyek**.                                      |
| **Selesai** |                    Ketika pekerjaan proyek selesai, Anda dapat mengubah tahapan ke **Selesai**. Ketika tahapan proyek diatur ke selesai, dapat dipahami bahwa pekerjaan 100% selesai tetapi proyek dibiarkan terbuka untuk waktu yang tertunda atau entri pengeluaran direkam.                     |
|  **Tutup**   |           Ketika semua transaksi telah tercatat pada proyek dan Anda tidak berharap lagi untuk login, Anda dapat secara manual mengatur tahapan ke **Tutup**. Ketika proyek diatur ke **Tutup**, Anda tidak dapat mencatat lebih banyak transaksi pada proyek dan proyek akan menjadi hanya baca.           |

## <a name="to-track-a-projects-status"></a>Untuk melacak status proyek  

1.  Pergi ke **Project Service > Proyek**.  

2.  Klik proyek yang ingin Anda kerjakan.  

3.  Di bar di bagian atas layar, pilih panah bawah di sebelah nama proyek, dan kemudian klik **Pelacakan Proyek**.  

4.  Pilih **pelacakan usaha** atau **pelacakan biaya** dalam daftar drop-down di atas daftar tugas.  

5.  Klik dua kali setiap tugas untuk mengeditnya. Anda juga dapat memindahkan atau mengubah ukuran Bar di Gantt chart untuk mengubah waktu dan kemajuan untuk tugas.  

### <a name="see-also"></a>Lihat Juga  
 [Panduan Manajer Proyek](../project-service/project-manager-guide.md)
