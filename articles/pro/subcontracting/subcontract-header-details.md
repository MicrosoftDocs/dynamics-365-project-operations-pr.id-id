---
title: Rincian header untuk subkontrak
description: Topik ini menjelaskan fungsi yang diberikan pada header subkontrak dalam Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fade0ff876486ad60ffd9ad618be7864c1b28185
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598170"
---
# <a name="header-details-for-subcontracts"></a>Rincian header untuk subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Topik ini menjelaskan fungsi yang diberikan pada header subkontrak dalam Dynamics 365 Project Operations.

Saat Manajer Proyek merencanakan dan mengeksekusi proyek, mereka mungkin mempekerjakan subkontraktor dan membeli produk maupun layanan dari vendor. Bila Manajer Proyek harus membeli produk atau layanan, mereka dapat membuat subkontrak dalam Project Operations.

Untuk membuat subkontrak, selesaikan langkah-langkah berikut.

1. Di panel navigasi, pilih **Subkontrak**, dan pada halaman **Subkontrak**, pilih **Baru**.
2. Masukkan informasi yang diperlukan dan kemudian pilih **Simpan**.

    Tabel berikut memberikan informasi tentang bidang pada halaman **header Subkontrak**.

    | Bidang | KETERANGAN |Dampak Fungsional |
    |---|------|---| 
    | Nama | Nama Subkontrak. | Di semua daftar drop-down subkontrak, nama subkontrak tercantum di kolom pertama untuk membantu Anda mengidentifikasi subkontrak. | 
    | KETERANGAN | Deskripsi singkat tentang layanan dan produk yang dibeli pada subkontrak. | Tidak Ada |
    | Vendor | Nama perusahaan tempat membeli produk dan layanan. Rekaman Akun ini memiliki jenis relasi **Vendor** atau **Pemasok**. | Berdasarkan vendor yang dipilih, nilai default akan secara otomatis dimasukkan untuk bidang berikut:<br/> **• Mata Uang** </br> **• Daftar Harga** </br> **• Ketentuan Pembayaran**</br> **• Alamat Pembayaran**</br> **• Alamat Penagihan**</br> **• Nama Penagihan** </br>**• Manajer Akun Vendor**|
    | Tanggal Subkontrak | Tanggal saat subkontrak dibuat. | Tanggal subkontrak digunakan untuk memilih daftar harga pembelian yang benar, baik dari daftar harga yang dilampirkan ke vendor terkait maupun dari parameter proyek. |
    | Alasan Status | Status Subkontrak. | Status menentukan lokasi subkontrak dalam proses bisnis dan apakah dapat diedit. <br/>Nilai mencakup:<br>• **Draf**: Subkontrak dapat diedit. Anda hanya dapat mengedit subkontrak dengan status **Draf**.<br/>• **Dikonfirmasi**: Negosiasi dengan vendor telah selesai dan subkontrak disetujui untuk pengiriman. <br/>• **Ditutup**: Pengiriman pada subkontrak selesai.<br/>• **Dibatalkan**: Subkontrak dibatalkan dan tidak ada pengiriman yang direncanakan.  | 
    | Mata uang | Mata uang yang digunakan untuk membeli produk dan layanan. Nilai default akan secara otomatis dimasukkan dari akun vendor, namun dapat diubah. | Mata uang subkontrak digunakan untuk memilih daftar harga pembelian baik dari daftar harga yang dilampirkan ke vendor terkait maupun dari parameter proyek. Daftar harga dalam mata uang lain tidak dapat dikaitkan dengan subkontrak. Biaya waktu, pengeluaran, dan bahan yang dikirimkan sumber daya vendor dari subkontrak ini dicatat dalam mata uang ini pada proyek. Setelah rekaman subkontrak disimpan, mata uang pada subkontrak tidak dapat diubah.|
    | Unit Kontrak | Divisi perusahaan yang menandatangani kontrak pembelian atau subkontrak dengan vendor. | Tidak Ada |
    | Syarat Pembayaran | Persyaratan pembayaran pada faktur vendor yang dikeluarkan pada subkontrak ini. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Persyaratan pembayaran dari subkontrak disalin ke semua faktur vendor yang terkait dengan subkontrak ini. Persyaratan pembayaran dapat diperbarui jika subkontrak memiliki status **Draf**. | 
    | Alamat Pembayaran | Alamat vendor untuk pengiriman pembayaran. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Alamat pembayaran dari subkontrak disalin sebagai alamat pembayaran untuk semua faktur vendor yang dibuat untuk subkontrak ini. Alamat pembayaran dapat diperbarui jika subkontrak memiliki status **Draf**.|
    | Nama Penagihan | Nama orang atau divisi di perusahaan vendor yang akan mengirim faktur. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Nilai **Nama penagihan** dari subkontrak disalin ke semua faktur vendor yang terkait dengan subkontrak ini. Bidang ini dapat diperbarui jika subkontrak memiliki status **Draf**.|
    | Alamat Penagihan | Alamat yang digunakan pada faktur dari vendor. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Alamat ini adalah alamat "faktur dari" pada faktur vendor yang dibuat untuk subkontrak ini. |
    | Subtotal | Jika subkontrak tidak memiliki baris, masukkan subtotal pesanan sebelum pajak. Jika subkontrak memiliki baris, bidang ini hanya dapat dibaca. Jumlah yang ditampilkan adalah jumlah subtotal dari semua baris pada subkontrak. | Tidak Ada |
    | Total Pajak | Jika subkontrak tidak memiliki baris, masukkan total pajak pada subkontrak ini. Jika subkontrak memiliki baris, bidang ini hanya dapat dibaca. Jumlah yang ditampilkan adalah jumlah dari jumlah pajak dari semua baris pada subkontrak. | Tidak Ada |
    | Jumlah Total | Data bidang terhitung ini menunjukkan jumlah total subkontrak setelah pajak disertakan. | Tidak Ada |
    | Tanggal Dikonfirmasi | Tanggal subkontrak Dikonfirmasi. | Tidak Ada |
    | Diminta Oleh | Secara default, bidang ini diatur ke nama pengguna yang membuat subkontrak. Namun, pembuat subkontrak dapat mengubah nilai untuk menunjukkan orang yang mereka buat subkontraknya atas nama mereka. | Tidak Ada |
    | Manajer Akun Vendor | Nama kontak utama akun vendor. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. Anda dapat memilih kontak yang berbeda sebagai manajer akun vendor subkontrak. | Anda dapat mengkonfigurasikan pemberitahuan email untuk memberitahukan kontak bila perubahan dibuat pada subkontrak sebagai hasil dari negosiasi harga. |
