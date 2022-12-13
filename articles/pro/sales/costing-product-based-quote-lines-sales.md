---
title: Menentukan biaya baris kuotasi berbasis produk
description: artikel ini menyediakan informasi tentang menerapkan harga biaya ke baris kuotasi berbasis produk.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825615"
---
# <a name="costing-product-based-quote-lines"></a>Menentukan biaya baris kuotasi berbasis produk

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Baris kuotasi berbasis produk di Dynamics 365 Project Operations juga memiliki bidang **Harga Biaya**. Bidang ini digunakan untuk melacak harga untuk produk pada penghitungan baris kuotasi dan untuk profitabilitas hilir.

Bila baris kuotasi berbasis produk dibuat untuk produk Katalog, biaya baris kuotasi berbasis produk akan diisi default dari bidang **biaya standar** dalam Katalog Produk. Bidang biaya standar di Katalog Produk diatur dalam mata uang dasar organisasi. Biaya unit default pada baris kuotasi berdasarkan produk dikonversi ke mata uang penjualan pada kuotasi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Biaya per unit pada baris kuotasi berbasis produk

Tujuan memiliki biaya unit pada baris kuotasi berbasis produk adalah untuk memungkinkan biaya yang berbeda untuk produk untuk setiap penjualan. Ini bukan skenario umum, namun terkadang biaya produk dapat didiskon oleh pemasok tergantung pada pelanggan penjualan akhir.

Misalnya:

Fabrikam robotik memasang lengan robotik di lini perakitan A Datum Corporation. Fabrikam menyediakan layanan penginstalan tetapi senjata robotik Diperoleh dari Trey Robotika. Jika pemasangan senjata robot di A Datum Corporation membuka industri vertikal baru untuk lengan robot Trey, Trey dapat memberikan diskon khusus untuk penawaran ini ke fabrikam.

Dalam kasus ini, fabrikam akan membuat baris kuotasi berbasis produk untuk lengan robot dan memasukkan biaya khusus per unit untuk kuotasi ini. Biaya ini berbeda dari biaya standar lengan Trey Robotic.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
