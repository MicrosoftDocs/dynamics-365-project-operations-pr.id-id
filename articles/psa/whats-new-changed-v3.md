---
title: Yang baru atau yang diubah di Project Service Automation versi 3
description: Topik ini menyediakan informasi tentang apa yang baru dan diubah dalam Project Service Automation versi 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 15925cb88cc413f9a23a25e89ddd29668e9171de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581656"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Yang baru atau yang diubah di Project Service Automation versi 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



Topik ini menyediakan informasi tentang perubahan ke antarmuka pengguna (UI), fungsi, dan terminologi di Project Service Automation antara versi 2 atau versi 1 dan versi 3.

## <a name="project-scheduling"></a>Penjadwalan proyek
Jadwal proyek, yang dikenal sebagai struktur rincian kerja (WBS) di versi sebelumnya, telah diubah namanya menjadi Jadwal dan diakses dengan mengklik tab **Jadwal**. 

![Jadwal proyek.](media/psa-schedule-01.png)

Jadwal sekarang memiliki permukaan baru untuk interaksi yang modern dan dapat diakses. Namun, Mesin penjadwalan Project Service Automation yang mendasari tidak berubah. Tombol kontrol di pita jadwal kisi memungkinkan Anda berinteraksi dengan jadwal yang serupa dengan versi Project Service Automation sebelumnya. Perubahan tambahan terhadap jadwal mencakup:

- **Diagram Gantt** - diagram Gantt tidak lagi ada. Visualisasi Gannt baru akan kembali di pembaruan mendatang.
- **Header kolom** - Anda dapat menyembunyikan header kolom di kisi dengan mengeklik indikator turun di sebelah judul kolom. 
- **Kolom** -Anda dapat menampilkan kolom tersembunyi dengan mengklik **Tambah kolom**. 
- **Kategori transaksi** - pencarian **kategori transaksi** telah ditambahkan ke kisi jadwal dan ditampilkan secara default. 
 
## <a name="project-templates"></a>Template Proyek
Perubahan berikut telah dibuat untuk fungsionalitas template proyek.

### <a name="create-a-project-template"></a>Buat Template Proyek 
Anda dapat membuat template proyek dalam versi 3 yang serupa dengan versi sebelumnya dari Project Service Automation. Template dapat berisi hanya jadwal dan jadwal dapat mencakup tugas, namun tidak diperlukan. Jika jadwal memiliki tugas, mereka hanya dapat digunakan untuk sumber daya generik. Anda dapat membuat persyaratan sumber daya untuk sumber daya generik, namun tidak dapat dipesan dengan sumber daya nyata dalam template. Anda tidak dapat memesan sumber daya nyata ke tim dalam template. 

### <a name="create-a-template-from-an-existing-template"></a>Membuat template dari template yang ada
Bila Anda membuat template proyek baru dari template yang ada di Project Service Automation versi 3, hal berikut terjadi: 

- Jadwal proyek sumber disalin ke template. 
- Sumber daya generik disalin ke tim dan tugas Sumber daya generik disalin di atasnya. Persyaratan untuk sumber daya generik tidak disalin. 

### <a name="create-a-template-from-an-existing-project"></a>Membuat template dari proyek yang ada
Bila Anda membuat template proyek baru dari proyek yang ada, hal berikut terjadi: 

- Jadwal proyek sumber disalin ke template. 
- Sumber daya generik disalin ke tim dan tugas Sumber daya generik dipertahankan. Persyaratan untuk sumber daya generik tidak disalin.    
- Sumber daya bernama, baik yang ditetapkan maupun tidak ditetapkan akan dihapus dari tim dan digantikan dengan sumber daya generik.
- Jika ada, informasi pelanggan akan dihapus. 
- Jika ada, referensi ke kuotasi dan kontrak akan dihapus. 

### <a name="create-a-project-from-a-template"></a>Buat Proyek dari Template
Di Project Service Automation versi 3, Bila Anda membuat proyek proyek baru dari template, hal berikut terjadi:

- Jadwal, tim, dan tugas disalin ke proyek baru.   
- Tanggal mulai adalah tanggal penyalinan atau tanggal yang dipilih oleh pengguna.   
- Untuk setiap anggota tim generik yang memiliki persyaratan sumber daya dalam template, persyaratan tidak disalin atau dibuat secara otomatis. Anda akan perlu membuat mereka. 

## <a name="copy-a-project"></a>Salin Proyek
Di Project Service Automation versi 3, Bila Anda membuat menyalin proyek, hal berikut terjadi: 

- Perkiraan tanggal mulai disalin, namun dapat diubah.  
- Jadwal dan tugas proyek disalin. 
- Sumber daya generik dan tugas mereka disalin. Persyaratan sumber daya untuk sumber daya generik tidak disalin. Anda akan perlu membuat kembali mereka. 
- Sumber daya riil dan tugas mereka tidak disalin. Namun, mereka akan digantikan oleh sumber daya generik. 
- Aktual tidak disalin ke proyek baru. 

## <a name="move-a-scheduled-project"></a>Memindahkan proyek terjadwal
Saat Anda memindahkan jadwal proyek yang ada ke depan, terjadi hal berikut: 

- Tanggal tugas secara otomatis akan dipindahkan agar sesuai dengan periode pergerakan. 
- Sumber daya umum yang ditetapkan tetap ditetapkan.   
- Jika dihasilkan sebelum proyek dipindah, persyaratan untuk sumber daya generik tetap sama, dan tidak dibuat ulang secara otomatis. Anda akan perlu membuat mereka lagi untuk mencerminkan penugasan baru karena pergerakan tugas. 
- Tugas pada sumber daya nyata akan berubah sesuai dengan pergerakan tanggal tugas. Pemesanan pada sumber daya nyata tidak berubah. Anda harus memodifikasi Pemesanan menggunakan tampilan rekonsiliasi. 
- Sumber daya tim dengan Pemesanan namun tidak ada penugasan tidak berubah. 
- Aktual tidak dipindahkan. 

## <a name="estimates"></a>Perkiraan
Perkiraan telah dipecah menjadi dua tab, **penetapan sumber daya**, dan **perkiraan**. Tab **penetapan sumber daya** berisi perkiraan upaya dan menampilkan penetapan sumber daya untuk tugas dalam tampilan yang berfase waktu. Anda dapat mengedit perkiraan berdasarkan apa yang dihasilkan mesin penjadwalan.

![Tugas sumber daya yang menunjukkan perkiraan upaya dan tugas sumber daya untuk tugas.](media/resource-assignments-tab-02.png)

Tab **perkiraan** menunjukkan biaya dan jumlah penjualan untuk tugas sumber daya. Jumlah bersifat hanya baca. Harga dan harga penjualan sekarang didorong dari tugas anggota tim pada jadwal. Ini berarti bahwa jika Anda memiliki tugas tanpa penetapan, tugas akan ditampilkan dalam keranjang belum ditetapkan. Ini juga berarti bahwa tanpa **peran**, yang merupakan dimensi harga default, tidak akan ada perkiraan biaya atau penjualan jika Anda memiliki pelanggan atau kontrak/kuotasi yang terkait dengan proyek. 

![Tab perkiraan menunjukkan biaya dan jumlah penjualan.](media/estimates-tab-03.png)
  
Kategori juga didukung pada tugas di tampilan jadwal. Pengelompokan berdasarkan Kategori pada tampilan berdasar waktu dari perkiraan akan memberikan pengalaman yang lebih baik, terutama bila Anda juga memiliki perkiraan pengeluaran dalam proyek Anda. Perkiraan pengeluaran dimasukkan menggunakan kisi pada tab terpisah. 

Perkiraan biaya dapat dimasukkan di kisi pada tab **Perkiraan pengeluaran**. 

![Tab perkiraan pengeluaran menampilkan kisi perkiraan pengeluaran.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Manajemen sumber daya
Dalam Project Service Automation versi 3, dengan UI klien terpadu baru dan perubahan pada hubungan antara Pemesanan dan tugas, staf proyek dengan sumber daya generik atau nyata telah berubah secara dramatis dari versi 2 dan versi 1. Namun, konsep sumber daya yang dapat dipesan, baik **Real** maupun **generik** tetap sama, seperti anggota tim, persyaratan, tugas, dan Pemesanan.   

![Menggunakan Pengambil sumber daya.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Menetapkan sumber daya nyata yang dapat dipesan 
Di Project Service Automation versi 3, Pemesanan dan penetapan tugas tidak terkait erat seperti di versi sebelumnya dari Project Service Automation. Anda dapat menggunakan kisi tim untuk memesan anggota tim **sungguhan**, mirip dengan di dalam pasar.

Menggunakan pemilih sumber daya pada jadwal, Anda dapat memilih anggota tim yang dibuat di tampilan tim, lalu menetapkannya ke tugas. Anda dapat terus menetapkan tugas kepada mereka, bahkan melewati Pemesanan. Gunakan tab **rekonsiliasi** untuk merekonsiliasi anggota tim yang memiliki perbedaan dalam pemesanan dan tugas.

Pemilih sumber daya akan menampilkan anggota tim untuk proyek. Anda juga dapat menggunakan pemilih sumber daya untuk mencari dan melihat sumber daya memulai yang dapat dipesan yang belum menjadi bagian dari tim proyek. Anda dapat menetapkannya ke tugas dan mereka akan menjadi bagian dari tim proyek. Anda akan perlu memesan mereka menggunakan **papan jadwal** atau tab **rekonsiliasi**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Tetapkan sumber daya generik yang dapat dipesan pada tim tugas dan proyek, lalu penuhi dengan sumber daya nyata melalui papan jadwal 
Dalam Project Service Automation versi 3, fungsi Buat tim tidak digunakan untuk sumber daya generik. Namun, Anda dapat membuat dan langsung menetapkan sumber daya generik dari jadwal dengan mengetikkan nama posisi sumber daya generik di sel sumber daya dari jadwal. Atau, Anda dapat memilih ikon sumber daya di sel kemudian menggunakan pemilih sumber daya, ketikkan nama sumber daya umum yang ingin Anda buat. Ini akan membuka panel pembuatan cepat yang memungkinkan Anda mengatur peran dan unit organisasi anggota tim sumber daya generik. Setelah Anda membuat sumber daya, maka ditetapkan ke tugas dan Anda dapat terus menetapkan sumber daya generik ke tugas lain dalam jadwal.    
 
Bila Anda telah menetapkan sumber daya ke semua tugas yang sesuai, Anda dapat membuat persyaratan sumber daya, lalu memenuhinya dengan melakukan pemesanan langsung dengan **papan jadwal** atau dengan mengajukan permintaan sumber daya. Anda juga dapat menambahkan sumber daya generik langsung ke kisi anggota tim. 

Sumber daya umum ditambahkan ke tim proyek tanpa persyaratan sumber daya dan dengan tanggal mulai/akhir proyek hingga persyaratan sumber daya dibuat. Untuk membuat persyaratan, pilih sumber daya generik, lalu klik **buat**. Tautan persyaratan sekarang ditampilkan dan jam yang diperlukan akan diisi dengan jam yang ditetapkan. Anda dapat mengeklik tautan untuk membuka dan memperbarui persyaratan.
  
Bila Pemesanan selesai dan sepenuhnya terpenuhi dengan sumber daya bernama, maka sumber daya generik akan digantikan dengan sumber daya bernama, dan tugas pada jadwal akan diperbarui dengan sumber daya bernama. 

Sumber daya yang diusulkan untuk persyaratan sekarang disimpan di tab, bukan bagian terpisah.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Pemenuhan sumber daya generik dengan beberapa sumber daya bernama
Bila persyaratan terpenuhi dengan beberapa sumber daya, sumber daya generik tetap berada di tim dan ditetapkan ke tugas. Anggota tim yang bernama yang dipesan tidak ditetapkan sebagai bagian dari posisi. Manajer proyek dapat menetapkan pekerjaan yang dibutuhkan dengan sumber daya riil.  Tampilan **rekonsiliasi** memberikan uraian Pemesanan di beberapa sumber daya menjadi ke beberapa penetapan tugas. Hal ini tidak dilakukan secara otomatis karena dalam skenario yang lebih rumit, seperti di mana Anda memiliki bundel tugas yang membuat persyaratan, maksud dari bagaimana manajer proyek ingin menugaskan, harus diasumsikan. Karena sistem tidak dapat memahami maksud, kemungkinannya adalah asumsi cenderung akan berbeda dari yang dimaksudkan dan hasil yang tidak tepat atau tidak terduga akan terjadi. Hasil yang dapat diprediksi adalah bahwa sumber daya generik tetap ditugaskan hingga manajer proyek dengan sengaja menetapkan sumber daya dengan menggunakan tampilan **rekonsiliasi**.

### <a name="reconciliation"></a>Rekonsiliasi
Tab **Rekonsiliasi** menampilkan Pemesanan dan semua tugas untuk setiap anggota tim proyek. Tampilan ini menunjukkan sel mana yang menunjukkan titik dari bulan ke hari. Tampilan ini membantu manajer proyek merekonsiliasi Pemesanan anggota tim dan tugas mereka untuk tim proyek mereka. Hal ini berguna karena Pemesanan dan penugasan tugas tidak digabungkan dengan erat, sehingga dapat lebih fleksibel saat merencanakan proyek. 

![Tab Rekonsiliasi menampilkan Pemesanan dan semua tugas untuk anggota tim proyek.](media/resource-reconciliation-tab-06.png)

Untuk setiap sumber daya, tampilan akan mengambil perbedaan antara Pemesanan anggota tim dan Rollup penetapan tugas mereka dan menampilkan dua perbedaan berikut yang dapat terjadi dengan Pemesanan dan penetapan dalam proyek: 

- **Kekurangan Pemesanan** – kekurangan Pemesanan terjadi bila sumber daya memiliki lebih banyak tugas daripada Pemesanan. Karena kapasitas ini belum dicadangkan, manajer proyek dapat memperbaiki ini dengan memperluas Pemesanan sumber daya untuk mengatasi kekurangan. 
- **Pemesanan berlebih** – kelebihan Pemesanan terjadi saat sumber daya telah dipesan ke proyek namun belum ditetapkan ke tugas.  Ini mungkin kejadian yang dapat diterima jika, misalnya, sumber daya telah dipesan sebelum penetapan tugas terjadi. Namun dalam kasus lain, sumber daya mungkin tidak direncanakan untuk ditetapkan, dan PM harus mempertimbangkan membatalkan pemesanan sumber daya untuk memungkinkan kapasitas yang akan digunakan untuk proyek lain. 

Ketika Anda memiliki penetapan tugas untuk sumber daya, namun tidak ada pemesanan (kekurangan pemesanan), Anda dapat memilih agregat kekurangan pemesanan itu, lalu klik **Perluas Pemesanan**. Dari sini, Anda dapat melihat Pemesanan yang diperlukan untuk menangani kekurangan sumber daya dan ketersediaan mereka. 
 
## <a name="time-and-expense"></a>Waktu dan Pengeluaran
Bagian ini menyediakan informasi tentang perubahan waktu, pengeluaran, dan persetujuan dalam versi 3 dari Project Service Automation. Sebagai bagian dari solusi Dynamics 365 Project Service Automation, fitur **entri waktu** telah diperbarui untuk meningkatkan kerangka Antarmuka Terpadu. Ini memungkinkan hadirnya antarmuka pengguna yang konsisten dan seragam yang mengikuti desain responsif untuk tampilan optimal pada ukuran layar atau perangkat apa pun. 

### <a name="landing-page"></a>Halaman arahan
Pengalaman entri waktu kustom yang tidak dapat diperluas telah ditolak dalam versi 3. Namun, sekarang ada pengalaman kisi asli yang dapat diperluas dan dapat diakses. Anda dapat mengakses fungsi entri waktu menggunakan peta situs di sebelah kiri. Dengan perubahan ini, Anda tidak akan lagi dapat memasukkan waktu selama satu minggu pada satu waktu. Namun, Anda harus membuat entri waktu untuk setiap hari di kisi. Setelah beberapa entri waktu dibuat, pengguna dapat massal membuat entri waktu dengan fungsi **salin** yang dijelaskan nanti di topik ini. 

![halaman arahan entri waktu.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Buat entri waktu baru 
Klik **baru** di pita untuk membuka halaman Buat cepat untuk entri waktu yang memungkinkan Anda memasukkan durasi dalam menit, jam, atau hari. Untuk melakukan ini, cukup mulai mengetik h, m, atau d bersama dengan kuantitas.  

![Pembuatan Cepat Entri Waktu.](media/quick-create-time-entry-08.png)

Bidang pencarian didukung oleh tampilan sistem. Misalnya, setelah Anda memasukkan informasi proyek, bidang **tugas proyek** diatur secara default ke tampilan **tugas proyek yang terbuka**. Untuk membuat entri waktu untuk tugas yang tidak ditetapkan ke pengguna, klik **Ubah tampilan** di pencarian, lalu pilih **semua tugas proyek aktif**. Setelah entri waktu dibuat dan ditampilkan di kisi, Anda dapat mengedit nilai baris apa pun secara langsung di kisi.  

### <a name="bulk-createcopy"></a>Buat/Salin massal 
Setelah beberapa entri waktu dibuat, Anda dapat menggunakan fungsi salin untuk membuat entri waktu tambahan secara massal. Klik **Salin** untuk membuka dialog **salin**. Di **dari periode: tanggal mulai**, atur rentang tanggal periode waktu yang harus disalin. Di **hingga periode: tanggal mulai**, tentukan tanggal saat entri waktu harus dibuat. Klik **Salin** untuk menyalin entri waktu ke hari yang sesuai dalam minggu yang ditunjukkan dalam **hingga periode**. Misalnya, entri waktu Senin dari pekan lalu akan disalin ke hari Senin dalam pekan yang ditentukan sebagai **hingga periode**. 

![Salin entri Waktu secara massal.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Impor data 
Tugas dan pertukaran mengikuti pola UI yang sama, yang memungkinkan pengguna menentukan rentang tanggal dari waktu saat pemesanan harus diimpor. Kemudian Anda harus secara eksplisit memilih Pemesanan yang akan disalin ke dalam entri waktu **draf**. Di versi 3, Anda tidak dapat lagi melihat pola entri waktu yang **disarankan** di kisi dan kalender.  

### <a name="change-in-calendar-control"></a>Perubahan di kontrol kalender
Di versi 3, kami telah beralih dari kontrol kalender kustom dan sekarang menggunakan kalender UC untuk menampilkan entri waktu selama seminggu. Dengan kalender ini, Anda dapat melihat hari, Minggu, dan bulan. 

> [!NOTE]
> Pembatasan kalender adalah bahwa kontrol ini tidak mendukung tindakan pada item kalender individual. Misalnya, Anda tidak akan dapat memilih satu item kalender atau lebih dan mengirimkan atau menghapus item tersebut. Mengklik item kalender akan membuka halaman **entitas entri waktu** untuk tindakan tambahan. 

### <a name="extensibility"></a>Ekstensibilitas
**Mengambil data di bidang kustom dalam entitas entri waktu dan pengeluaran saja** -entri waktu menggunakan kisi yang dapat diedit, kisi hanya baca, dan kontrol kalender dari platform. Semua kontrol ini adalah bawaan dan oleh karena itu akan mendukung penyesuaian. Dalam Project Service Automation versi 3, Anda dapat menambahkan bidang kustom tambahan, mengkonfigurasi bidang pencarian, dan mencadangkan dengan tampilan kustom. Anda juga dapat mengatur logika bisnis kustom berdasarkan nilai yang dipilih di bidang kustom.  

**Tangkap data di bidang kustom dalam entri waktu dan pengeluaran dan lakukan propagasi melalui entitas yang mendukung alur pengajuan dan persetujuan** -pemrosesan umum waktu entri ditunjukkan dalam diagram berikut.

![Proses Alur entri waktu.](media/process-time-entries-10.png)

Jika persyaratan bisnis menetapkan bahwa entitas waktu dan pengeluaran harus mengambil dimensi harga kustom dan menyebarkan nilai yang diatur berdasarkan sumber daya waktu dan memasukkan sumber daya dalam dimensi harga kustom melalui semua entitas di grafik sebelumnya, lihat [Konfigurasikan bidang kustom sebagai dimensi harga](set-up-pricing-dimensions.md)

Untuk mendukung persyaratan bisnis di mana entitas waktu dan biaya harus mengambil dimensi non-harga kustom dan menyebarkan nilai, Anda dapat menggunakan konfigurasi dimensi harga dan mengekspresikan dimensi kustom sebagai dimensi harga tanpa biaya atau tingkat tagihan. Skenario lain adalah menambahkan bidang kustom untuk setiap entitas, menggunakan nama bidang yang sama di semua entitas. Plug-in kustom dapat dibuat untuk mengaitkan rekaman di entitas yang berpartisipasi dalam alur pengiriman/persetujuan menggunakan entitas asal transaksi dan sambungan transaksi.  

### <a name="delegate-time-and-expense-entry"></a>Delegasi waktu dan entri pengeluaran
Platform Common Data Service tidak mendukung satu pengguna menyamar sebagai orang lain, yang berarti dalam versi 3 dari Project Service Automation tidak ada dukungan untuk delegasi waktu dan entri pengeluaran. Namun, mitra dan pelanggan telah memanfaatkan solusi untuk mengaktifkan dukungan untuk pengalaman delegasi entri waktu dalam versi 3. Ini hanya solusi dan bukan solusi lengkap, sehingga penting untuk memahami keterbatasan dan hanya menggunakan pendekatan ini jika keterbatasan dapat diterima. 

> [!IMPORTANT]
> Informasi ini hanya dapat dianggap sebagai panduan yang disarankan untuk penerapan kustom oleh mitra/pelanggan. Tim produk tidak akan menawarkan dukungan formal untuk fungsionalitas ini melalui saluran dukungan kami.

### <a name="customization-details"></a>Rincian Penyesuaian 
Penyesuaian memungkinkan Anda menambahkan **sumber daya yang dapat dipesan** ke pengalaman buat dan edit, yang akan memungkinkan pengguna bertindak sebagai delegasi dengan mengubah bidang **Pemesanan sumber daya** ke pengguna lain yang waktu dan entri pengeluarannya harus direkam. Langkah-langkah berikut ini mencakup delegasi entri waktu. Informasi yang sama berlaku untuk delegasi entri pengeluaran. 
 
1.  Pastikan bahwa pengguna yang didelegasikan memiliki akses keamanan global pada tugas proyek dan proyek. 
1.  Karena **sumber daya yang dapat dipesan**, yang merupakan bidang pada entitas **entri waktu**, tidak terpapar pada halaman **buat cepat**, Anda harus menambahkannya.

    -atau-

    Buat tampilan kustom, yang mencakup kolom **sumber daya yang dapat dipesan**, untuk hanya menampilkan entri waktu yang dibuat untuk sumber daya. Publikasikan penyesuaian pada desainer modul aplikasi untuk tampilan ini untuk menampilkan **pemilih tampilan** di halaman **entri waktu**. Ada dua plug-in yang menangani pengaturan manajer untuk entri waktu non-proyek:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Buat plug-in baru untuk menimpa bidang **manajer** ke manajer pengguna yang ditetapkan di bidang **sumber daya dapat dipesan**. Gunakan **tahapan eksekusi** yang sama sebagai plug-in out-of-band (OOB) (pra-validasi) dan gunakan **perintah eksekusi** yang lebih tinggi dari plug-in OOB (lebih dari 1). Ini akan memastikan bahwa plug-in kustom dijalankan setelah plug-in OOB.  
 
### <a name="end-user-experience"></a>Pengalaman Pengguna akhir
1.  Bila Anda membuat entri waktu di halaman Buat cepat, masukkan rincian tugas proyek dan proyek, lalu pilih pengguna pada bidang **sumber daya dapat dipesan** yang entri waktunya perlu direkam. 
2.  Secara default, bidang ini default untuk pengguna yang masuk, namun mengingat bahwa pengguna mengesampingkan bidang ini, entri waktu sekarang dibuat untuk **sumber daya yang dapat dipesan** yang dipilih.
3.  Bila Anda mengirimkan entri waktu yang Anda buat untuk rekaman ini, entri akan diantre untuk pemberi izin dalam proyek sebagaimana mestinya. 
4.  Bila Anda menarik entri waktu yang dibuat untuk pengguna lain, entri waktu akan dikembalikan ke status **draf** dengan bidang **sumber daya dapat dipesan** yang diatur ke pengguna lain. 
5.  Atau, Anda dapat beralih ke tampilan kustom untuk memfilter entri waktu yang dibuat untuk pengguna lain. 
 
### <a name="limitations"></a>Batasan
Fungsi **Salin** dan **impor** berfungsi hanya dalam konteks pengguna yang masuk. Ini berarti bahwa entri waktu tidak dapat menyalin atau mengimpor entri waktu yang dibuat untuk pengguna yang masuk seperti sumber daya dapat dipesan.

Entri waktu yang bukan untuk proyek akan diarahkan untuk disetujui manajer sumber daya dapat dipesan hanya jika langkah 4 di bagian **rincian penyesuaian** di atas selesai. Jika tidak, entri waktu non-proyek untuk pengguna lain akan salah diteruskan ke manajer pengguna yang masuk. 

### <a name="other-changes"></a>Perubahan lainnya 
Fungsi **Pemesanan dan tugas** telah dihapus. 

## <a name="multidimensional-pricing"></a>Harga multidimensi
Untuk memaksimalkan fleksibilitas dan memenuhi kebutuhan bisnis yang berbeda, versi 3 dari Project Service Automation mendukung aplikasi terpisah dari set dimensi harga ke biaya dan tingkat tagihan. Nilai dimensi dapat diatur sebagai default, lalu disebarkan di seluruh proses penetapan harga dan biaya dari pembuatan profil sumber daya ke entri waktu ke aktual proyek. Konfigurasi khusus pelanggan dan modifikasi atau ekstensi memanfaatkan infrastruktur penyesuaian standar.

Project Service Automation menggunakan seperangkat dimensi harga dan peran dan unit sumber daya default, serta memungkinkan konfigurasi harga dan biaya untuk setiap peran dan kombinasi unit organisasi.

Untuk pelanggan Project Service Automation yang ingin terus menggunakan bidang Bawaan sebagai dimensi harga dalam versi 3, tidak akan ada perubahan yang dapat diamati. Anda dapat terus menggunakan Project Service Automation seperti biasa. Namun, jika Anda perlu harga atau biaya untuk sumber daya Anda menggunakan atribut tambahan lainnya, versi 3 memungkinkan untuk menambahkan dimensi harga kustom Anda sendiri ke Project Service Automation . Perluasan dari dimensi harga kustom adalah pengalaman konfigurasi yang rumit. 

## <a name="quotes-and-contracts"></a>Kuotasi dan kontrak
Dalam versi 3 Project Service Automation, aspek pengaturan dan manajemen untuk kuotasi dan kontrak telah berubah. Bagian berikut ini menyediakan informasi yang lebih rinci.

### <a name="set-up-chargeability-options"></a>Konfigurasi Pilihan ketertagihan
Di versi 1 dan 2, konfigurasi penagihan untuk peran dan kategori untuk kuotasi dan kontrak tertentu dilakukan menggunakan tampilan **ketertagihan** yang ada di navigasi atas baris kuotasi atau baris kontrak. Ini juga di mana Anda dapat mengkonfigurasi harga untuk peran dan kategori pengeluaran tersebut.

Setelah versi 3, konfigurasi pilihan ketertagihan berdasarkan peran dan kategori pengeluaran akan dilakukan pada tingkat baris kuotasi atau kontrak. Konfigurasi harga terpisah dari penyiapan kemampuan ketertagihan. Anda akan dapat menemukan **peran yang dibebankan biaya** dan **kategori berbayar** sebagai tab pada **baris kuotasi** dan halaman  **baris kontrak** tanpa harus menggunakan navigasi atas.

![Peran yang dikenakan biaya.](media/chargeable-12.png)
 
Konfigurasi peran yang dibebankan biaya dan kategori berbayar juga memanfaatkan kontrol kisi yang dapat diedit secara Bawaan. Untuk setiap peran dan kategori, pilihan yang didukung untuk jenis penagihan selama fase penentuan dan kontrak tetap tidak diubah dari versi sebelumnya sebagai **dibebankan biaya** dan **tidak dikenakan biaya**. **Gratis** ini bukan jenis yang didukung selama fase kuotasi atau kontrak. **Gratis** hanya didukung selama persetujuan waktu atau biaya.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Membuat dan mengedit harga kustom untuk kuotasi Project Service Automation dan kontrak proyek
Dalam versi 1 dan 2, menggunakan daftar harga kustom untuk kuotasi dan kontrak tertentu dilakukan menggunakan **Edit harga** pada tampilan **ketertagihan**. Tampilan **ketertagihan** terletak di navigasi atas baris kuotasi atau baris kontrak. Ini juga di mana Anda dapat mengkonfigurasi pilihan ketertagihan untuk peran dan atau kategori pengeluaran.

Pada versi 3, membuat, dan menggunakan daftar harga proyek kustom pada kuotasi Project Service Automation dan kontrak proyek Project Service Automation telah dipisahkan dari pengaturan ketertagihan. Kuotasi Project Service Automation dan kontrak proyek Project Service Automation memiliki tab baru yang disebut **daftar harga proyek**. Tab ini menunjukkan tampilan terkait dari semua daftar harga proyek yang dilampirkan ke kuotasi Project Service Automation atau kontrak proyek. Untuk membuat daftar harga kustom dari daftar harga yang ada dan telah terkait dengan kuotasi atau kontrak proyek, klik **buat harga kustom**. Ini akan membuat salinan semua daftar harga terkait dan melampirkannya ke kuotasi atau kontrak. Anda sekarang dapat membuka daftar harga dan mengedit harga kategori peran atau pengeluaran sehingga perubahan harga tersebut hanya akan berlaku pada kuotasi atau kontrak ini. 
  
Grafik berikut adalah sebelum daftar harga kustom telah dibuat.

![Sebelum daftar harga kustom.](media/before-custom-price-lists-13.png)

Grafik berikut ditampilkan setelah daftar harga kustom telah dibuat.

![Setelah daftar harga kustom.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Keterlambatan singkat mungkin terjadi antara saat Anda mengeklik **buat harga kustom** hingga saat daftar harga kustom dibuat. Sebaiknya refresh kisi, bukan mengeklik beberapa kali. Daftar harga kustom telah dibuat jika nama daftar harga terkait telah ditambahi nama kuotasi atau nama kontrak proyek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
