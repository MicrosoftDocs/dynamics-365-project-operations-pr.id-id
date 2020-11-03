---
title: Menentukan biaya baris kontrak berbasis produk
description: Topik ini menyediakan informasi tentang pembuatan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/20/2020
ms.locfileid: "4078715"
---
# <a name="costing-product-based-contract-lines"></a>Menentukan biaya baris kontrak berbasis produk

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Baris kontrak berbasis produk di Dynamics 365 Project Operations mencakup bidang **harga biaya** , yang menyimpan harga produk untuk penghitungan profitabilitas hilir.

Bila baris kontrak berbasis produk dibuat untuk produk Katalog, biaya baris kontrak berbasis produk akan diisi default dari bidang **biaya standar** dalam Katalog Produk. Bidang **biaya standar** di Katalog Produk diatur dalam mata uang dasar organisasi. Bila unit biaya di-default pada baris kontrak, maka akan diubah menjadi mata uang penjualan pada kontrak.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Biaya per unit pada baris kontrak berbasis produk

Memiliki biaya unit pada baris kontrak berbasis produk memungkinkan biaya produk yang berbeda untuk setiap penjualan unit. Meskipun tidak selalu diperlukan, ada skenario tertentu dengan biaya produk yang dapat didiskon untuk pelanggan oleh pemasok. Pertimbangkan skenario berikut:

Fabrikam robotik memasang lengan robotik di lini perakitan Adatum Corporation. Fabrikam menyediakan layanan penginstalan tetapi senjata robotik Diperoleh dari Trey Research. Jika pemasangan senjata robot di Adatum Corporation membuka industri vertikal baru untuk lengan robot Trey Research, mereka dapat menawarkan diskon khusus untuk penawaran ini ke fabrikam. Dalam kasus ini, fabrikam membuat baris kontrak berbasis produk untuk lengan robot dan input per unit biaya untuk kontrak ini yang berbeda dari biaya standar lengan robot dari Trey Research.
