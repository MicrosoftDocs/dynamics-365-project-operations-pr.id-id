---
title: Anggota tim proyek subkontrak
description: Ini topik menjelaskan cara mensubkontrakkan anggota tim proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903040"
---
# <a name="subcontracting-project-team-members"></a>Anggota tim proyek subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Dynamics 365 Project Operations Microsoft, Anda dapat memilih untuk mensubkontrakkan anggota tim proyek yang tidak tertekuk atau dikelola.

- Anggota tim proyek yang tidak terganggu memiliki sumber daya generik yang ditugaskan.
- Anggota tim yang dikelola memiliki sumber daya bernama yang ditugaskan.

Ketika Anda menghubungkan anggota tim proyek ke baris subkontrak, tugas apa pun dengan tugas yang dimiliki anggota tim akan dikenakan biaya ulang berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak.  Pada **tab Perkiraan** pada halaman Detail **Proyek**, pilih tombol **Perbarui harga untuk melihat harga yang** diperbarui dan/atau biaya yang dihasilkan dari keputusan untuk subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang tidak terganggu
**Halaman detail Anggota Tim memiliki bidang baris** subkontrak dan subkontrak yang memungkinkan manajer proyek untuk mengungkapkan bagaimana mereka ingin menarik kapasitas yang diperlukan dari subkontrak. Untuk mensubkontrakkan anggota tim proyek sebagai sumber daya generik, ikuti langkah-langkah berikut:

1.  Pilih subkontrak pada **halaman detail anggota** Tim.

2.  Anda hanya dapat memilih subkontrak dengan **Status Draf** atau **Dikonfirmasi**. **Subkontrak** tertutup atau Dibatalkan tidak dapat **dipilih**. 

3.  Bidang **garis Subkontrak** menjadi terlihat setelah Anda memilih subkontrak.

4.  Di **bidang baris Subkontrak,** Anda hanya dapat memilih baris subkontrak yang untuk waktu. Anda tidak dapat memilih baris subkontrak untuk biaya atau materi.

5.  Peran untuk catatan anggota tim proyek perlu mencocokkan peran pada garis subkontrak. Ini memastikan bahwa waktu untuk peran yang sedang diperkirakan pada proyek adalah peran yang sama yang dibeli pada baris subkontrak. 

Ketika anggota tim generik dikaitkan dengan baris subkontrak dan subkontrak, **bidang tipe Pekerja pada baris anggota tim generik akan diperbarui ke Pekerja Kontrak dan Validitas** **·** **Subkontrak** akan diatur ke **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang dikelola
Seperti anggota tim generik atau tidak terganggu, kapasitas anggota tim staf yang diperlukan pada suatu proyek juga dapat dihubungkan ke subkontrak. Untuk mensubkontrakkan anggota tim proyek bernama, ikuti langkah-langkah berikut:

1.  Pastikan bahwa sumber daya bernama diatur sebagai jenis pekerja kontrak sumber daya yang dapat dipesan. Juga, pastikan bahwa **bidang Vendor pada sumber daya yang dapat dipesan cocok dengan vendor pada** subkontrak yang Anda pilih. 

2.  Anda hanya dapat memilih subkontrak dalam **Status Draf** atau **Terkonfirmasi.** **Subkontrak** tertutup atau Dibatalkan tidak dapat **dipilih**. 

3.  Bidang **garis Subkontrak** menjadi terlihat setelah Anda memilih subkontrak.

4.  Di **bidang baris Subkontrak,** Anda hanya dapat memilih baris subkontrak yang untuk waktu. Anda tidak dapat memilih baris subkontrak untuk biaya atau materi.

5.  Peran untuk catatan anggota tim proyek perlu mencocokkan peran pada garis subkontrak. Ini memastikan bahwa waktu untuk peran yang sedang diperkirakan pada proyek adalah peran yang sama yang dibeli pada baris subkontrak. 

Anggota tim proyek bernama yang ditetapkan sebagai jenis pekerja kontrak **sumber daya yang dapat dipesan akan ditampilkan dengan status validitas** subkontrak **tidak valid jika mereka tidak terkait dengan** subkontrak. Ketika anggota tim proyek bernama dikaitkan dengan baris subkontrak dan subkontrak, **bidang tipe Pekerja di baris anggota tim akan memperbarui ke Pekerja Kontrak dan Validitas** **·** **Subkontrak** akan diatur ke **Valid**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
