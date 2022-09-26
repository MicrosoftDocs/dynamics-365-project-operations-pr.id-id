---
title: Mencatat waktu, pengeluaran, dan penggunaan bahan untuk komponen subkontrak
description: Artikel ini menjelaskan bagaimana waktu, pengeluaran, dan penggunaan material yang dicatat pada proyek dari komponen yang disubkontrakkan dilacak oleh Microsoft Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Mencatat waktu, pengeluaran, dan penggunaan material pada proyek untuk komponen yang disubkontrakkan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Artikel ini menjelaskan bagaimana waktu, pengeluaran, dan penggunaan material yang dicatat pada proyek dari komponen yang disubkontrakkan dilacak oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Penetapan biaya untuk waktu subkontraktor pada proyek
Dalam Operasi Proyek, pekerja kontrak dapat mencatat waktu pada proyek dengan cara yang sama seperti karyawan. Saat memasukkan waktu pada proyek dan/atau tugas proyek, pekerja kontrak dapat memilih jalur subkontrak dan subkontrak tertentu.

Ketika waktu yang diajukan oleh pekerja kontrak disetujui, biaya proyek dicatat menggunakan tarif biaya unit yang ditetapkan untuk sumber daya pekerja kontrak tersebut **di bagian Harga** peran dari daftar harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Biaya untuk biaya subkontrak pada proyek
Saat memasukkan biaya yang dikeluarkan untuk proyek, Anda dapat memilih jalur subkontrak dan subkontrak pada entri biaya. 

Ketika entri pengeluaran ini diajukan dan disetujui, biaya pengeluaran dicatat pada proyek berdasarkan biaya unit yang disiapkan untuk kategori transaksi tersebut **di bagian Harga** kategori dari daftar harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Penetapan biaya untuk bahan yang disubkontrakkan pada proyek
Saat memasukkan penggunaan material pada proyek, Anda dapat memilih baris subkontrak dan subkontrak pada log penggunaan material. Ketika log penggunaan material diserahkan dan disetujui, biaya material dicatat pada proyek berdasarkan biaya unit yang disiapkan untuk produk tersebut **di bagian Item daftar** harga dari daftar harga subkontrak.

Penggunaan material juga dapat direkam untuk produk write-in pada proyek. Jenis penggunaan material ini juga dapat ditautkan ke garis subkontrak dan subkontrak. Saat merekam penggunaan bahan untuk produk write-in, Anda harus memasukkan biaya per unit produk write-in. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
