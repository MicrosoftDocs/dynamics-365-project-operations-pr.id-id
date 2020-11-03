---
title: Tinjau akumulasi faktur pada proyek dan kontrak proyek
description: Topik ini menyediakan informasi tentang cara meninjau waktu, pengeluaran, dan akumulasi produk, serta cara menandainya sebagai siap digunakan untuk faktur.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078693"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Tinjau akumulasi faktur pada proyek dan kontrak proyek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bila transaksi siap untuk membuat dan memproses faktur, transaksi harus ditandai **siap untuk faktur**. Topik ini menjelaskan jenis transaksi yang dapat dibuat.

## <a name="review-the-time-and-material-billing-backlog"></a>Tinjau akumulasi penagihan waktu dan material

Bila entri waktu atau biaya diajukan dan disetujui untuk proyek, PSA membuat aktual proyek. Jika kombinasi proyek dan kelas transaksi dipetakan ke baris kontrak untuk proyek waktu dan bahan, dua aktual dibuat saat entri disetujui:

- Biaya Aktual 
- Aktual Penjualan Belum Tertagih

Aktual penjualan yang tidak ditagihkan menunjukkan akumulasi tagihan, dan status penagihan mereka harus diatur ke **siap untuk faktur**. Saat faktur proyek dibuat, aktual penjualan yang tidak ditagih yang ditandai **siap untuk faktur** disalin sebagai rincian baris faktur.

Untuk meninjau akumulasi tagihan untuk waktu dan material, buka **Sales** \> **penagihan** \> **Akumulasi penagihan waktu dan material**. Pilih Semua aktual penjualan yang tidak ditagih yang siap ditagih, lalu pilih **siap untuk faktur**. Status tagihan aktual ini diubah ke **siap untuk faktur**.

![Akumulasi Penagihan Waktu dan Material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Tinjau Akumulasi Penagihan Produk

Dalam PSA, ketika kontrak proyek memiliki baris kontrak berbasis produk, baris tersebut dipertimbangkan untuk faktur setiap kali faktur dibuat untuk kontrak proyek. Setiap produk yang memiliki baris kontrak yang ditandai **siap untuk faktur** disalin ke faktur proyek sebagai baris faktur proyek.

Untuk meninjau jaminan akumulasi produk, buka **penjualan** \> **tagihan** \> **Akumulasi tagihan produk**. Pilih Semua baris kontrak berbasis produk yang siap ditagih, lalu pilih **siap untuk faktur**. Status tagihan baris ini diubah ke **siap untuk faktur**.

![Akumulasi Penagihan Produk](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Meninjau tonggak waktu penagihan pada kontrak harga tetap

Setiap baris kontrak proyek yang memiliki metode penagihan harga tetap harus menentukan tonggak waktu kontrak. tonggak waktu waktu kontrak ini dapat ditagih hanya jika ditAndai siap **untuk faktur**. 

Untuk meninjau tonggak waktu penagihan, buka **Sales** \> **tagihan** \> **tonggak waktu harga tetap**. Pilih tonggak waktu yang siap ditagih yang siap ditagih, lalu pilih **siap untuk faktur**. Status tagihan tonggak waktu ini diubah ke **siap untuk faktur**.

![Tonggak waktu Harga Tetap](media/FPBacklog.png)
