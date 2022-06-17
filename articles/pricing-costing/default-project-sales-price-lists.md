---
title: Daftar harga default
description: Artikel ini menyediakan informasi tentang penjualan default dan daftar harga biaya dalam Operasi Proyek.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7a8f99cd03e5c2c15941c17469cc5632765b0fdc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917718"
---
# <a name="default-price-lists"></a>Daftar harga default

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

## <a name="sales-price-lists"></a>Daftar harga penjualan

Setiap kuotasi dan kontrak proyek di Dynamics 365 Project Operations berisi daftar harga penjualan default. 

### <a name="price-list-default-on-project-quotes"></a>Daftar harga default pada kuotasi proyek
Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang default pada kuotasi proyek:

1. Sistem melihat daftar harga yang dilampirkan ke daftar harga proyek akun. 
2. Jika ada daftar harga proyek yang melekat pada rekaman akun, sistem melihat daftar harga penjualan yang melekat pada parameter proyek yang sesuai dengan mata uang kuotasi proyek.
3. Selanjutnya, sistem memeriksa efektivitas tanggal daftar harga yang cocok dengan rentang tanggal kuotasi proyek. Khususnya, tanggal kuotasi dibuat.
4. Jika ada beberapa daftar harga yang efektif untuk tanggal kuotasi proyek, semua daftar harga default pada kuotasi proyek.
5. Jika tidak ada daftar harga yang berlaku untuk tanggal kuotasi proyek, tidak ada daftar harga proyek default pada kuotasi proyek. Pesan peringatan akan terjadi pada kuotasi proyek. Pesan menyatakan bahwa aktual dan estimasi pada proyek tidak akan diberi harga karena tidak ada daftar harga proyek terlampir.

### <a name="price-list-default-on-project-contracts"></a>Daftar harga default pada kontrak proyek 
Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang default pada kontrak proyek:

1. Jika kontrak dibuat dari kuotasi, daftar harga proyek pada kuotasi disalin secara terpisah dan dilampirkan ke kontrak proyek.
2. Jika kontrak dibuat dari awal, sistem melihat daftar harga yang dilampirkan ke daftar harga proyek akun. Jika tidak ada daftar harga proyek yang melekat pada rekaman akun, sistem mencari daftar harga penjualan yang melekat pada parameter proyek yang sesuai dengan mata uang kontrak proyek.
4. Selanjutnya, sistem memeriksa efektivitas tanggal daftar harga yang cocok dengan rentang tanggal kontrak proyek. Khususnya, tanggal kontrak dibuat.
5. Jika ada beberapa daftar harga yang efektif untuk tanggal kontrak, semua daftar harga default pada kontrak.
6. Jika tidak ada daftar harga yang berlaku untuk tanggal kontrak, tidak ada daftar harga proyek default pada kontrak. Pesan peringatan akan terjadi pada kontrak proyek. Pesan menyatakan bahwa aktual dan estimasi pada proyek tidak akan diberi harga karena tidak ada daftar harga proyek terlampir.

## <a name="cost-price-lists"></a>Daftar Harga Biaya

Daftar harga biaya tidak default ke entitas mana pun dalam Project Operations. Menentukan daftar harga biaya yang akan digunakan untuk biaya proyek selalu dilakukan saat ini. Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang digunakan untuk biaya proyek:

1. Sistem ini pertama kali melihat daftar harga yang melekat pada unit organisasi kontrak proyek.
2. Sistem kemudian melihat efektivitas tanggal dari daftar harga yang cocok dengan tanggal estimasi masuk atau baris aktual. Dalam situasi ini, *baris estimasi* mengacu pada ketiga konteks estimasi dalam Project Operations:

    - Baris estimasi proyek
    - Detail baris kuotasi
    - Rincian Baris Kontrak
  
3. Jika ada beberapa daftar harga yang efektif untuk tanggal pada estimasi masuk atau aktual, daftar harga yang paling baru dibuat akan dipilih.
4. Jika tidak ada daftar harga proyek yang melekat pada unit organisasi kontrak proyek, sistem melihat daftar harga biaya yang melekat pada parameter proyek yang sesuai dengan mata uang proyek.
5. Selanjutnya sistem melihat efektivitas tanggal dari daftar harga yang cocok dengan tanggal estimasi masuk atau baris aktual. 
6. Jika ada beberapa daftar harga yang efektif untuk tanggal pada estimasi masuk atau aktual, daftar harga yang paling baru dibuat akan dipilih.
7. Jika tidak ada daftar harga biaya yang melekat pada parameter proyek yang sesuai dengan mata uang dan tanggal efektif, sistem men-default tarif biaya ke nol (0) pada estimasi masuk atau baris aktual.


[!INCLUDE[footer-include](../includes/footer-banner.md)]