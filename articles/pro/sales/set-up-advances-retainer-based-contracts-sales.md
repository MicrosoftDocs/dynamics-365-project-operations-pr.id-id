---
title: Kontrak berbasis uang muka dan panjar - lite
description: Topik ini memberikan informasi tentang uang muka dan model kontrak berbasis panjar dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180871"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Kontrak berbasis uang muka dan panjar - lite


_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Dynamics 365 Project Operations mendukung kontrak berbasis panjar. Kontrak berbasis panjar adalah serangkaian negosiasi pembayaran terdistribusi merata yang akan ditagih oleh pelanggan selama durasi proyek. Jenis kontrak ini biasanya digunakan untuk model penagihan berdasarkan waktu dan bahan atau berdasarkan konsumsi di mana ada kebutuhan untuk memberikan pelanggan faktur yang dapat diprediksi dan jadwal pembayaran. Aktual pendapatan yang diperoleh setiap periode akan direkonsiliasi dengan pembayaran yang diterima dari pelanggan pada awal periode. Sesuai dengan konsep model penagihan waktu dan material, nilai pendapatan yang diperoleh di setiap periode dapat berbeda dengan biaya yang dikeluarkan. Jika pendapatan yang diperoleh lebih dari jumlah yang diterima pada awal periode, perusahaan pengiriman proyek dapat:

- Hanya memfaktur pelanggan untuk kelebihannya 
- Menunda rekonsiliasi pendapatan ke periode faktur berikutnya dan melakukan satu tagihan akhir di akhir proyek untuk setiap pendapatan yang tidak dapat direkonsiliasi

Perbedaan utama antara model kontrak berbasis panjar dan model kontrak harga tetap dalam Project Operations adalah bahwa dalam model kontrak harga tetap, jumlah faktur tidak ditautkan atau dihubungkan ke biaya yang dikeluarkan. Faktur mengikuti pendekatan berbasis tonggak pencapaian yang disesuaikan dengan biaya yang dikeluarkan selama periode tersebut. Pada kontrak berbasis panjar, pendapatan yang dapat ditagih akan dicatat berdasarkan metode penagihan pada baris kontrak. Bila metode penagihan adalah waktu dan material, pendapatan yang disetujui akan dikaitkan dengan biaya yang dikeluarkan dalam periode tertentu dan dapat bervariasi dari periode ke periode. Namun, pelanggan hanya ditagih untuk jumlah pada panjar berkala. Sistem menggunakan faktur lain di akhir periode untuk merekonsiliasi pendapatan yang dapat ditagih yang tercatat selama periode terhadap jumlah di mana pelanggan ditagih pada awal periode.

Keuntungan dari metode ini adalah bahwa biaya pelanggan menjadi diprediksi dalam jadwal panjar, tidak seperti pada model waktu dan material umumnya. Organisasi yang melaksanakan proyek juga memiliki beberapa ruang untuk menutupi risiko pemulihan biaya yang ditimbulkan karena meningkatnya cakupan yang tidak akan dimungkinkan oleh model harga tetap.

Selain jadwal berbasis panjar periodik, Project Operations dapat mencatat uang muka satu kali dari pelanggan dan merekonsiliasinya terhadap komponen biaya proyek yang berbeda.

Panjar di Project Operations tidak tersedia untuk digunakan hingga ditagih kepada pelanggan. Hal ini ditunjukkan oleh bidang berikut pada subkisi untuk panjar dan uang muka.

| Bidang | KETERANGAN | Dampak hilir |
| --- | --- | --- |
| Jumlah Tersedia | Jumlah yang tersedia untuk digunakan pada rekaman panjar atau uang muka. | Hingga panjar atau uang muka ditagih, ia tidak tersedia untuk digunakan yang berarti jumlah yang tersedia akan menjadi nol. |
| Jumlah Digunakan | Jumlah yang sudah digunakan pada panjar atau uang muka. | Panjar atau uang muka sebagian dapat direkonsiliasi pada faktur dengan biaya aktual yang akan memiliki beberapa bagian yang ditandai sebagai telah digunakan atau dikonsumsi. Sisa jumlah panjar atau uang muka tersedia untuk direkonsiliasi pada faktur berikutnya dengan biaya aktual. |
