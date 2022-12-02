---
title: Perkiraan biaya penetapan sumber daya subkontrak
description: Artikel ini menjelaskan beberapa cara Microsoft Dynamics 365 Project Operations menghitung perkiraan biaya penugasan sumber daya subkontrak.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522658"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Perkiraan biaya penetapan sumber daya subkontrak

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Penugasan tugas anggota tim proyek subkontrak dihitung biayanya menggunakan daftar harga **Pembelian** yang dilampirkan ke subkontrak pada catatan anggota tim terkait. Hal ini berbeda dengan bagaimana penugasan sumber daya karyawan dihitung biayanya di mana penugasan tugas sumber daya karyawan dihitung biayanya menggunakan daftar harga **Biaya** yang dilampirkan ke dalam unit kontrak proyek. 

Untuk anggota tim proyek generik yang disubkontrakkan, penugasan biayanya menggunakan pengaturan harga berbasis peran dalam daftar harga pembelian yang dilampirkan pada subkontrak. Harga pembelian juga dapat diatur khusus untuk setiap sumber daya. Harga khusus sumber daya ini akan menjadi prioritas ketika biaya penugasan tugas anggota tim proyek yang bernama adalah pekerja kontrak. 

Prioritas penggunaan harga pembelian khusus peran versus khusus sumber daya didorong oleh penyiapan prioritas dimensi harga di **Parameter > Dimensi harga berbasis jumlah**.

Fungsi turunan dinamis harga berdasarkan konfigurasi dimensi untuk harga pembelian subkontraktor ini mirip dengan cara diturunkannya biaya dan tingkat tagihan untuk karyawan penuh waktu. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Membuat penugasan tugas untuk mendapatkan estimasi biaya sumber daya subkontraktor

Penugasan tugas untuk subkontraktor dapat dibuat dengan dua cara: 
- Pilih tab **Tugas**.
- Pilih tab **Tim**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Membuat penugasan sumber daya menggunakan tab Tugas
Menggunakan daftar **Sumber Daya** dalam tab **Tugas** untuk tugas tertentu, Anda dapat membuat penugasan tugas untuk sumber daya bernama atau sumber daya generik. Jika Anda memilih sumber daya bernama dari drop-down **Sumber Daya yang Ditetapkan** pada tugas dan sumber daya ini adalah pekerja kontrak, sumber daya bernama ditetapkan ke tugas dan rekaman anggota tim proyek yang terkait dibuat dengan jenis pekerja yang diatur ke **Pekerja Kontrak** dan **Validitas** diatur ke **Tidak Valid**. Sebagai langkah berikutnya, Anda harus membuka rekaman anggota tim proyek dan memilih subkontrak dan baris subkontrak. Langkah ini akan memperbarui penugasan tugas untuk memiliki referensi ke subkontrak dan baris subkontrak dan juga akan memperbarui status anggota tim menjadi **Valid**.

Jika Anda memilih untuk membuat anggota tim generik dari drop-down **Sumber Daya** pada tugas, dialog **Pembuatan anggota tim generik** akan memungkinkan Anda memilih subkontrak dan baris subkontrak. Bila sumber daya generik ditetapkan ke tugas dan rekaman anggota tim proyek yang terkait sudah dibuat, Anda akan melihat bahwa rekaman anggota tim proyek dibuat dengan jenis pekerja yang diatur ke **Pekerja Kontrak** dan **Validitas** diatur ke **Valid**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Membuat anggota tim proyek menggunakan tab Tim
Menggunakan tab Tim di proyek, Anda dapat membuat generik atau anggota tim bernama. Saat membuat anggota tim, Anda dapat memilih subkontrak dan baris subkontrak. Setelah anggota tim dibuat, Anda harus menetapkan anggota tim ke tugas menggunakan drop-down **Sumber Daya** drop-down pada tugas. 

## <a name="updating-estimates"></a>Estimasi pembaruan
Setelah menetapkan anggota tim proyek ke tugas, Anda harus menavigasi ke tab **Estimasi** pada proyek dan memilih **Perbarui harga** untuk memastikan bahwa tingkat biaya penugasan sumber daya subkontrak diperbarui berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. Estimasi tidak dibuat untuk tugas yang tidak ditentukan di Microsoft Dynamics 365 Project Operations. Karenanya, Anda harus membuat penugasan tugas hingga harga dan biaya berbagai tugas pada proyek Anda. 

> [CATATAN!] Anggota tim proyek yang memiliki **Jenis pekerja** sebagai **Pekerja Kontrak** tetapi tidak memiliki referensi subkontrak ditandai sebagai **Tidak Valid** pada kisi **Anggota tim proyek**. Jika jika ada anggota tim proyek dengan status ini, buka rekaman anggota tim proyek dan secara manual memperbarui bidang subkontrak dan baris subkontrak sehingga estimasi biaya keuangan bisa secara akurat mencerminkan biaya subkontraktor pada tab **Estimasi**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
