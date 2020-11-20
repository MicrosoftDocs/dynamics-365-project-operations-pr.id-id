---
title: Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas
description: Topik ini menyediakan informasi tentang cara pemesanan sumber daya bernama untuk tim proyek dan menetapkan tugas.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130177"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda dapat menambahkan sumber daya bernama ke tim proyek Anda dengan memesan secara langsung ke tim. Untuk melakukannya, selesaikan langkah-langkah berikut:

1. Di Project Service Automation, buka **proyek**, lalu pilih proyek yang terbuka yang Anda lakukan saat pemesanan.
2. Pada halaman **proyek**, pada tab **tim**, klik **baru**. 

![Menambahkan anggota tim dari tab tim](media/RM-how-to-1.png)

3. Di kotak dialog **Buat Cepat anggota tim proyek**, pilih sumber daya yang dapat dipesan. Bidang **peran** akan terisi dengan peran default sumber daya jika telah ditugaskan. Anda dapat mengubah peran jika diperlukan. 
4. Pilih tanggal dari dan hingga untuk kebutuhan sumber daya dan pilih metode alokasi kapasitas sumber daya. 
5. Jika Anda ingin agar anggota tim menjadi pemberi izin proyek, Pilih **ya** di bidang **pemberi izin proyek**. Ini akan berarti bahwa anggota tim dapat menyetujui entri waktu dan biaya yang diajukan untuk proyek ini. 
6. Klik **Simpan**.

![Menambahkan anggota tim pada formulir pembuatan cepat](media/RM-how-to-2.png)


Anda sekarang dapat menetapkan sumber daya yang dipesan untuk tugas pada proyek. Pada halaman **proyek**, klik tab **jadwal** untuk menetapkan tugas ke sumber daya baru. Pemilih sumber daya yang diluncurkan dari bidang **sumber daya** di kisi tugas akan menampilkan anggota tim yang dapat Anda pilih.

![Menetapkan anggota tim ke tugas pada tab jadwal](media/RM-how-to-3.png)

Dalam versi 3 untuk Project Service Automation (PSA), Pemesanan sumber daya dan penetapan tugas tidak digabungkan dengan ketat. Ini berarti bahwa saat Anda menggunakan pemilih sumber daya dalam jadwal, Anda dapat menetapkan tugas untuk anggota tim lebih lama dibandingkan Pemesanan mereka tercakup dalam proyek.
Anda dapat melihat perbedaan antara Pemesanan anggota tim dan tugas pada tab **tim** atau pada tab **rekonsiliasi sumber daya**. Anda juga dapat mendamaikan perbedaan antara Pemesanan dan tugas untuk sumber daya dengan tingkat yang lebih rinci.

![Tab rekonsiliasi Sumber Daya](media/RM-how-to-4.png)

Anda juga dapat menggunakan pemilih sumber daya pada tab **jadwal** untuk mencari dan memilih sumber daya yang dapat dipesan yang belum menjadi bagian dari tim proyek. Ini ditampilkan dalam pemilih sumber daya sebagai **sumber daya lainnya**.

![Menetapkan sumber daya anggota non-tim ke tugas](media/RM-how-to-5.png)

Bila Anda melakukannya, sumber daya akan ditambahkan ke tim proyek dan ditetapkan ke tugas, namun tidak ada Pemesanan yang dibuat.

![Anggota tim dengan tugas dan tanpa Pemesanan](media/RM-how-to-6.png)

Anda dapat menggunakan tab **rekonsiliasi** untuk memperluas kemampuan Pemesanan atau **papan jadwal** untuk memesan kapasitas sumber daya ke proyek.

![Memperluas Pemesanan untuk anggota tim pada tab rekonsiliasi sumber daya](media/RM-how-to-7.png)

Setelah anggota tim dipesan pada proyek Anda, Anda dapat menggunakan memelihara Pemesanan atau menggunakan papan jadwal secara langsung untuk mengelola Pemesanan.
