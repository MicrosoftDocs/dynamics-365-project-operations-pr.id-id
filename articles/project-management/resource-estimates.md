---
title: Estimasi keuangan untuk waktu sumber daya pada proyek
description: Topik ini menyediakan informasi tentang cara menghitung estimasi keuangan untuk waktu.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010790"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimasi keuangan untuk waktu sumber daya pada proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Estimasi keuangan untuk waktu dihitung berdasarkan tiga faktor: 

- Jenis anggota tim generik atau bernama yang ditetapkan ke setiap tugas node leaf pada rencana proyek. 
- Jenis atau kompleksitas pekerjaan.
- Penyebaran upaya untuk penugasan sumber daya pada tugas. 

Dua faktor pertama mempengaruhi biaya unit atau tingkat tagihan penetapan sumber daya. Biaya unit atau tingkat tagihan penetapan sumber daya ditentukan berdasarkan atribut sumber daya yang ditetapkan. Atribut ini mencakup unit organisasional yang memiliki sumber daya dan peran standar sumber daya. Anda juga dapat menambahkan atribut kustom yang relevan ke bisnis untuk sumber daya, seperti judul standar atau tingkat pengalaman, dan membuatnya mempengaruhi biaya per unit atau tingkat tagihan penetapan.
Selain atribut sumber daya, atribut pekerjaan, seperti tugas, juga dapat mempengaruhi tingkat tagihan unit atau tingkat biaya penetapan. Misalnya, bila tugas tertentu lebih kompleks, penetapan sumber daya ke tugas tertentu akan menghasilkan biaya unit atau tingkat tagihan yang lebih tinggi dibandingkan tugas yang kurang kompleks.   

Faktor ketiga menyediakan kuantitas jam pada tingkat tersebut. Dalam kasus saat tugas mencakup dua periode harga, kemungkinan bagian pertama dari penetapan sumber daya untuk tugas tersebut dikenakan biaya dan harga yang berbeda dari bagian kedua tugas. Perkiraan upaya pada setiap penetapan sumber daya adalah nilai kompleks yang tersimpan dengan distribusi upaya harian per hari.

Untuk petunjuk rinci tentang cara mengkonfigurasi atribut kustom pekerjaan dan sumber daya sebagai dimensi harga dan biaya, lihat [ikhtisar Dimensi Harga](../pricing-costing/pricing-dimensions-overview.md).

Perkiraan keuangan untuk setiap penetapan sumber daya dihitung sebagai **tingkat/jam untuk penugasan yang dikalikan dengan jumlah jam.**  Sama seperti perkiraan upaya, perkiraan keuangan untuk biaya dan pendapatan untuk setiap penetapan sumber daya adalah nilai kompleks yang tersimpan dengan distribusi harian jumlah moneter per hari. 

## <a name="summarizing-financial-estimates-for-time"></a>Meringkas estimasi keuangan untuk waktu
Perkiraan keuangan untuk waktu pada tugas node leaf adalah jumlah estimasi keuangan pada semua penugasan sumber daya untuk tugas tersebut.

Perkiraan keuangan untuk waktu pada tugas ringkasan atau induk adalah jumlah estimasi keuangan pada semua tugas anaknya. Ini adalah perkiraan biaya tenaga kerja dalam proyek. 

![Estimasi sumber daya](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Harga biaya dan mata uang biaya default

Harga biaya default berasal dari daftar harga yang dilampirkan ke unit kontrak proyek. Mata uang biaya proyek selalu adalah mata uang dari unit kontrak pada proyek. Pada penetapan sumber daya, perkiraan keuangan untuk biaya disimpan dalam mata uang biaya proyek. Terkadang, mata uang yang mengatur tingkat biaya dalam daftar harga berbeda dari mata uang biaya proyek. Dalam kasus ini, aplikasi mengkonversi mata uang dengan harga biaya yang diatur untuk mata uang proyek. Pada kisi **Estimasi**, semua estimasi biaya ditampilkan dan diringkas dalam mata uang biaya proyek. 

## <a name="default-bill-rate-and-sales-currency"></a>Default tarif tagihan dan mata uang penjualan

Harga penjualan default berasal dari daftar harga proyek yang dilampirkan ke kontrak proyek terkait jika transaksi dimenangkan, atau dari kuotasi proyek terkait jika penawaran masih dalam tahapan pra penjualan. Mata uang penjualan proyek selalu adalah mata uang dari kuotasi proyek atau kontrak proyek. Pada penetapan sumber daya, perkiraan keuangan untuk penjualan disimpan dalam mata uang penjualan proyek. Tidak seperti biaya, harga penjualan yang diatur dalam daftar harga tidak akan pernah berbeda dengan mata uang penjualan proyek. Tidak ada skenario yang memerlukan konversi mata uang. Pada kisi **Estimasi**, semua estimasi penjualan ditampilkan dan diringkas dalam mata uang penjualan proyek. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
