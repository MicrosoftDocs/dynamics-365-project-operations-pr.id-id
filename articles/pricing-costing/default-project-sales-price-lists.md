---
title: Daftar harga default
description: Topik ini menyediakan informasi tentang daftar harga biaya dan penjualan default dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078363"
---
# <a name="default-price-lists"></a>Daftar harga default

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

## <a name="sales-price-lists"></a>Daftar harga penjualan

Setiap penawaran dan kontrak proyek di Dynamics 365 Project Operations berisi daftar harga penjualan default. 

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
