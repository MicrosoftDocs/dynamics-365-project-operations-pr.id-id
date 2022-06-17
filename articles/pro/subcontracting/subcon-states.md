---
title: Menyatakan transisi pada subkontrak
description: Artikel ini menjelaskan transisi status pada subkontrak di Microsoft Dynamics 365 Project Operations saat subkontrak dibuat, dijalankan, dan ditutup.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919742"
---
# <a name="state-transitions-on-a-subcontract"></a>Menyatakan transisi pada subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini menjelaskan transisi status pada subkontrak di Microsoft Dynamics 365 Project Operations. Setiap negara bagian direpresentasikan sebagai draf, dikonfirmasi, ditutup, atau dibatalkan. Gambar berikut mewakili transisi status.

![Model status subkontrak](../media/SubconStates.png)  

Tabel berikut ini memberikan deskripsi tentang apa yang diwakili oleh setiap status dalam siklus hidup subkontrak dalam Operasi Proyek.

| Provinsi | Deskripsi | Transisi yang diizinkan |
| --- | --- | --- |
| Draf | Ini mewakili keadaan awal subkontrak. Negosiasi dengan vendor sedang berlangsung. Garis dan harga dapat dimodifikasi. Subkontrak di negara bagian ini dapat digunakan untuk memperkirakan dan staf memproyeksikan persyaratan untuk sumber daya dan bahan. Ini juga dapat dirujuk tepat waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini dapat diedit dan dihapus. | Dikonfirmasi |
| Dikonfirmasi | Ini merupakan tahap subkontrak setelah negosiasi dengan vendor tentang harga dan item baris yang dibeli selesai. Namun, pengiriman bahan dan/atau pekerjaan aktual dengan sumber daya yang disubkontrakkan masih berlangsung. Subkontrak di negara bagian ini dapat digunakan untuk memperkirakan dan staf memproyeksikan persyaratan untuk sumber daya dan bahan. Ini juga dapat dirujuk tepat waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. Tombol **Batal** memungkinkan Anda membatalkan subkontrak yang dikonfirmasi. Tombol **Buka kembali** memungkinkan Anda membuka kembali subkontrak untuk mengembalikannya ke **status Draf**. Gunakan tombol **Tutup** untuk menutup subkontrak yang dikonfirmasi. | Tutup <br> Dibatalkan <br> Draf |
| Tutup | Ini merupakan tahap subkontrak ketika pengiriman aktual materi dan / atau pekerjaan oleh sumber daya yang disubkontrakkan selesai. Subkontrak di negara bagian ini tidak dapat lagi digunakan untuk memperkirakan dan staf memproyeksikan persyaratan untuk sumber daya dan bahan. Selain itu, tidak dapat lagi dirujuk tepat waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |
| Dibatalkan | Ini merupakan tahap subkontrak ketika pengiriman material yang sebenarnya dan/atau pekerjaan dengan sumber daya yang disubkontrakkan tidak lagi diperlukan. Subkontrak dalam keadaan ini tidak dapat digunakan untuk memperkirakan dan persyaratan proyek staf untuk sumber daya dan bahan juga tidak, dapat dirujuk tepat waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
