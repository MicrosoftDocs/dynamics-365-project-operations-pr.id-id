---
title: Menentukan biaya baris kontrak berbasis produk - lite
description: Topik ini menyediakan informasi tentang pembuatan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764463"
---
# <a name="cost-product-based-contract-lines---lite"></a>Menentukan biaya baris kontrak berbasis produk - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Baris kontrak berbasis produk di Dynamics 365 Project Operations mencakup bidang **Harga Biaya**, yang menyimpan harga biaya produk untuk perhitungan profitabilitas hilir.

Bila baris kontrak berbasis produk dibuat untuk produk katalog, biaya baris di-default dari bidang **Biaya Standar** di katalog produk. Bidang **biaya standar** di Katalog Produk diatur dalam mata uang dasar organisasi. Bila unit biaya di-default pada baris kontrak, maka akan diubah menjadi mata uang penjualan pada kontrak.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Biaya per unit pada baris kontrak berbasis produk

Memiliki biaya unit pada baris kontrak berbasis produk memungkinkan biaya produk yang berbeda untuk setiap penjualan unit. Meskipun tidak selalu diperlukan, ada skenario tertentu dengan biaya produk yang dapat didiskon untuk pelanggan oleh pemasok. Pertimbangkan skenario berikut:

Fabrikam robotik memasang lengan robotik di lini perakitan Adatum Corporation. Fabrikam menyediakan layanan penginstalan, namun lengan robot berasal dari Trey Research. Jika pemasangan senjata robot di Adatum Corporation membuka industri vertikal baru untuk lengan robot Trey Research, mereka dapat menawarkan diskon khusus untuk penawaran ini ke fabrikam. Dalam kasus ini, Fabrikam membuat baris kontrak berbasis produk untuk Robotic Arms. Biaya per unit dimasukkan untuk kontrak ini. Biayanya berbeda dengan biaya lengan robot dari Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]