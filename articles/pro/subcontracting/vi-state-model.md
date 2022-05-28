---
title: Transisi status pada faktur vendor
description: Ini topik menjelaskan transisi status pada faktur vendor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584692"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transisi status pada faktur vendor

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Ini topik menjelaskan transisi status pada faktur vendor di Microsoft Dynamics 365 Project Operations. Status berikut digunakan: Draf, Dalam peninjauan **,** Dikonfirmasi **,** Ditahan **, dan** Dibatalkan **.** **·**

Ilustrasi berikut menunjukkan transisi status.

![Model transisi status subkontrak.](../media/VI_State_Model.jpg)

Tabel berikut menjelaskan apa yang diwakili oleh setiap status dalam siklus hidup faktur vendor di Operasi Proyek.

| Provinsi | Deskripsi | Transisi yang diizinkan |
| --- | --- | --- |
| Draf | Status ini adalah status awal faktur vendor. Garis dan harga tunduk pada modifikasi. Faktur vendor dalam status ini dapat diedit dan dihapus. | Dalam proses |
| Sedang ditinjau | Status ini mewakili status pemrosesan faktur vendor. Setidaknya satu baris faktur vendor memiliki status **verifikasi Sedang berlangsung**. | Dikonfirmasi, Ditahan |
| Dikonfirmasi | Status ini mewakili tahap faktur vendor di mana aplikasi telah membuat aktual biaya untuk setiap baris faktur vendor. Setiap aktual biaya terkait yang dicocokkan dengan baris faktur vendor telah dibalik dan diganti dengan aktual biaya dari baris faktur vendor tersebut. Faktur vendor dalam status ini tidak dapat diedit atau dihapus. Anda dapat menggunakan tombol **Batalkan** untuk membatalkan faktur vendor yang dikonfirmasi. Tindakan Batalkan membalikkan dampak tindakan Konfirmasi. | Dibatalkan |
| Ditahan | <p>Status ini merupakan tahap faktur vendor di mana faktur vendor tidak dapat bergerak karena masalah dengan faktur atau status vendor. Faktur vendor di negara bagian ini tidak dapat dikonfirmasi, dibatalkan, diedit, atau dihapus.</p><p>Anda dapat menggunakan tindakan Buka kembali untuk memindahkan faktur vendor ke **status Draf** atau **Dalam peninjauan**. Jika setidaknya satu baris pada faktur vendor memiliki status **verifikasi Sedang berlangsung** atau **Selesai**, faktur vendor akan dibuka kembali di **status Dalam peninjauan**. Jika semua baris pada faktur vendor memiliki status **verifikasi Tidak dimulai**, faktur vendor akan dibuka kembali di **status Draf**.</p> | Draft, Dalam ulasan |
| Dibatalkan | Keadaan ini merupakan tahap subkontrak di mana pengiriman bahan dan / atau pekerjaan yang sebenarnya oleh sumber daya subkontrak tidak lagi diperlukan. Subkontrak dalam keadaan ini tidak dapat digunakan untuk memperkirakan dan staf persyaratan proyek untuk sumber daya dan bahan, dan juga tidak dapat dirujuk pada waktu, biaya, dan penggunaan material pada proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
