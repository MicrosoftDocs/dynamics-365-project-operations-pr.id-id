---
title: Menimpa daftar harga penjualan proyek
description: Topik ini menyediakan informasi tentang pembuatan daftar harga penjualan kustom.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b26947822eb8e87b3b36fcde9c99c6ee69375aa942a5641112b9b1109dcaa26c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009580"
---
# <a name="override-project-sales-price-lists"></a>Menimpa daftar harga penjualan proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

## <a name="customer-specific-project-price-lists"></a>Daftar harga proyek khusus pelanggan

Perjanjian harga spesifik pelanggan dapat diatur sebagai daftar harga proyek pada record akun di Dynamics 365 Project Operations.

Untuk membuat daftar harga proyek khusus pelanggan, di area **penjualan**, navigasi ke rekaman akun.

1. Buka halaman daftar **akun**.
2. Cari dan klik dua kali rekaman pelanggan untuk membuka halaman rincian **akun**.
3. Pada tab **Daftar Harga Proyek**, pilih **+ Daftar Harga Proyek Baru**.
4. Pada halaman **daftar harga proyek baru**, pilih daftar harga dari drop-down. Hanya daftar harga yang konteksnya diatur ke **penjualan** dan yang mata uangnya sesuai dengan mata uang akun yang disertakan.
5. Namai asosiasi tersebut, lalu pilih **Simpan**. Daftar harga proyek khusus pelanggan dibuat. Daftar harga ini akan digunakan untuk harga proyek default pada kuotasi proyek atau kontrak yang dibuat untuk pelanggan ini saat tanggal pembuatan kuotasi atau kontrak proyek jatuh dalam efektivitas tanggal dari daftar harga.

## <a name="custom-pricing-on-project-quotes"></a>Harga kustom pada kuotasi proyek

Pada kuotasi proyek, Anda dapat memiliki harga proyek yang diawali dengan daftar harga standar default yang di-default dari pelanggan atau dari parameter proyek.

Bila Anda memerlukan harga kustom untuk pekerjaan yang terkait dengan proyek pada kuotasi tertentu, Anda dapat mendapatkannya dari daftar harga proyek yang terkait dengan entitas.

Selesaikan langkah-langkah berikut untuk mengkonfigurasi harga proyek khusus kuotasi.

1. Buka kuotasi proyek, dan pilih tab **daftar harga proyek**.
2. Dalam subgrid, pilih **Buat harga kustom**.

Semua daftar harga proyek yang dilampirkan ke kuotasi akan disalin ke daftar harga baru. Nama dari daftar harga baru menunjukkan nama kuotasi dengan stempel waktu tanggal saat daftar harga ini dibuat.

Anda dapat menggunakan masing-masing daftar harga dan melakukan pembaruan terhadap harga tenaga kerja (harga peran) dan pengeluaran (harga kategori). Harga ini akan berlaku hanya untuk kuotasi proyek ini.

## <a name="price-lists-on-a-project-contract"></a>Daftar Harga pada Kontrak Proyek

Pada kontrak proyek, harga proyek selalu default sebagai daftar harga kustom dengan nama kontrak dan stempel waktu tanggal dibuat yang ditambahkan ke nama. Hal ini berlaku apakah kontrak dibuat saat kuotasi dimenangkan atau jika kontrak dibuat dari awal. Jika diperlukan, Anda dapat menghapus Asosiasi ini ke daftar harga kustom dan mengaitkan daftar harga standar ke kontrak proyek sebagai gantinya.

Bila Anda mengaitkan daftar harga standar ke daftar harga proyek pada kuotasi atau kontrak, setiap perubahan yang dibuat pada harga dalam daftar harga akan mempengaruhi semua kuotasi dan kontrak yang menggunakan daftar harga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]