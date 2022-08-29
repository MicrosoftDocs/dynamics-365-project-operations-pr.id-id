---
title: Perkiraan biaya penetapan sumber daya subkontrak
description: Artikel ini menjelaskan beberapa cara Microsoft Dynamics 365 Project Operations menghitung estimasi biaya penugasan sumber daya yang disubkontrakkan.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262063"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Perkiraan biaya penetapan sumber daya subkontrak

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Penugasan tugas anggota tim proyek yang disubkontrakkan dikenakan biaya menggunakan **daftar harga Pembelian** yang dilampirkan ke subkontrak pada catatan anggota tim terkait. Ini berbeda dengan bagaimana penugasan sumber daya karyawan dikenakan biaya di mana penugasan tugas sumber daya karyawan dikenakan biaya menggunakan **daftar Harga biaya** yang dilampirkan pada unit kontrak proyek. 

Untuk anggota tim proyek generik yang disubkontrakkan, penugasan dikenakan biaya menggunakan pengaturan harga berbasis peran dalam daftar harga pembelian yang dilampirkan pada subkontrak. Harga pembelian juga dapat diatur khusus untuk setiap sumber daya. Harga khusus sumber daya ini akan diprioritaskan ketika penetapan biaya tugas dari anggota tim proyek yang disebutkan adalah pekerja kontrak. 

Prioritas penggunaan harga pembelian khusus peran versus spesifik sumber daya didorong oleh penyiapan prioritas dimensi harga dalam **Parameter > dimensi penetapan harga berbasis jumlah**.

Fungsionalitas harga yang diturunkan secara dinamis berdasarkan pengaturan dimensi untuk harga pembelian subkontraktor ini mirip dengan bagaimana biaya dan tarif tagihan diturunkan untuk karyawan penuh waktu. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Membuat penetapan tugas untuk mendapatkan perkiraan biaya sumber daya subkontraktor

Penetapan tugas untuk subkontraktor dapat dibuat dengan dua cara: 
- Menggunakan tab **Tugas**.
- Menggunakan tab **Tim**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Membuat penetapan sumber daya menggunakan tab Tugas
Dengan menggunakan **daftar Sumber Daya** di tab **Tugas** untuk tugas tertentu, Anda bisa membuat penetapan tugas untuk sumber daya bernama atau sumber daya generik. Jika Anda memilih sumber daya bernama dari **drop-down Sumber Daya** yang Ditetapkan pada tugas dan sumber daya ini adalah pekerja kontrak, sumber daya bernama ditetapkan ke tugas dan catatan anggota tim proyek yang sesuai dibuat dengan jenis pekerja yang diatur ke **Pekerja** Kontrak dan **Validitas diatur ke** Tidak **Validitas**. Sebagai langkah berikutnya, Anda harus membuka catatan anggota tim proyek dan memilih baris subkontrak dan subkontrak. Ini akan memperbarui penetapan tugas untuk memiliki referensi ke baris subkontrak dan subkontrak dan juga akan memperbarui status anggota tim ke **Valid**.

Jika Anda memilih untuk membuat anggota tim generik dari **drop-down Sumber Daya** yang Ditetapkan pada tugas, **dialog Pembuatan** anggota tim generik akan memungkinkan Anda memilih baris subkontrak dan subkontrak. Ketika sumber daya generik ditetapkan ke tugas dan catatan anggota tim proyek yang sesuai dibuat, Anda akan melihat bahwa catatan anggota tim proyek dibuat dengan jenis pekerja yang diatur ke **Pekerja Kontrak dan** Validitas **diatur ke** Valid **·**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Membuat anggota tim proyek menggunakan tab Tim
Dengan menggunakan tab Tim pada proyek, Anda dapat membuat anggota tim generik atau bernama. Saat membuat anggota tim, Anda dapat memilih baris subkontrak dan subkontrak. Setelah anggota tim dibuat, Anda harus menetapkan anggota tim ke tugas menggunakan **drop-down Sumber Daya** yang Ditetapkan pada tugas tersebut. 

## <a name="updating-estimates"></a>Memperbarui perkiraan
Setelah anda menetapkan anggota tim proyek untuk tugas, anda harus menavigasi ke **tab Perkiraan** pada proyek dan memilih **Perbarui harga** untuk memastikan bahwa tarif biaya penugasan sumber daya subkontraktor diperbarui berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. Perkiraan tidak dibuat untuk tugas yang belum ditetapkan di Microsoft Dynamics 365 Project Operations. Akibatnya, Anda harus membuat tugas tugas untuk menentukan harga dan biaya berbagai tugas pada proyek Anda. 

> [CATATAN!] Anggota tim proyek yang memiliki **tipe** Pekerja sebagai **pekerja** Kontrak tetapi tidak memiliki referensi subkontrak ditandai sebagai **Tidak Valid** pada **kisi anggota** tim Proyek. Jika ada anggota tim proyek dengan status ini, buka catatan anggota tim proyek dan perbarui bidang baris subkontrak dan subkontrak secara manual sehingga perkiraan biaya keuangan secara akurat mencerminkan biaya subkontraktor pada **tab Perkiraan**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
