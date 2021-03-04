---
title: Mengelola estimasi pendapatan
description: Topik ini berisi informasi tentang cara menggunakan estimasi pendapatan untuk berbagai proyek.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531459"
---
# <a name="manage-revenue-estimates"></a>Mengelola estimasi pendapatan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Anda dapat membuat, menghitung, memposting, membalik, atau menghilangkan estimasi pendapatan. Anda dapat melakukannya, baik secara manual maupun menggunakan proses berkala. Topik ini berisi informasi tentang cara menggunakan estimasi pendapatan untuk berbagai proyek.

### <a name="manage-revenue-estimates-manually"></a>Mengelola estimasi pendapatan secara manual

Pada proyek estimasi pendapatan harga tetap atau halaman **Estimasi permintaan** (**Manajemen dan akuntansi proyek** > **Laporan pertanyaan** > **Estimasi pertanyaan dan laporan**), pilih **Estimasi**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Mengelola estimasi pendapatan menggunakan proses berkala

Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Estimasi** dan pilih proses yang terkait.

## <a name="create-a-revenue-estimate"></a>Membuat estimasi pendapatan

Lakukan langkah-langkah berikut untuk membuat estimasi pendapatan. 

1. Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Estimasi**.
2. Pilih **baru**. Pada halaman **Pembuatan estimasi**, pilih parameter berikut:

   - **Kode periode** : Kode ini menentukan seberapa sering estimasi akan diposting.
   - **Tanggal estimasi**: Tanggal estimasi diproses.
   - **Kontinu**: Pilih kotak centang ini untuk membuat estimasi hanya apabila estimasi diposting pada periode sebelumnya atau jika estimasi merupakan estimasi pertama yang telah dibuat. Jika tidak dipilih, estimasi akan dibuat meskipun estimasi tidak diposting pada periode sebelumnya.
   - **Metode biaya penyelesaian**: Menentukan cara membuat estimasi pekerjaan proyek yang tersisa. Untuk informasi lebih lanjut, lihat [metode biaya penyelesaian](cost-complete-methods.md).
   - **Metode penyelesaian**: Pilih metode penyelesaian dari pilihan berikut:
     - **Otomatis**: Persentase penyelesaian dihitung secara otomatis dan berdasarkan pada baris biaya yang tercakup dalam perhitungan. Template biaya menentukan baris biaya yang disertakan.
     - **Manual**: Persentase penyelesaian setara dengan persentase penyelesaian estimasi terakhir. Setelah estimasi dibuat, Anda dapat mengubah **Penghitungan manual** pada halaman **Estimasi**.
     - **Dari template biaya**: Kombinasi dari metode otomatis dan manual. Pilihan ini diatur secara otomatis atau manual, tergantung pada nilai default dalam template biaya.
   - **Model prakiraan**: Memilih model prakiraan untuk estimasi.
   - **Daftar estimasi cetak**: Membuat dan menampilkan daftar estimasi. Daftar berisi status fungsi saat ini. Anda dapat mencetak peringatan tentang estimasi pada laporan. Kondisi berikut menyebabkan peringatan muncul di daftar estimasi:
     - Persentase penyelesaian lebih dari 100 persen.
     - Persentase penyelesaian kurang dari nol persen.
     - Jumlah negatif di kolom **Untuk diselesaikan**.
     - Estimasi tanpa jumlah kontrak yang sesuai.
     - Estimasi tanpa estimasi biaya terlampir.
   - **Tampilkan Infolog**: Pilih pilihan ini untuk menerima pesan berisi informasi tentang estimasi proyek yang diproses saat pekerjaan berjalan.


## <a name="post-wip-or-accruals"></a>Memposting WIP atau akrual

Setelah estimasi dievaluasi, estimasi tersebut dikelola, dikurang atau ditingkatkan. Selanjutnya Anda dapat memposting WIP saat menggunakan prinsip penilaian **Kontrak yang telah selesai**, atau memposting akrual saat Anda menggunakan prinsip penilaian **Persentase yang telah selesai**.
  
Status periode estimasi berubah dari **Dibuat** menjadi **Diposting**.

## <a name="reverse-wip-or-accruals"></a>WIP Terbalik atau akrual

Gunakan pilihan balik untuk kredit yang telah memposting WIP atau akrual, lalu buat estimasi untuk periode tersebut.

> [!NOTE]
> Untuk membalikkan periode yang berada di antara beberapa periode lain, balikkan periode estimasi yang diperlukan, lalu posting ulang. Karena semua periode berikutnya tergantung pada estimasi dari periode sebelumnya, jangan lewati periode apa pun.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Hilangkan estimasi proyek dan selesaikan proyek

Langkah terakhir dalam proses estimasi adalah menghilangkan estimasi proyek dan mengakhiri proyek harga tetap saat persentase penyelesaian mencapai 100 persen.

Berikut adalah yang akan terjadi saat Anda menjalankan penghapusan:

- Untuk proyek harga tetap dengan kontrak yang telah diselesaikan, nilai WIP diperoleh dari akun saldo dan diposting ke akun laba dan rugi.
- Untuk proyek harga tetap dengan persentase yang telah selesai, akrual akan dihapus dari akun laba dan rugi.

Estimasi akan berubah status menjadi **Dihilangkan**.

> [!NOTE]
> Dalam kasus khusus, persentase dapat melampaui 100 persen. Bila ini terjadi, kurangi persentase penyelesaian dengan menggunakan **Atur biaya ke metode penyelesaian nol** untuk mencapai 100 persen.

## <a name="reverse-elimination"></a>Penghilangan terbalik

1. Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Estimasi** > **Penghilangan terbalik**. 
2. Pada Panel Tindakan, di tab **Proses**, dalam grup **Kelola**, pilih **Estimasi**. 
3. Pilih **Penghilangan terbalik**.

Gunakan halaman ini untuk membalik semua penghilangan dengan tanggal estimasi yang ditentukan dan dengan status estimasi **Dihilangkan**. Status transaksi berubah setelah Anda memilih bidang yang sesuai.

Hal ini juga secara otomatis mengubah status proyek ke **Dalam proses** jika tahapan proyek diatur selesai. Status estimasi periode proyek berubah kembali ke **Diposting**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]