---
title: Estimasi biaya tugas sumber daya subkontrak
description: Ini topik menjelaskan beberapa bagaimana Microsoft Dynamics 365 Project Operations menghitung estimasi biaya penugasan sumber daya subkontrak.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903686"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimasi biaya tugas sumber daya subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Tugas anggota tim proyek subkontrak dikenakan biaya menggunakan **daftar harga Pembelian yang** dilampirkan ke subkontrak pada catatan anggota tim terkait. Ini berbeda dari bagaimana tugas sumber daya karyawan dikenakan biaya di mana tugas sumber daya karyawan dikenakan biaya menggunakan **daftar harga Biaya yang melekat pada unit kontraktor** proyek. 

Untuk anggota tim proyek generik yang disubkontrakkan, tugas dikenakan biaya menggunakan pengaturan harga berbasis peran dalam daftar harga pembelian yang melekat pada subkontrak. Harga pembelian juga dapat diatur khusus untuk setiap sumber daya. Harga khusus sumber daya ini akan diberikan prioritas ketika biaya tugas anggota tim proyek bernama adalah pekerja kontrak. 

Prioritas menggunakan harga pembelian spesifik peran versus spesifik sumber daya didorong oleh pengaturan prioritas dimensi harga dalam **Parameter > dimensi penetapan harga berbasis jumlah**.

Fungsi harga yang berasal secara dinamis berdasarkan pengaturan dimensi untuk harga pembelian subkontraktor mirip dengan bagaimana biaya dan tarif tagihan diturunkan untuk karyawan penuh waktu. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Membuat tugas untuk mendapatkan perkiraan biaya sumber daya subkontraktor

Tugas untuk subkontraktor dapat dibuat dengan dua cara: 
- Menggunakan **tab** Tugas.
- Menggunakan **tab** Tim.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Membuat tugas sumber daya menggunakan tab Tugas
Menggunakan **daftar Sumber Daya** di tab Tugas untuk tugas **tertentu**, Anda dapat membuat tugas untuk sumber daya bernama atau sumber daya generik. Jika Anda memilih sumber daya bernama dari **drop-down Sumber Daya yang Ditetapkan** pada tugas dan sumber daya ini adalah pekerja kontrak, sumber daya bernama ditugaskan ke tugas dan catatan anggota tim proyek yang sesuai dibuat dengan tipe pekerja yang ditetapkan ke Pekerja Kontrak **dan Validitas diatur ke Tidak Valid** **·** **·**. Sebagai langkah selanjutnya, Anda harus membuka catatan anggota tim proyek dan memilih baris subkontrak dan subkontrak. Ini akan memperbarui tugas untuk memiliki referensi ke baris subkontrak dan subkontrak dan juga akan memperbarui status anggota tim ke **Valid**.

Jika Anda memilih untuk membuat anggota tim generik dari **drop-down Sumber Daya yang Ditugaskan** pada tugas, **dialog pembuatan anggota tim Generik akan memungkinkan Anda untuk memilih baris** subkontrak dan subkontrak. Ketika sumber daya generik ditugaskan untuk tugas dan catatan anggota tim proyek yang sesuai dibuat, Anda akan melihat bahwa catatan anggota tim proyek dibuat dengan tipe pekerja yang ditetapkan untuk **Pekerja Kontrak dan Validitas ditetapkan ke Valid** **·** **·**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Membuat anggota tim proyek menggunakan tab Tim
Dengan menggunakan tab Tim pada proyek, Anda dapat membuat anggota tim generik atau bernama. Saat membuat anggota tim, Anda dapat memilih baris subkontrak dan subkontrak. Setelah anggota tim dibuat, Anda harus menetapkan anggota tim ke tugas menggunakan **drop-down Sumber Daya yang Ditetapkan** pada tugas. 

## <a name="updating-estimates"></a>Memperbarui perkiraan
Setelah Anda menugaskan anggota tim proyek untuk tugas, Anda perlu menavigasi ke **tab Perkiraan pada proyek dan pilih** **Perbarui harga untuk memastikan bahwa tingkat** biaya penugasan sumber daya subkontraktor diperbarui berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. Perkiraan tidak dihasilkan untuk tugas yang tidak ditetapkan di Microsoft Dynamics 365 Project Operations. Akibatnya, Anda perlu membuat tugas untuk harga dan biaya berbagai tugas pada proyek Anda. 

> [CATATAN!] Anggota tim proyek yang memiliki **tipe Pekerja sebagai pekerja Kontrak tetapi tidak memiliki referensi** **subkontrak** ditandai sebagai **Tidak Valid pada jaringan anggota tim** **Proyek**. Jika ada anggota tim proyek dengan status ini, buka catatan anggota tim proyek dan perbarui bidang garis subkontrak dan subkontrak secara manual sehingga perkiraan biaya keuangan secara akurat mencerminkan biaya subkontraktor pada **tab** Perkiraan. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
