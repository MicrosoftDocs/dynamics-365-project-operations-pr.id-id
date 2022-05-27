---
title: Bagaimana keterkaitan antara pemesanan sumber daya dan penugasan tugas
description: Topik ini menyediakan informasi tentang cara mengelola sumber daya bernama, pemesanan sumber daya, serta penetapan tugas dan bagaimana keterkaitannya satu sama lain.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 953d7ca1995eae823fd29d0a9e85ff6a2a2eb59b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575483"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Bagaimana keterkaitan antara pemesanan sumber daya dan penugasan tugas

[!include [banner](../includes/psa-now-project-operations.md)]

Sumber daya bernama dapat dipesan ke tim proyek, dan ditetapkan dengan tugas proyek dalam dua cara:

- Sumber daya dapat dipesan secara langsung ke proyek dan ditetapkan ke tugas proyek.
- Tugas dapat ditetapkan ke sumber daya generik, yang kemudian digunakan untuk mencari dan mengganti generik dengan sumber daya bernama. 

Dalam kedua kasus, tindakan Pemesanan sumber daya mencadangkan kapasitas sumber daya.

Manajer Proyek yang merencanakan proyek bertanggung jawab atas rencana proyek dan jadwal. Dengan menggunakan sumber daya generik untuk tugas dan kemudian menghasilkan permintaan sumber daya dari itu manajer proyek dapat memesan sumber daya ke proyek dengan kontur yang ditentukan dalam rencana proyek. Mereka dapat memesan sumber daya ke proyek dan kemudian menetapkan mereka untuk tugas, namun tidak ada cara untuk menyesuaikan kontur Pemesanan dengan kontur tugas. Pemesanan tidak mempengaruhi jadwal proyek.

Pertimbangkan proyek kompleks dengan beberapa tugas tumpang tindih di mana beberapa sumber daya dari jenis yang sama tersebut harus bekerja secara bersamaan. Jika sumber daya diberikan kontur yang berbeda dari agregat tugas mereka, sulit untuk memodifikasi tugas-tugas yang cocok dengan kontur Pemesanan untuk tugas diskrit dan kontur asli mereka.

Di contoh di bawah ini, total upaya yang diperlukan oleh sumber daya yang sama dari rangkaian empat tugas adalah 62 jam selama periode dua minggu dan ada kontur tertentu. Jika sumber daya Bob dipesan 62 jam selama dua minggu yang sama tetapi dengan kontur berbeda, kebutuhan dan Pemesanan selaras.

| **Kontur tugas**    | **Total Jam** | Se 6/4 | Se 6/5 | Ra 6/6 | Ka 6/7 | Ju 6/8 | Sa 6/9 | Mi 6/10 | Se 6/11 | Se 6/12 | Ra 6/13 | Ka 6/14 | Ju 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tugas 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tugas 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tugas 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tugas 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Total**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Ketersediaan Bob
| **Pemesanan Sumber Daya** | **Total Jam** | Se 6/4 | Se 6/5 | Ra 6/6 | Ka 6/7 | Ju 6/8 | Sa 6/9 | Mi 6/10 | Se 6/11 | Se 6/12 | Ra 6/13 | Ka 6/14 | Ju 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Namun, tidak ada cara sistematis untuk menetapkan kontur jam tercatat ke tugas per hari. Jika manajer proyek akan mengubah jadwal proyek untuk memenuhi ketersediaan sumber daya, maka mereka akan harus menghapus penetapan dan mengubah semua tugas yang sesuai dengan kontur pemesanan.

Dalam kasus di mana organisasi telah memberikan tugas perencanaan proyek kepada manajer proyek dan manajer sumber daya, manajer proyek mengatur jadwal, dan yang mencakup contouring pekerjaan yang diperlukan. Manajer sumber daya tidak boleh dapat mempengaruhi jadwal tanpa pengetahuan manajer proyek dengan mengubah upaya kontur saat pemesanan sumber daya nyata. Jika Manajer sumber daya memenuhi sesuatu yang berbeda dari yang manajer proyek minta, mereka harus melakukan Perjanjian tentang perubahan yang diperlukan dalam jadwal proyek.

Karena Pemesanan dan tugas tidak berhubungan erat, Anda akan dapat memesan kontur yang berbeda dari kontur tugas, atau mengubah tugas untuk mengakibatkan situasi di mana Pemesanan dan tugas tidak selaras.

**Tampilan rekonsiliasi** memungkinkan manajer proyek untuk melihat Pemesanan dan tugas untuk tiap anggota tim proyek. Tampilan menggunakan warna dan arsiran untuk menampilkan di mana ada ketidaksesuaian antara Pemesanan anggota tim dan tugas. Berdasarkan informasi ini, manajer proyek dapat mengambil tindakan perbaikan baik memperpanjang Pemesanan sumber daya untuk kasus bila ada tugas dan tidak ada pemesanan atau Batal memesan jika sumber daya dipesan tetapi tidak memiliki tugas.

> [!NOTE]
> Jika Anda memindahkan tugas yang telah Anda bentuk sendiri, kontur ini tidak dipertahankan. Kontur dibuat ulang sesuai kalender proyek ke akun untuk perubahan dalam jam pekerjaan dan hari libur. Ini sengaja karena sistem tidak tahu maksud kontur aslinya dan tidak dapat menentukan apakah sebaiknya mempertahankan kontur tersebut dalam jangka waktu yang baru. Karena Pemesanan dan tugas terhubung, Pemesanan mempertahankan kontur Pemesanan asli. Dalam kasus ini, Anda harus membatalkan dan memesan ulang untuk kontur tugas baru.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
