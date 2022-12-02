---
title: Mencatat waktu, pengeluaran, dan penggunaan bahan untuk komponen subkontrak
description: Artikel ini menjelaskan cara kerja, pengeluaran, dan penggunaan bahan yang direkam pada proyek dari komponen subkontrak yang dilacak oleh Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522517"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Mencatat waktu, pengeluaran, dan penggunaan bahan pada proyek untuk komponen subkontrak

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Artikel ini menjelaskan cara kerja, pengeluaran, dan penggunaan bahan yang direkam pada proyek dari komponen subkontrak yang dilacak oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Biaya untuk waktu subkontraktor pada proyek
Dalam Project Operations, pekerja kontrak dapat merekam waktu pada proyek dengan cara yang sama seperti karyawan. Saat memasukkan waktu pada proyek dan/atau tugas proyek, pekerja kontrak dapat memilih baris subkontrak dan subkontrak spesifik.

Bila waktu yang diajukan oleh pekerja kontrak disetujui, biaya proyek dicatat menggunakan tingkat biaya unit yang disiapkan untuk sumber daya pekerja kontrak tersebut di bagian **Harga Peran** dari daftar harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Biaya untuk pengeluaran subkontrak pada proyek
Saat memasukkan pengeluaran yang dikeluarkan pada proyek, Anda dapat memilih baris subkontrak dan subkontrak pada entri pengeluaran. 

Bila entri pengeluaran ini diajukan dan disetujui, biaya pengeluaran dicatat di proyek berdasarkan biaya unit yang disiapkan untuk kategori transaksi di bagian **Harga Kategori** dari daftar harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Biaya untuk bahan subkontrak pada proyek
Saat memasukkan penggunaan bahan pada proyek, Anda dapat memilih baris subkontrak dan subkontrak pada log penggunaan bahan. Bila log penggunaan bahan diajukan dan disetujui, biaya bahan dicatat di proyek berdasarkan biaya unit yang disiapkan untuk produk tersebut di bagian **item daftar harga** dari daftar harga subkontrak.

Penggunaan bahan juga dapat dicatat untuk produk pilihan pada proyek. Jenis penggunaan bahan ini juga dapat ditautkan ke baris subkontrak dan subkontrak. Ketika mencatat penggunaan materi untuk produk pilihan, Anda harus memasukkan biaya per unit produk pilihan. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
