---
title: Menyatakan transisi pada faktur vendor
description: Artikel ini menjelaskan transisi status pada faktur vendor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934324"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Menyatakan transisi pada faktur vendor

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini menjelaskan transisi status pada faktur vendor di Microsoft Dynamics 365 Project Operations. Status berikut digunakan: Draf **,** Dalam peninjauan **,** Dikonfirmasi **,** Ditahan **, dan** Dibatalkan **.**

Ilustrasi berikut menunjukkan transisi status.

![Model transisi status subkontrak.](../media/VI_State_Model.jpg)

Tabel berikut menjelaskan apa yang diwakili oleh setiap status dalam siklus hidup faktur vendor dalam Operasi Proyek.

| Provinsi | Deskripsi | Transisi yang diizinkan |
| --- | --- | --- |
| Draf | Status ini adalah status awal faktur vendor. Garis dan harga dapat dimodifikasi. Faktur vendor dalam status ini dapat diedit dan dihapus. | Dalam proses |
| Sedang ditinjau | Status ini mewakili status pemrosesan faktur vendor. Setidaknya satu baris faktur vendor memiliki status **verifikasi Sedang berlangsung**. | Dikonfirmasi, Ditahan |
| Dikonfirmasi | Status ini mewakili tahap faktur vendor di mana aplikasi telah membuat aktual biaya untuk setiap baris faktur vendor. Setiap aktual biaya tertaut yang dicocokkan dengan baris faktur vendor telah dibalik dan diganti dengan aktual biaya dari baris faktur vendor tersebut. Faktur vendor dalam status ini tidak dapat diedit atau dihapus. Anda dapat menggunakan tombol **Batal** untuk membatalkan faktur vendor yang dikonfirmasi. Tindakan Batalkan membatalkan membalikkan dampak tindakan Konfirmasi. | Dibatalkan |
| Ditahan | <p>Status ini mewakili tahap faktur vendor di mana faktur vendor tidak dapat dipindahkan karena masalah dengan faktur atau status vendor. Faktur vendor dalam status ini tidak dapat dikonfirmasi, dibatalkan, diedit, atau dihapus.</p><p>Anda dapat menggunakan tindakan Buka kembali untuk memindahkan faktur vendor ke **Draf** atau **Dalam status Peninjauan**. Jika setidaknya satu baris pada faktur vendor memiliki status **verifikasi Sedang Berlangsung** atau **Selesai**, faktur vendor akan dibuka kembali dalam **status Dalam peninjauan**. Jika semua baris pada faktur vendor memiliki status **verifikasi Tidak dimulai**, faktur vendor akan dibuka kembali di **negara bagian Draf**.</p> | Draf, Dalam peninjauan |
| Dibatalkan | Keadaan ini mewakili tahap subkontrak di mana pengiriman aktual materi dan / atau pekerjaan oleh sumber daya yang disubkontrakkan tidak lagi diperlukan. Subkontrak di negara bagian ini tidak dapat digunakan untuk memperkirakan dan staf persyaratan proyek untuk sumber daya dan bahan, dan juga tidak dapat dirujuk tepat waktu, biaya, dan penggunaan material pada suatu proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
