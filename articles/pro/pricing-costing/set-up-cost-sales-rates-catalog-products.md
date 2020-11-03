---
title: Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog
description: Topik ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078551"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.

Karena produk tidak dapat diperkirakan atau digunakan pada proyek dalam Project Operations, tidak perlu menetapkan harga katalog produk pada daftar harga proyek untuk kuotasi dan kontrak.

Harga katalog produk harus disiapkan di bidang **Harga Produk** dari kuotasi, kontrak, atau akun. Jangan menyiapkan harga katalog produk dalam daftar harga proyek untuk entitas ini. Daftar harga proyek eksklusif untuk Project Operations. Ada logika bisnis khusus aplikasi yang menyalin daftar harga dari kuotasi ke kontrak. Hasilnya adalah Daftar Harga proyek Khusus Kontrak. Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar. Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak. Ini berarti bahwa daftar harga produk tidak berdampak pada kinerja proses kemenangan kuotasi.
