---
title: Mengelola anggota tim
description: Topik ini menyediakan informasi tentang pemesanan sumber daya bernama untuk tim proyek dan tetapkan tugas.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961885"
---
# <a name="maintain-team-members"></a>Mengelola anggota tim

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda dapat menambahkan sumber daya bernama ke tim proyek Anda dengan memesan secara langsung ke tim.

1. Di Dynamics 365 Project Operations, buka **proyek**, lalu pilih proyek yang terbuka yang Anda lakukan pemesanannya.
2. Pada halaman **proyek**, pada tab **tim**, pilih **baru**. 
3. Di kotak dialog **Buat Cepat anggota tim proyek**, pilih sumber daya yang dapat dipesan. Bidang **peran** akan terisi dengan peran default sumber daya jika telah ditugaskan. Anda dapat mengubah peran. 
4. Pilih tanggal dari dan hingga untuk kebutuhan sumber daya dan pilih metode alokasi kapasitas sumber daya. 
5. Jika Anda ingin agar anggota tim menjadi pemberi persetujuan proyek, Pilih **ya** di bidang **pemberi persetujuan proyek**. Anggota tim dapat menyetujui entri waktu dan biaya yang diajukan untuk proyek ini. 
6. Pilih **Simpan**.

Anda sekarang dapat menetapkan sumber daya yang dipesan untuk tugas pada proyek. Pada halaman **proyek**, di tab **jadwal**, tetapkan tugas ke sumber daya baru. Pemilih sumber daya yang diluncurkan dari bidang **sumber daya** di kisi tugas akan menampilkan anggota tim yang dapat Anda pilih.


Dalam Project Operations, Pemesanan sumber daya, dan penetapan tugas tidak digabungkan dengan ketat. Saat Anda menggunakan pemilih sumber daya dalam jadwal, Anda dapat menetapkan tugas untuk anggota tim lebih lama dibandingkan Pemesanan mereka tercakup dalam proyek.

Perbedaan antara Pemesanan anggota tim dan penetapan ditampilkan pada tab **tim** dan **rekonsiliasi sumber daya**. Anda juga dapat mendamaikan perbedaan antara Pemesanan dan tugas untuk sumber daya dengan tingkat yang lebih rinci.

Gunakan pemilih sumber daya pada tab **jadwal** untuk mencari dan memilih sumber daya yang dapat dipesan yang belum menjadi bagian dari tim proyek. Sumber daya ini ditampilkan dalam pemilih sumber daya sebagai **sumber daya lainnya**.

Saat Anda menentukan pilihan, sumber daya akan ditambahkan ke tim proyek dan ditetapkan ke tugas, namun tidak ada Pemesanan yang dibuat.

Anda dapat menggunakan tab **rekonsiliasi** untuk memperluas kemampuan Pemesanan atau **papan jadwal** untuk memesan kapasitas sumber daya ke proyek.

Setelah anggota tim dipesan pada proyek Anda, Anda dapat menggunakan **memelihara Pemesanan** atau **papan jadwal** secara langsung untuk mengelola Pemesanan.
