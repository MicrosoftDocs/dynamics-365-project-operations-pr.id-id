---
title: Koneksi transaksi - Tautkan aktual dengan jenis transaksi yang berbeda
description: Artikel ini menjelaskan bagaimana koneksi transaksi digunakan untuk menautkan aktual dari berbagai jenis untuk membantu melacak profitabilitas, backlog penagihan, dan perhitungan pendapatan yang ditagih versus tidak ditagih.
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

Catatan koneksi transaksi dibuat untuk menghubungkan aktual dari berbagai jenis saat waktu, pengeluaran, atau penggunaan material bergerak dalam siklus hidupnya dari kutipan atau tahap pra-penjualan ke tahap kontrak, persetujuan dan/atau penarikan kembali, faktur, dan potensi kredit atau faktur korektif.

Contoh berikut menunjukkan pemrosesan tipikal waktu entri dalam siklus hidup proyek Project Operations.

> ![Memproses entri waktu dalam Operasi Proyek.](media/basic-guide-17.png)

Pemrosesan entri waktu dalam siklus hidup proyek Operasi Proyek mengikuti langkah-langkah berikut: 

1. Pengajuan entri waktu menyebabkan dua baris jurnal dibuat: satu untuk biaya dan satu untuk penjualan yang tidak ditagih. 
2. Persetujuan akhirnya dari entri waktu menyebabkan dua aktual dibuat: satu untuk biaya dan satu untuk penjualan yang tidak ditagih. 2 aktual ini ditautkan menggunakan koneksi transaksi.
3. Saat pengguna membuat faktur proyek, transaksi baris faktur dibuat menggunakan data dari nilai aktual penjualan yang belum ditagih.
4. Ketika faktur dikonfirmasi, ini menciptakan dua aktual baru: pembalikan penjualan yang tidak ditagih dan aktual penjualan yang ditagih. Pembalikan penjualan yang tidak ditagih dan aktual penjualan asli yang tidak ditagih terhubung menggunakan koneksi transaksi yang terbalik. Penjualan yang ditagih dan aktual penjualan asli yang belum ditagih juga terhubung untuk menunjukkan hubungan antara apa yang dulunya merupakan pendapatan backlog atau work in progress (WIP) dengan apa yang sekarang ditagih pendapatan.   

Setiap peristiwa dalam alur kerja pemrosesan memicu pembuatan rekaman dalam **tabel koneksi** Transaksi. Ini membantu membangun jejak Relasi antara catatan yang dibuat di seluruh entri waktu, baris jurnal, aktual, dan detail baris faktur.

Tabel berikut ini memperlihatkan rekaman dalam **entitas Koneksi** transaksi untuk alur kerja sebelumnya.

|Aktivitas                   |Transaksi 1                 |Peran Transaksi 1 |Jenis Transaksi 1       |Transaksi 2          |Peran Transaksi 2 |Jenis Transaksi 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Pengajuan entri waktu   |GUID baris jurnal (penjualan)     |Penjualan Belum Tertagih |msdyn_journalline            |GUID baris jurnal (biaya)     |Biaya            |msdyn_journalline  |
|Persetujuan Waktu           |GUID Aktual Belum Tertagih (Penjualan)  |Penjualan Belum Tertagih |msdyn_actual                 |GUID Aktual Biaya (biaya)       |Biaya            |msdyn_actual       |
|Pembuatan Faktur        |GUID Rincian Baris Faktur      |Penjualan yang Ditagih   |msdyn_invoicelinetransaction |GUID Aktual Penjualan Belum Tertagih   |Penjualan Belum Tertagih  |msdyn_actual       |
|Konfirmasi Faktur    |Membalikkan GUID aktual         |Balik      |msdyn_actual                 |GUID Penjualan Belum Tertagih Asli |Asli        |msdyn_actual       |
|                        |GUID Penjualan Tertagih             |Penjualan yang Ditagih   |msdyn_actual                 |GUID Aktual Penjualan Belum Tertagih   |Penjualan Belum Tertagih  |msdyn_actual       |
|Koreksi faktur draft |GUID Transaksi Baris Faktur|Mengganti      |msdyn_invoicelinetransaction |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |
|Konfirmasi Koreksi faktur|GUID Pembalikan penjualan tertagih  |Balik      |msdyn_actual                 |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |
|                        |GUID Penjualan Baru yang Belum Ditagih |Mengganti            |msdyn_actual                 |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |


Ilustrasi berikut menunjukkan link yang dibuat antara berbagai jenis aktual di berbagai peristiwa menggunakan contoh entri waktu dalam Operasi Proyek.

> ![Bagaimana aktual dari berbagai jenis terkait satu sama lain dalam Operasi Proyek.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
