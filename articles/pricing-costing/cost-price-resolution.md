---
title: Menyelesaikan harga biaya untuk estimasi dan aktual
description: Topik ini memberikan informasi tentang bagaimana harga biaya untuk estimasi dan aktual diselesaikan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275677"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Menyelesaikan harga biaya untuk estimasi dan aktual

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menangani harga biaya dan daftar harga biaya untuk perkiraan dan aktual, sistem menggunakan informasi di bidang **Tanggal**, **Mata Uang**, dan **Unit Kontrak** dari proyek terkait. Setelah daftar harga biaya diselesaikan, aplikasi menyelesaikan tarif biaya.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Menangani tarif biaya pada baris aktual dan estimasi untuk Waktu

Baris estimasi untuk Waktu adalah detail baris kontrak dan kuotasi untuk penetapan waktu dan sumber daya pada proyek.

Setelah daftar harga biaya diselesaikan, sistem menggunakan bidang **Peran**, **Perusahaan Sumber Daya**, dan **Unit Sumber daya** pada baris estimasi untuk waktu untuk dicocokkan dengan baris harga peran dalam daftar harga. Kecocokan ini mengasumsikan bahwa Anda menggunakan dimensi harga bawaan untuk biaya tenaga kerja. Jika sebaliknya Anda mengonfigurasi sistem untuk mencocokkan bidang, bukan, atau selain **Peran**, **Perusahaan Sumber daya**, dan **Unit sumber daya**, maka kombinasi yang berbeda akan digunakan untuk mengambil garis harga peran yang cocok. Jika aplikasi menemukan baris harga peran yang memiliki tarif biaya untuk kombinasi **Peran**, **Perusahaan Sumber daya**, dan **Unit Sumber daya**, yaitu tarif biaya default. Jika aplikasi tidak dapat mencocokkan nilai **Peran**, **Unit Sumber daya**, dan **Unit Sumber daya** maka aplikasi mengambil baris harga peran dengan peran yang cocok, tetapi nilai null **Unit Sumber Daya**. Setelah memiliki rekaman harga peran yang cocok, tarif biaya mengambil default dari rekaman itu. 

> [!NOTE]
> Jika Anda mengonfigurasi prioritas **Peran** yang berbeda, **Perusahaan Sumber Daya**, dan **Unit Sumber Daya**, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku ini akan berubah sesuai dengan itu. Sistem mengambil rekaman harga peran dengan nilai yang cocok dengan setiap nilai dimensi harga dalam urutan prioritas dengan baris yang memiliki nilai kosong untuk dimensi tersebut diletakkan di akhir.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menangani tarif biaya pada baris aktual dan estimasi untuk pengeluaran

Baris estimasi untuk pengeluaran adalah detail baris kontrak dan kuotasi untuk pengeluaran dan baris estimasi pengeluaran pada proyek.

Setelah daftar harga biaya diselesaikan, sistem menggunakan kombinasi bidang **Kategori** dan **Unit**, dan pada baris estimasi untuk pengeluaran untuk dicocokkan dengan baris **Harga Kategori** di daftar harga yang telah diselesaikan. Jika sistem menemukan garis harga kategori yang memiliki tarif biaya untuk kombinasi bidang **Kategori** dan **Unit**, tarif biaya adalah default. Jika sistem tidak dapat mencocokkan nilai **Kategori** dan **Unit**, atau jika mampu menemukan baris harga kategori yang cocok tetapi metode harga bukan **Harga Per Unit**, tarif biaya default ke nol(0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]