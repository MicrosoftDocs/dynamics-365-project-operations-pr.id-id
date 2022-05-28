---
title: Buat estimasi penjualan dan biaya proyek apabila sumber daya yang dapat dipesan mengisi beberapa peran pada suatu proyek
description: Topik ini menjelaskan cara menggunakan dimensi harga untuk mendukung estimasi harga dan biaya untuk sumber daya yang mengisi beberapa peran pada satu proyek.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2cc632d43bfcbdd23c1d06ff5203385bccf9926d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589154"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Buat estimasi penjualan dan biaya proyek apabila sumber daya yang dapat dipesan mengisi beberapa peran pada suatu proyek 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite - menangani faktur proforma, dan Project Operations untuk skenario berbasis stok/produksi_ 

Perusahaan berbasis proyek sering memiliki kebutuhan akan satu sumber daya untuk mengisi beberapa peran dalam suatu proyek. Setiap peran dapat memiliki harga dan diatur dengan cara yang berbeda. Ini berarti bahwa waktu sumber daya yang sama pada satu proyek dapat memperoleh estimasi keuangan yang berbeda tergantung pada tarif biaya dan tagihan untuk setiap peran. Anda dapat mengonfigurasikan nilai pada record anggota tim untuk sumber daya yang diberi nama dengan penimpaan berbeda pada setiap tugas yang ditetapkan oleh anggota tim.

Contoh berikut memandu Anda mudahnya penimpaan sederhana suatu nilai memungkinkan sumber daya untuk memiliki beberapa peran pada satu proyek dengan tarif tagihan dan biaya yang berbeda.

## <a name="create-tasks"></a>Membuat tugas
Untuk membuat tugas, Anda harus menambahkan tugas, serta tugas rangkuman, setelah itu Anda harus menetapkan tugas sebelum menambahkan durasi tugas. 

### <a name="add-tasks-and-summary-tasks"></a>Menambahkan tugas dan tugas rangkuman
Untuk menambahkan tugas, lakukan langkah-langkah berikut:

1. Buka **Proyek** dan buka proyek yang ingin Anda tambahi tugas.
2. Pilih **Tambahkan tugas baru**. Namai tugas, lalu tekan **Enter**.
3. Masukkan nama tugas lainnya, lalu tekan **Enter**. Ulangi langkah ini hingga Anda memiliki daftar lengkap tugas.
3. Untuk membuat indentasi tugas di dalam tugas **Rangkuman**, pilih tiga titik vertikal sesuai nama tugas, lalu pilih **Buat Subtugas**. 

  > [!TIP]
  > Untuk memilih lebih dari satu tugas, pilih tugas, tekan dan tahan **Ctrl**, lalu pilih tugas lain.
  >
  > Anda juga dapat memilih **Promosikan subtugas** untuk memindahkan tugas dari dalam tugas **Rangkuman**.

### <a name="assign-tasks"></a>Menetapkan tugas

Lakukan langkah-langkah berikut untuk menetapkan tugas.

1. Di kolom **Tetapkan ke** untuk suatu tugas, pilih ikon orang.
2. Pilih anggota tim dari daftar atau masukkan teks untuk mencari nama.

### <a name="add-task-duration-and-columns"></a>Menambahkan durasi dan kolom tugas

Sering kali paling mudah untuk mulai membangun proyek Anda dengan durasi. Lakukan langkah-langkah berikut untuk menambahkan durasi tugas.

1. Di kolom **Durasi** untuk tugas, ketik jumlah hari yang mungkin diperlukan untuk menyelesaikan tugas. Jika Anda ingin menggunakan satuan waktu yang berbeda, masukkan angka ditambah kata **jam**, **minggu**, atau **bulan**.
2. Jika Anda ingin tugas Anda muncul sebagai tonggak pencapaian berbentuk berlian pada tampilan **Garis waktu**, di kolom **Durasi**, masukkan **0 hari**.
3. Tekan **Enter** untuk membuka bidang **Durasi** tugas berikutnya, dan lanjutkan memasukkan durasi.

  > [!NOTE]
  > Anda tidak dapat memasukkan durasi untuk tugas rangkuman.

Anda dapat menambahkan kolom ke proyek Anda untuk memberikan rincian lebih lanjut. Untuk melakukannya, pilih **Tambah kolom**. 

Untuk informasi lebih lanjut, lihat [Membuat proyek](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Mengonfigurasikan peran dan unit organisasi untuk anggota tim proyek yang umum
Lakukan langkah-langkah berikut untuk mengonfigurasi peran dan unit organisasi untuk anggota tim yang umum.

1. Pada halaman **Tugas**, pilih baris **Tugas** untuk **Tugas A**. 
2. Di **Ditetapkan Ke**, pilih **Tambah sumber daya umum**. Tindakan ini akan membuka halaman **Buat Cepat Anggota Tim**.
3. Pada halaman **Buat cepat anggota tim**, tentukan atribut anggota tim umum yang dapat melakukan tugas ini.
4. Pilih peran dan unit organisasi yang sesuai, lalu pilih **Simpan dan tutup**. Anggota tim umum dibuat dan ditetapkan ke tugas ini. 
5. Ulangi langkah 1-4 untuk **Tugas B**. Namun, **Tugas B** harus memiliki peran dan unit organisasi yang berbeda yang ditetapkan untuk anggota tim umum dibandingkan **Tugas A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Mengonfigurasikan peran dan unit organisasi untuk tugas proyek
Lakukan langkah-langkah berikut untuk mengonfigurasi peran dan unit organisasi untuk satu tugas.

1. Setelah Anda membuat **Tugas A**, pilih tugas, lalu pilih ikon **i** untuk membuka panel **Rincian Tugas**. 
2. Di panel **Rincian Tugas**, gulir ke bawah, lalu pilih **Rincian Tampilan** untuk membuka halaman **Rincian Tugas**.
3. Pada halaman **Rincian Tugas**, dalam **Peran** dan **Unit Organisasi**, tambahkan nilai yang akan diperlukan oleh sumber daya untuk melakukan tugas ini. 

  > [!NOTE]
  > Jika Anda menyelesaikan skenario ini menggunakan data demo Project Operations, pilih **Prospek Konsultasi** untuk peran, dan **Fabrikam US** sebagai unit organisasi.

4. Pilih **Tugas B** , dan kemudian pilih tugas.
5. Pilih ikon **i** untuk membuka panel **Rincian Tugas**. 
6. Di panel **Rincian Tugas**, gulir ke bawah, lalu pilih **Rincian tampilan** untuk membuka halaman **Rincian Tugas**.
7. Pada halaman **Rincian Tugas**, dalam **Peran** dan **Unit Organisasi**, tambahkan nilai yang diperlukan sumber daya untuk melakukan tugas ini. Nilai dalam **Peran** dan **Unit Organisasi** untuk **Tugas B** harus berbeda dengan yang digunakan untuk **Tugas A**. 

  > [!NOTE]
  > Jika Anda menyelesaikan skenario ini menggunakan data demo Project Operations, pilih **Teknisi Jaringan** untuk peran, dan **Fabrikam US** sebagai unit organisasi.

8. Simpan dan tutup halaman **Rincian Tugas**. 

## <a name="team-member-and-estimates-behavior"></a>Anggota tim dan estimasi perilaku 
Untuk memahami perilaku pada kisi **Anggota Tim** dan estimasi, lakukan langkah-langkah berikut.

1. Di kisi **Anggota Tim**, pilih dua anggota tim umum, lalu pilih **Buat Persyaratan**. Ini akan membuat persyaratan sumber daya. 
2. Pilih baris anggota tim untuk **Prospek Konsultasi**, lalu pilih **Pesan**. Papan jadwal terbuka dengan daftar sumber daya. Pilih sumber daya, lalu pilih **Pesan** untuk memesan sumber daya untuk persyaratan tersebut.
3. Pilih baris anggota tim untuk **Teknisi Jaringan**, lalu pilih **Pesan**. Papan jadwal terbuka dengan daftar sumber daya. Pilih sumber daya yang sama seperti di atas, lalu pilih **Pesan** untuk memesan sumber daya untuk persyaratan tersebut.

### <a name="team-member-grid"></a>Kisi anggota tim 

Di kisi **Anggota Tim**, dua record anggota tim umum akan dihapus dan diganti dengan hanya satu sumber daya. Terdapat satu kumpulan nilai untuk sumber daya tersebut, yang merupakan kumpulan nilai default untuk **Peran** dan **Unit Organisasi**.

Saat Anda memperluas baris untuk record anggota tim tersebut, Anda dapat melihat tugas yang berbeda pada record anggota tim untuk kedua tugas. Setiap baris tugas memiliki nilai spesifik tugas untuk **Peran** dan **Unit Organisasi**. 

### <a name="estimates-grid"></a>Kisi Perkiraan 

Di kiri **Estimasi**, kedua tugas untuk sumber daya yang sama memiliki harga berbeda. Tugas untuk sumber daya pada **Tugas A** dihargai menggunakan nilai atribut **Peran** dari **Prospek Konsultasi**. Tugas untuk sumber daya yang sama pada **Tugas B** dihargai menggunakan nilai atribut **Peran** dari **Teknisi Jaringan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]