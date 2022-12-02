---
title: Mengonfigurasi jarak tempuh dengan menggunakan tingkat tarif jarak tempuh
description: Artikel ini memberikan informasi tentang tarif jarak tempuh dan tingkat tarif jarak tempuh.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064282"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Mengonfigurasi jarak tempuh dengan menggunakan tingkat tarif jarak tempuh

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Bila pengeluaran dilaporkan dan kategori pengeluaran yang dipilih adalah **Jarak tempuh**, jumlah untuk baris pengeluaran tersebut dihitung sesuai dengan jumlah *tarif per jarak tempuh*. Jumlah ini ditentukan menggunakan tingkat jarak tempuh yang ditentukan atau jika tingkat jarak tempuh tidak ditetapkan, dengan mengikuti tarif standar jarak tempuh. 

Tingkat tarif jarak tempuh dapat diatur dengan membuka **Manajemen Pengeluaran** > **Pengaturan** > **Umum** > **Kategori pengeluaran** > **Jarak tempuh** > **Pengaturan kategori**.

Setelah meningkatkan ke 10.0.18, jika organisasi menggunakan kategori pengeluaran jarak tempuh, pertimbangkan untuk mengaktifkan fitur jarak tempuh setelah meninjau perubahan desain di bawah. 

Desain baru tingkat tingkat tarif jarak tempuh mempengaruhi bagaimana nilai di bidang **Kuantitas** diproses. Sebelum rilis 10.0.18, nilai di bidang **Kuantitas** dianggap sebagai batas bawah. Ketika akumulasi melewati nilai tersebut, tarif terkait digunakan.  Pada 10.0.18, nilai di bidang **Kuantitas** dianggap sebagai batas atas. tarif yang sesuai digunakan saat akumulasi jarak tempuh kurang dari nilai pada bidang **Kuantitas**.  Model baru untuk tingkat jarak tempuh membantu konsistensi di seluruh tingkat jarak tempuh dan kegunaan yang lebih baik.   

Semua laporan pengeluaran yang disetujui akan dihitung ulang selama posting sesuai dengan desain baru.

## <a name="example"></a>Contoh
 
### <a name="before-version-10018"></a>Sebelum versi 10.0.18
Dengan dua tingkat tarif jarak tempuh, bidang **Kuantitas** di setiap tingkat menunjukkan batas jarak tempuh yang lebih rendah. Saat ini, tingkat satu memiliki nilai nol (0) dan tarif 0,45, dan tingkat dua memiliki nilai 1000 dan tarif 0,25. Jika mil atau kilometer yang terakumulasi melewati nilai di bidang, tarif terkait akan digunakan. Jika tidak ada baris dengan kuantitas nol, sistem menggunakan tarif jarak tempuh yang ditentukan dalam manajemen Pengeluaran. 
 
Jika karyawan mengirimkan laporan pengeluaran dengan 1.500 kilometer, dua baris jarak tempuh pada laporan pengeluaran yang dikirim adalah: 1000 (tarif 0,45) + 500 (tarif 0,25) = 575,00.

### <a name="after-version-10018"></a>Setelah versi 10.0.18
Di 10.0.18, bidang **Kuantitas** di tiap tingkat menunjukkan batas atas tingkat. Saat ini, tingkat satu memiliki nilai 999 dan tarif 0,45, dan tingkat dua memiliki nilai 999,999,999.00 dan tarif 0,25. Jika mil atau kilometer yang terakumulasi melewati nilai di bidang **Kuantitas**, tarif terkait akan digunakan. Jika semua batas atas terlewati, sistem menggunakan tarif jarak tempuh yang ditentukan dalam manajemen Pengeluaran. 
 
Untuk menghitung skenario yang sama dengan benar, pengaturan tingkat harus diubah. Bidang **Kuantitas** di tingkat satu memiliki nilai 999,00 dan nilai 999.999.999,00 di tingkat dua. Jika karyawan melebihi total kuantitas kilometer atau kilometer di tingkat satu, sistem akan menggunakan tarif jarak tempuh yang ditentukan dalam manajemen Pengeluaran. 
  
Jika karyawan mengajukan laporan pengeluaran dengan 1.500 kilometer, dua baris jarak tempuh pada laporan pengeluaran yang diajukan adalah: 1000 (tarif 0,45) + 500 (tarif 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Aktifkan perhitungan jumlah jarak tempuh untuk beberapa tingkat jarak tempuh dengan fitur tingkat yang sama

Fitur **Perhitungan jumlah jarak tempuh untuk beberapa tingkat jarak tempuh dengan tarif** menyempurnakan perhitungan tarif jarak tempuh. Selesaikan langkah-langkah berikut untuk mengaktifkan fitur ini.

1. Buka **Ruang kerja** > **Manajemen Fitur**. 
2. Dalam daftar, cari dan pilih **perhitungan jumlah jarak tempuh untuk beberapa tingkat jarak tempuh dengan tarif yang sama**, lalu pilih **Aktifkan sekarang**.

Setelah Anda mengaktifkan fitur, atur ulang tingkat jarak tempuh untuk dengan benar mencerminkan nilai bidang **Kuantitas**. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Aktifkan fitur Penghitungan total jarak tempuh berdasarkan tahun fiskal

fitur **Penghitungan total jarak tempuh berdasarkan tahun fiskal** ini mengaktifkan pengaturan baru dalam parameter manajemen Pengeluaran yang melakukan perhitungan total jarak tempuh tahun fiskal dan bukan tahun kalender. Selesaikan langkah-langkah berikut untuk mengaktifkan fitur ini.

1. Buka **Ruang kerja** > **Manajemen Fitur**.
1. Dalam daftar, cari dan pilih **perhitungan total jarak tempuh menurut tahun fiskal**, lalu pilih **Aktifkan sekarang**.
1. Buka **manajemen Pengeluaran** > **Konfigurasi** > **Umum** > **parameter Management Pengeluaran**.
1. Pada halaman **Parameter manajemen pengeluaran**, cari dan aktifkan **Gunakan tahun fiskal untuk total jarak tempuh**.

Setelah Anda mengaktifkan **Penggunaan tahun fiskal untuk total jarak tempuh**, total jarak tempuh dihitung dengan tahun fiskal.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
