---
title: pengaturan proyek
description: Topik ini menyediakan informasi tentang pengaturan manajemen proyek.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148152"
---
# <a name="project-settings"></a>pengaturan proyek

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Gunakan pengaturan berikut untuk mengakses fitur Perencanaan proyek.

## <a name="work-template"></a>Template kerja

Untuk membuat jadwal proyek, Anda membuat template kalender proyek yang mendefinisikan jumlah jam kerja setiap hari dan penutupan bisnis apapun. Untuk membuat template kalender proyek, Anda mengaitkan template kerja dengan bidang **template kalender** untuk proyek. Ikuti langkah berikut untuk membuat template kerja.

1. Dalam PSA, di panel navigasi kiri, klik **sumber daya**. 
2. Di halaman daftar **sumber daya**, buka rekaman pengguna, lalu pilih **Tampilkan Jam Kerja**.

  > [!NOTE]
  > Pastikan Anda mengizinkan pop-up di halaman browser. Dengan demikian, Anda dapat melihat jam kerja yang ditetapkan untuk sumber daya.
  
3. Pada tab **tampilan bulanan**, klik **Atur**. Daftar tiga pilihan muncul: 

  - Jadwal Mingguan Baru
  - Jadwal Kerja untuk Satu Hari
  - Waktu Nonaktif

> ![Pilihan konfigurasi](media/project-13.png)

4. Pilih **jadwal mingguan baru**, lalu Atur pilihan untuk jadwal sumber daya ini. Anda dapat mengatur jadwal mingguan yang berulang, parameter jam harian, penutupan bisnis, dan banyak lagi.
5. Atur rentang tanggal, pilih **Simpan**, lalu klik **tutup**. 
6. Kembali ke halaman daftar **sumber daya**, dan pilih sumber daya yang Anda tetapkan jam kerja. 
7. Pilih **Atur kalender sebagai** untuk mengatur template kerja. 
8. Di kotak dialog **template kerja**, masukkan nama untuk template kerja, lalu pilih **Terapkan**. 

Sekarang Anda dapat mengaitkan template kerja dengan template kalender proyek.

## <a name="resource-roles"></a>Peran Sumber Daya

Istilah *peran sumber daya* merujuk pada seperangkat keterampilan, kompetensi, dan sertifikasi yang harus dimiliki oleh seseorang untuk melakukan serangkaian tugas tertentu pada suatu proyek. PSA memungkinkan Anda mata uang biaya dan tagihan waktu sumber daya berdasarkan peran yang terkait dengan sumber daya. Setiap organisasi harus mengkonfigurasi peran ini dengan menggunakan navigasi kiri pada menu **Project Service**.

Setiap organisasi harus mengkonfigurasi peran ini di halaman **kategori sumber daya aktif**. Untuk membuka Halaman ini, di panel navigasi kiri, pilih **peran sumber daya**.

## <a name="price-lists"></a>Daftar Harga

Daftar harga memungkinkan Anda menetapkan biaya dan harga penjualan untuk peran sumber, kategori pengeluaran, produk, dan elemen lain dalam organisasi. Sebelum Anda membuat perkiraan keuangan untuk pekerjaan yang harus dilaksanakan untuk proyek, Anda harus membuat daftar harga biaya dan penjualan cadangan. Di bagian parameter, Anda juga harus mengkonfigurasi daftar harga dan harga penjualan default yang berlaku untuk semua proyek yang dibuat di organisasi. Pada halaman **parameter proyek aktif**, pastikan Anda mengkonfigurasi daftar biaya dan harga penjualan default.
