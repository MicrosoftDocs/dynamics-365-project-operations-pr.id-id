---
title: Opsi subkontrak untuk anggota tim proyek
description: Ini topik menjelaskan opsi subkontrak untuk anggota tim proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aacd2f97d3120a854c78fe87e512fad1c43b9651
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600194"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opsi subkontrak untuk anggota tim proyek

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Microsoft Dynamics 365 Project Operations, Anda dapat mengevaluasi opsi subkontrak yang tersedia untuk satu atau beberapa anggota tim proyek. Opsi subkontrak yang tersedia memungkinkan Anda untuk:

- Buat subkontrak baru dan/atau buat jalur baru pada subkontrak yang ada untuk anggota tim proyek yang dipilih. 
- Cadangan terhadap subkontrak dan subkontrak yang sudah ada. 

Anda dapat memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek generik atau memilih dari anggota tim proyek yang telah dikelola dengan sumber daya bernama yang merupakan pekerja kontrak. 

Tidak ada opsi subkontrak yang tersedia untuk hal-hal berikut:

- Anggota tim proyek yang telah dikelola dengan seorang karyawan. 
- Anggota tim proyek yang sudah terkait dengan subkontrak dan subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang tidak terafiliasi

Untuk meninjau dan memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek generik atau tanpa staf, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa catatan anggota tim proyek di mana sumber daya adalah sumber daya generik.
2. Pastikan tidak ada catatan anggota tim proyek yang dipilih yang sudah disubkontrakkan. 
3. Pilih **Opsi** subkontrak pada sub kisi anggota tim proyek. Dialog **Opsi** subkontrak terbuka. 
4. Jika Anda hanya memilih satu catatan anggota tim proyek di langkah 1, maka opsi berikut akan tersedia:
    - Buat jalur subkontrak baru. 
    - Cadangan terhadap subkontrak yang ada Jika Anda memilih beberapa catatan anggota tim proyek di langkah 1, maka satu-satunya pilihan yang tersedia adalah membuat jalur subkontrak baru.
5. Opsi untuk mencadangkan terhadap jalur subkontrak yang ada memungkinkan Anda untuk memilih subkontrak dan subkontrak yang ingin Anda pesan. Saat memilih jalur subkontrak untuk kapasitas cadangan, Anda harus memastikan bahwa jalur subkontrak yang dipilih adalah untuk waktu dan bahwa peran yang diperlukan pada anggota tim proyek sesuai dengan peran yang dibeli pada jalur subkontrak.
6. Ketika Anda memilih untuk membuat jalur subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda untuk memilih subkontrak yang ingin Anda buat baris ini. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam **status Draf**. Dengan opsi ini untuk membuat jalur subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu jalur subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap jalur subkontrak yang dibuat. 
7. Ketika anggota tim generik dikaitkan dengan subkontrak dan subkontrak, **bidang tipe** Pekerja pada baris anggota tim generik akan diperbarui ke **Pekerja** Kontrak dan **nilai Validitas** Subkontrak akan diatur ke **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek staf

Seperti anggota tim generik atau tanpa staf, Anda juga dapat melihat opsi subkontrak untuk anggota tim proyek staf selama anggota tim yang dikelola adalah pekerja kontrak. Untuk meninjau dan memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek yang dikelola atau bernama, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa catatan anggota tim proyek di mana sumber daya adalah pekerja kontrak bernama.
2. Pastikan bahwa tidak ada catatan anggota tim proyek yang dipilih yang sudah disubkontrakkan. 
3. Pilih **Opsi** subkontrak pada sub kisi anggota tim proyek. Dialog **Opsi** subkontrak terbuka. 
4. Jika Anda hanya memilih satu catatan anggota tim proyek di langkah 1, maka opsi berikut akan tersedia:
      - Buat jalur subkontrak baru.
      - Cadangan terhadap subkontrak yang ada.
  Jika Anda memilih beberapa catatan anggota tim proyek di langkah 1, maka satu-satunya opsi yang tersedia adalah membuat jalur subkontrak baru.
5. Opsi untuk mencadangkan terhadap jalur subkontrak yang ada memungkinkan Anda untuk memilih subkontrak dan subkontrak yang ingin Anda pesan. Saat memilih jalur subkontrak untuk cadangan kapasitas, Anda harus memastikan hal-hal berikut:
      - Jalur subkontrak yang dipilih adalah untuk waktu. 
      - Peran yang diperlukan pada anggota tim proyek sesuai dengan peran yang dibeli pada jalur subkontrak. 
      - Vendor yang terkait dengan pekerja kontrak sama dengan vendor pada subkontrak.
6. Ketika Anda memilih untuk membuat jalur subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda untuk memilih subkontrak yang ingin Anda buat baris ini. Dengan opsi ini, Anda harus memastikan bahwa vendor tempat pekerja kontrak berada sama dengan vendor pada subkontrak. 
7. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam **status Draf**. Dengan opsi ini untuk membuat jalur subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu jalur subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap jalur subkontrak yang dibuat.  
8. Ketika anggota tim yang disebutkan terkait dengan subkontrak dan subkontrak, **bidang tipe** Pekerja pada baris anggota tim yang disebutkan akan diperbarui menjadi **Pekerja** Kontrak dan **nilai Validitas** Subkontrak akan diatur ke **Valid**.

## <a name="re-costing-subcontractor-assignments"></a>Re-costing tugas subkontraktor

Ketika anggota tim proyek (generik atau bernama) ditautkan ke jalur subkontrak menggunakan **dialog Opsi** subkontrak, setiap tugas untuk tugas yang dimiliki anggota tim akan dikenakan biaya ulang berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. **Pada tab Perkiraan** pada **halaman Detail** Proyek, pilih **tombol Perbarui harga untuk melihat harga dan/atau biaya yang diperbarui akibat keputusan untuk mensubkontrakkan**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
