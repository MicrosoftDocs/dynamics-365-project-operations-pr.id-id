---
title: Memperpanjang entri waktu
description: Topik ini menyediakan informasi tentang cara pengembang mampu memperpanjang kontrol entri waktu.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930884"
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

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Tambahkan entri waktu kustom untuk penggunaan Anda sendiri.

Entri waktu adalah entitas inti yang dirancang untuk digunakan dalam beberapa skenario. Pada Gelombang 1 April 2020, solusi inti TESA diperkenalkan, yang menyediakan entitas **pengaturan** dan peran keamanan **pengguna entri waktu** baru. Bidang baru, **msdyn_start** dan **msdyn_end** yang memiliki hubungan langsung dengan **msdyn_duration**, juga disertakan. Entitas baru, peran keamanan, dan bidang memungkinkan pendekatan yang lebih terpadu untuk waktu di beberapa produk.


### <a name="time-source-entity"></a>Entitas Sumber Waktu
| Bidang | KETERANGAN | 
|-------|------------|
| Nama  | Nama entri sumber waktu yang digunakan sebagai nilai pilihan selama pembuatan entri waktu. |
| Sumber waktu default [sumber waktu: IsDefault] | Secara default, hanya satu sumber waktu yang dapat ditandai pada sumber waktu default. Kemampuan ini memungkinkan entri default ke sumber waktu jika tidak ada yang ditentukan. |
|Jenis sumber waktu [sumber waktu: sourcetype] | Jenis sumber adalah pilihan (jenis sumber entri waktu) yang memungkinkan Asosiasi sumber waktu ke aplikasi. Nilai tambahan akan ditambahkan ke rangkaian pilihan ini saat aplikasi tambahan ditambahkan. Perhatikan bahwa nilai cadangan Microsoft lebih dari 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entri waktu dan entitas sumber waktu
Setiap entri waktu dikaitkan ke rekaman sumber waktu. Rekaman ini menentukan bagaimana dan aplikasi mana yang harus memproses entri waktu.

Entri waktu selalu merupakan satu blok waktu berdekatan dengan awal, akhir, dan durasi yang ditautkan.

Logika akan secara otomatis memperbarui rekaman entri waktu dalam situasi berikut:

- Jika dua dari tiga bidang berikut disediakan, maka yang ketiga akan dihitung secara otomatis 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Bidang, **msdyn_start,** dan **msdyn_end** sadar zona waktu.
- Entri waktu yang dibuat dengan hanya **msdyn_date** dan **msdyn_duration** yang ditentukan akan dimulai pada tengah malam, dan **msdyn_start** dan **msdyn_end** akan diperbarui sesuai dengan itu.

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

- Tambahkan bidang kustom ke kotak dialog buat cepat
- Konfigurasikan kisi untuk menampilkan bidang kustom.
- Tambahkan bidang kustom ke alur tugas Edit baris atau aliran tugas Edit sel.

Anda juga harus memastikan bahwa bidang baru memiliki validasi yang diperlukan di alur tugas Edit sel atau baris. Sebagai bagian dari langkah ini, Anda harus mengunci bidang, berdasarkan status entri waktu.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tambahkan bidang kustom ke kotak dialog buat cepat
Anda harus menambahkan bidang kustom ke kotak dialog **buat cepat waktu pembuatan entri waktu**. Pengguna kemudian dapat memasukkan nilai saat mereka menambahkan entri waktu dengan memilih **baru**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan kisi untuk menampilkan bidang kustom
Ada dua cara untuk menambahkan bidang kustom ke kisi entri mingguan waktu:

  - Menyesuaikan tampilan dan menambahkan bidang kustom
  - Buat entri waktu kustom default baru 


**Menyesuaikan tampilan dan menambahkan bidang kustom**

Anda dapat menyesuaikan tampilan **entri waktu mingguan saya** dan menambahkan bidang kustom ke dalamnya. Anda dapat memilih posisi dan ukuran bidang kustom di kisi dengan mengedit properti tersebut dalam tampilan.

**Buat entri waktu kustom default baru** 

Tampilan ini harus berisi bidang **Deskripsi** dan **komentar eksternal**, selain kolom yang ingin Anda miliki di kisi. 

1. Pilih posisi, ukuran, dan urutan default kisi dengan mengedit properti tersebut dalam tampilan. 
2. Konfigurasikan kontrol kustom untuk tampilan ini sehingga merupakan kontrol **kisi entri waktu**. 
3. Tambahkan kontrol ini ke tampilan, dan pilih untuk web, ponsel, dan tablet. 
4. Konfigurasikan parameter untuk kisi entri mingguan waktu. Atur bidang **tanggal mulai** ke **msdyn_date**, atur bidang **durasi** menjadi **msdyn_duration**, dan atur bidang **status** menjadi **msdyn_entrystatus**. 
5. Untuk tampilan default, bidang **daftar status baca-saja** diatur ke **192350002,192350003,192350004**, bidang **aliran tugas Edit baris** diatur ke **msdyn_timeentryrowedit,** dan Bidang **Alur tugas Edit sel** diatur ke **msdyn_timeentryedit**. 
6. Anda dapat menyesuaikan bidang ini untuk menambahkan atau menghapus status baca-saja, atau menggunakan pengalaman berbasis tugas (TBX) yang berbeda untuk pengeditan baris atau sel. Bidang ini harus terikat ke nilai statis.


> [!NOTE] 
> Kedua pilihan akan menghilangkan beberapa filter bawaan pada entitas **proyek** dan **tugas proyek**, sehingga semua tampilan pencarian untuk entitas akan terlihat. Per default, hanya tampilan pencarian yang relevan yang dapat dilihat.
Anda harus menentukan alur tugas yang sesuai untuk bidang kustom. Kemungkinan besar, jika Anda menambahkan bidang ke kisi, harus masuk di alur Edit tugas baris yang digunakan untuk bidang yang berlaku untuk seluruh baris entri waktu. Jika bidang kustom memiliki nilai unik setiap hari, seperti bidang kustom untuk **waktu berakhir**, bidang tersebut harus masuk dalam alur tugas Edit sel.

Untuk menambahkan bidang kustom ke alur tugas, tarik elemen **bidang** ke posisi yang sesuai pada halaman, lalu Atur properti bidang. Atur properti **sumber** ke **entri waktu**, dan atur properti **bidang data** ke bidang kustom. Properti **bidang** menentukan nama tampilan pada halaman tbx. Pilih **Terapkan** untuk menyimpan perubahan ke bidang, lalu pilih **Perbarui** untuk menyimpan perubahan ke halaman.

Untuk menggunakan halaman TBX kustom baru, buat proses baru. Atur kategori ke **alur proses bisnis**, atur entri entitas ke **waktu**, dan atur jenis proses bisnis untuk **menjalankan proses sebagai alur tugas**. Dalam **properti**, properti **nama halaman** harus diatur ke nama tampilan halaman. Tambahkan semua bidang yang relevan ke halaman TBX. Simpan dan Aktifkan proses, lalu Perbarui properti kontrol kustom untuk alur tugas yang relevan dengan nilai **nama** pada proses.

### <a name="add-new-option-set-values"></a>Tambahkan Nilai Rangkaian Pilihan baru
Untuk menambahkan nilai rangkaian pilihan ke bidang siap pakai, buka halaman pengeditan untuk bidang, lalu di dalam **jenis**, pilih **Edit** di sebelah rangkaian pilihan. Selanjutnya, tambahkan pilihan baru yang memiliki label dan warna kustom. Jika Anda ingin menambahkan status entri waktu baru, bidang siap pakai diberi nama **status entri**, bukan **status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Menentukan status entri waktu baru sebagai hanya baca
Untuk menetapkan status entri waktu baru sebagai hanya baca, tambahkan nilai entri waktu baru ke properti **daftar status hanya baca**. Bagian diedit dari kisi entri waktu akan dikunci untuk baris yang memiliki status baru.
Selanjutnya, tambahkan aturan bisnis untuk mengunci semua bidang pada waktu halaman tbx **Edit baris entri waktu** dan **Edit entri waktu**. Anda dapat mengakses aturan bisnis untuk halaman ini dengan membuka editor alur proses bisnis untuk halaman, lalu memilih **aturan bisnis**. Anda dapat menambahkan status baru ke kondisi di aturan bisnis yang ada, atau Anda dapat menambahkan aturan bisnis baru untuk status baru.

### <a name="add-custom-validation-rules"></a>Tambahkan aturan validasi kustom
Ada dua jenis aturan validasi yang dapat Anda tambahkan untuk pengalaman entri kisi waktu mingguan:

- Aturan bisnis sisi klien yang berfungsi di kotak dialog buat cepat dan pada halaman TBX.
- Validasi plugin sisi server yang berlaku untuk semua pembaruan entri waktu.

#### <a name="business-rules"></a>Aturan bisnis
Gunakan aturan bisnis untuk mengunci dan membuka kunci bidang, masukkan nilai default di bidang, dan tentukan validasi yang memerlukan informasi hanya dari rekaman entri waktu saat ini. Anda dapat mengakses aturan bisnis untuk halaman TBX dengan membuka editor alur proses bisnis untuk halaman, lalu memilih **aturan bisnis**. Selanjutnya, Anda dapat mengedit aturan bisnis yang ada atau menambahkan aturan bisnis baru. Untuk validasi yang lebih disesuaikan, Anda dapat menggunakan aturan bisnis untuk menjalankan JavaScript.

#### <a name="plug-in-validations"></a>Validasi plug-in
Anda harus menggunakan validasi plug-in untuk validasi yang memerlukan konteks lebih daripada tersedia di rekaman entri satu kali, atau untuk validasi yang ingin Anda jalankan pada pembaruan inline di kisi. Untuk menyelesaikan validasi, buat plug-in kustom pada entitas **entri waktu**.
