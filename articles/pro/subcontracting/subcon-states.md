---
title: Transisi negara pada subkontrak
description: Ini topik menjelaskan transisi negara pada subkontrak di Microsoft Dynamics 365 Project Operations sebagai subkontrak dibuat, dieksekusi, dan ditutup.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903690"
---
# <a name="state-transitions-on-a-subcontract"></a>Transisi negara pada subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Ini topik menjelaskan transisi negara pada subkontrak di Microsoft Dynamics 365 Project Operations. Setiap negara diwakili sebagai draft, dikonfirmasi, ditutup, atau dibatalkan. Gambar berikut mewakili transisi negara.

![Model status subkontrak](../media/SubconStates.png)  

Tabel berikut memberikan deskripsi tentang apa yang diwakili masing-masing negara bagian dalam siklus hidup subkontrak dalam Operasi Proyek.

| Provinsi | Deskripsi | Transisi yang diizinkan |
| --- | --- | --- |
| Draf | Ini merupakan keadaan awal dari subkontrak. Negosiasi dengan vendor sedang berlangsung. Garis dan harga tunduk pada modifikasi. Subkontrak di negara bagian ini dapat digunakan untuk memperkirakan dan persyaratan proyek staf untuk sumber daya dan bahan. Hal ini juga dapat dirujuk pada waktu, biaya, dan penggunaan material pada sebuah proyek. Subkontrak dalam keadaan ini dapat diedit dan dihapus. | Dikonfirmasi |
| Dikonfirmasi | Ini merupakan tahap subkontrak setelah negosiasi dengan vendor tentang harga dan item baris yang dibeli selesai. Namun, pengiriman bahan dan / atau pekerjaan yang sebenarnya oleh sumber daya subkontrak masih berlangsung. Subkontrak di negara bagian ini dapat digunakan untuk memperkirakan dan persyaratan proyek staf untuk sumber daya dan bahan. Hal ini juga dapat dirujuk pada waktu, biaya, dan penggunaan material pada sebuah proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. Tombol **Batalkan** memungkinkan Anda membatalkan subkontrak yang dikonfirmasi. Tombol **Buka Kembali memungkinkan Anda untuk membuka kembali** subkontrak untuk membawanya kembali ke **status** Draft. Gunakan **tombol Tutup** untuk menutup subkontrak yang dikonfirmasi. | Tutup <br> Dibatalkan <br> Draf |
| Tutup | Ini merupakan tahap subkontrak ketika pengiriman bahan dan / atau pekerjaan aktual oleh sumber daya subkontrak selesai. Subkontrak di negara bagian ini tidak dapat lagi digunakan untuk memperkirakan dan persyaratan proyek staf untuk sumber daya dan bahan. Juga, tidak dapat lagi dirujuk tepat waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |
| Dibatalkan | Ini merupakan tahap subkontrak ketika pengiriman bahan dan / atau pekerjaan aktual oleh sumber daya subkontrak tidak lagi diperlukan. Subkontrak dalam keadaan ini tidak dapat digunakan untuk memperkirakan dan persyaratan proyek staf untuk sumber daya dan bahan atau, dapat dirujuk tepat waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
