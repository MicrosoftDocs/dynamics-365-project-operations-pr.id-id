---
title: Menyatakan transisi pada faktur vendor
description: Artikel ini menjelaskan transisi status pada faktur vendor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261020"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Menyatakan transisi pada faktur vendor

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini menjelaskan transisi status pada faktur vendor di Microsoft Dynamics 365 Project Operations. Status bagian berikut digunakan: **Draf**, **sedang ditinjau**, **Terkonfirmasi**, **Ditahan**, dan **Dibatalkan**.

Ilustrasi berikut menampilkan transisi status.

![Model transisi status subkontrak.](../media/VI_State_Model.jpg)

Tabel berikut menjelaskan apa yang ditunjukkan setiap status dalam siklus hidup faktur vendor dalam Project Operations.

| Provinsi | Description | Transisi yang diizinkan |
| --- | --- | --- |
| Draf | Kondisi ini adalah status awal faktur vendor. Baris dan harga tergantung modifikasi. Faktur Vendor dalam status ini dapat diedit dan dihapus. | Sedang diproses |
| Sedang ditinjau | Kondisi ini mewakili status pemrosesan faktur vendor. Sekurangnya satu baris faktur vendor memiliki status verifikasi **Sedang berlangsung**. | Dikonfirmasi, Ditahan |
| Dikonfirmasi | Kondisi ini menunjukkan tahapan faktur vendor dengan aplikasi telah membuat aktual biaya untuk setiap baris faktur vendor. Aktual biaya tertaut yang cocok dengan baris faktur vendor telah dibalik dan dibandingkan dengan aktual biaya dari baris faktur vendor tersebut. Faktur Vendor dalam status ini tidak dapat diedit atau dihapus. Anda dapat menggunakan tombol **Batal** untuk membatalkan faktur vendor terkonfirmasi. Tindakan Batal akan mengembalikan dampak tindakan Konfirmasi. | Dibatalkan |
| Ditahan | <p>Kondisi ini menunjukkan tahapan faktur vendor dengan faktur vendor tidak dapat bergerak karena masalah dengan faktur atau status vendor. Faktur vendor dalam status ini tidak dapat diedit, dibatalkan, diedit, atau dihapus.</p><p>Anda dapat menggunakan tindakan Buka kembali untuk memindahkan faktur vendor ke status **Draf** atau **sedang ditinjau**. Jika sekurangnya satu baris pada faktur vendor memiliki status verifikasi **Sedang Berlangsung** atau **Selesai**, faktur vendor akan dibuka kembali dalam status **sedang ditinjau**. Jika semua baris pada faktur vendor memiliki status verifikasi **belum dimulai**, faktur vendor akan dibuka kembali dalam status **Draf**.</p> | Draf, Sedang Ditinjau |
| Dibatalkan | Status Ini menunjukkan tahapan subkontrak di mana pengiriman bahan aktual dan/atau pekerjaan dengan sumber daya subkontrak sudah tidak dibutuhkan lagi. Subkontrak dalam status ini tidak dapat digunakan untuk memperkirakan dan mengelola persyaratan proyek untuk sumber daya dan bahan, dan juga tidak dapat dirujuk pada waktu, pengeluaran, dan penggunaan bahan pada proyek. Subkontrak dalam status ini tidak dapat diedit atau dihapus. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
