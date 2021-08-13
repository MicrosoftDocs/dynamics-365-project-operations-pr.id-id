---
title: Menentukan biaya baris kuotasi berbasis produk
description: Topik ini menyediakan informasi tentang menerapkan harga biaya ke baris kuotasi berbasis produk.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d9c03fa1a8f43cc110565efbafd7f5aba69f65f96bec7f15f2bd492123f639c7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001885"
---
# <a name="costing-product-based-quote-lines"></a>Menentukan biaya baris kuotasi berbasis produk

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Baris kuotasi berbasis produk di Dynamics 365 Project Operations juga memiliki bidang **Harga Biaya**. Bidang ini digunakan untuk melacak harga untuk produk pada penghitungan baris kuotasi dan untuk profitabilitas hilir.

Bila baris kuotasi berbasis produk dibuat untuk produk Katalog, biaya baris kuotasi berbasis produk akan diisi default dari bidang **biaya standar** dalam Katalog Produk. Bidang biaya standar di Katalog Produk diatur dalam mata uang dasar organisasi. Biaya unit default pada baris kuotasi berdasarkan produk dikonversi ke mata uang penjualan pada kuotasi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Biaya per unit pada baris kuotasi berbasis produk

Tujuan memiliki biaya unit pada baris kuotasi berbasis produk adalah untuk memungkinkan biaya yang berbeda untuk produk untuk setiap penjualan. Ini bukan skenario umum, namun terkadang biaya produk dapat didiskon oleh pemasok tergantung pada pelanggan penjualan akhir.

Misalnya:

Fabrikam robotik memasang lengan robotik di lini perakitan A Datum Corporation. Fabrikam menyediakan layanan penginstalan tetapi senjata robotik Diperoleh dari Trey Robotika. Jika pemasangan senjata robot di A Datum Corporation membuka industri vertikal baru untuk lengan robot Trey, Trey dapat memberikan diskon khusus untuk penawaran ini ke fabrikam.

Dalam kasus ini, fabrikam akan membuat baris kuotasi berbasis produk untuk lengan robot dan memasukkan biaya khusus per unit untuk kuotasi ini. Biaya ini berbeda dari biaya standar lengan Trey Robotic.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]