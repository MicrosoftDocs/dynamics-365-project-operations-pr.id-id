---
title: Koneksi transaksi - Menautkan aktual dari berbagai jenis transaksi
description: Ini topik menjelaskan bagaimana koneksi transaksi digunakan untuk menghubungkan aktual dari berbagai jenis untuk membantu melacak profitabilitas, penagihan backlog, dan ditagih versus perhitungan pendapatan yang tidak ditagih.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580782"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Koneksi transaksi - Menautkan aktual dari berbagai jenis transaksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Catatan koneksi transaksi dibuat untuk menghubungkan aktual dari berbagai jenis saat waktu, biaya, atau penggunaan material bergerak dalam siklus hidupnya dari tahap penawaran atau pra-penjualan ke tahap kontrak, persetujuan dan / atau penarikan, faktur, dan berpotensi kredit atau faktur korektif.

Contoh berikut menunjukkan pemrosesan tipikal waktu entri dalam siklus hidup proyek Project Operations.

> ![Memproses entri waktu dalam Operasi Proyek.](media/basic-guide-17.png)

Pemrosesan entri waktu dalam siklus hidup proyek Operasi Proyek mengikuti langkah-langkah berikut: 

1. Pengajuan entri waktu menyebabkan dua baris jurnal dibuat: satu untuk biaya dan satu untuk penjualan yang tidak ditagih. 
2. Persetujuan akhirnya dari entri waktu menyebabkan dua aktual dibuat: satu untuk biaya dan satu untuk penjualan yang tidak ditagih. Kedua aktual ini ditautkan menggunakan koneksi transaksi.
3. Saat pengguna membuat faktur proyek, transaksi baris faktur dibuat menggunakan data dari nilai aktual penjualan yang belum ditagih.
4. Ketika faktur dikonfirmasi, ini menciptakan dua aktual baru: pembalikan penjualan yang tidak ditagih dan penjualan yang ditagih aktual. Pembalikan penjualan yang tidak ditagih dan penjualan asli yang tidak ditagih sebenarnya terhubung menggunakan koneksi transaksi pembalikan. Penjualan yang ditagih dan aktual penjualan asli yang tidak ditagih juga terhubung untuk menunjukkan hubungan antara apa yang dulunya backlog atau pendapatan work in progress (WIP) dengan apa yang sekarang ditagih pendapatan.   

Setiap peristiwa dalam alur kerja pemrosesan memicu pembuatan catatan dalam **tabel Koneksi** transaksi. Ini membantu membangun jejak Relasi antara catatan yang dibuat di seluruh entri waktu, baris jurnal, aktual, dan detail baris faktur.

Tabel berikut menunjukkan catatan dalam **entitas koneksi** Transaksi untuk alur kerja sebelumnya.

|Aktivitas                   |Transaksi 1                 |Peran Transaksi 1 |Jenis Transaksi 1       |Transaksi 2          |Peran Transaksi 2 |Jenis Transaksi 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Pengajuan entri waktu   |GUID baris jurnal (penjualan)     |Penjualan Belum Tertagih |msdyn_journalline            |GUID baris jurnal (biaya)     |Biaya            |msdyn_journalline  |
|Persetujuan Waktu           |GUID Aktual Belum Tertagih (Penjualan)  |Penjualan Belum Tertagih |msdyn_actual                 |GUID Aktual Biaya (biaya)       |Biaya            |msdyn_actual       |
|Pembuatan Faktur        |GUID Rincian Baris Faktur      |Penjualan yang Ditagih   |msdyn_invoicelinetransaction |GUID Aktual Penjualan Belum Tertagih   |Penjualan Belum Tertagih  |msdyn_actual       |
|Konfirmasi Faktur    |Membalikkan GUID aktual         |Balik      |msdyn_actual                 |GUID Penjualan Belum Tertagih Asli |Asli        |msdyn_actual       |
|                        |GUID Penjualan Tertagih             |Penjualan yang Ditagih   |msdyn_actual                 |GUID Aktual Penjualan Belum Tertagih   |Penjualan Belum Tertagih  |msdyn_actual       |
|Koreksi faktur draft |GUID Transaksi Baris Faktur|Mengganti      |msdyn_invoicelinetransaction |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |
|Konfirmasi Koreksi faktur|GUID Pembalikan penjualan tertagih  |Balik      |msdyn_actual                 |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |
|                        |GUID Penjualan Baru yang Tidak Ditagih |Mengganti            |msdyn_actual                 |GUID Penjualan Tertagih            |Asli        |msdyn_actual       |


Ilustrasi berikut menunjukkan tautan yang dibuat di antara berbagai jenis aktual di berbagai acara menggunakan contoh entri waktu dalam Operasi Proyek.

> ![Bagaimana aktual dari berbagai jenis terkait satu sama lain dalam Operasi Proyek.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
