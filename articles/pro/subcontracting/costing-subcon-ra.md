---
title: Perkiraan biaya penetapan sumber daya subkontrak
description: Ini topik menjelaskan beberapa cara Microsoft Dynamics 365 Project Operations menghitung estimasi biaya penugasan sumber daya subkontrak.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f276e12713261538d1e7520dac17243e578db433
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596698"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Perkiraan biaya penetapan sumber daya subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Penugasan tugas anggota tim proyek subkontrak dikenakan biaya menggunakan **daftar Harga pembelian** yang dilampirkan ke subkontrak pada catatan anggota tim terkait. Ini berbeda dari bagaimana tugas sumber daya karyawan dikenakan biaya di mana tugas tugas sumber daya karyawan dikenakan biaya menggunakan **daftar harga Biaya** yang melekat pada unit kontrak proyek. 

Untuk anggota tim proyek generik yang disubkontrakkan, tugas dikenakan biaya menggunakan pengaturan harga berbasis peran dalam daftar harga pembelian yang dilampirkan ke subkontrak. Harga pembelian juga dapat diatur khusus untuk setiap sumber daya. Harga khusus sumber daya ini akan diprioritaskan ketika tugas biaya tugas anggota tim proyek yang disebutkan adalah pekerja kontrak. 

Prioritas menggunakan harga pembelian khusus peran versus spesifik sumber daya didorong oleh pengaturan prioritas dimensi harga dalam **Parameter > Dimensi harga berbasis jumlah**.

Fungsi menurunkan harga secara dinamis berdasarkan pengaturan dimensi untuk harga pembelian subkontraktor ini mirip dengan bagaimana biaya dan tarif tagihan diturunkan untuk karyawan penuh waktu. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Membuat tugas tugas untuk mendapatkan perkiraan biaya sumber daya subkontraktor

Tugas tugas untuk subkontraktor dapat dibuat dengan dua cara: 
- Menggunakan tab **Tugas**.
- Menggunakan tab **Tim**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Membuat penetapan sumber daya menggunakan tab Tugas
**Menggunakan daftar Sumber Daya** di **tab Tugas** untuk tugas tertentu, Anda dapat membuat penetapan tugas untuk sumber daya bernama atau sumber daya generik. Jika Anda memilih sumber daya bernama dari **drop-down Sumber Daya** yang Ditetapkan pada tugas dan sumber daya ini adalah pekerja kontrak, sumber daya bernama ditetapkan ke tugas dan catatan anggota tim proyek yang sesuai dibuat dengan jenis pekerja yang diatur ke **Pekerja** Kontrak dan **Validitas** diatur ke **Tidak Valid**. Sebagai langkah selanjutnya, Anda harus membuka catatan anggota tim proyek dan memilih jalur subkontrak dan subkontrak. Ini akan memperbarui penugasan tugas untuk memiliki referensi ke jalur subkontrak dan subkontrak dan juga akan memperbarui status anggota tim menjadi **Valid**.

Jika Anda memilih untuk membuat anggota tim generik dari **drop-down Sumber Daya** yang Ditetapkan pada tugas tersebut, **dialog pembuatan** anggota tim Generik akan memungkinkan Anda memilih subkontrak dan subkontrak baris. Ketika sumber daya generik ditetapkan ke tugas dan catatan anggota tim proyek yang sesuai dibuat, Anda akan melihat bahwa catatan anggota tim proyek dibuat dengan jenis pekerja diatur ke **Pekerja** Kontrak dan **Validitas** diatur ke **Valid**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Membuat anggota tim proyek menggunakan tab Tim
Dengan menggunakan tab Tim pada proyek, Anda dapat membuat anggota tim generik atau bernama. Saat membuat anggota tim, Anda dapat memilih subkontrak dan subkontrak. Setelah anggota tim dibuat, Anda harus menetapkan anggota tim ke tugas menggunakan **drop-down Sumber Daya** yang Ditetapkan pada tugas tersebut. 

## <a name="updating-estimates"></a>Memperbarui estimasi
Setelah Anda menugaskan anggota tim proyek untuk tugas, Anda harus menavigasi ke **tab Perkiraan** pada proyek dan memilih **Perbarui harga** untuk memastikan bahwa tarif biaya penugasan sumber daya subkontraktor diperbarui berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. Estimasi tidak dihasilkan untuk tugas yang tidak ditetapkan di Microsoft Dynamics 365 Project Operations. Akibatnya, Anda perlu membuat tugas tugas untuk menentukan harga dan biaya berbagai tugas pada proyek Anda. 

> [CATATAN!] Anggota tim proyek yang memiliki **tipe** Pekerja sebagai **pekerja** Kontrak tetapi tidak memiliki referensi subkontrak ditandai sebagai **Tidak Valid** pada **kisi anggota** tim Proyek. Jika ada anggota tim proyek dengan status ini, buka catatan anggota tim proyek dan perbarui bidang jalur subkontrak dan subkontrak secara manual sehingga perkiraan biaya keuangan secara akurat mencerminkan biaya subkontraktor pada **tab Perkiraan**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
