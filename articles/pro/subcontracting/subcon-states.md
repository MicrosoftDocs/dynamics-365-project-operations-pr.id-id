---
title: Menyatakan transisi pada subkontrak
description: Artikel ini menjelaskan transisi status pada subkontrak di Microsoft Dynamics 365 Project Operations saat subkontrak dibuat, dijalankan, dan ditutup.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522938"
---
# <a name="state-transitions-on-a-subcontract"></a>Menyatakan transisi pada subkontrak 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Artikel ini menjelaskan transisi status pada subkontrak di Microsoft Dynamics 365 Project Operations. Setiap status dinyatakan sebagai draf, terkonfirmasi, ditutup, atau dibatalkan. Gambar berikut menunjukkan transisi status.

![Model status subkontrak](../media/SubconStates.png)  

Tabel berikut memberikan deskripsi tentang apa yang menunjukkan setiap status dalam siklus hidup subkontrak dalam Project Operations.

| Provinsi | Description | Transisi yang diizinkan |
| --- | --- | --- |
| Draf | Ini menunjukkan status awal subkontrak. Negosiasi dengan vendor sedang berlangsung. Baris dan harga tergantung modifikasi. Subkontrak dengan status ini dapat digunakan untuk memperkirakan dan mengelola persyaratan proyek untuk sumber daya dan materi. Hal ini juga dapat merujuk pada waktu, pengeluaran, dan penggunaan materi pada proyek. Subkontrak dalam status ini dapat diedit dan dihapus. | Dikonfirmasi |
| Dikonfirmasi | Ini menunjukkan tahapan subkontrak setelah negosiasi dengan vendor pada harga dan item baris yang dibeli telah selesai. Namun, pengiriman aktual materi dan/atau pekerjaan dengan sumber daya subkontrak masih berlangsung. Subkontrak dengan status ini dapat digunakan untuk memperkirakan dan mengelola persyaratan proyek untuk sumber daya dan materi. Hal ini juga dapat merujuk pada waktu, pengeluaran, dan penggunaan materi pada proyek. Subkontrak dalam status ini tidak diedit atau dihapus. Tombol **Batal** memungkinkan Anda membatalkan subkontrak terkonfirmasi. Tombol **Buka ulang** memungkinkan Anda membuka kembali subkontrak untuk mengembalikannya ke status **Draf**. Gunakan tombol **Tutup** untuk menutup subkontrak terkonfirmasi. | Tutup <br> Dibatalkan <br> Draf |
| Tutup | Ini menunjukkan tahapan subkontrak ketika pengiriman materi aktual dan/atau pekerjaan dengan sumber daya subkontrak sudah selesai. Subkontrak dengan status ini tidak bisa lagi digunakan untuk memperkirakan dan mengelola persyaratan proyek untuk sumber daya dan materi. Selain itu juga tidak bisa dirujuk pada waktu, pengeluaran, dan penggunaan materi pada proyek. Subkontrak dalam status ini tidak diedit atau dihapus. | Tidak ada |
| Dibatalkan | Ini menunjukkan tahapan subkontrak ketika pengiriman materi aktual dan/atau pekerjaan dengan sumber daya subkontrak sudah tidak dibutuhkan lagi. Subkontrak dalam status ini tidak dapat digunakan untuk memperkirakan dan mengelola persyaratan proyek untuk sumber daya dan materi atau, dapat dirujuk pada waktu, pengeluaran, dan penggunaan materi pada proyek. Subkontrak dalam status ini tidak diedit atau dihapus. | Tidak ada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
