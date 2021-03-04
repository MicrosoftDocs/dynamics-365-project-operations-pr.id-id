---
title: Mengatur daftar harga penjualan
description: Topik ini menyediakan informasi topik tentang daftar harga penjualan untuk penentuan harga proyek.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176255"
---
# <a name="set-up-a-sales-price-list"></a>Mengatur daftar harga penjualan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Untuk kuotasi dan kontrak proyek, daftar harga proyek memiliki pola penggantian harga yang berbeda dari daftar harga produk. Pada baris kuotasi Katalog Produk, Anda dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi, karena setiap baris kuotasi mengarah ke satu item Katalog. Namun, pada baris kuotasi berbasis proyek, Anda tidak dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi. Anda dapat menggunakan daftar harga proyek untuk bekerja dengan dua pola timpa yang berbeda.

> [!NOTE]
> Sebaiknya Anda memiliki daftar harga terpisah untuk sumber daya proyek dan item Katalog Anda, karena perbedaan perilaku antara keduanya saat Anda mengganti harga.

Setiap entitas berikut dapat memiliki satu atau beberapa daftar harga penjualan terkait untuk harga proyek:

- Pelanggan (Akun) 
- Peluang 
- Kuotasi 
- Kontrak Proyek

Asosiasi entitas ini dengan daftar harga ditunjukkan oleh daftar harga proyek. Anda dapat mengaitkan satu atau beberapa daftar harga dengan entitas pelanggan, peluang, kuotasi, dan entitas penjualan kontrak proyek.

Daftar harga proyek default tidak secara otomatis dimasukkan ke rekaman pelanggan. Namun, Anda dapat melampirkan daftar harga proyek secara manual ke rekaman pelanggan. Namun demikian, Anda harus melampirkan daftar harga proyek secara manual hanya bila Anda memiliki perjanjian harga kustom dengan pelanggan. 

Bila daftar harga proyek dilampirkan ke entitas penjualan, informasi berikut divalidasi:

- Daftar harga memiliki konteks **penjualan**. 
- Mata uang daftar harga cocok dengan mata uang pelanggan. 

Pada kontrak proyek, urutan prioritas berikut digunakan untuk secara otomatis mengatur daftar harga proyek yang terkait:

1. Kuotasi
2. Peluang
3. Pelanggan 
4. Pengaturan global 

Bila daftar harga proyek dimasukkan secara default, sistem memvalidasi bahwa mata uang cocok dengan mata uang pelanggan, dan bahwa daftar harga default yang telah dimasukkan memiliki konteks **penjualan**.

Anda dapat mengaitkan beberapa daftar harga proyek dengan entitas pelanggan, peluang, kuotasi, dan entitas kontrak proyek. Kemampuan ini mendukung harga default spesifik tanggal untuk kontrak proyek berjalan lama, di mana Anda memerlukan lebih dari satu daftar harga untuk menjelaskan pembaruan harga yang terjadi karena inflasi. Namun, jika daftar harga yang Anda kaitkan dengan pelanggan, peluang, kuotasi, atau entitas kontrak proyek memiliki efektivitas tanggal tumpang tindih, harga default mungkin salah. Oleh karena itu, Anda harus memastikan bahwa daftar harga proyek yang memiliki efektivitas tanggal tumpang tindih tidak terkait dengan entitas tersebut.


[!INCLUDE[footer-include](../includes/footer-banner.md)]