---
title: Mensubkontrakkan anggota tim proyek
description: Ini topik menjelaskan cara mensubkontrakkan anggota tim proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587850"
---
# <a name="subcontracting-project-team-members"></a>Mensubkontrakkan anggota tim proyek

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Microsoft Dynamics 365 Project Operations, Anda dapat memilih untuk mensubkontrakkan anggota tim proyek yang tidak memiliki staf atau staf.

- Anggota tim proyek yang tidak memiliki staf memiliki sumber daya generik yang ditetapkan.
- Anggota tim staf memiliki sumber daya bernama yang ditugaskan.

Saat Anda menautkan anggota tim proyek ke saluran subkontrak, tugas apa pun untuk tugas yang dimiliki anggota tim akan direkosongkan berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak.  **Pada tab Perkiraan** pada **halaman Detail** Proyek, pilih **tombol Perbarui harga untuk melihat harga dan/atau biaya yang diperbarui akibat keputusan untuk mensubkontrakkan**. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang tidak terafiliasi
Halaman **detail** Anggota Tim memiliki bidang subkontrak dan subkontrak yang memungkinkan manajer proyek untuk mengungkapkan bagaimana mereka ingin menarik kapasitas yang diperlukan dari subkontrak. Untuk mensubkontrakkan anggota tim proyek sebagai sumber daya generik, ikuti langkah-langkah berikut:

1.  Pilih subkontrak di **halaman Detail** anggota tim.

2.  Anda hanya dapat memilih subkontrak dengan **status Draft** atau **Confirmed**. **Subkontrak tertutup** **atau** dibatalkan tidak dapat dipilih. 

3.  Bidang **garis** Subkontrak menjadi terlihat setelah Anda memilih subkontrak.

4.  **Di bidang subkontrak**, Anda hanya dapat memilih jalur subkontrak yang sesuai waktu. Anda tidak dapat memilih jalur subkontrak untuk biaya atau material.

5.  Peran untuk catatan anggota tim proyek harus sesuai dengan peran pada jalur subkontrak. Ini memastikan bahwa waktu untuk peran yang diperkirakan pada proyek adalah peran yang sama yang dibeli pada jalur subkontrak. 

Ketika anggota tim generik dikaitkan dengan jalur subkontrak dan subkontrak, **bidang tipe** Pekerja pada baris anggota tim generik akan diperbarui ke **Pekerja** Kontrak dan **Validitas** Subkontrak akan diatur ke **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek staf
Seperti anggota tim generik atau tanpa staf, kapasitas anggota tim staf yang diperlukan pada proyek juga dapat dikaitkan dengan subkontrak. Untuk mensubkontrakkan anggota tim proyek bernama, ikuti langkah-langkah berikut:

1.  Pastikan bahwa sumber daya bernama disiapkan sebagai jenis sumber daya yang dapat dipesan oleh pekerja kontrak. Juga, pastikan bahwa **bidang Vendor** pada sumber daya yang dapat dipesan cocok dengan vendor pada subkontrak yang Anda pilih. 

2.  Anda hanya dapat memilih subkontrak dalam **status Draf** atau **Dikonfirmasi**. **Subkontrak tertutup** **atau** dibatalkan tidak dapat dipilih. 

3.  Bidang **garis** Subkontrak menjadi terlihat setelah Anda memilih subkontrak.

4.  **Di bidang subkontrak**, Anda hanya dapat memilih jalur subkontrak yang sesuai waktu. Anda tidak dapat memilih jalur subkontrak untuk biaya atau material.

5.  Peran untuk catatan anggota tim proyek harus sesuai dengan peran pada jalur subkontrak. Ini memastikan bahwa waktu untuk peran yang diperkirakan pada proyek adalah peran yang sama yang dibeli pada jalur subkontrak. 

Anggota tim proyek bernama yang ditetapkan sebagai jenis pekerja kontrak sumber **daya** yang dapat dipesan akan ditampilkan dengan status **validitas subkontrak tidak valid** jika mereka tidak terkait dengan subkontrak. Ketika anggota tim proyek bernama dikaitkan dengan jalur subkontrak dan subkontrak, **bidang tipe** Pekerja di baris anggota tim akan diperbarui menjadi **Pekerja** Kontrak dan **Validitas** Subkontrak akan diatur ke **Valid**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
