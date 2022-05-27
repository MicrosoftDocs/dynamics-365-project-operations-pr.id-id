---
title: Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite
description: Topik ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk item dalam katalog produk.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576826"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.

Dalam Project Operations, produk tidak dapat diperkirakan atau digunakan pada proyek, sehingga harga katalog produk tidak perlu ditetapkan pada daftar harga proyek untuk penawaran dan kontrak.

Gunakan bidang **Harga Produk** dari kuotasi, kontrak, atau akun untuk menyiapkan harga katalog produk. Jangan siapkan harga katalog produk dalam daftar harga proyek. Daftar harga proyek eksklusif untuk Project Operations. Logika bisnis khusus aplikasi menyalin daftar harga dari kuotasi ke kontrak. Hasilnya adalah Daftar Harga proyek Khusus Kontrak. Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar. Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak. Karena tidak ada penyalinan yang terlibat, kinerja proses kuotasi tidak terpengaruh.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]