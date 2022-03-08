---
title: Menentukan biaya baris kuotasi berbasis produk
description: Topik ini menyediakan informasi tentang menerapkan harga biaya ke baris kuotasi berbasis produk.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078387"
---
# <a name="costing-product-based-quote-lines"></a>Menentukan biaya baris kuotasi berbasis produk

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Baris kuotasi berbasis produk di Dynamics 365 Project Operations juga memiliki bidang **harga biaya**. Bidang ini digunakan untuk melacak harga untuk produk pada penghitungan baris kuotasi dan untuk profitabilitas hilir.

Bila baris kuotasi berbasis produk dibuat untuk produk Katalog, biaya baris kuotasi berbasis produk akan diisi default dari bidang **biaya standar** dalam Katalog Produk. Bidang biaya standar di Katalog Produk diatur dalam mata uang dasar organisasi. Biaya unit default pada baris kuotasi berdasarkan produk dikonversi ke mata uang penjualan pada kuotasi.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Biaya per unit pada baris kuotasi berbasis produk

Tujuan memiliki biaya unit pada baris kuotasi berbasis produk adalah untuk memungkinkan biaya yang berbeda untuk produk untuk setiap penjualan. Ini bukan skenario umum, namun terkadang biaya produk dapat didiskon oleh pemasok tergantung pada pelanggan penjualan akhir.

Misalnya:

Fabrikam robotik memasang lengan robotik di lini perakitan A Datum Corporation. Fabrikam menyediakan layanan penginstalan tetapi senjata robotik Diperoleh dari Trey Robotika. Jika pemasangan senjata robot di A Datum Corporation membuka industri vertikal baru untuk lengan robot Trey, Trey dapat memberikan diskon khusus untuk penawaran ini ke fabrikam.

Dalam kasus ini, fabrikam akan membuat baris kuotasi berbasis produk untuk lengan robot dan memasukkan biaya khusus per unit untuk kuotasi ini. Biaya ini berbeda dari biaya standar lengan Trey Robotic.
