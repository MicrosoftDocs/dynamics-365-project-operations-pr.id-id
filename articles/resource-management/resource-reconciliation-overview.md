---
title: Ikhtisar rekonsiliasi sumber daya
description: Topik ini menyediakan informasi tentang memastikan pemesanan sumber daya dan penetapan untuk proyek diselaraskan.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125722"
---
# <a name="resource-reconciliation-overview"></a>Ikhtisar rekonsiliasi sumber daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Untuk anggota tim, Pemesanan dan tugas secara longgar digabungkan. Dengan kata lain, sumber daya dapat memiliki tugas namun tidak ada pemesanan, atau mereka dapat memiliki Pemesanan namun tidak ada tugas. Idealnya, Pemesanan dan penetapan harus selaras, sehingga sumber daya memiliki kapasitas untuk melakukan tugas tugas. Namun, Pemesanan mungkin didasarkan pada ketersediaan, dan waktu tugas dapat berubah saat proyek berlanjut. Oleh karena itu, pasangan longgar Pemesanan dan penugasan memberikan fleksibilitas.

Tab **rekonsiliasi** di formulir **Proyek** memungkinkan manajer proyek merekonsiliasi Pemesanan anggota tim dan tugas mereka untuk tim proyek.

Tab **rekonsiliasi** juga menampilkan Pemesanan dan tugas hingga tingkat penetapan tugas individual untuk setiap anggota tim. Jam ditampilkan di sel yang menunjukkan periode waktu dari bulan ke hari.

Tab juga menampilkan Total keseluruhan bersih untuk proyek, bersama dengan kolom **total**.

Untuk setiap sumber daya, tab akan menghitung perbedaan antara Pemesanan anggota tim dan Rollup tugas anggota tim. Idealnya, perbedaan ini harus 0 (nol). Dengan kata lain, tidak ada perbedaan antara Pemesanan dan tugas. Perbedaan berwarna dan berarsir untuk menarik perhatian ke dua kondisi:

- **Kekurangan Pemesanan** – kekurangan Pemesanan terjadi bila sumber daya memiliki lebih banyak tugas daripada Pemesanan. Karena kapasitas ini belum dicadangkan, manajer proyek mungkin ingin memperbaiki kondisi ini dengan memperluas Pemesanan sumber daya untuk mengatasi defisit.
- **Pemesanan berlebih** – kelebihan Pemesanan terjadi saat sumber daya telah dipesan ke proyek namun belum ditetapkan ke tugas. Kondisi ini mungkin dapat diterima dalam kasus saat sumber daya dipesan ke proyek sebelum penetapan tugas terjadi. Namun, dalam kasus lain, sumber daya tidak direncanakan untuk ditetapkan ke tugas. Dalam kasus ini, manajer proyek harus mempertimbangkan membatalkan pemesanan sumber daya, sehingga kapasitas dapat digunakan untuk proyek lain.

Dalam kasus tertentu, bila Anda melihat waktu pada tingkat yang lebih tinggi daripada tingkat hari (misalnya, tingkat bulan), Anda mungkin melihat perbedaan bersih nol untuk sumber daya (dengan kata lain, Pemesanan = penetapan). Namun, jika Anda melihat waktu di tingkat minggu, Anda mungkin melihat bahwa ada tugas yang dilakukan nol jam dan Pemesanan 40 jam di minggu pertama, namun penetapan 40 jam dan Pemesanan dalam nol jam di minggu kedua. Secara keseluruhan, Pemesanan dan penugasan akan didamaikan, namun berbeda dari satu minggu ke hari berikutnya.

Bila Anda melihat waktu di tingkat yang lebih tinggi, sel dalam tab **rekonsiliasi** memiliki indikator untuk menginformasikan bahwa ada perbedaan pada tingkat yang lebih rendah. Dengan mengklik dua kali di sel, Anda dapat memperbesar untuk melihat perbedaannya. Anda kemudian dapat klik kanan untuk memperkecil. Dengan memilih sumber daya, lalu menggunakan kontrol **perbedaan berikutnya** pada Toolbar kisi, Anda dapat membuka perbedaan berikutnya antara Pemesanan dan tugas untuk sumber daya tersebut. Selanjutnya Anda dapat menggunakan kontrol **perbedaan sebelumnya** untuk kembali. Anda juga dapat menonaktifkan indikator perbedaan dan perilaku navigasi dalam **pengaturan**.


Jika Anda memiliki penetapan tugas untuk sumber daya, namun tidak ada pemesanan, pada halaman **proyek**, pada tab **rekonsiliasi**, pilih kekurangan Pemesanan, lalu pilih **Perluas Pemesanan**. Kotak dialog **Perluas Pemesanan** muncul dan menunjukkan Pemesanan yang diperlukan untuk mengatasi kekurangan sumber daya. Juga menampilkan Pemesanan sumber daya yang ada di seluruh proyek atau entitas yang dapat dijadwalkan lainnya. Jika Anda memilih **OK** untuk membuat pemesanan untuk sumber daya, terlepas dari ketersediaan sumber daya tersebut, Anda dapat menyebabkan pemesanan berlebihan.

Manajer proyek atau manajer sumber daya kemudian dapat menggunakan papan jadwal untuk mengelola setiap situasi dengan sumber daya yang dipesan berlebihan di luar kapasitasnya.

