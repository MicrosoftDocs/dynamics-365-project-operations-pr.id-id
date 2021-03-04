---
title: Ikhtisar rekonsiliasi sumber daya
description: Informasi topik ini memberikan informasi yang membantu Anda memastikan bahwa pemesanan dan penetapan sumber daya untuk proyek selaras.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
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
ms.openlocfilehash: 8723cfad1e7cd07774e37023c5427b0a5833a554
ms.sourcegitcommit: cffc84187007b34211c90babef8af5152d4d92ea
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/12/2021
ms.locfileid: "4849628"
---
# <a name="resource-reconciliation-overview"></a>Ikhtisar rekonsiliasi sumber daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Untuk anggota tim, Pemesanan dan tugas secara longgar digabungkan. Dengan kata lain, sumber daya dapat memiliki tugas dan tidak ada pemesanan, atau mereka dapat memiliki Pemesanan dan tidak ada tugas. Idealnya, Pemesanan dan penetapan harus selaras, sehingga sumber daya memiliki kapasitas untuk melakukan tugas tugas. Namun, Pemesanan mungkin didasarkan pada ketersediaan, dan waktu tugas dapat berubah saat proyek berlanjut. Oleh karena itu, pasangan longgar Pemesanan dan penugasan memberikan fleksibilitas.

Tab **rekonsiliasi** di halaman **Proyek** memungkinkan manajer proyek merekonsiliasi Pemesanan anggota tim dan tugas mereka untuk tim proyek.

Tab **rekonsiliasi** menampilkan Pemesanan dan tugas hingga tingkat penetapan tugas individual untuk setiap anggota tim. Jam ditampilkan di sel yang mewakili periode waktu dari bulan ke hari. Tab juga menampilkan Total keseluruhan bersih untuk proyek, bersama dengan kolom **total**.

Untuk setiap sumber daya, tab **Rekonsiliasi** akan menghitung perbedaan antara Pemesanan anggota tim dan Rollup tugas anggota tim itu. Idealnya, perbedaan ini harus 0 (nol). Dengan kata lain, tidak ada perbedaan antara Pemesanan dan tugas. Perbedaan berwarna dan berarsir untuk menarik perhatian ke dua kondisi:

- **Kekurangan Pemesanan** – kekurangan Pemesanan terjadi bila sumber daya memiliki lebih banyak tugas daripada Pemesanan. Karena kapasitas tersebut belum dicadangkan, manajer proyek mungkin ingin memperbaiki kondisi ini dengan memperluas Pemesanan sumber daya untuk mengatasi defisit.
- **Pemesanan berlebih** – kelebihan Pemesanan terjadi saat sumber daya telah dipesan ke proyek namun belum ditetapkan ke tugas. Kondisi ini mungkin dapat diterima dalam kasus saat sumber daya dipesan ke proyek sebelum penetapan tugas terjadi. Namun, dalam kasus lain, dengan tidak ada rencana untuk menetapkan sumber daya ke tugas, manajer proyek harus mempertimbangkan untuk membatalkan pemesanan sumber daya. Dengan begitu, kapasitas dapat digunakan untuk proyek lain.

Dalam kasus tertentu, bila Anda melihat waktu pada tingkat yang lebih tinggi daripada tingkat hari (misalnya, tingkat bulan), Anda mungkin melihat perbedaan bersih nol untuk sumber daya (dengan kata lain, Pemesanan sama dengan penetapan). Namun, jika Anda melihat waktu di tingkat minggu, Anda mungkin melihat bahwa ada tugas yang dilakukan nol jam dan Pemesanan 40 jam di minggu pertama, namun penetapan 40 jam dan Pemesanan dalam nol jam di minggu kedua. Secara keseluruhan, Pemesanan dan penugasan akan didamaikan, namun berbeda dari satu minggu ke hari berikutnya.

Bila Anda melihat waktu di tingkat yang lebih tinggi, sel di tab **rekonsiliasi** memiliki indikator untuk menginformasikan bahwa ada perbedaan pada tingkat yang lebih rendah. Dengan mengetuk dua kali atau mengklik dua kali di sel, Anda dapat memperbesar untuk melihat perbedaannya. Anda kemudian dapat memilih dan menahan (atau mengeklik kanan) untuk memperkecil. Dengan memilih sumber daya, lalu menggunakan kontrol **perbedaan berikutnya** pada Toolbar kisi, Anda dapat membuka perbedaan berikutnya antara Pemesanan dan tugas untuk sumber daya tersebut. Selanjutnya Anda dapat menggunakan kontrol **perbedaan sebelumnya** untuk kembali. Anda juga dapat menonaktifkan indikator perbedaan dan perilaku navigasi dalam **pengaturan**.

Jika Anda memiliki penetapan tugas untuk sumber daya, pilih kekurangan pemesanan di tab **Rekonsiliasi** dari halaman **proyek**, kemudian pilih **Perluas Pemesanan**. Kotak dialog **Perluas Pemesanan** yang muncul dan menunjukkan Pemesanan yang diperlukan untuk mengatasi kekurangan sumber daya. Kotak dialog juga menampilkan Pemesanan sumber daya yang ada di seluruh proyek atau entitas yang dapat dijadwalkan lainnya. Jika Anda memilih **OK** untuk membuat pemesanan untuk sumber daya, terlepas dari ketersediaan sumber daya tersebut, Anda dapat menyebabkan pemesanan berlebihan.

Pemesanan yang dibuat melalui tindakan **Perluas Pemesanan** dikaitkan dengan kebutuhan proyek utama. Bila perluasan diawali, persyaratan khusus yang harus diperluas tidak dapat ditentukan karena sumber daya mungkin terkait dengan lebih dari satu persyaratan untuk proyek.

Manajer proyek atau manajer sumber daya kemudian dapat menggunakan papan jadwal untuk mengelola setiap situasi dengan sumber daya yang dipesan berlebihan di luar kapasitasnya.


[!INCLUDE[footer-include](../includes/footer-banner.md)]