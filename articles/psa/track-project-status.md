---
title: Lacak status proyek
description: Cara melacak status proyek di Project Service
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149592"
---
# <a name="track-a-projects-status-project-service"></a>Melacak status proyek (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

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
 [Panduan Manajer Proyek](../psa/project-manager-guide.md)
