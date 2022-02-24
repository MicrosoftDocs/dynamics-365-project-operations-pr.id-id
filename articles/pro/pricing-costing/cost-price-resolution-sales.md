---
title: Menangani harga biaya pada aktual dan estimasi proyek
description: Pembaruan topik memberikan informasi tentang cara menangani harga biaya pada estimasi proyek dan aktual.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9f20631f41c560f1a4047aaaa624fa4e8651c687
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877269"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Menangani harga biaya pada aktual dan estimasi proyek 

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Untuk menangani harga biaya dan daftar harga biaya untuk perkiraan dan aktual, sistem menggunakan informasi di bidang **Tanggal**, **Mata Uang**, dan **Unit Kontrak** dari proyek terkait. Setelah daftar harga biaya diselesaikan, aplikasi menyelesaikan tarif biaya.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Menangani tarif biaya pada baris aktual dan estimasi untuk Waktu

Baris estimasi untuk Waktu adalah detail baris kontrak dan kuotasi untuk penetapan waktu dan sumber daya pada proyek.

Setelah daftar harga biaya teratasi, bidang **Peran** dan **Unit sumber daya** pada baris perkiraan untuk Waktu dicocokkan dengan garis harga peran dalam daftar harga. Kecocokan ini mengasumsikan bahwa Anda menggunakan dimensi harga standar untuk biaya tenaga kerja. Jika sebaliknya Anda mengonfigurasi sistem untuk mencocokkan bidang, bukan, atau selain **Peran** dan **Unit sumber daya**, maka kombinasi yang berbeda akan digunakan untuk mengambil garis harga peran yang cocok. Jika aplikasi menemukan baris harga peran yang memiliki tarif biaya untuk kombinasi **Peran** dan **Unit Sumber daya**, yaitu tarif biaya default. Jika aplikasi tidak dapat mencocokkan nilai **Peran** dan **Unit Sumber daya** maka aplikasi mengambil baris harga peran dengan peran yang cocok, tetapi nilai null **Unit Sumber Daya**. Setelah memiliki rekaman harga peran yang cocok, tarif biaya mengambil default dari rekaman itu. 

> [!NOTE]
> Jika Anda mengonfigurasi prioritas **Peran** dan **Unit Sumber Daya** yang berbeda, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku ini akan berubah sesuai dengan itu. Sistem mengambil rekaman harga peran dengan nilai yang cocok dengan setiap nilai dimensi harga dalam urutan prioritas dengan baris yang memiliki nilai kosong untuk dimensi tersebut diletakkan di akhir.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menangani tarif biaya pada baris aktual dan estimasi untuk pengeluaran

Baris estimasi untuk pengeluaran adalah detail baris kontrak dan kuotasi untuk pengeluaran dan baris estimasi pengeluaran pada proyek.

Setelah daftar harga biaya ditangani, sistem menggunakan kombinasi bidang **Kategori** dan **Unit** pada baris perkiraan pengeluaran yang cocok dengan baris **Harga Kategori** pada daftar harga yang diselesaikan. Jika sistem menemukan garis harga kategori yang memiliki tarif biaya untuk kombinasi bidang **Kategori** dan **Unit**, tarif biaya adalah default. Jika sistem tidak dapat sesuai dengan nilai **Kategori** dan **Unit**, atau jika sistem dapat menemukan baris harga kategori yang cocok, namun metode harga bukan **Harga Per Unit**, tingkat biaya akan berubah menjadi nol (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menangani tingkat biaya pada baris aktual dan estimasi untuk bahan

Baris estimasi untuk bahan adalah detail baris kuotasi dan kontrak untuk bahan dan baris estimasi bahan pada proyek.

Setelah daftar harga biaya ditangani, sistem menggunakan kombinasi bidang **Produk** dan **Unit** pada baris estimasi untuk agar estimasi bahan sesuai dengan baris **Item Daftar Harga** pada daftar harga yang ditangani. Jika sistem menemukan baris harga produk yang memiliki tingkat biaya untuk kombinasi bidang **Produk** dan **Unit**, maka tingkat biaya akan di-default. Jika sistem tidak dapat sesuai dengan nilai **Produk** dan **Unit**, atau jika sistem dapat menemukan baris item daftar harga yang cocok, namun metode harga didasarkan pada biaya Standar atau Biaya saat ini dan tidak ditentukan pada produk, biaya unit diatur default ke nol.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
