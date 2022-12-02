---
title: Mentransfer anggaran proyek di akhir tahun fiskal
description: Artikel ini menyediakan informasi tentang cara mentransfer sisa jumlah anggaran ke masa depan dan membuat rincian register anggaran.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5b4e768cb78d6a6cb76b3c338fd76363d5290ebd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684048"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Mentransfer anggaran proyek di akhir tahun fiskal

[!include [banner](../includes/banner.md)]

Saat mengerjakan proyek selama beberapa tahun, anda mungkin memiliki anggaran yang tersisa di akhir tahun fiskal. Anda dapat mentransfer sisa jumlah anggaran ke tahun mendatang, dan membuat rincian register anggaran untuk jumlah di akun buku besar terkait. Sebelum Anda meneruskan jumlah yang tersisa, tinjau dan analisis jumlah anggaran yang tersisa.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Meninjau dan menganalisis jumlah anggaran tersisa

Selesaikan langkah-langkah berikut untuk meninjau jumlah anggaran akhir tahun untuk proyek, namun tidak meneruskan jumlah ke depan.

1. Buka **manajemen proyek dan akuntansi** > **periodik** > **anggaran** > **Teruskan anggaran**. 
2. Pada halaman **proses meneruskan anggaran proyek**, pada tab **pilihan akhir tahun**, verifikasikan bahwa **Teruskan jumlah anggaran proyek yang tersisa** tidak diaktifkan.
3. Pada tab **parameter**, di bidang **tahun anggaran proyek**, pilih tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa. 
4. Pada bidang **Pembukaan tahun fiskal**, pilih tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa. 
5. Di bidang **dari model perkiraan**, pilih **anggaran tersisa**. 
6. Untuk menyertakan proyek yang memenuhi kriteria yang Anda pilih dan tidak memiliki anggaran tersisa, pilih **Tampilkan nol tersisa**.  
7. Pada tab **pilih anggaran**, pilih **ambil semua anggaran** untuk memuat semua anggaran yang sesuai dengan kriteria yang dipilih, lalu pilih **proses**. 
8. Untuk merancang kueri database yang memuat kumpulan anggaran tertentu ke dalam panel, pilih **ambil anggaran yang dipilih**.

Untuk informasi lebih lanjut tentang baris tertentu di panel, pilih baris, lalu pilih **Lihat rincian anggaran** atau **Lihat akun**.

## <a name="carry-forward-remaining-budget-amounts"></a>Teruskan jumlah anggaran yang tersisa 

Bila Anda memproses jumlah anggaran yang tersisa, Anda dapat membuat transaksi di buku besar untuk jumlah yang Anda teruskan. Untuk membuat transaksi buku besar, selesaikan langkah-langkah di bagian, [Teruskan jumlah anggaran dan buat transaksi buku besar](#carry-forward). 

> [!NOTE]
> Jumlah anggaran yang diteruskan akan ditransfer ke model perkiraan yang dipilih di halaman **model perkiraan** sebagai model perkiraan teruskan.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Meneruskan jumlah anggaran dan membuat transaksi buku besar

1.  Pilih **manajemen proyek dan akuntansi** > **periodik** > **anggaran** > **Teruskan anggaran**. 
2. Pada halaman **proses meneruskan anggaran proyek**, pilih **akhir tahun**, lalu Aktifkan Teruskan **jumlah anggaran proyek yang tersisa**, dan **buat entri daftar anggaran dalam buku besar**. 
3. Pada tab **parameter**, di grup bidang **parameter proyek**, pilih yang berikut:

   - **Tahun anggaran proyek**: pilih awal tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa. 
   - **Laba-rugi**: buat transaksi laba-rugi di buku besar. 
   -  **WIP**: membuat transaksi pekerjaan dalam proses (WIP) di buku besar.
   -  **Penggajian**: Buat transaksi alokasi gaji di buku besar. 

5. Pada grup bidang **Buku besar**, berikan informasi berikut: 

   - Pada bidang **Pembukaan tahun fiskal**, pilih tahun fiskal yang ingin anda transfer jumlah sisa anggarannya untuk proyek. Nilai default-nya adalah satu tahun setelah nilai dalam bidang **tahun anggaran proyek**.
   -  Di **Periode penerusan**, pilih periode yang akan dibuat rincian register anggarannya di buku besar. Biasanya ini adalah periode pertama di pembukaan tahun fiskal.

6. Pada grup bidang **Salin dari/ke**, berikan informasi berikut:

   - Di bidang **dari model perkiraan**, pilih model anggaran perkiraan proyek yang terkait dengan jumlah anggaran tersisa yang akan ditransfer untuk proyek. 
   - Di bidang **Ke model anggaran buku besar**, pilih model anggaran buku besar yang terkait dengan jumlah anggaran tersisa yang akan ditransfer ke buku besar. 
   -  Pilih **Transfer mata uang penjualan** untuk menggunakan mata uang penjualan proyek untuk transaksi buku besar umum yang dibuat saat Anda mentransfer jumlah anggaran untuk proyek. Bila pilihan tidak dipilih, transaksi menggunakan mata uang akuntansi. 
   -  Pilih **Tampilkan nol yang tersisa** untuk menyertakan proyek yang tidak memiliki jumlah anggaran tersisa, namun memenuhi kriteria lain yang Anda pilih di proyek yang ditampilkan di panel bawah.

7. Pada tab **pilih anggaran**, pilih **ambil semua anggaran** untuk memuat semua anggaran yang sesuai dengan kriteria yang dipilih. Jika Anda memilih untuk merancang kueri database yang memuat kumpulan anggaran proyek tertentu ke dalam panel, pilih **ambil anggaran yang dipilih**.
8. Untuk setiap proyek yang akan diproses, pilih pilihan di awal baris untuk proyek.

    > [!TIP]
    > Untuk memilih semua atau sebagian besar proyek, pilih tanda centang di sudut kiri atas. Untuk mengecualikan pemrosesan setiap proyek, kosongkan tanda centang untuk proyek tersebut.

9. Untuk mentransfer jumlah anggaran yang tersisa untuk proyek yang dipilih ke tahun fiskal yang dipilih dan membuat rincian register anggaran di buku besar, pilih **proses**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Meneruskan jumlah anggaran tanpa membuat transaksi buku besar

1. Buka **manajemen proyek dan akuntansi** > **periodik** > **anggaran** > **Teruskan anggaran**.
2. Pada halaman **proses meneruskan anggaran proyek**, pada bidang **pilihan akhir tahun**, pilih **Teruskan jumlah anggaran proyek yang tersisa**.
3. Pada grup **parameter**, di bidang **tahun anggaran proyek**, pilih tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa.
4. Pada grup **Salin dari/ke**, berikan informasi berikut:

   - Di bidang **dari model perkiraan**, pilih model anggaran perkiraan proyek yang terkait dengan jumlah anggaran tersisa yang akan ditransfer untuk proyek. 
   - Untuk menyertakan proyek yang tidak memiliki jumlah anggaran tersisa, namun memenuhi kriteria lain yang Anda pilih, pilih **Tampilkan nol tersisa**.
   - Pada grup **pilih anggaran**, pilih **ambil semua anggaran** untuk memuat semua anggaran yang sesuai dengan kriteria yang dipilih. Untuk merancang kueri database yang memuat kumpulan anggaran proyek tertentu ke dalam panel, pilih **ambil anggaran yang dipilih**.

5. Untuk setiap proyek yang akan diproses, pilih pilihan di awal baris untuk proyek. 
6. Pilih **proses** untuk mentransfer jumlah anggaran yang tersisa untuk proyek yang dipilih ke tahun fiskal yang dipilih.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
