---
title: Penerimaan dan biaya proyek
description: Topik ini menyediakan informasi tentang memperkirakan biaya proyek dan pendapatan.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e9d82a6c-0164-4177-838b-c34571be041c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3eb52d97fbd5df0364bc9a1a1ef11a0a0f7ee127
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752522"
---
# <a name="project-costs-and-revenue"></a>Penerimaan dan biaya proyek

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Perkiraan proyek memberikan tampilan keuangan untuk pekerjaan yang diperkirakan dan dijadwalkan pada jadwal proyek. Tab **Estimasi** pada halaman **proyek** menunjukkan dampak biaya dan pendapatan dari pekerjaan yang Anda rencanakan. Ia juga menyediakan informasi tentang banyak dimensi yang telah ditentukan. 

> ![tab Perkiraan](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Biaya dan nilai penjualan proyek

Daftar harga mendefinisikan biaya dan tarif tagihan untuk peran dalam proyek. Anda dapat menentukan dampak biaya dan pendapatan pekerjaan, berdasarkan peran yang terkait dengan nama posisi dan sumber daya bernama yang ditetapkan ke tugas. Jika ada tugas yang tidak memiliki tugas (generik atau bernama), Anda tidak dapat memperoleh perkiraan biaya atau penjualan. Nilai biaya dan penjualan mempertimbangkan tanggal yang ditentukan dalam daftar harga.

### <a name="default-cost-price"></a>Daftar Harga Default  

Setiap proyek adalah milik suatu organisasi. Organisasi ini ditampilkan di bidang **unit kontrak** dalam proyek. Daftar harga yang terkait dengan unit kontrak digunakan untuk menentukan harga biaya per unit. Untuk menentukan harga biaya yang benar pada peran untuk tanggal yang ditentukan pada baris perkiraan, cari kombinasi dari peran, unit dan unit organisasi dalam daftar harga biaya. 

Sehingga harga biayanya dapat dihitung, semua tugas harus ditetapkan ke sumber daya. Tugas yang tidak ditetapkan akan memiliki harga biaya 0,00.

Jika kombinasi peran, unit, dan unit organisasi tidak menghasilkan harga dari daftar harga unit kontrak, sistem akan mengabaikan unit. Sebaliknya, ia mencari kombinasi hanya peran dan unit organisasi. Jika ada harga biaya yang ditemukan, faktor konversi digunakan untuk mengonversinya ke unit yang Anda pilih pada baris perkiraan.

Jika kombinasi peran dan unit organisasi tidak menghasilkan harga biaya, sistem akan mengabaikan unit organisasi. Sebaliknya, ia mencari kombinasi peran dan unit untuk mengatur harga default (setelah konversi diterapkan).

Jika sistem tidak menemukan harga untuk peran, maka harga biaya pada baris perkiraan diatur dengan nilai default **0,00**. Semua biaya di jumlah baris perkiraan biaya proyek dicatat dalam mata uang unit kontrak.

> [!NOTE]
> Secara default, Microsoft Dynamics 365 menyimpan jumlah biaya dalam mata uang dasar Anda. Namun, jumlah biaya yang ditampilkan pada tab **perkiraan** berada dalam mata uang unit kontrak.  

### <a name="default-sales-price"></a>Harga Penjualan Default 

Daftar harga penjualan ditentukan baik oleh entitas penjualan yang terhubung ke proyek atau pelanggan proyek. Bila entitas penjualan, seperti peluang, kuotasi, atau kontrak, terkait dengan proyek, harga penjualan entitas penjualan ditentukan berdasarkan daftar harga yang terkait dengan kuotasi atau kontrak. Jika kuotasi atau kontrak memiliki daftar harga kustom, daftar harga ini digunakan sebagai harga penjualan default untuk perkiraan proyek. Jika tidak ada keterkaitan dengan entitas penjualan, daftar harga penjualan default dari parameter digunakan sebagai daftar harga penjualan default proyek yang disesuaikan dengan mata uang pelanggan yang ditentukan pada proyek.

Setiap baris perkiraan memiliki unit sumber daya yang terkait dengannya. Unit sumber daya menunjukkan unit organisasi yang menjadi asal pemesanan sumber daya untuk menyelesaikan tugas. Untuk menentukan harga penjualan untuk peran yang terkait, Cari kombinasi unit peran, unit, dan sumber daya dalam daftar harga penjualan. Jika tidak ada penetapan pada tugas, harga penjualan untuk tugas adalah 0,00.

Jika kombinasi peran, unit, dan unit sumber daya tidak menghasilkan harga penjualan dari daftar harga penjualan, sistem akan mengabaikan unit. Sebaliknya, ia mencari kombinasi hanya peran dan unit sumber daya. Jika ada harga penjualan yang ditemukan, faktor konversi digunakan untuk mengonversinya ke unit yang Anda pilih pada baris perkiraan penjualan. 

Jika kombinasi peran dan unit sumber daya tidak menghasilkan harga penjualan dari daftar harga penjualan, sistem akan mengabaikan unit sumber daya. Sebaliknya, ia mencari kombinasi peran dan unit untuk mengatur harga default (setelah konversi diterapkan).

Jika sistem tidak menemukan harga untuk peran, maka harga penjualan pada baris perkiraan diatur dengan nilai default **0,00**.

Tab **perkiraan** memiliki tampilan kisi yang menampilkan baris perkiraan. Kisi mencakup kolom untuk unit, harga biaya total, dan harga penjualan total, seperti ditunjukkan dalam ilustrasi berikut. 

> ![Tampilan kisi pada tab perkiraan](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Tampilan bertahap waktu dari estimasi proyek

Tampilan bertahap waktu perkiraan proyek menunjukkan perkiraan data dari tampilan kisi di seluruh Timeline, dalam skala waktu yang Anda pilih. Secara default, data perkiraan berpusat pada dimensi **peran**.

> ![Tampilan bertahap waktu untuk estimasi proyek](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Mengalokasikan estimasi upaya berdasarkan mode tugas

Di tampilan bertahap waktu, Anda mendistribusikan usaha total yang diperkirakan untuk tugas dengan mengalokasikan jam upaya per unit periode waktu dalam skala waktu pilihan. Modus tugas menentukan bagaimana upaya dialokasikan di masa tugas. Dua jenis alokasi adalah alokasi **merata** dan **berdasarkan jam kerja**.

### <a name="work-hours-based-allocation"></a>Jam kerja berbasis alokasi
 
Dalam mode tugas penjadwalan otomatis, jam default harian untuk sumber daya tugas ditetapkan pada tingkat jam kerja penuh. Perilaku ini berlaku ketika upaya dialokasikan dengan memisahkan seluruh durasi tugas dalam tampilan bertahap waktu. Misalnya, jika Anda memperkirakan bahwa tugas akan selesai pada satu sumber daya dalam skala waktu **Hari**, upaya yang dialokasikan setiap hari tidak akan melebihi jam kerja per hari yang didefinisikan dalam kalender proyek. Oleh karena itu, alokasi usaha selalu memastikan bahwa sumber daya diperkirakan untuk dimanfaatkan untuk sehari penuh.

### <a name="even-allocation"></a>Alokasi merata

Dalam mode tugas yang dijadwalkan secara manual, jam kerja dari kalender proyek tidak digunakan. Sebaliknya, Jadwal tugas didasarkan pada input pengguna. Untuk tugas tersebut, alokasi upaya per unit jangka waktu skala waktu pilihan tidak memiliki faktor pembatas apapun. Upaya total pada tugas dipecah dan dialokasikan dengan sama untuk masing-masing unit jangka waktu pada skala waktu pilihan. Dengan demikian, modus tugas yang didefinisikan pada tugas menentukan distribusi usaha atau alokasi usaha per unit jangka waktu di perkiraan bertahap waktu.

## <a name="grouping-and-time-phasing-options"></a>Pengelompokan dan opsi pentahapan waktu

Tampilan bertahap waktu menampilkan distribusi usaha, biaya, dan perkiraan penjualan pada per hari, Mingguan, bulanan, atau tahunan. Secara default, data perkiraan berpusat pada dimensi **peran**. Namun, Anda dapat menggunakan pilihan **kelompokkan berdasarkan** untuk berporos pada dua dimensi lain: **kategori** dan **sumberdaya**.

Di tampilan kisi dan tampilan berdasar waktu, Anda dapat memilih bidang yang akan ditampilkan. Total untuk setiap blok waktu ditampilkan di bagian bawah proyek. Mereka menunjukkan Total perkiraan upaya, biaya, dan penjualan untuk hari, Minggu, bulan, atau tahun. Harga penjualan dan harga biaya default adalah efektif tanggal. Dengan kata lain, perubahan untuk setiap sumber daya, berdasarkan tampilan bertahap waktu yang Anda pilih.

## <a name="expense-estimates"></a>Perkiraan pengeluaran

Tombol **Tambah perkiraan biaya baru** di tampilan kisi memungkinkan Anda merekam setiap pengeluaran yang terjadi dalam proyek, namun yang tidak terkait langsung dengan tenaga kerja. Anda dapat merekam perkiraan pengeluaran untuk tugas tertentu atau untuk seluruh proyek. Pilih kategori pengeluaran dan tanggal tentatif bila Anda memperkirakan akan dikenakan biaya. Jika harga biaya yang terkait dan daftar harga penjualan memiliki harga default (atau persentase markup yang didefinisikan untuk kategori pengeluaran) mereka otomatis dimasukkan pada baris perkiraan saat asosiasi terjadi.
