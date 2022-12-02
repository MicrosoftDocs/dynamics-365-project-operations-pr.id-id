---
title: Opsi subkontrak untuk anggota tim proyek
description: Artikel ini menjelaskan opsi subkontrak untuk anggota tim proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522282"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opsi subkontrak untuk anggota tim proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Di Microsoft Dynamics 365 Project Operations, Anda dapat mengevaluasi pilihan subkontrak yang tersedia untuk satu atau lebih banyak anggota tim proyek. Opsi subkontrak yang tersedia memungkinkan Anda untuk:

- Membuat subkontrak baru dan/atau membuat baris baru pada subkontrak yang ada untuk anggota tim proyek yang dipilih. 
- Cadangan terhadap subkontrak dan baris subkontrak yang sudah ada. 

Anda dapat memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek generik atau memilih dari anggota tim proyek yang telah dikelola dengan sumber daya bernama yang merupakan pekerja kontrak. 

Tidak ada opsi subkontrak yang tersedia untuk hal berikut:

- Anggota tim proyek yang telah dikelola dengan karyawan. 
- Anggota tim proyek yang sudah dikaitkan dengan subkontrak dan baris subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Membuat subkontrak anggota tim proyek yang belum dikelola

Untuk memeriksa dan memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek generik atau tidak memiliki staf, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa rekaman anggota tim proyek dengan sumber dayanya adalah sumber daya generik.
2. Pastikan tidak ada satu pun dari rekaman anggota tim proyek yang dipilih yang sudah dilakukan subkontrak. 
3. Pilih **Opsi subkontrak pada** subkisi anggota tim proyek. Dialog **Opsi Subkontrak** terbuka. 
4. Jika Anda hanya memilih satu rekaman anggota tim proyek pada langkah 1, maka opsi berikut akan tersedia:
    - Buat baris subkontrak baru. 
    - Cadangan dengan subkontrak yang ada Jika Anda memilih beberapa rekaman anggota tim proyek pada langkah 1, maka satu-satunya opsi yang tersedia adalah membuat baris subkontrak baru.
5. Pilihan untuk mencadangkan dengan baris subkontrak yang ada memungkinkan Anda memilih subkontrak dan baris subkontrak yang akan disimpan. Saat memilih baris subkontrak untuk cadangan kapasitas, Anda harus memastikan bahwa baris subkontrak yang dipilih tepat waktu dan peran yang diperlukan pada anggota tim proyek sesuai dengan peran yang dibeli pada baris subkontrak.
6. Bila Anda memilih untuk membuat baris subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda memilih subkontrak yang ingin Anda buatkan baris ini. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam status **Draf**. Dengan pilihan ini untuk membuat baris subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu baris subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap baris subkontrak yang dibuat. 
7. Bila anggota tim generik dikaitkan dengan subkontrak dan baris subkontrak, bidang **Jenis pekerja** pada baris anggota tim generik akan diperbarui ke **Pekerja Kontrak** dan nilai **Validitas Subkontrak** akan diatur ke **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Membuat subkontrak anggota tim proyek sudah dikelola

Seperti anggota tim generik atau anggota tim yang belum dikelola, Anda juga dapat melihat pilihan subkontrak untuk anggota tim proyek yang dikelola selama anggota tim yang dikelola adalah pekerja kontrak. Untuk meninjau dan memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek yang dikelola dan bernama, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa rekaman anggota tim proyek dengan sumber dayanya adalah pekerja kontrak bernama.
2. Pastikan tidak ada satu pun dari rekaman anggota tim proyek yang dipilih sudah dilakukan subkontrak. 
3. Pilih **Opsi subkontrak pada** subkisi anggota tim proyek. Dialog **Opsi Subkontrak** terbuka. 
4. Jika Anda hanya memilih satu rekaman anggota tim proyek pada langkah 1, maka opsi berikut akan tersedia:
      - Buat baris subkontrak baru.
      - Mencadangkan subkontrak yang ada.
  Jika Anda memilih beberapa rekaman anggota tim pada langkah 1, maka opsi yang tersedia hanya untuk membuat baris subkontrak baru.
5. Pilihan untuk mencadangkan dengan baris subkontrak yang ada memungkinkan Anda memilih subkontrak dan baris subkontrak yang akan disimpan. Saat memilih baris subkontrak untuk cadangan kapasitas, Anda harus memastikan hal berikut:
      - Baris subkontrak yang dipilih untuk waktu. 
      - Peran yang diperlukan pada anggota tim proyek sesuai peran yang dibeli pada baris subkontrak. 
      - Vendor yang terkait dengan pekerja kontrak sama dengan vendor pada subkontrak.
6. Bila Anda memilih untuk membuat baris subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda memilih subkontrak yang ingin Anda buatkan baris ini. Dengan opsi ini, Anda harus memastikan bahwa vendor tempat pekerja kontrak sama dengan vendor di subkontrak. 
7. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam status **Draf**. Dengan pilihan ini untuk membuat baris subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu baris subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap baris subkontrak yang dibuat.  
8. Bila anggota tim bernama dikaitkan dengan subkontrak dan baris subkontrak, bidang **Jenis pekerja** pada baris anggota tim bernama akan diperbarui ke **Pekerja Kontrak** dan nilai **Validitas Subkontrak** akan diatur ke **Valid**.

## <a name="re-costing-subcontractor-assignments"></a>Menentukan ulang biaya penugasan subkontraktor

Bila anggota tim proyek (generik atau bernama) ditautkan ke baris subkontrak menggunakan dialog **Opsi Subkontrak**, setiap penugasan untuk tugas yang dikenakan biaya ulang anggota tim berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. Pada **Estimasi** di halaman **Rincian Proyek**, pilih tombol **Perbarui harga** untuk melihat harga yang diperbarui dan/atau biaya yang dihasilkan dari keputusan untuk mengurangi kontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
