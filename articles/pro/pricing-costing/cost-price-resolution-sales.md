---
title: Menyelesaikan harga biaya pada estimasi dan aktual - lite
description: Topik ini memberikan informasi tentang bagaimana harga biaya pada estimasi dan aktual diselesaikan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764597"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Menyelesaikan harga biaya pada estimasi dan aktual - lite

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
