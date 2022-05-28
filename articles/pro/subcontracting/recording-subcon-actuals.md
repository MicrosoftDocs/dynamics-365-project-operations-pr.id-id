---
title: Mencatat waktu, pengeluaran, dan penggunaan bahan untuk komponen subkontrak
description: Ini topik menjelaskan bagaimana waktu, biaya, dan penggunaan material yang dicatat pada proyek-proyek dari komponen subkontrak dilacak oleh Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a31b4a1092cc4829cbfc789e8b8e30030b2826b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599228"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Waktu pencatatan, pengeluaran, dan penggunaan material pada proyek untuk komponen subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Ini topik menjelaskan bagaimana waktu, biaya, dan penggunaan material yang dicatat pada proyek-proyek dari komponen subkontrak dilacak oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Biaya untuk waktu subkontraktor pada proyek
Dalam Operasi Proyek, pekerja kontrak dapat mencatat waktu pada proyek dengan cara yang sama seperti karyawan. Saat memasukkan waktu pada proyek dan / atau tugas proyek, pekerja kontrak dapat memilih subkontrak dan subkontrak tertentu.

Ketika waktu yang diajukan oleh pekerja kontrak disetujui, biaya proyek dicatat menggunakan tarif biaya unit yang ditetapkan untuk sumber daya pekerja kontrak di **bagian Harga** peran dari daftar harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Biaya untuk biaya subkontrak pada proyek
Saat memasukkan biaya yang dikeluarkan pada proyek, Anda dapat memilih jalur subkontrak dan subkontrak pada entri pengeluaran. 

Ketika entri biaya ini diajukan dan disetujui, biaya pengeluaran dicatat pada proyek berdasarkan biaya unit yang disiapkan untuk kategori transaksi tersebut **di bagian Harga** kategori dari daftar harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Biaya untuk bahan subkontrak pada proyek
Saat memasukkan penggunaan material pada proyek, Anda dapat memilih jalur subkontrak dan subkontrak pada log penggunaan material. Ketika log penggunaan material diserahkan dan disetujui, biaya material dicatat pada proyek berdasarkan biaya unit yang disiapkan untuk produk tersebut **di bagian Item** daftar harga dari daftar harga.

Penggunaan material juga dapat dicatat untuk produk tulis pada proyek. Jenis penggunaan material ini juga dapat dikaitkan dengan jalur subkontrak dan subkontrak. Saat merekam penggunaan materi untuk produk tulis, Anda harus memasukkan biaya per unit produk tulis. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
