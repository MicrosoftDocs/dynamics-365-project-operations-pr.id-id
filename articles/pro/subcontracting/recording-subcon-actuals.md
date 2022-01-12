---
title: Mencatat waktu, pengeluaran, dan penggunaan material untuk komponen subkontrak
description: Ini topik menjelaskan bagaimana waktu, biaya, dan penggunaan material yang tercatat pada proyek-proyek dari komponen subkontrak dilacak oleh Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903689"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Mencatat waktu, pengeluaran, dan penggunaan material pada proyek untuk komponen subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Ini topik menjelaskan bagaimana waktu, biaya, dan penggunaan material yang tercatat pada proyek-proyek dari komponen subkontrak dilacak oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Biaya untuk waktu subkontraktor pada proyek
Dalam Operasi Proyek, pekerja kontrak dapat mencatat waktu pada proyek dengan cara yang sama seperti karyawan. Saat memasuki waktu pada proyek dan / atau tugas proyek, pekerja kontrak dapat memilih jalur subkontrak dan subkontrak tertentu.

Ketika waktu yang diajukan oleh pekerja kontrak disetujui, biaya proyek dicatat menggunakan tingkat biaya unit yang disiapkan untuk sumber daya pekerja kontrak di **bagian harga Peran dari daftar harga pembelian pada** subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Biaya untuk biaya subkontrak pada proyek
Saat memasukkan biaya yang dikeluarkan pada proyek, Anda dapat memilih baris subkontrak dan subkontrak pada entri biaya. 

Ketika entri biaya ini diajukan dan disetujui, biaya biaya dicatat pada proyek berdasarkan biaya unit yang ditetapkan untuk kategori transaksi tersebut di **bagian harga Kategori dari daftar harga pembelian pada** subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Biaya untuk bahan subkontrak pada proyek
Saat memasukkan penggunaan material pada proyek, Anda dapat memilih baris subkontrak dan subkontrak pada log penggunaan material. Ketika log penggunaan material diserahkan dan disetujui, biaya material dicatat pada proyek berdasarkan biaya unit yang disiapkan untuk produk tersebut di **bagian item daftar Harga dari daftar harga** subkontrak.

Penggunaan material juga dapat dicatat untuk menulis-dalam produk pada proyek-proyek. Jenis penggunaan material ini juga dapat dihubungkan ke garis subkontrak dan subkontrak. Saat merekam penggunaan materi untuk produk write-in, Anda perlu memasukkan biaya per unit dari produk write-in. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
