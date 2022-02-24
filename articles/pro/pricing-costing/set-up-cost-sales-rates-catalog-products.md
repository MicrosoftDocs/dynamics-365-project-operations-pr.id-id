---
title: Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite
description: Topik ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764556"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.

Dalam Project Operations, produk tidak dapat diperkirakan atau digunakan pada proyek, sehingga harga katalog produk tidak perlu ditetapkan pada daftar harga proyek untuk penawaran dan kontrak.

Gunakan bidang **Harga Produk** dari kuotasi, kontrak, atau akun untuk menyiapkan harga katalog produk. Jangan siapkan harga katalog produk dalam daftar harga proyek. Daftar harga proyek eksklusif untuk Project Operations. Logika bisnis khusus aplikasi menyalin daftar harga dari kuotasi ke kontrak. Hasilnya adalah Daftar Harga proyek Khusus Kontrak. Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar. Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak. Karena tidak ada penyalinan yang terlibat, kinerja proses kuotasi tidak terpengaruh.
