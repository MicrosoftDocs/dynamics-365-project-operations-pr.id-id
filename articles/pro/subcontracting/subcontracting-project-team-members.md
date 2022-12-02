---
title: Mensubkontrakkan anggota tim proyek
description: Artikel ini menjelaskan cara membuat subkontrak untuk anggota tim proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522799"
---
# <a name="subcontracting-project-team-members"></a>Mensubkontrakkan anggota tim proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dalam Microsoft Dynamics 365 Project Operations, Anda dapat memilih untuk membuat subkontrak anggota tim proyek yang belum dan sudah dikelola.

- Anggota tim proyek yang belum dikelola memiliki sumber daya generik yang ditetapkan.
- Anggota tim yang dikelola memiliki sumber daya bernama yang ditetapkan.

Bila Anda menautkan anggota tim proyek ke baris subkontrak, penugasan ke tugas yang anggota tim akan ditentukan ulang biayanya berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak.  Pada **Estimasi** di halaman **Rincian Proyek**, pilih tombol **Perbarui harga** untuk melihat harga yang diperbarui dan/atau biaya yang dihasilkan dari keputusan untuk mengurangi kontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Membuat subkontrak anggota tim proyek yang belum dikelola
Halaman **rincian Anggota Tim** memiliki bidang subkontrak dan baris subkontrak yang memungkinkan manajer proyek menunjukkan cara mereka ingin menarik kapasitas sing diperlukan dari subkontrak. Untuk membuat subkontrak anggota tim proyek sebagai sumber daya generik, ikuti langkah-langkah berikut:

1.  Pilih subkontrak pada halaman **Rincin anggota tim**.

2.  Anda hanya dapat memilih subkontrak dengan **Draf** atau status **Terkonfirmasi**. Subkontrak **Ditutup** atau **Dibatalkan** tidak dapat dipilih. 

3.  Bidang **Baris subkontrak** menjadi terlihat setelah Anda memilih subkontrak.

4.  Di bidang **Baris subkontrak**, Anda hanya dapat memilih baris subkontrak yang sudah waktunya. Anda tidak dapat memilih baris subkontrak untuk pengeluaran atau materi.

5.  Peran untuk rekaman anggota tim proyek harus sesuai dengan peran pada baris subkontrak. Langkah ini memastikan bahwa waktu untuk peran yang sedang diperkirakan pada proyek adalah peran yang sama yang dibeli pada baris subkontrak. 

Bila anggota tim generik dikaitkan dengan subkontrak dan baris subkontrak, bidang **Jenis pekerja** pada baris anggota tim generik akan diperbarui ke **Pekerja Kontrak** dan nilai **Validitas Subkontrak** akan diatur ke **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Membuat subkontrak anggota tim proyek sudah dikelola
Seperti anggota tim generik atau yang belum dikelola, kapasitas anggota tim yang dikelola diperlukan pada proyek juga dapat ditautkan ke subkontrak. Untuk membuat subkontrak anggota tim proyek bernama, ikuti langkah-langkah berikut:

1.  Pastikan bahwa sumber daya bernama disiapkan sebagai jenis pekerja kontrak sumber daya yang dapat dipesan. Selain itu, pastikan bahwa bidang **Vendor** pada sumber daya yang dapat dipesan cocok dengan vendor pada subkontrak yang Anda pilih. 

2.  Anda hanya dapat memilih subkontrak di dalam **Draf** atau status **Terkonfirmasi**. Subkontrak **Ditutup** atau **Dibatalkan** tidak dapat dipilih. 

3.  Bidang **Baris subkontrak** menjadi terlihat setelah Anda memilih subkontrak.

4.  Di bidang **Baris subkontrak**, Anda hanya dapat memilih baris subkontrak yang sudah waktunya. Anda tidak dapat memilih baris subkontrak untuk pengeluaran atau materi.

5.  Peran untuk rekaman anggota tim proyek harus sesuai dengan peran pada baris subkontrak. Langkah ini memastikan bahwa waktu untuk peran yang sedang diperkirakan pada proyek adalah peran yang sama yang dibeli pada baris subkontrak. 

Anggota tim proyek bernama sing disiapkan sebagai jenis pekerja kontrak **Sumber daya yang bisa dipesan** akan ditampilkan dengan status validitas **Tidak valid** jika tidak ditautkan dengan subkontrak. Saat anggota tim proyek bernama dikaitkan dengan subkontrak dan baris subkontrak, bidang **Jenis pekerja** dalam baris anggota tim generik akan diperbarui ke **Pekerja Kontrak** dan nilai **Validitas Subkontrak** akan diatur ke **Valid**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
