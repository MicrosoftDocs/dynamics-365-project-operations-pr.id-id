---
title: Koneksi transaksi - Tautkan aktual dengan jenis transaksi yang berbeda
description: Artikel ini menjelaskan cara koneksi transaksi digunakan untuk menghubungkan aktual dari berbagai jenis untuk membantu melacak profitabilitas, penagihan backlog, dan menjeda perhitungan pendapatan yang belum ditagih.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926090"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Koneksi transaksi - Tautkan aktual dengan jenis transaksi yang berbeda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Rekaman koneksi transaksi dibuat untuk menautkan aktual dari berbagai jenis waktu, pengeluaran, atau penggunaan bahan yang bergerak dalam siklus hidupnya dari tahapan kuotasi, atau pra-penjualan ke tahapan kontrak, perjanjian dan/atau penarikan, faktur, dan kemungkinan faktur kredit atau perbaikan.

Contoh berikut menunjukkan pemrosesan tipikal waktu entri dalam siklus hidup proyek Project Operations.

> ![Memproses entri waktu di Project Operations.](media/basic-guide-17.png)

Pemrosesan entri waktu dalam siklus hidup proyek Project Operations mengikuti langkah-langkah ini: 

1. Pengajuan entri waktu menyebabkan dua baris jurnal dibuat: satu untuk biaya dan satu untuk penjualan yang belum ditagih. 
2. Persetujuan akhir entri waktu menyebabkan dua nilai aktual dibuat: satu untuk biaya dan satu untuk penjualan yang belum ditagih. 2 aktual ini ditautkan menggunakan koneksi transaksi.
3. Saat pengguna membuat faktur proyek, transaksi baris faktur dibuat menggunakan data dari nilai aktual penjualan yang belum ditagih.
4. Setelah faktur dikonfirmasi, ini membuat dua aktual baru: pembalikan aktual penjualan yang belum ditagih dan penjualan tertagih. Pembalikan penjualan belum ditagih dan aktual penjualan belum ditagih asli tersambung menggunakan koneksi transaksi pembalikan. Aktual penjualan ditagih dan aktual penjualan belum ditagih asli juga tersambung untuk menampilkan tautan antara pendapatan yang dulunya adalah backlog atau pekerjaan dalam proses (WIP) ke pendapatan yang sekarang ditagih.   

Setiap aktivitas dalam alur kerja pemrosesan memicu pembuatan rekaman dalam tabel **koneksi Transaksi**. Ini membantu membuat pelacakan relasi antara rekaman yang dibuat di seluruh entri waktu, baris jurnal, aktual, dan rincian baris faktur.

Tabel berikut Menampilkan rekaman di entitas **koneksi transaksi** untuk alur kerja sebelumnya.

|Aktivitas                   |Transaksi 1                 |Peran Transaksi 1 |Jenis Transaksi 1       |Transaksi 2          |Peran Transaksi 2 |Jenis Transaksi 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Pengajuan entri waktu   |GUID baris jurnal (penjualan)     |Penjualan Belum Tertagih |msdyn_journalline            |GUID baris jurnal (biaya)     |Biaya            |msdyn_journalline  |
|Persetujuan Waktu           |GUID Aktual Belum Tertagih (Penjualan)  |Penjualan Belum Tertagih |msdyn_actual                 |GUID Aktual Biaya (biaya)       |Biaya            |msdyn_actual       |
|Pembuatan Faktur        |GUID Rincian Baris Faktur      |Penjualan yang Ditagih   |msdyn_invoicelinetransaction |GUID Aktual Penjualan Belum Tertagih   |Penjualan Belum Tertagih  |msdyn_actual       |
|Konfirmasi Faktur    |Membalikkan GUID aktual         |Balik      |msdyn_actual                 |GUID Penjualan Belum Tertagih Asli |Asli        |msdyn_actual       |
|                        |GUID Penjualan Tertagih             |Penjualan yang Ditagih   |msdyn_actual                 |GUID Aktual Penjualan Belum Tertagih   |Penjualan Belum Tertagih  |msdyn_actual       |
|Koreksi faktur draft |GUID Transaksi Baris Faktur|Mengganti      |msdyn_invoicelinetransaction |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |
|Konfirmasi Koreksi faktur|GUID Pembalikan penjualan tertagih  |Balik      |msdyn_actual                 |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |
|                        |GUID Penjualan belum tertagih baru |Mengganti            |msdyn_actual                 |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |


Ilustrasi berikut menampilkan tautan yang dibuat antara berbagai jenis aktual pada berbagai aktivitas menggunakan contoh entri waktu di Project Operations.

> ![Bagaimana aktual dari berbagai jenis terhubung satu sama lain di Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
