---
title: Mensubkontrakkan anggota tim proyek
description: Artikel ini menjelaskan cara mensubkontrakkan anggota tim proyek di Microsoft Dynamics 365 Project Operations.
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

Di Microsoft Dynamics 365 Project Operations, Anda dapat memilih untuk mensubkontrakkan anggota tim proyek yang tidak terikat atau memiliki staf.

- Anggota tim proyek yang tidak terikat memiliki sumber daya generik yang ditetapkan.
- Anggota tim yang dikelola memiliki sumber daya bernama yang ditugaskan.

Saat Anda menautkan anggota tim proyek ke baris subkontrak, setiap penugasan ke tugas yang dimiliki anggota tim akan direkapitulasi berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak.  Pada tab Perkiraan di halaman Detail **Proyek, pilih tombol** Perbarui harga untuk melihat harga yang diperbarui dan/atau biaya yang dihasilkan dari keputusan untuk mensubkontrakkan **.** **·** 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang tidak berpesta
Halaman **detail** Anggota Tim memiliki bidang baris subkontrak dan subkontrak yang memungkinkan manajer proyek untuk mengungkapkan bagaimana mereka ingin menarik kapasitas yang diperlukan dari subkontrak. Untuk mensubkontrakkan anggota tim proyek sebagai sumber daya generik, ikuti langkah-langkah berikut:

1.  Pilih subkontrak di **halaman Detail** anggota tim.

2.  Anda hanya dapat memilih subkontrak dengan **status Draf** atau **Dikonfirmasi**. **Subkontrak** tertutup atau **Dibatalkan** tidak dapat dipilih. 

3.  Bidang **garis** Subkontrak menjadi terlihat setelah Anda memilih subkontrak.

4.  **Di bidang garis** Subkontrak, Anda hanya dapat memilih baris subkontrak yang tepat waktu. Anda tidak dapat memilih jalur subkontrak untuk pengeluaran atau materi.

5.  Peran untuk catatan anggota tim proyek harus sesuai dengan peran pada garis subkontrak. Ini memastikan bahwa waktu untuk peran yang sedang diperkirakan pada proyek adalah peran yang sama yang dibeli di jalur subkontrak. 

Ketika anggota tim generik dikaitkan dengan garis subkontrak dan subkontrak, bidang jenis **Pekerja pada baris anggota tim generik akan diperbarui menjadi** Pekerja **Kontrak dan** Validitas Subkontrak akan diatur ke **Validitas** **.**

## <a name="subcontracting-a-staffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang dikelola staf
Seperti anggota tim generik atau tidak berpesan, kapasitas anggota tim yang dikelola yang diperlukan pada suatu proyek juga dapat dikaitkan dengan subkontrak. Untuk mensubkontrakkan anggota tim proyek bernama, ikuti langkah-langkah berikut:

1.  Pastikan bahwa sumber daya bernama diatur sebagai jenis sumber daya yang dapat dipesan oleh pekerja kontrak. Selain itu, pastikan bahwa **bidang Vendor** pada sumber daya yang dapat dipesan cocok dengan vendor pada subkontrak yang Anda pilih. 

2.  Anda hanya dapat memilih subkontrak dalam **status Draf** atau **Terkonfirmasi**. **Subkontrak** tertutup atau **Dibatalkan** tidak dapat dipilih. 

3.  Bidang **garis** Subkontrak menjadi terlihat setelah Anda memilih subkontrak.

4.  **Di bidang garis** Subkontrak, Anda hanya dapat memilih baris subkontrak yang tepat waktu. Anda tidak dapat memilih jalur subkontrak untuk pengeluaran atau materi.

5.  Peran untuk catatan anggota tim proyek harus sesuai dengan peran pada garis subkontrak. Ini memastikan bahwa waktu untuk peran yang sedang diperkirakan pada proyek adalah peran yang sama yang dibeli di jalur subkontrak. 

Anggota tim proyek bernama yang ditetapkan sebagai jenis sumber daya **yang dapat dipesan oleh** pekerja kontrak akan ditampilkan dengan status **validitas subkontrak Tidak valid** jika mereka tidak ditautkan dengan subkontrak. Ketika anggota tim proyek yang bernama dikaitkan dengan baris subkontrak dan subkontrak, **bidang Jenis** pekerja di baris anggota tim akan diperbarui menjadi **Pekerja** Kontrak dan **Validitas** Subkontrak akan diatur ke **Valid**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
