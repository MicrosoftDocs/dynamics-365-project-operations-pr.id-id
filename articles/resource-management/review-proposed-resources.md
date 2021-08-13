---
title: Tinjau sumber daya yang diusulkan
description: Topik ini menyediakan informasi tentang cara mengusulkan sumber daya proyek.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a9d3f7b9194b29859ee1479fea8158067e22e819e8f190ef1659e14b7c0cd6b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998015"
---
# <a name="review-proposed-resources"></a>Tinjau sumber daya yang diusulkan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek menggunakan permintaan sumber daya.

1. Dari kisi permintaan atau permintaan itu sendiri, pilih **Cari sumber daya**.
2. Di halaman **asisten jadwal**, pilih sumber daya, lalu di panel **buat Pemesanan sumber daya**, di bidang **status Pemesanan**, pilih **Pesan**.

Terjadi pembaruan status berikut:

- Di halaman **asisten jadwal**, indikator status diperbarui untuk menunjukkan bahwa Pemesanan diajukan, bukan pesanan definitif.
- Pada permintaan sumber daya, status berubah menjadi **perlu ditinjau**.
- Pada tab **tim** proyek , nilai **status permintaan** anggota tim generik diubah ke **perlu ditinjau**.

Manajer proyek dapat menerima atau menolak usulan tersebut.

Bila manajer sumber daya memproses permintaan sumber daya, mereka dapat menggunakan salah satu dari pendekatan berikut:

- Mengusulkan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk memenuhi jam yang diperlukan. Jam yang diusulkan kemudian dipecah di antara beberapa sumber daya yang dapat memenuhi jam yang diperlukan. Dalam skenario ini, jam tidak dapat tumpang tindih.
- Mengusulkan sumber daya yang lebih sedikit daripada yang diperlukan. Dalam skenario ini, kapasitas sumber daya yang diusulkan kurang dari jam yang diperlukan yang ditentukan pemohon. Oleh karena itu, bila pemohon menerima sumber daya yang diusulkan, persyaratan sumber daya yang tidak terpenuhi dibuat untuk merekam permintaan yang tersisa.
- Memesan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk menyelesaikan pekerjaan.
- Memesan sumber daya yang lebih sedikit daripada yang diperlukan. Dalam skenario ini, jam yang dipesan kurang dari jam yang diperlukan. Sistem akan memandu Anda mengajukan sumber daya dan bukan Pemesanan, sehingga pemohon dapat memverifikasi dan melacak permintaan yang tersisa.

## <a name="resource-availability"></a>Ketersediaan Sumber Daya

Sangat penting bagi manajer sumber daya untuk dapat melihat ketersediaan sumber daya dan memperbarui Pemesanan. Dalam kasus tertentu, tidak ada permintaan formal (permintaan sumber daya), namun manajer sumber daya harus merespons permintaan yang tidak direncanakan yang berasal dari saluran seperti email, panggilan telepon, atau pesan instan. Manajer sumber daya menggunakan papan jadwal untuk memperbarui sumber daya dan Pemesanan.

Jam kerja sumber daya digunakan sebagai dasar untuk menghitung ketersediaan sumber daya. Pemesanan sumber daya menghabiskan kapasitas sumber daya.

Papan jadwal menggunakan warna dan arsiran untuk menampilkan Pemesanan, ketersediaan, dan pesanan berlebihan, dan juga status pemesanan. Pengaturan di pengaturan papan jadwal memungkinkan Anda menampilkan legenda.

Jika tanda panah menunjuk ke kanan muncul di samping sumber daya yang dapat dipesan individual pada papan jadwal, sumber daya dapat diperluas untuk menampilkan rincian pekerjaan yang dipesan sumber dayanya.

Karena Dynamics 365 Project Operations menggunakan mesin Universal Resource Scheduling, jika Anda juga telah menginstal Dynamics 365 Field Service, Anda dapat melihat rincian pemesanan sumber daya untuk proyek, perintah kerja, dan entitas lain yang telah Anda gunakan untuk memperpanjang penjadwalan.

Untuk melihat rincian lebih lanjut tentang sumber daya individual, klik kanan untuk membuka kartu sumber daya.



[!INCLUDE[footer-include](../includes/footer-banner.md)]