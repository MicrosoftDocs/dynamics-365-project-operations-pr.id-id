---
title: Daftar harga default
description: Artikel ini menyediakan informasi tentang penjualan default dan daftar harga biaya dalam Operasi Proyek.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410266"
---
# <a name="default-price-lists"></a>Daftar harga default

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

## <a name="sales-price-lists"></a>Daftar harga penjualan

Setiap kuotasi dan kontrak proyek di Dynamics 365 Project Operations berisi daftar harga penjualan default. 

### <a name="price-list-default-on-project-quotes"></a>Daftar harga default pada kuotasi proyek
Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang default pada kuotasi proyek:

1. Sistem melihat daftar harga yang dilampirkan ke daftar harga proyek akun. 
1. Jika tidak ada daftar harga proyek yang dilampirkan ke catatan akun, sistem akan melihat daftar harga penjualan yang dilampirkan ke parameter proyek yang cocok dengan mata uang kutipan proyek.
1. Selanjutnya, sistem memeriksa efektivitas tanggal daftar harga yang cocok dengan rentang tanggal kuotasi proyek. Khususnya, tanggal kuotasi dibuat.
1. Jika ada beberapa daftar harga yang efektif untuk tanggal kuotasi proyek, semua daftar harga default pada kuotasi proyek.
1. Jika tidak ada daftar harga yang berlaku untuk tanggal kuotasi proyek, tidak ada daftar harga proyek default pada kuotasi proyek. Pesan peringatan akan terjadi pada kuotasi proyek. Pesan menyatakan bahwa aktual dan estimasi pada proyek tidak akan diberi harga karena tidak ada daftar harga proyek terlampir.

### <a name="price-list-default-on-project-contracts"></a>Daftar harga default pada kontrak proyek 
Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang default pada kontrak proyek:

1. Jika kontrak dibuat dari kuotasi, daftar harga proyek pada kuotasi disalin secara terpisah dan dilampirkan ke kontrak proyek.
1. Jika kontrak dibuat dari awal, sistem melihat daftar harga yang dilampirkan ke daftar harga proyek akun. Jika tidak ada daftar harga proyek yang melekat pada rekaman akun, sistem mencari daftar harga penjualan yang melekat pada parameter proyek yang sesuai dengan mata uang kontrak proyek.
1. Selanjutnya, sistem memeriksa efektivitas tanggal daftar harga yang cocok dengan rentang tanggal kontrak proyek. Khususnya, tanggal kontrak dibuat.
1. Jika ada beberapa daftar harga yang efektif untuk tanggal kontrak, semua daftar harga default pada kontrak.
1. Jika tidak ada daftar harga yang berlaku untuk tanggal kontrak, tidak ada daftar harga proyek default pada kontrak. Pesan peringatan akan terjadi pada kontrak proyek. Pesan menyatakan bahwa aktual dan estimasi pada proyek tidak akan diberi harga karena tidak ada daftar harga proyek terlampir.

## <a name="cost-price-lists"></a>Daftar Harga Biaya

Daftar harga biaya tidak default ke entitas mana pun dalam Project Operations. Menentukan daftar harga biaya yang akan digunakan untuk biaya proyek selalu dilakukan berdasarkan per transaksi. Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang digunakan untuk biaya proyek:

1. Sistem melihat daftar harga yang melekat pada unit organisasi kontraktor proyek.
1. Selanjutnya, sistem melihat efektivitas tanggal dari daftar harga yang sesuai dengan tanggal konteks perkiraan yang masuk atau konteks aktual.

    - *Konteks perkiraan* mengacu pada salah satu dari tiga konteks estimasi dalam Operasi Proyek:

        - Baris estimasi proyek
        - Detail baris kuotasi
        - Rincian Baris Kontrak

    - *Konteks aktual* mengacu pada salah satu dari tiga sumber untuk aktual dalam Operasi Proyek:

       - Entri baris jurnal yang dibuat secara manual, atau baris jurnal koreksi yang dibuat dalam jurnal koreksi
       - Baris jurnal yang dibuat selama pengiriman waktu, pengeluaran, atau log penggunaan material
       - Rincian Baris Faktur

    Ketika Operasi Proyek cocok dengan efektivitas tanggal dari baris jurnal yang masuk atau detail baris faktur dalam *konteks* aktual, operasi tersebut **menggunakan bidang Tanggal** transaksi.

    - Jika beberapa daftar harga berlaku untuk tanggal konteks perkiraan masuk atau konteks aktual, daftar harga yang terakhir dibuat akan dipilih.
    - Jika tidak ada daftar harga yang dilampirkan ke unit organisasi kontraktor proyek, sistem akan melihat daftar harga biaya yang dilampirkan pada parameter proyek yang sesuai dengan mata uang proyek.

## <a name="enable-multi-currency-cost-price-list"></a>Aktifkan daftar harga biaya multi-mata uang

Pengaturan ini dapat ditemukan di **Parameter** Pengaturan \>**·**. Nilai default adalah **Tidak**.

Ketika pengaturan ini diaktifkan (yaitu, nilainya diatur ke **Ya**), sistem berperilaku dengan cara berikut:

- Ini memungkinkan daftar harga biaya dalam mata uang apa pun untuk dikaitkan dengan unit organisasi. Misalnya, daftar harga biaya dalam mata uang EUR dapat dilampirkan ke unit organisasi dalam mata uang USD. Sistem akan terus memvalidasi bahwa daftar harga biaya yang dilampirkan ke unit organisasi tidak memiliki efektivitas tanggal yang tumpang tindih.
- Ini memvalidasi bahwa daftar harga biaya yang dilampirkan ke parameter proyek tidak memiliki efektivitas tanggal yang tumpang tindih, bahkan jika mereka memiliki mata uang yang berbeda. Perilaku ini berbeda dari perilaku default (yaitu, perilaku ketika nilai diatur ke **Tidak**). Dalam perilaku default, hanya daftar harga biaya yang memiliki mata uang yang sama yang **divalidasi** untuk efektivitas tanggal yang tidak tumpang tindih.
- Untuk konteks transaksi yang masuk, ini menentukan daftar harga biaya berdasarkan efektivitas tanggal saja. Perilaku ini berbeda dari perilaku default, di mana sistem memilih daftar harga biaya yang cocok dengan mata uang proyek dan efektivitas tanggal.

Karena perubahan perilaku ini, pelanggan Operasi Proyek akan dapat mempertahankan daftar harga biaya global yang akan relevan untuk seluruh perusahaan. Mereka tidak perlu memiliki daftar harga di setiap mata uang operasi. Daftar harga global akan memiliki efektivitas tanggal dan akan memungkinkan tarif biaya diatur dalam mata uang apa pun untuk kombinasi tertentu dari nilai dimensi harga. Mata uang daftar harga biaya hanya digunakan untuk memasukkan nilai default saat **Harga peran,** harga **Kategori**, dan **catatan item daftar** Harga dibuat. Ini tidak akan digunakan untuk menentukan daftar harga.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
