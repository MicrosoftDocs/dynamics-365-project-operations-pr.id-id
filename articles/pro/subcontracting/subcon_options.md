---
title: Opsi subkontrak untuk anggota tim proyek
description: Ini topik menjelaskan opsi subkontrak untuk anggota tim proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903041"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opsi subkontrak untuk anggota tim proyek

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Dynamics 365 Project Operations Microsoft, Anda dapat mengevaluasi opsi subkontrak yang tersedia untuk satu atau beberapa anggota tim proyek. Opsi subkontrak yang tersedia memungkinkan Anda untuk:

- Buat subkontrak baru dan/atau buat baris baru pada subkontrak yang ada untuk anggota tim proyek yang dipilih. 
- Cadangan terhadap garis subkontrak dan subkontrak yang sudah ada. 

Anda dapat memilih dari opsi subkontrak yang tersedia untuk anggota tim proyek generik atau memilih dari anggota tim proyek yang telah dikelola dengan sumber daya bernama yang merupakan pekerja kontrak. 

Tidak ada opsi subkontrak yang tersedia untuk hal-hal berikut:

- Anggota tim proyek yang telah dikelola dengan seorang karyawan. 
- Anggota tim proyek yang sudah terkait dengan garis subkontrak dan subkontrak. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang tidak terganggu

Untuk meninjau dan memilih opsi subkontrak yang tersedia untuk anggota tim proyek generik atau tidak terganggu, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa catatan anggota tim proyek di mana sumber daya adalah sumber daya generik.
2. Pastikan bahwa tidak ada catatan anggota tim proyek yang dipilih yang sudah disubkontrakkan. 
3. Pilih **Opsi Subkontrak** pada sub grid anggota tim proyek. **Dialog opsi Subkontrak** terbuka. 
4. Jika Anda hanya memilih satu catatan anggota tim proyek di langkah 1, maka opsi berikut akan tersedia:
    - Buat baris subkontrak baru. 
    - Cadangan terhadap subkontrak yang ada Jika Anda memilih beberapa catatan anggota tim proyek di langkah 1, maka satu-satunya opsi yang tersedia adalah membuat baris subkontrak baru.
5. Opsi untuk memesan terhadap garis subkontrak yang ada memungkinkan Anda memilih garis subkontrak dan subkontrak yang ingin Anda pesan. Saat memilih garis subkontrak untuk kapasitas cadangan, Anda harus memastikan bahwa baris subkontrak yang dipilih adalah untuk waktu dan bahwa peran yang diperlukan pada anggota tim proyek sesuai dengan peran yang dibeli pada baris subkontrak.
6. Ketika Anda memilih untuk membuat baris subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda untuk memilih subkontrak yang ingin Anda buat baris-baris ini. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam **status** Draf. Dengan opsi ini untuk membuat baris subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu baris subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap baris subkontrak yang dibuat. 
7. Ketika anggota tim generik dikaitkan dengan baris subkontrak dan subkontrak, **bidang tipe Pekerja pada baris anggota tim generik akan diperbarui menjadi Pekerja Kontrak dan nilai** Validitas **·** **Subkontrak** akan ditetapkan ke **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Mensubkontrakkan anggota tim proyek yang dikelola

Seperti anggota tim generik atau tidak terganggu, Anda juga dapat melihat opsi subkontrak untuk anggota tim proyek yang dikelola selama anggota tim yang dikelola adalah pekerja kontrak. Untuk meninjau dan memilih opsi subkontrak yang tersedia untuk anggota tim proyek yang dikelola atau diberi nama, ikuti langkah-langkah berikut:

1. Pilih satu atau beberapa catatan anggota tim proyek di mana sumber daya adalah pekerja kontrak bernama.
2. Pastikan bahwa tidak ada catatan anggota tim proyek yang dipilih yang sudah disubkontrakkan. 
3. Pilih **Opsi Subkontrak** pada sub grid anggota tim proyek. **Dialog opsi Subkontrak** terbuka. 
4. Jika Anda hanya memilih satu catatan anggota tim proyek di langkah 1, maka opsi berikut akan tersedia:
      - Buat baris subkontrak baru.
      - Cadangan terhadap subkontrak yang ada.
  Jika Anda memilih beberapa catatan anggota tim proyek di langkah 1, maka satu-satunya opsi yang tersedia adalah membuat baris subkontrak baru.
5. Opsi untuk memesan terhadap garis subkontrak yang ada memungkinkan Anda memilih garis subkontrak dan subkontrak yang ingin Anda pesan. Saat memilih baris subkontrak untuk kapasitas cadangan, Anda harus memastikan hal-hal berikut:
      - Garis subkontrak yang dipilih adalah untuk waktu. 
      - Peran yang diperlukan pada anggota tim proyek sesuai dengan peran yang dibeli di garis subkontrak. 
      - Vendor yang terkait dengan pekerja kontrak sama dengan vendor di subkontrak.
6. Ketika Anda memilih untuk membuat baris subkontrak baru untuk anggota tim proyek, sistem akan memungkinkan Anda untuk memilih subkontrak yang ingin Anda buat baris-baris ini. Dengan opsi ini, Anda harus memastikan bahwa vendor milik pekerja kontrak sama dengan vendor di subkontrak. 
7. Subkontrak yang Anda pilih untuk membuat baris baru harus dalam **status** Draf. Dengan opsi ini untuk membuat baris subkontrak baru untuk anggota tim proyek yang dipilih, sistem akan membuat satu baris subkontrak untuk waktu untuk setiap anggota tim proyek. Peran, jam, dan tanggal akan disalin dari anggota tim proyek ke setiap baris subkontrak yang dibuat.  
8. Ketika anggota tim bernama dikaitkan dengan baris subkontrak dan subkontrak, **bidang tipe Pekerja pada baris anggota tim bernama akan diperbarui menjadi Pekerja Kontrak dan nilai** Validitas **·** **Subkontrak** akan ditetapkan ke **Valid**.

## <a name="re-costing-subcontractor-assignments"></a>Tugas subkontraktor biaya ulang

Ketika anggota tim proyek (generik atau bernama) terkait dengan baris subkontrak menggunakan **dialog opsi Subkontrak,** tugas apa pun untuk tugas yang dimiliki anggota tim akan dikenakan biaya ulang berdasarkan daftar harga pembelian yang dilampirkan ke subkontrak. Pada **tab Perkiraan** pada halaman Detail **Proyek**, pilih tombol **Perbarui harga untuk melihat harga yang** diperbarui dan/atau biaya yang dihasilkan dari keputusan untuk subkontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
