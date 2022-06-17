---
title: Menonaktifkan daftar harga
description: Artikel ini menjelaskan cara menonaktifkan atau menghapus daftar harga yang tidak digunakan atau yang lama.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56bd498d2cb892bdf0c7514d0918e3873098b8d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924388"
---
# <a name="deactivate-price-lists"></a>Menonaktifkan daftar harga 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Untuk menghilangkan daftar harga lama atau yang tidak digunakan dari Dynamics 365 Project Operations, ada dua langkah yang harus diselesaikan. 

1. Hilangkan atau hapus daftar harga dari halaman tertentu.
2. Nonaktifkan atau hapus daftar harga dari daftar harga Aktif pada halaman **Daftar Harga**.

>[!IMPORTANT]
> Anda harus menyelesaikan kedua langkah tersebut untuk sepenuhnya menghilangkan daftar harga. Hanya melakukan langkah 2, yakni secara langsung menghapus atau menonaktifkan daftar harga dari tampilan Daftar Harga Aktif, tidak memadai. Anda juga harus menghapus keterkaitan daftar harga ini dari semua tempat yang disebutkan pada langkah 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Hapus daftar harga dari halaman tertentu
1. Untuk menghapus daftar harga dari Project Operations, buka halaman berikut:  

      - Halaman **Parameter Proyek** > tab **Daftar harga**
      - Halaman **Unit Organisasional** > kisi **Daftar Harga**
      - Halaman **Akun** > kisi **Daftar Harga Proyek**
      - Halaman **Kuotasi Proyek** > kisi **Daftar Harga Proyek**: Berlaku untuk semua kuotasi proyek aktif.
      - Halaman **Kontrak Proyek** > kisi **Daftar Harga Proyek**: Berlaku untuk semua kontrak proyek aktif.

 2. Untuk setiap halaman, Anda harus memilih daftar harga yang akan dihapus, kemudian memilih **Hapus**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Hapus atau nonaktifkan daftar harga dari halaman Daftar Harga
 
1. Untuk menghapus daftar harga dari daftar harga aktif, buka **Penjualan** > **Pelanggan** > **Daftar Harga**. 
2. Pilih daftar harga yang akan dihapus, lalu pilih **hapus**. Jika daftar harga direferensikan pada transaksi yang ada, Anda tidak akan dapat menghapusnya. Jika hal ini terjadi, Anda dapat menonaktifkan daftar harga sehingga tidak muncul dalam tampilan apa pun. 
3. Untuk menonaktifkan daftar harga, pilih kembali daftar harga, lalu pilih **Nonaktifkan**.   
