---
title: Manajemen subkontrak dalam Project Operations
description: Artikel ini memberikan ikhtisar proses manajemen subkontrak komprehensif umumnya di organisasi berdasarkan proyek.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522329"
---
# <a name="subcontract-management-in-project-operations"></a>Manajemen subkontrak dalam Project Operations


_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Artikel ini memberikan ikhtisar proses manajemen subkontrak komprehensif di organisasi berdasarkan proyek. Subkontrak untuk layanan biasanya menggunakan alur proses bisnis yang ditampilkan pada diagram berikut.

![Mensubkontrak alur proses](../media/SubcontractingProcessFlow.png)

Daftar berikut memberikan deskripsi langkah demi langkah tentang proses subkontrak.

1. Manajer proyek membuat subkontrak dengan vendor. Secara default, daftar harga yang dilampirkan ke rekaman vendor digunakan untuk subkontrak. Akun vendor memiliki jenis relasi **Vendor** atau **Pemasok**.
2. Manajer proyek dapat memerinci semua pembelian sebagai item baris pada subkontrak. Baris subkontrak dapat untuk waktu, pengeluaran, atau produk. Kelas transaksi baris subkontrak menentukan tujuan baris tersebut.
3. Manajer akun vendor dan manajer proyek dapat mengulang proses subkontrak. Harga dapat disesuaikan dalam daftar harga Pembelian yang dilampirkan ke Subkontrak.
4. Pada titik ini atau versi yang lebih baru dalam proses, jika baris subkontrak adalah untuk waktu, manajer akun vendor mengaitkan kontak vendor dengan setiap baris subkontrak. Keterkaitan ini memberikan informasi kepada manajer proyek yang sedang mengerjakan subkontrak. Bila kontak vendor dikaitkan dengan baris subkontrak, sistem secara otomatis membuat sumber daya yang dapat dipesan dari kontak, jika sumber daya yang dapat dipesan belum ada.
5. Metode penagihan di setiap baris subkontrak dapat adalah **Harga Tetap** atau **Waktu dan Bahan**. Untuk baris subkontrak harga tetap, jadwal faktur berbasis pencapaian dikonfigurasikan.
6.  Setelah subkontrak disiapkan dan negosiasi selesai, itu dikonfirmasi. Subkontrak terkonfirmasi tidak dapat diedit, namun jika perubahan terjadi, subkontrak dapat 'dibuka kembali untuk pengeditan', yang akan menetapkan status dari **Terkonfirmasi** kembali ke **Draf** dan negosiasi dapat dibuka ulang. 
7.  Saat membuat anggota tim generik pada proyek, anggota tim dapat dikaitkan ke baris subkontrak. Hal ini menunjukkan perlunya mengadakan staf anggota tim generik dengan kapasitas subkontraktor.
8.  Anggota tim yang bernama dapat dibuat secara langsung pada proyek atau dibuat dengan memesannya menggunakan pengalaman penjadwalan sumber daya. Jika anggota tim proyek yang bernama adalah pekerja kontrak, dimungkinkan untuk mengaitkannya ke baris subkontrak. Langkah ini akan menarik turun kapasitas yang tersedia pada baris subkontrak.
9.  Sumber daya subkontraktor dapat mencatat waktu, pengeluaran, dan penggunaan bahan pada proyek dan tugas proyek, kemudian mengajukan untuk disetujui. Hal ini serupa untuk karyawan. Saat waktu perekaman, pekerja kontrak dapat memilih baris subkontrak dan subkontrak spesifik.
10. Setelah disetujui, waktu yang disetujui oleh subkontrak akan merekam aktual biaya proyek berdasarkan harga pembelian pekerja kontrak atau peran yang mereka lakukan pada proyek.
11. Faktur vendor dan item baris faktur vendor dapat direkam dalam sistem untuk pekerjaan yang dilakukan oleh sumber daya vendor atau produk yang diselesaikan oleh vendor. Baris faktur vendor harus khusus untuk proyek dan untuk kelas transaksi waktu, pengeluaran, produk/bahan, tahapan, atau biaya. Atau, baris faktur vendor dapat mereferensikan baris subkontrak.
12. Sistem akan secara otomatis mengaitkan semua aktual biaya yang sesuai dengan baris subkontrak dan proyek ke faktur vendor. Hal ini akan memudahkan proses kecocokan dan verifikasi 3 cara.
13. Manajer proyek kemudian dapat meninjau aktual proyek yang sesuai secara otomatis, menghilangkan atau menambahkan aktual biaya proyek lainnya, dan menyelesaikan proses verifikasi.
14. Menyelesaikan proses verifikasi di semua baris akan menandai faktur vendor sebagai **Siap untuk Pembayaran**. Pada tahap ini, faktur dan baris vendor dapat ditransfer ke sistem Akuntansi atau Utang untuk memproses pembayaran ke vendor. Biaya proyek yang direkam sebelumnya akan dikembalikan dan biaya aktual dari baris faktur vendor akan direkam pada proyek.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Baris subkontrak berbasis kuantitas dan baris subkontrak berbasis kerja

Baris kontrak dapat berbasis kuantitas atau pekerjaan. 

Bila baris subkontrak **berbasis kuantitas**, kuantitas yang dibeli di baris subkontrak untuk waktu, pengeluaran, atau bahan dapat digunakan pada proyek apa pun.

Bila baris subkontrak **berbasis kerja**, baris subkontrak dipetakan ke badan kerja yang ditunjukkan oleh node dalam rencana proyek. Nilai baris subkontrak adalah jumlah semua komponen yang diperlukan untuk menghasilkan badan kerja tersebut. Ini dimodelkan sebagai detail baris subkontrak dan dapat merupakan kumpulan waktu, pengeluaran, atau bahan. Untuk baris subkontrak berbasis kerja, baris subkontrak juga dikhususkan untuk satu proyek. Jenis subkontrak ini tidak didukung oleh Project Operations untuk saat ini.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

