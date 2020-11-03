---
title: Tinjau sumber daya yang diusulkan
description: Topik ini menyediakan informasi tentang cara mengusulkan sumber daya proyek.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078451"
---
# <a name="review-proposed-resources"></a>Tinjau sumber daya yang diusulkan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek menggunakan permintaan sumber daya.

1. Dari kisi permintaan atau permintaan itu sendiri, pilih **Cari sumber daya**.
2. Di halaman **asisten jadwal** , pilih sumber daya, lalu di panel **buat Pemesanan sumber daya** , di bidang **status Pemesanan** , pilih **Pesan**.

Terjadi pembaruan status berikut:

- Di halaman **asisten jadwal** , indikator status diperbarui untuk menunjukkan bahwa Pemesanan diajukan, bukan pesanan definitif.
- Pada permintaan sumber daya, status berubah menjadi **perlu ditinjau**.
- Pada tab **tim** proyek , nilai **status permintaan** anggota tim generik diubah ke **perlu ditinjau**.

Manajer proyek dapat menerima atau menolak usulan tersebut.

Bila manajer sumber daya memproses permintaan sumber daya, mereka dapat menggunakan salah satu dari pendekatan berikut:

- Mengusulkan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk memenuhi jam yang diperlukan. Jam yang diusulkan kemudian dipecah di antara beberapa sumber daya yang dapat memenuhi jam yang diperlukan. Dalam skenario ini, jam tidak dapat tumpang tindih.
- Mengusulkan sumber daya yang lebih sedikit daripada yang diperlukan. Dalam skenario ini, kapasitas sumber daya yang diusulkan kurang dari jam yang diperlukan yang ditentukan pemohon. Oleh karena itu, bila pemohon menerima sumber daya yang diusulkan, persyaratan sumber daya yang tidak terpenuhi dibuat untuk merekam permintaan yang tersisa.
- Memesan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk menyelesaikan pekerjaan.
- Memesan sumber daya yang lebih sedikit daripada yang diperlukan. Dalam skenario ini, jam yang dipesan kurang dari jam yang diperlukan. Sistem akan memandu Anda mengajukan sumber daya dan bukan Pemesanan, sehingga pemohon dapat memverifikasi dan melacak permintaan yang tersisa.

## <a name="billable-utilization"></a>Pemanfaatan yang dapat ditagih

Sumber daya dapat memiliki pemanfaatan yang dapat ditagih. Pemanfaatan target ini didefinisikan sebagai atribut pada peran default sumber daya atau diatur pada rekaman sumber daya yang dapat dipesan individual. Penghitungan pemanfaatan didasarkan pada jam aktual yang dilaporkan sumber daya menggunakan entri waktu yang disetujui.

Rumus berikut digunakan untuk menghitung pemanfaatan:

- Pemanfaatan dapat ditagih = Jam aktual dapat ditagih ÷ kapasitas sumber daya
- Pemanfaatan tidak dapat ditagih = waktu aktual dengan ID jenis penagihan = tidak dikenakan biaya, gratis, atau tidak tersedia ÷ kapasitas sumber daya
- Internal = waktu aktual tanpa kontrak penjualan ÷ kapasitas sumber daya
- Kapasitas sumber daya = jam kerja sumber daya – izin absen – hari tidak bekerja

Anda dapat menemukan tampilan **pemanfaatan sumber daya** di panel **sumber daya**.

Setiap sel di kisi mewakili persentase pemanfaatan yang dapat ditagih dari sumber daya dalam periode tertentu, seperti hari, pekan atau bulan. Rumus berikut digunakan untuk mewarnai sel:

- **Hijau:** Pemanfaatan yang ditagih \>= pemanfaatan sumber daya target
- **Kuning:** target pemanfaatan – 20 \<= pemanfaatan ditagih \< target pemanfaatan.
- **mérah:** Pemanfaatan yang ditagih \< pemanfaatan target – 20.

Karena tampilan **pemanfaatan sumber daya** didasarkan pada papan jadwal, Anda dapat menggunakan kemampuan pemfilteran papan jadwal untuk memfilter hasil.

Kisi-kisi mengharuskan Anda menetapkan Pemanfaatan peran atau sumber daya individual. Untuk melakukan konfigurasi ini, buka **sumber daya** \> **peran sumber daya**.

Selain itu, peran default harus ditetapkan ke setiap sumber daya yang dapat dipesan. Buka **Sumber Daya** \> **Sumber daya**. Pada tab **Project Service** , periksa apakah peran sumber daya ditentukan, dan bidang **merupakan default** untuk diatur ke **ya**. Anda dapat menambahkan peran tambahan di mana **merupakan default = Tidak**. Peran jika **merupakan default = Ya** digunakan untuk mengevaluasi pemanfaatan sumber daya terhadap target untuk peran tersebut.

Di tab **Project Service** , Anda juga dapat menetapkan pemanfaatan target individual untuk sumber daya. Perhitungan pemanfaatan kemudian menggunakan pemanfaatan target untuk mengevaluasi target sumber daya bukan target dari peran default sumber daya.

Pemanfaatan ditampilkan untuk sumber daya hanya jika sumber daya telah disetujui, waktu yang dapat ditagih selama periode yang ditampilkan di kisi.

## <a name="resource-availability"></a>Ketersediaan Sumber Daya

Sangat penting bagi manajer sumber daya untuk dapat melihat ketersediaan sumber daya dan memperbarui Pemesanan. Dalam kasus tertentu, tidak ada permintaan formal (permintaan sumber daya), namun manajer sumber daya harus merespons permintaan yang tidak direncanakan yang berasal dari saluran seperti email, panggilan telepon, atau pesan instan. Manajer sumber daya menggunakan papan jadwal untuk memperbarui sumber daya dan Pemesanan.

Jam kerja sumber daya digunakan sebagai dasar untuk menghitung ketersediaan sumber daya. Pemesanan sumber daya menghabiskan kapasitas sumber daya.

Papan jadwal menggunakan warna dan arsiran untuk menampilkan Pemesanan, ketersediaan, dan pesanan berlebihan, dan juga status pemesanan. Pengaturan di pengaturan papan jadwal memungkinkan Anda menampilkan legenda.

Jika tanda panah menunjuk ke kanan muncul di samping sumber daya yang dapat dipesan individual pada papan jadwal, sumber daya dapat diperluas untuk menampilkan rincian pekerjaan yang dipesan sumber dayanya.

Karena Dynamics 365 Project Operations menggunakan mesin Universal Resource Scheduling, jika Anda juga telah menginstal Dynamics 365 Field Service, Anda dapat melihat rincian pemesanan sumber daya untuk proyek, perintah kerja, dan entitas lain yang telah Anda gunakan untuk memperpanjang penjadwalan.

Untuk melihat rincian lebih lanjut tentang sumber daya individual, klik kanan untuk membuka kartu sumber daya.

