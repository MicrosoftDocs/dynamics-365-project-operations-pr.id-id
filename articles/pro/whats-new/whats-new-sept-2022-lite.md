---
title: Yang baru di bulan September 2022 - Penyebaran Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis September 2022 penyebaran Dynamics 365 Project Operations Microsoft lite.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634856"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Yang baru di bulan September 2022 - Penyebaran Project Operations lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam versi lingkungan 4.46.0.60 Dataverse

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

| Area fitur | Nama fitur | Informasi selengkapnya |
| --- | --- | --- |
| Manajemen peluang | **Revisi dan Aktivasi Quotes**<br>Operasi Proyek membawa dukungan penuh dari proses penjualan. Kutipan proyek dapat diaktifkan untuk mewakili keadaan di mana kutipan bersifat baca-saja dan sedang ditinjau. Kutipan yang diaktifkan dapat direvisi untuk membuat kutipan baru yang memiliki nomor revisi tambahan. Kutipan proyek yang diaktifkan atau revisi kutipan dapat ditutup sebagai menang atau kalah. | [Mengaktifkan dan merevisi kuotasi proyek](/dynamics365/project-operations/sales/activation-and-revision) |
| Penagihan dan Harga | **Harga agnostik zona waktu default**<br>Operasi Proyek telah memperkenalkan konsep tanggal agnostik zona waktu pada semua aktual proyek. Bidang baru, Tanggal **transaksi, sekarang tersedia di baris jurnal dan aktual, dan akan digunakan untuk menyimpan tanggal ketika transaksi terjadi,** tetapi tanpa mengubah tanggal tersebut menjadi Waktu Universal Terkoordinasi. Tanggal ini akan digunakan untuk proses hilirisasi seperti default harga dan pembuatan faktur. | <p>[Tentukan tarif biaya untuk estimasi dan aktual berbasis proyek](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Tentukan harga penjualan untuk perkiraan dan aktual berbasis proyek](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Penagihan dan Harga | **Penggantian harga efektif tanggal dalam Operasi Proyek**<br>Penggantian harga efektif tanggal menyediakan cara untuk mengganti atau mengubah harga tertentu dalam daftar harga. | [Penggantian harga efektif tanggal](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Waktu dan Pengeluaran | **Pemberi Persetujuan Global**<br>Fitur ini memungkinkan vendor perangkat lunak independen (ISV) dan persetujuan terpusat, terlepas dari status proyek atau anggota tim dalam proyek. | [Keamanan dan persetujuan](/dynamics365/project-operations/approvals/approvals-security) |
|Perencanaan dan Pelacakan Proyek|**Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan** </br> </br>API pengeditan kontur penugasan sumber daya memungkinkan pengembang secara terprogram menentukan upaya penerima tugas di seluruh rentang tanggal yang didukung untuk perencanaan upaya bertahap waktu yang lebih terperinci.|[Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2754422 | Perkiraan Material dan Biaya tidak mengalir ke Dynamics 365 Finance ketika proyek disalin dalam format Dataverse. |
| Waktu dan Pengeluaran | 2787409 | Pemberi persetujuan yang tidak valid dapat menyetujui entri waktu non-proyek. |
| Manajemen peluang | 2788907 | Pesan kesalahan yang diperbarui pada validasi keunikan untuk baris pesanan yang menyertakan bendera. |
| Waktu dan Pengeluaran | 2842253 | Penanganan pengecualian nol untuk persetujuan waktu. |
| Penagihan dan Harga | 2844181 | Kegagalan untuk mendapatkan ID korelasi memblokir pembuatan faktur. |
| Penagihan dan Harga | 2876628 | QLD, CLD - Resolusi daftar harga perkiraan harus menggunakan bidang rentang tanggal lama dari daftar harga. |
| Subkontrak | 2893222 | Jika tidak ada peran yang ditentukan untuk baris subkontrak, seharusnya dimungkinkan untuk memilih baris tersebut pada anggota tim untuk peran apa pun. |
