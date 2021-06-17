---
title: Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite
description: Topik ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk item dalam katalog produk.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004329"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.

Dalam Project Operations, produk tidak dapat diperkirakan atau digunakan pada proyek, sehingga harga katalog produk tidak perlu ditetapkan pada daftar harga proyek untuk penawaran dan kontrak.

Gunakan bidang **Harga Produk** dari kuotasi, kontrak, atau akun untuk menyiapkan harga katalog produk. Jangan siapkan harga katalog produk dalam daftar harga proyek. Daftar harga proyek eksklusif untuk Project Operations. Logika bisnis khusus aplikasi menyalin daftar harga dari kuotasi ke kontrak. Hasilnya adalah Daftar Harga proyek Khusus Kontrak. Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar. Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak. Karena tidak ada penyalinan yang terlibat, kinerja proses kuotasi tidak terpengaruh.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]