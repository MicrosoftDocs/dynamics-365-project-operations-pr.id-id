---
title: Produk
description: Topik ini menyediakan informasi tentang katalog produk yang dapat anda gunakan untuk memberikan informasi kepada pelanggan tentang produk dan harga yang ditawarkan organisasi anda.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 085b7e4d9274f8c8d94d7a84109cfa782acf3dbb9241bfd25ecb8c2f329e1bb8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986855"
---
# <a name="products"></a>Produk

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Produk adalah tulang punggung dari bisnis Anda. Katalog Produk di Dynamics 365 Sales Professional adalah kumpulan produk dan informasi harga. Buat lebih mudah untuk perwakilan penjualan Anda untuk meningkatkan penjualan mereka dengan membuat Katalog Produk dengan cepat.

## <a name="add-a-product"></a>Tambah produk

1.  Pastikan bahwa Anda memiliki peran manajer penjualan profesional atau administrator sistem sehingga Anda dapat menambahkan produk di Dynamics 365 Sales Professional.
2.  Di peta situs, di dalam **Konfigurasi**, pilih **Produk**.
3.  Pilih **tambah produk** dan isi informasi berikut:

    -  **Nama**
    -  **ID produk**
    -  **Induk**: Pilih keluarga produk induk untuk produk. Jika Anda membuat produk anak dalam keluarga produk, nama produk induk kelompok diisi di sini. Hal ini tidak dapat diubah setelah rekaman disimpan.
    -  **Berlaku dari**/**Berlaku hingga:** Tentukan periode yang valid untuk produk dengan memilih **Berlaku dari** dan **Berlaku hingga** tanggal.
    -  **Grup unit**: Pilih grup unit. Grup unit adalah kumpulan berbagai unit produk yang dijual dan mendefinisikan bagaimana masing-masing item ini dikelompokkan ke dalam jumlah yang lebih besar. Misalnya, jika Anda menambahkan benih sebagai produk, Anda mungkin telah membuat sebuah kelompok unit yang disebut "Benih", dan didefinisikan dengan unit utama sebagai "paket."
    -  **Unit Default**: Pilih unit paling umum yang akan digunakan dalam penjualan produk. Unit adalah jumlah atau pengukuran penjualan produk Anda. Misalnya, jika Anda menambahkan benih sebagai produk, Anda dapat menjual mereka dalam paket, kotak, atau palet. Masing-masing menjadi sebuah unit produk. Jika benih sebagian besar dijual dalam paket, pilih sebagai unit.
    -  **Daftar Harga Default**: Jika ini merupakan produk baru, bidang ini hanya baca. Sebelum memilih daftar harga default, Anda harus menyelesaikan semua bidang yang diperlukan, kemudian menyimpan rekaman. Meskipun daftar harga default tidak diperlukan, setelah Anda menyimpan rekaman produk, sangat dianjurkan untuk mengatur daftar harga default untuk masing-masing produk. Kemudian, jika rekaman pelanggan tidak berisi daftar harga, Sales dapat menggunakan daftar harga default untuk menghasilkan kuotasi, pesanan, dan faktur.
    -  **Desimal yang Didukung**: Masukkan bilangan bulat antara 0 hingga 5. Jika produk tidak dapat dibagi menjadi kuantitas pecahan, masukkan 0. Presisi bidang **kuantitas** di kuotasi, pesanan, atau rekaman produk faktur divalidasi terhadap nilai di bidang ini jika produk tidak memiliki daftar harga yang terkait.
    -  **Subjek**: Kaitkan produk ini dengan subjek. Anda dapat menggunakan subjek untuk mengkategorikan produk dan untuk memfilter laporan.

4.  Pilih **Simpan**.
5.  Di tab **detail tambahan**, di bagian **item daftar harga**, pilih ikon **perintah lainnya**, dan kemudian pilih **Tambahkan item daftar harga baru**.
7.  Di tab **rincian tambahan**, di bagian **relasi produk**, pilih ikon **perintah lainnya**, dan kemudian pilih **menambahkan relasi produk baru**.
8.  Di formulir **Relasi produk baru**, masukkan rincian berikut, dan pada bilah perintah, pilih **Simpan dan Tutup**:

    -   **Produk terkait**: Pilih produk yang Anda ingin menambahkan sebagai produk terkait untuk catatan produk yang sudah ada yang sedang Anda kerjakan.
    -   **Jenis Relasi Penjualan**: Pilih Apakah Anda ingin menambahkan produk sebagai up-Selling, penjualan silang, aksesori, atau produk pengganti.
    -   **Arah**: Pilih Apakah hubungan antara produk akan satu arah atau dua arah. Bila Anda memilih Satu Arah, produk yang Anda pilih di **produk terkait** akan ditampilkan sebagai rekomendasi untuk produk sudah ada tapi tidak sebaliknya.

9.  Pada formulir produk, pilih **Simpan**.

## <a name="import-products"></a>Impor produk

Anda dapat menggunakan template impor untuk membawa data produk massal ke dalam Dynamics 365 Sales.

## <a name="revise-a-product"></a>Merevisi produk

Tetap perbarui persediaan produk dengan cepat merevisi properti untuk produk-produk seperti yang diperlukan, dan publikasi ulang informasi sehingga Anda dapat melihat perubahan terbaru persediaan produk.

1.  Pastikan Anda memiliki salah satu peran keamanan berikut atau izin yang setara: Administrator Sistem, Penyesuai Sistem, Manajer Penjualan, Wakil Direktur Utama Penjualan, Wakil Direktur Utama Pemasaran, atau CEO Manajer Bisnis.
2.  Di peta situs, pilih **Produk**.
3.  Buka produk aktif yang Anda ingin ubah, dan pada bilah perintah, pilih **Revisi**.
4.  Dalam kotak dialog **Konfirmasikan Revisi**, pilih **Konfirmasi**. Ini akan mengubah status produk **Sedang direvisi**.
5.  Setelah Anda selesai membuat perubahan, pada bilah perintah, pilih **terbitkan**.

    > [!TIP]
    > Untuk mengembalikan perubahan dan melanjutkan versi aktif terakhir dari produk, pilih **Pulihkan**. Ini mengubah status produk kembali ke **aktif**.

## <a name="clone-a-product"></a>Kloning produk 

Ketika Anda membuat produk baru, hemat waktu dengan kloning yang sudah ada. Hal ini menciptakan salinan asli catatan dengan semua rincian kecuali nama dan ID.

1.  Pastikan Anda memiliki salah satu peran keamanan berikut atau izin yang setara: Administrator Sistem, Penyesuai Sistem, Manajer Penjualan, Wakil Direktur Utama Penjualan, Wakil Direktur Utama Pemasaran, atau CEO Manajer Bisnis.
2.  Di peta situs, pilih **Produk**.
3.  Pilih rekaman produk yang ingin Anda clone, dan pada bilah perintah, pilih **klon**. Kotak dialog konfirmasi akan ditampilkan.
4.  Pilih **Konfirmasi**.

Catatan produk baru akan terbuka dengan rincian yang sama seperti yang asli kecuali untuk nama dan ID.

## <a name="retire-a-product"></a>Menghentikan produk 

Jika organisasi Anda tidak menjual produk lagi, pensiunkan sehingga produk ini tidak lagi tersedia untuk Anda.

1.  Pastikan Anda memiliki peran keamanan Administrator Sistem atau Manajer Sales Professional atau izin yang setara.
2.  Di peta situs, pilih **Produk**.
3.  Buka produk aktif yang Anda ingin pensiunkan, dan pada bilah perintah, pilih **Pensiunkan**.
4.  Dalam kotak dialog **Konfirmasikan Pemensiunan**, pilih **Konfirmasi**.


## <a name="delete-a-product"></a>Hapus Produk

Untuk berhenti menjual produk, hapuslah.

> [!IMPORTANT]
> Anda tidak dapat memulihkan rekaman yang dihapus.

1.  Pastikan Anda memiliki peran keamanan Administrator Sistem atau Manajer Sales Professional atau izin yang setara.
2.  Di peta situs, pilih **Produk**.
3.  Pilih rekaman produk yang ingin Anda hapus, dan pada bilah perintah, pilih **hapus**.
4.  Dalam kotak dialog **Konfirmasikan Penghapusan**, pilih **Lanjutkan**.
 
 ## <a name="quantity-factors-for-products"></a>Faktor kuantitas untuk produk

Faktor kuantitas mendukung penjualan produk berbasis langganan. Untuk produk berbasis langganan, kuantitas pada kuotasi atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.

Biasanya, harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan. Namun, Anda dapat menggunakan Deskripsi waktu lain. Selama proses penjualan, harga pada baris kuotasi biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan TI. Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda. Kuantitas yang digunakan untuk menghitung jumlah baris kuotasi adalah produk dari jumlah pengguna dan jumlah bulan langganan.

Faktor kuantitas mengandalkan atribut produk. Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, Anda dapat menandai subset properti tersebut, atau semua properti, sebagai faktor kuantitas.

Sistem memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas. Bila produk yang memiliki faktor kuantitas dikonfigurasi untuk ditambahkan ke baris kuotasi, bidang **kuantitas** pada baris kuotasi menjadi bidang hanya baca. Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, kuantitas baris kuotasi dihitung.

Misalnya, jika ada properti berikut: 

- **Jumlah pengguna**: jumlah pengguna 
- **Jumlah bulan**: jumlah bulan langganan
- **SKU Produk** 

Properti **Jumlah pengguna** dan **Jumlah bulan** dapat ditandai sebagai faktor kuantitas dengan mengedit properti lini produk. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]