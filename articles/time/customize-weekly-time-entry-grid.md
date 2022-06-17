---
title: Memperpanjang entri waktu
description: Artikel ini menyediakan informasi tentang bagaimana pengembang dapat memperpanjang kontrol entri waktu.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914774"
---
# <a name="extending-time-entries"></a>Memperpanjang entri waktu

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mencakup kontrol kustom entri waktu yang dapat diperpanjang. Kontrol ini termasuk fitur berikut:

- Masukkan waktu secara horizontal selama seminggu
- Total berdasarkan hari, baris, atau minggu
- Salin baris atau minggu
- Entri waktu melalui HH:mm atau HH.hh (secara otomatis mengkonversi ke HH.hh)
- Impor dari tugas, pemesanan, atau janji temu

Memperluas entri waktu dimungkinkan di dua area:
- [Tambahkan entri waktu kustom untuk penggunaan Anda sendiri](#add)
- [Menyesuaikan kontrol entri waktu mingguan](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Tambahkan entri waktu kustom untuk penggunaan Anda sendiri

Entri waktu adalah entitas inti yang digunakan dalam beberapa skenario. Pada April Gelombang 1 2020, solusi inti TESA diperkenalkan. TESA menyediakan entitas **Pengaturan** dan peran keamanan **Pengguna Entri Waktu** baru. Bidang baru, **msdyn_start** dan **msdyn_end** yang memiliki hubungan langsung dengan **msdyn_duration**, juga disertakan. Entitas baru, peran keamanan, dan bidang memungkinkan pendekatan yang lebih terpadu untuk waktu di beberapa produk.


### <a name="time-source-entity"></a>Entitas Sumber Waktu
| Bidang | KETERANGAN | 
|-------|------------|
| Nama  | Nama entri sumber waktu yang digunakan sebagai nilai pilihan selama pembuatan entri waktu. |
| Sumber waktu default [sumber waktu: IsDefault] | Secara default, hanya satu sumber waktu yang dapat ditandai pada default. Ini memungkinkan entri default ke sumber waktu jika tidak ada yang ditentukan. |
|Jenis sumber waktu [sumber waktu: sourcetype] | Jenis sumber adalah pilihan (jenis sumber entri waktu) yang memungkinkan Asosiasi sumber waktu ke aplikasi. Nilai cadangan Microsoft lebih dari 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entri waktu dan entitas sumber waktu
Setiap entri waktu dikaitkan ke rekaman sumber waktu. Catatan ini menentukan aplikasi mana yang harus memproses entri waktu dan bagaimana caranya.

Entri waktu selalu merupakan satu blok waktu berdekatan dengan awal, akhir, dan durasi yang ditautkan.

Logika akan secara otomatis memperbarui rekaman entri waktu dalam situasi berikut:

- Jika dua dari tiga bidang berikut disediakan, maka yang ketiga akan dihitung secara otomatis: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Bidang **msdyn_start** dan **msdyn_end** sadar zona waktu.
- Entri waktu yang dibuat hanya dengan **msdyn_date** dan **msdyn_duration** yang ditentukan akan dimulai pada tengah malam. Bidang **msdyn_start** dan **msdyn_end** akan diperbarui sesuai dengan ini.

#### <a name="time-entry-types"></a>Jenis Entri Waktu

Rekaman entri waktu memiliki jenis terkait yang menentukan perilaku di alur pengajuan untuk aplikasi terkait.

|Label | Nilai|
|-----|-----|
|Saat Istirahat   |192,355,000|
|Perjalanan | 192,355,001|
|Lembur   | 192,354,320|
|Kerja   | 192,350,000|
|Absensi    | 192,350,001|
|Liburan   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Menyesuaikan kontrol entri waktu mingguan
Pengembang dapat menambahkan bidang tambahan dan pencarian ke entitas lain, dan menerapkan aturan bisnis kustom untuk mendukung skenario bisnis mereka.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Tambahkan bidang kustom dengan pencarian ke entitas lain
Ada tiga langkah utama untuk menambahkan bidang kustom ke kisi entri mingguan waktu.

1. Tambahkan bidang kustom ke kotak **dialog Buat** cepat.
2. Konfigurasikan kisi untuk menampilkan bidang kustom.
3. Tambahkan bidang kustom ke **halaman Edit** baris atau **Edit** entri waktu, sebagaimana mestinya.

Pastikan bahwa bidang baru memiliki validasi yang diperlukan pada **halaman Edit** baris atau **Edit** entri waktu. Sebagai bagian dari tugas ini, kunci bidang, berdasarkan status entri waktu.

Saat Anda menambahkan bidang kustom ke **kisi entri** Waktu lalu membuat entri waktu langsung dalam kisi, bidang kustom untuk entri tersebut secara otomatis diatur sehingga cocok dengan baris tersebut. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Menambahkan bidang kustom ke kotak dialog Buat cepat
Tambahkan bidang kustom ke **kotak dialog Buat cepat: Buat Entri** Waktu. Pengguna kemudian dapat memasukkan nilai saat mereka menambahkan entri waktu dengan memilih **baru**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan kisi untuk menampilkan bidang kustom
Ada dua cara menambahkan bidang kustom ke **kisi entri** waktu Mingguan.

- **Kustomisasi tampilan Entri** Waktu Mingguan Saya, dan tambahkan bidang kustom ke dalamnya. Anda dapat menentukan posisi dan ukuran bidang kustom dalam kisi dengan mengedit properti dalam tampilan.
- Buat tampilan entri waktu kustom baru, dan atur sebagai tampilan default. Tampilan ini harus berisi **bidang Deskripsi** dan **Komentar** eksternal selain kolom yang Anda inginkan untuk disertakan dalam kisi. Anda dapat menentukan posisi, ukuran, dan urutan urutan default kisi dengan mengedit properti dalam tampilan. Selanjutnya, konfigurasikan kontrol kustom untuk tampilan ini sehingga merupakan kontrol **kisi entri waktu**. Tambahkan kontrol ke tampilan, dan pilih untuk **Web**, **Telepon**, dan **Tablet**. Selanjutnya, konfigurasikan parameter untuk **kisi entri** waktu mingguan. **Atur bidang Tanggal** mulai ke **tanggal\_ msdyn**, atur **bidang Durasi** ke **durasi\_ msdyn**, dan atur **bidang Status** ke **msdyn\_ entrystatus**. Bidang **Daftar** Status Baca-saja diatur ke **192350002 (Disetujui)**, **192350003 (Dikirim)**, atau **192350004 (Ingat Diminta)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Menambahkan bidang kustom ke halaman edit yang sesuai
Halaman yang digunakan untuk mengedit entri waktu atau deretan entri waktu dapat ditemukan di bawah **Formulir**. Tombol **Edit entri** dalam kisi membuka **halaman entri** Edit, dan tombol **Edit baris** membuka **halaman Edit** baris. Anda dapat mengedit halaman ini sehingga menyertakan bidang kustom.

Kedua opsi menghapus beberapa pemfilteran out-of-box pada **entitas Project** dan **Project Task**, sehingga semua tampilan pencarian untuk entitas terlihat. Per default, hanya tampilan pencarian yang relevan yang dapat dilihat.

Anda harus menentukan halaman yang sesuai untuk bidang kustom. Kemungkinan besar, jika Anda menambahkan bidang ke kisi, itu harus masuk ke **halaman Edit** baris yang digunakan untuk bidang yang berlaku untuk seluruh baris entri waktu. Jika bidang kustom memiliki nilai unik dalam baris setiap hari (misalnya, jika itu adalah bidang kustom untuk akhir zaman), bidang tersebut harus masuk ke **halaman Edit** entri waktu.

Untuk menambahkan bidang kustom ke halaman, seret elemen Bidang **ke posisi yang** sesuai pada halaman, lalu atur propertinya.

### <a name="add-new-option-set-values"></a>Tambahkan Nilai Rangkaian Pilihan baru
Untuk menambahkan nilai rangkaian pilihan ke bidang di luar kotak, ikuti langkah-langkah berikut.

1. Buka halaman pengeditan untuk bidang tersebut, lalu, di bawah **Tipe**, pilih **Edit** di samping rangkaian pilihan.
2. Tambahkan pilihan baru yang memiliki label dan warna kustom. Jika Anda ingin menambahkan status entri waktu baru, bidang di luar kotak bernama **Status** Entri.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Menentukan status entri waktu baru sebagai hanya baca
Untuk menetapkan status entri waktu baru sebagai hanya baca, tambahkan nilai entri waktu baru ke properti **daftar status hanya baca**. Pastikan untuk menambahkan nomor, bukan label. Bagian yang dapat diedit dari kisi entri waktu sekarang akan dikunci untuk baris yang memiliki status baru. Untuk mengatur **properti Daftar** Status Baca-Saja secara berbeda untuk tampilan Entri **Waktu yang berbeda**, tambahkan **kisi entri** Waktu di bagian Kontrol **kustom tampilan**, dan konfigurasikan parameter yang sesuai.

Selanjutnya, tambahkan aturan bisnis untuk mengunci semua bidang pada **halaman Edit** baris dan **Edit** entri waktu. Untuk mengakses aturan bisnis untuk halaman ini, buka editor formulir untuk setiap halaman, lalu pilih **Aturan bisnis**. Anda dapat menambahkan status baru ke kondisi di aturan bisnis yang ada, atau Anda dapat menambahkan aturan bisnis baru untuk status baru.

### <a name="add-custom-validation-rules"></a>Tambahkan aturan validasi kustom
Anda dapat menambahkan dua tipe aturan validasi untuk **pengalaman kisi entri** waktu mingguan:

- Aturan bisnis sisi klien yang berfungsi di halaman
- Validasi plug-in sisi server yang berlaku untuk pembaruan entri sepanjang masa

#### <a name="client-side-business-rules"></a>Aturan bisnis sisi klien
Gunakan aturan bisnis untuk mengunci dan membuka kunci bidang, masukkan nilai default di bidang, dan tentukan validasi yang memerlukan informasi hanya dari rekaman entri waktu saat ini. Untuk mengakses aturan bisnis untuk halaman, buka editor formulir, lalu pilih **Aturan bisnis**. Selanjutnya, Anda dapat mengedit aturan bisnis yang ada atau menambahkan aturan bisnis baru.

#### <a name="server-side-plug-in-validations"></a>Validasi plug-in sisi server
Anda harus menggunakan validasi plug-in untuk validasi apa pun yang memerlukan lebih banyak konteks daripada yang tersedia dalam satu catatan entri waktu. Anda juga harus menggunakannya untuk validasi apa pun yang ingin Anda jalankan pada pembaruan sebaris di grid. Untuk menyelesaikan validasi, buat plug-in kustom pada **entitas Entri** Waktu.

### <a name="limits"></a>Batas
Saat ini, **kisi entri** Waktu memiliki batas ukuran 500 baris. Jika ada lebih dari 500 baris, baris berlebih tidak akan ditampilkan. Tidak ada cara untuk meningkatkan batas ukuran ini.

### <a name="copying-time-entries"></a>Menyalin entri waktu
Gunakan tampilan **Salin Kolom Entri Waktu** untuk menentukan daftar bidang yang akan disalin selama entri waktu. **Tanggal** dan **Durasi** adalah bidang yang diperlukan dan tidak boleh dihapus dari tampilan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
