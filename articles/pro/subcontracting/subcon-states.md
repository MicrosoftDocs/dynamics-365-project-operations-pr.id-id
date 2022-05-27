---
title: Menyatakan transisi pada subkontrak
description: Ini topik menjelaskan transisi status pada subkontrak di Microsoft Dynamics 365 Project Operations saat subkontrak dibuat, dieksekusi, dan ditutup.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c9533d046398c708c55467e6b1a25acf6abade3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579172"
---
# <a name="state-transitions-on-a-subcontract"></a>Menyatakan transisi pada subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Ini topik menjelaskan transisi status pada subkontrak di Microsoft Dynamics 365 Project Operations. Setiap negara bagian direpresentasikan sebagai draf, dikonfirmasi, ditutup, atau dibatalkan. Gambar berikut mewakili transisi status.

![Model negara subkontrak](../media/SubconStates.png)  

Tabel berikut memberikan deskripsi tentang apa yang diwakili setiap negara bagian dalam siklus hidup subkontrak dalam Operasi Proyek.

| Provinsi | Deskripsi | Transisi yang diizinkan |
| --- | --- | --- |
| Draf | Ini merupakan keadaan awal subkontrak. Negosiasi dengan vendor sedang berlangsung. Garis dan harga tunduk pada modifikasi. Subkontrak di negara bagian ini dapat digunakan untuk memperkirakan dan staf persyaratan proyek untuk sumber daya dan bahan. Hal ini juga dapat dirujuk pada waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini dapat diedit dan dihapus. | Dikonfirmasi |
| Dikonfirmasi | Ini merupakan tahap subkontrak setelah negosiasi dengan vendor tentang harga dan item baris yang dibeli selesai. Namun, pengiriman bahan dan / atau pekerjaan yang sebenarnya oleh sumber daya subkontrak masih berlangsung. Subkontrak di negara bagian ini dapat digunakan untuk memperkirakan dan staf persyaratan proyek untuk sumber daya dan bahan. Hal ini juga dapat dirujuk pada waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. Tombol **Batalkan** memungkinkan Anda membatalkan subkontrak yang dikonfirmasi. Tombol **Buka** kembali memungkinkan Anda membuka kembali subkontrak untuk membawanya kembali ke **status Draft**. Gunakan tombol **Tutup** untuk menutup subkontrak yang dikonfirmasi. | Tutup <br> Dibatalkan <br> Draf |
| Tutup | Ini merupakan tahap subkontrak ketika pengiriman bahan yang sebenarnya dan / atau pekerjaan oleh sumber daya subkontrak selesai. Subkontrak di negara bagian ini tidak dapat lagi digunakan untuk memperkirakan dan staf persyaratan proyek untuk sumber daya dan bahan. Juga, tidak dapat lagi direferensikan pada waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |
| Dibatalkan | Ini merupakan tahap subkontrak ketika pengiriman bahan dan / atau pekerjaan yang sebenarnya oleh sumber daya subkontrak tidak lagi diperlukan. Subkontrak dalam keadaan ini tidak dapat digunakan untuk memperkirakan dan staf persyaratan proyek untuk sumber daya dan bahan atau, dapat dirujuk pada waktu, biaya, dan penggunaan material pada proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
