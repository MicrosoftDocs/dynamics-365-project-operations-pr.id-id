---
title: Opsi subkontrak untuk anggota tim proyek
description: Artikel ini menjelaskan opsi subkontrak untuk anggota tim proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261610"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opsi subkontrak untuk anggota tim proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Microsoft Dynamics 365 Project Operations, Anda dapat mengevaluasi opsi subkontrak yang tersedia untuk satu atau beberapa anggota tim proyek. Opsi subkontrak yang tersedia memungkinkan Anda untuk:

- Buat subkontrak baru dan/atau buat baris baru pada subkontrak yang sudah ada untuk anggota tim proyek yang dipilih. 
- Cadangan terhadap garis subkontrak dan subkontrak yang sudah ada. 

Anda dapat memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek generik atau memilih dari anggota tim proyek yang telah dikelola dengan sumber daya bernama yang merupakan pekerja kontrak. 

Tidak ada opsi subkontrak yang tersedia untuk hal-hal berikut:

- Anggota tim proyek yang telah dikelola oleh seorang karyawan. 
- Anggota tim proyek yang sudah terkait dengan garis subkontrak dan subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang tidak berpesta

Untuk meninjau dan memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek generik atau tidak terseok-seok, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa rekaman anggota tim proyek di mana sumber daya adalah sumber daya generik.
2. Pastikan tidak ada catatan anggota tim proyek yang dipilih yang sudah disubkontrakkan. 
3. Pilih **Opsi** subkontrak pada sub-kisi anggota tim proyek. Dialog **Opsi** subkontrak terbuka. 
4. Jika Anda hanya memilih satu rekaman anggota tim proyek di langkah 1, maka opsi berikut akan tersedia:
    - Buat baris subkontrak baru. 
    - Cadangan terhadap subkontrak yang ada Jika Anda memilih beberapa rekaman anggota tim proyek di langkah 1, maka satu-satunya opsi yang tersedia adalah membuat baris subkontrak baru.
5. Opsi untuk memesan terhadap garis subkontrak yang ada memungkinkan Anda untuk memilih garis subkontrak dan subkontrak yang ingin Anda pesan. Saat memilih jalur subkontrak untuk mencadangkan kapasitas, Anda harus memastikan bahwa jalur subkontrak yang dipilih adalah untuk waktu dan bahwa peran yang diperlukan pada anggota tim proyek cocok dengan peran yang dibeli pada baris subkontrak.
6. Saat Anda memilih untuk membuat baris subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda untuk memilih subkontrak yang ingin Anda buat baris ini. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam **status Draf**. Dengan opsi ini untuk membuat jalur subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu baris subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap baris subkontrak yang dibuat. 
7. Ketika anggota tim generik dikaitkan dengan baris subkontrak dan subkontrak, bidang Jenis **pekerja pada baris anggota tim generik akan diperbarui menjadi** Pekerja **Kontrak dan** nilai Validitas Subkontrak akan diatur ke **Validitas** **.**

## <a name="subcontracting-a-staffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang dikelola staf

Seperti anggota tim generik atau tidak berpesan, Anda juga dapat melihat opsi subkontrak untuk anggota tim proyek yang dikelola selama anggota tim yang dikelola adalah pekerja kontrak. Untuk meninjau dan memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek yang memiliki staf atau bernama, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa catatan anggota tim proyek di mana sumber dayanya adalah pekerja kontrak bernama.
2. Pastikan tidak ada catatan anggota tim proyek yang dipilih yang sudah disubkontrakkan. 
3. Pilih **Opsi** subkontrak pada sub-kisi anggota tim proyek. Dialog **Opsi** subkontrak terbuka. 
4. Jika Anda hanya memilih satu rekaman anggota tim proyek di langkah 1, maka opsi berikut akan tersedia:
      - Buat baris subkontrak baru.
      - Cadangan terhadap subkontrak yang ada.
  Jika Anda memilih beberapa rekaman anggota tim proyek di langkah 1, maka satu-satunya opsi yang tersedia adalah membuat baris subkontrak baru.
5. Opsi untuk memesan terhadap garis subkontrak yang ada memungkinkan Anda untuk memilih garis subkontrak dan subkontrak yang ingin Anda pesan. Saat memilih jalur subkontrak untuk mencadangkan kapasitas, Anda harus memastikan hal berikut:
      - Garis subkontrak yang dipilih adalah untuk waktu. 
      - Peran yang diperlukan pada anggota tim proyek cocok dengan peran yang dibeli di jalur subkontrak. 
      - Vendor yang terkait dengan pekerja kontrak sama dengan vendor pada subkontrak.
6. Saat Anda memilih untuk membuat baris subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda untuk memilih subkontrak yang ingin Anda buat baris ini. Dengan opsi ini, Anda harus memastikan bahwa vendor tempat pekerja kontrak berada sama dengan vendor pada subkontrak. 
7. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam **status Draf**. Dengan opsi ini untuk membuat jalur subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu baris subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap baris subkontrak yang dibuat.  
8. Ketika anggota tim yang bernama dikaitkan dengan baris subkontrak dan subkontrak, bidang Jenis **pekerja pada baris anggota tim bernama akan diperbarui menjadi** Pekerja **Kontrak dan** nilai Validitas Subkontrak akan diatur ke **Validitas** **.**

## <a name="re-costing-subcontractor-assignments"></a>Penetapan biaya ulang subkontraktor

Ketika anggota tim proyek (generik atau bernama) ditautkan **ke baris subkontrak menggunakan dialog Opsi** subkontrak, setiap penugasan ke tugas yang dimiliki anggota tim akan dikenakan biaya ulang berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. Pada tab Perkiraan di halaman Detail **Proyek, pilih tombol** Perbarui harga untuk melihat harga yang diperbarui dan/atau biaya yang dihasilkan dari keputusan untuk mensubkontrakkan **.** **·**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
