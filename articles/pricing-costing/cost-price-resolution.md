---
title: Menyelesaikan harga biaya untuk estimasi dan aktual
description: Topik ini memberikan informasi tentang bagaimana harga biaya untuk estimasi dan aktual diselesaikan.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877316"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Menyelesaikan harga biaya untuk estimasi dan aktual

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menangani harga biaya dan daftar harga biaya untuk perkiraan dan aktual, sistem menggunakan informasi di bidang **Tanggal**, **Mata Uang**, dan **Unit Kontrak** dari proyek terkait. Setelah daftar harga biaya diselesaikan, aplikasi menyelesaikan tarif biaya.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Menangani tarif biaya pada baris aktual dan estimasi untuk Waktu

Baris estimasi untuk Waktu adalah detail baris kontrak dan kuotasi untuk penetapan waktu dan sumber daya pada proyek.

Setelah daftar harga biaya diselesaikan, sistem menggunakan bidang **Peran**, **Perusahaan Sumber Daya**, dan **Unit Sumber daya** pada baris estimasi untuk waktu untuk dicocokkan dengan baris harga peran dalam daftar harga. Kecocokan ini mengasumsikan bahwa Anda menggunakan dimensi harga bawaan untuk biaya tenaga kerja. Jika sebaliknya Anda mengonfigurasi sistem untuk mencocokkan bidang, bukan, atau selain **Peran**, **Perusahaan Sumber daya**, dan **Unit sumber daya**, maka kombinasi yang berbeda akan digunakan untuk mengambil garis harga peran yang cocok. Jika aplikasi menemukan baris harga peran yang memiliki tarif biaya untuk kombinasi **Peran**, **Perusahaan Sumber daya**, dan **Unit Sumber daya**, yaitu tarif biaya default. Jika aplikasi tidak sesuai dengan kombinasi nilai **Peran**, **Perusahaan sumber daya**, dan **Unit sumber daya**, aplikasi akan mengambil baris harga peran dengan nilai peran yang cocok, tetapi memiliki nilai nihil untuk **Unit sumber daya** dan **Perusahaan sumber daya**. Setelah rekaman harga peran yang cocok dengan nilai harga peran yang cocok ditemukan, tingkat biaya di-default dari rekaman tersebut. 

> [!NOTE]
> Jika Anda mengonfigurasi prioritas **Peran** yang berbeda, **Perusahaan Sumber Daya**, dan **Unit Sumber Daya**, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku ini akan berubah sesuai dengan itu. Sistem mengambil rekaman harga peran dengan nilai yang sesuai dengan tiap nilai dimensi harga dalam urutan prioritas dengan baris yang memiliki nilai nihil untuk dimensi tersebut yang terakhir dalam urutan prioritas.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menangani tarif biaya pada baris aktual dan estimasi untuk pengeluaran

Baris estimasi untuk pengeluaran adalah detail baris kontrak dan kuotasi untuk pengeluaran dan baris estimasi pengeluaran pada proyek.

Setelah daftar harga biaya diselesaikan, sistem menggunakan kombinasi bidang **Kategori** dan **Unit**, dan pada baris estimasi untuk pengeluaran untuk dicocokkan dengan baris **Harga Kategori** di daftar harga yang telah diselesaikan. Jika sistem menemukan garis harga kategori yang memiliki tarif biaya untuk kombinasi bidang **Kategori** dan **Unit**, tarif biaya adalah default. Jika sistem tidak dapat mencocokkan nilai **Kategori** dan **Unit**, atau jika mampu menemukan baris harga kategori yang cocok tetapi metode harga bukan **Harga Per Unit**, tarif biaya default ke nol(0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menangani tingkat biaya pada baris aktual dan estimasi untuk bahan

Baris estimasi untuk bahan adalah detail baris kuotasi dan kontrak untuk bahan dan baris estimasi bahan pada proyek.

Setelah daftar harga biaya ditangani, sistem menggunakan kombinasi bidang **Produk** dan **Unit** pada baris estimasi untuk agar estimasi bahan sesuai dengan baris **Item Daftar Harga** pada daftar harga yang ditangani. Jika sistem menemukan baris harga produk yang memiliki tingkat biaya untuk kombinasi bidang **Produk** dan **Unit**, maka tingkat biaya akan di-default. Jika sistem tidak dapat sesuai dengan nilai **Produk** dan **Unit**, biaya unit akan default ke nol. Default ini juga akan terjadi jika ada baris item daftar harga yang cocok, namun metode harga didasarkan pada biaya standar atau biaya saat ini yang tidak ditentukan dalam produk.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
