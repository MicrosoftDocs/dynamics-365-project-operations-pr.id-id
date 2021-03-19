---
title: Mengatur jadwal panjar
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi jadwal panjar di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d90781407f11c93b9fb9e0cd2446e102e216b8db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272272"
---
# <a name="set-up-a-retainer-schedule"></a>Mengatur jadwal panjar

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Jadwal panjar diatur pada halaman **Kontrak Proyek** di Dynamics 365 Project Operations.

1. Pada halaman **kontrak proyek**, pada tab **uang muka dan panjar**, pilih **Atur jadwal panjar**.
2. Pada halaman dialog yang terbuka, bidang yang tercantum dalam tabel berikut akan ditampilkan. Tabel ini memberikan gambaran tentang bagaimana nilai yang dimasukkan mempengaruhi atau mempengaruhi jadwal panjar yang akan dibuat.

| Bidang | KETERANGAN | Dampak hilir |
| --- | --- | --- |
| Pelanggan Kontrak Proyek | Pelanggan di kontrak yang akan ditagih untuk panjar atau uang muka ini. | Jika Anda memiliki beberapa pelanggan pada kontrak, dan jika Anda harus menagih masing-masing untuk panjar atau uang muka tertentu, buat secara manual satu faktur untuk setiap pelanggan. |
| Jadwal Mulai Panjar | Masukkan tanggal mulai jadwal panjar. | Tanggal ini mungkin bukan tanggal panjar atau uang muka pertama dibuat. Tanggal panjar atau uang muka pertama dibuat juga dipengaruhi oleh frekuensi faktur. |
| Jadwal Berakhir Panjar | Masukkan tanggal akhir jadwal panjar. | Tanggal ini mungkin bukan tanggal panjar atau uang muka terakhir dibuat. Tanggal panjar atau uang muka terakhir dibuat juga dipengaruhi oleh frekuensi faktur. |
| Jumlah Panjar yang Akan Dibuat | Bila Anda memasukkan jumlah panjar yang akan dibuat, sistem menggunakan tanggal mulai dan frekuensi untuk membuat nomor dalam bidang ini. | Bila bidang ini diperbarui secara manual, sistem akan mengabaikan nilai pada bidang **akhir jadwal panjar**, dan malah membuat jumlah panjar atau uang muka tertentu. |
| Frekuensi Faktur | Seberapa sering aplikasi akan membuat panjar dan uang muka. | Nilai ini langsung memengaruhi jumlah panjar dan uang muka serta tanggal pembuatan. |
| Jumlah Total | Jumlah total adalah jumlah yang dibagi menjadi panjar atau uang muka individual yang akan dibuat. | Tidak ada dampak hilir untuk bidang ini. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]