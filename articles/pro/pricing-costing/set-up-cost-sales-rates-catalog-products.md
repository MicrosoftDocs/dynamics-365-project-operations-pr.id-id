---
title: Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite
description: Topik ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176705"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.

Karena produk tidak dapat diperkirakan atau digunakan pada proyek dalam Project Operations, tidak perlu menetapkan harga katalog produk pada daftar harga proyek untuk kuotasi dan kontrak.

Harga katalog produk harus disiapkan di bidang **Harga Produk** dari kuotasi, kontrak, atau akun. Jangan menyiapkan harga katalog produk dalam daftar harga proyek untuk entitas ini. Daftar harga proyek eksklusif untuk Project Operations. Ada logika bisnis khusus aplikasi yang menyalin daftar harga dari kuotasi ke kontrak. Hasilnya adalah Daftar Harga proyek Khusus Kontrak. Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar. Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak. Ini berarti bahwa daftar harga produk tidak berdampak pada kinerja proses kemenangan kuotasi.
