---
title: Yang baru di bulan September 2022 - Penyebaran Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam penyebaran Microsoft Dynamics 365 Project Operations lite yang rilis pada September 2022.
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

- Project Operations dalam lingkungan Dataverse versi 4.46.0.60

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

| Area fitur | Nama fitur | Informasi selengkapnya |
| --- | --- | --- |
| Manajemen peluang | **Revisi dan Aktivasi Kuotasi**<br>Project Operations menghadirkan dukungan penuh proses penjualan. Kuotasi proyek dapat diaktifkan untuk menunjukkan status lokasi kuotasi hanya baca dan sedang ditinjau. Kuotasi yang diaktifkan dapat direvisi untuk membuat kuotasi baru yang memiliki penambahan jumlah revisi. Kuotasi proyek yang diaktifkan atau revisi kuotasi bisa ditutup sebagai menang atau kalah. | [Mengaktifkan dan merevisi kuotasi proyek](/dynamics365/project-operations/sales/activation-and-revision) |
| Penagihan dan Harga | **Default harga agnostis zona waktu**<br>Project Operations telah memperkenalkan konsep tanggal agnostis zona waktu pada semua aktual proyek. Bidang baru, **Tanggal transaksi**, sekarang tersedia pada baris dan lini jurnal, dan akan digunakan untuk menyimpan tanggal transaksi terjadi, namun tanpa mengkonversi tanggal tersebut ke Waktu Universal Terkoordinasi. Tanggal ini akan digunakan untuk proses hilir seperti default harga dan pembuatan faktur. | <p>[Menentukan harga penjualan untuk estimasi proyek dan aktual](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Menentukan harga penjualan untuk estimasi dan aktual berbasis proyek](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Penagihan dan Harga | **Penimpaan harga tanggal berlaku dalam Project Operations**<br>Penimpaan harga tanggal berlaku memberikan cara menimpa atau mengubah harga tertentu dalam daftar harga. | [Penimpaan harga tanggal berlaku](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Waktu dan Pengeluaran | **Pemberi Izin Global**<br>Fitur ini memungkinkan vendor perangkat lunak independen (ISV) dan persetujuan terpusat, apa pun status proyek atau anggota tim dalam proyek. | [Keamanan dan persetujuan](/dynamics365/project-operations/approvals/approvals-security) |
|Perencanaan dan Pelacakan Proyek|**Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan** </br> </br>API pengeditan kontur penugasan sumber daya memungkinkan pengembang secara terprogram menentukan upaya penerima tugas di semua rentang tanggal yang didukung untuk perencanaan upaya bertahap waktu yang lebih terperinci.|[Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2754422 | Estimasi Materi dan Pengeluaran tidak mengalir ke Dynamics 365 Finance saat proyek disalin dalam Dataverse. |
| Waktu dan Pengeluaran | 2787409 | Pemberi izin yang tidak valid dapat menyetujui entri waktu non-proyek. |
| Manajemen peluang | 2788907 | Pesan kesalahan yang diperbarui pada validasi keunikan untuk baris pesanan yang mencakup tanda bendera. |
| Waktu dan Pengeluaran | 2842253 | Penanganan pengecualian nihil untuk persetujuan waktu. |
| Penagihan dan Harga | 2844181 | Gagal mendapatkan blok ID korelasi memblokir pembuatan faktur. |
| Penagihan dan Harga | 2876628 | QLD, CLD - Memperkirakan resolusi daftar harga harus menggunakan bidang rentang tanggal warisan dari daftar harga. |
| Membuat subkontrak | 2893222 | Jika tidak ada peran yang ditentukan untuk baris subkontrak, maka baris tersebut dapat dipilih pada anggota tim untuk peran apa pun. |
