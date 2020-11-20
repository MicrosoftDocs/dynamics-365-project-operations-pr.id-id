---
title: Baris peluang berbasis produk - lite
description: Topik ini menyediakan informasi tentang item baris peluang berbasis produk dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176334"
---
# <a name="product-based-opportunity-lines---lite"></a>Baris peluang berbasis produk - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Lini peluang berbasis produk adalah item baris pada peluang. Baris ini dikirim ke pelanggan sebagai item baris yang berbeda pada faktur akhirnya tanpa layanan nilai tambah lainnya. Pembelanjaan dan konsumsi terkait tidak dilacak pada tugas proyek terkait mana pun.

Baris berbasis produk dapat berupa item Katalog atau produk pilihan. Sebagian besar fungsi pada baris berbasis produk peluang mengikuti fungsi yang disediakan oleh aplikasi Dynamics 365 Sales. Untuk informasi lebih lanjut tentang baris peluang berbasis produk, lihat [menambahkan produk ke peluang](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

Satu konsep tentang baris peluang berbasis produk yang spesifik untuk peluang berbasis proyek adalah **anggaran pelanggan**. Gunakan bidang ini untuk melacak jumlah yang bersedia dibayar pelanggan untuk item baris.

Jika metode pendapatan dari ringkasan peluang diatur ke **dihitung sistem**, nilai anggaran pelanggan di seluruh baris berbasis produk dan proyek diringkas untuk menghitung estimasi pendapatan.
