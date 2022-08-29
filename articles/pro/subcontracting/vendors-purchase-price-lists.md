---
title: Manajemen daftar harga vendor dan pembelian dalam Project Operations
description: Artikel ini memberikan informasi yang akan membantu Anda membuat dan memelihara data vendor dan daftar harga pembelian untuk subkontrak.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261891"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Manajemen daftar harga vendor dan pembelian dalam Project Operations


_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

## <a name="vendors-in-project-operations"></a>Vendor dalam Project Operations

Dalam Microsoft Dynamics 365 Project Operations, akun vendor memiliki jenis relasi **Vendor** atau **Pemasok**. Anda hanya dapat memilih rekaman akun yang memiliki salah satu jenis relasi ini sebagai vendor pada subkontrak.

Anda dapat mengaitkan satu atau beberapa daftar harga pembelian dengan rekaman vendor. Namun, setiap daftar harga pembelian yang terkait dengan rekaman vendor harus memiliki efekivitas tanggal yang berbeda. Project Operations tidak mendukung efektivitas tanggal yang tumpang tindih untuk daftar harga pembelian.

Secara default, bidang dan konsep berikut pada rekaman vendor digunakan untuk setiap subkontrak yang dibuat untuk vendor:

- Syarat Pembayaran
- Tagih pada kontak
- Kontak utama

    > [!NOTE]
    > Secara default, kontak utama vendor digunakan sebagai manajer akun vendor subkontrak.

- Mata uang
- Daftar Harga Pembelian saat ini

## <a name="purchase-price-lists-in-project-operations"></a>Daftar harga pembelian di Project Operations

Daftar harga tempat bidang **Konteks** diatur ke **Pembelian** dianggap sebagai daftar harga pembelian. Daftar harga pembelian dapat didefinisikan untuk mewakili katalog tingkat pembelian untuk waktu, pengeluaran, dan bahan. Daftar harga pembelian menyerupai daftar harga biaya dan penjualan di Project Operations. Konsep berikut berlaku untuk daftar harga pembelian dengan cara yang sama seperti yang berlaku untuk daftar harga biaya dan penjualan:

- **Efektivitas tanggal** – Daftar harga pembelian memiliki efektivitas tanggal. Efektivitas tanggal diwakili oleh bidang tanggal mulai dan tanggal akhir pada setiap daftar harga. Waktu antara tanggal mulai dan tanggal berakhir adalah periode efektif tanggal.
- **Mata uang** - Mata uang pada header daftar harga digunakan sebagai mata uang di mana harga pembelian dinyatakan untuk tenaga kerja, kategori pengeluaran, dan produk dalam katalog.
- **Unit waktu default** - Unit waktu default mengekspresikan harga tenaga kerja untuk pembelian. Bidang satuan waktu pada daftar harga hanya digunakan untuk menyediakan nilai default. Nilai tersebut dapat diubah pada baris harga peran individual.

Daftar harga pembelian dapat dilampirkan ke rekaman vendor sebagai asosiasi yang dikenal sebagai daftar harga proyek. Daftar harga ini digunakan untuk memasukkan harga default pada baris subkontrak. Secara default, ketika beberapa daftar harga pembelian dilampirkan ke rekaman vendor, daftar harga terbaru digunakan untuk subkontrak yang dibuat untuk vendor. Hanya daftar harga di mana bidang **Konteks** diatur ke **Pembelian** yang dapat dilampirkan ke rekaman vendor.

### <a name="subcontract-specific-purchase-price-lists"></a>Daftar harga pembelian khusus subkontrak

Daftar harga pembelian juga dapat dilampirkan ke subkontrak sebagai asosiasi yang dikenal sebagai daftar harga proyek. Daftar harga ini digunakan untuk memasukkan harga default pada baris subkontrak. Secara default, ketika beberapa daftar harga pembelian dilampirkan ke subkontrak, masing-masing harus memiliki efekivitas tanggal yang berbeda. Project Operations tidak mendukung efektivitas tanggal yang memiliki efektivitas tanggal tumpang tindih. Hanya daftar harga di mana bidang **Konteks** diatur ke **Pembelian** yang dapat dilampirkan ke subkontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
