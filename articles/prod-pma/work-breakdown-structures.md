---
title: Gambaran umum struktur rincian kerja
description: struktur rincian kerja (WBS) adalah deskripsi pekerjaan yang akan dilakukan untuk proyek. Ini adalah hierarki tugas yang menunjukkan pemahaman tim proyek tentang komposisi pekerjaan, dan ukuran, biaya, dan durasi masing-masing komponen atau tugas.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eddaf8a868845bde11c8bb7bc04f63777d628cf4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369425"
---
# <a name="work-breakdown-structures-overview"></a>Gambaran umum struktur rincian kerja

[!include [banner](../includes/banner.md)]

struktur rincian kerja (WBS) adalah deskripsi pekerjaan yang akan dilakukan untuk proyek. Ini adalah hierarki tugas yang menunjukkan pemahaman tim proyek tentang komposisi pekerjaan, dan ukuran, biaya, dan durasi masing-masing komponen atau tugas. WBS memiliki tiga tujuan utama:

-   Menjelaskan perincian atau komposisi pekerjaan dalam tugas.
-   Menjadwalkan kerja proyek.
-   Memperkirakan biaya setiap tugas.

Tingkat detail di WBS tergantung pada tingkat akurasi yang diperlukan dalam perkiraan dan tingkat pelacakan yang diperlukan terhadap perkiraan tersebut. Proyek yang memiliki toleransi yang sangat rendah untuk bergeser dari jadwal atau biaya biasanya memerlukan WBS yang lebih rinci, dan pelacakan yang teliti atas kemajuan kerja dan biaya terhadap WBS. Jenis proyek ini umum di industri konstruksi dan rekayasa. 

Sebaliknya, proyek di industri seperti media dan periklanan, perangkat lunak, dan infrastruktur TI cenderung menjadi jenis tersendiri, dan produktivitasnya relatif terhadap pengalaman dan kompetensi individu yang melakukan tugas. Oleh karena itu, industri ini menggunakan WBS untuk mendapatkan perkiraan ukuran proyek, bukan untuk melacak kemajuan proyek secara rinci. 

Membangun WBS adalah proses intensif yang biasanya dilakukan selama periode yang panjang, dan yang memerlukan kolaborasi dan informasi dari berbagai orang. Topik ini menjelaskan bagaimana anda dapat menggunakan peningkatan wbs untuk memenuhi kebutuhan anda akan estimasi dan pelacakan.

## <a name="prerequisites-for-creating-a-wbs"></a>Prasyarat untuk membuat WBS
Untuk membuat WBS, Anda harus dapat membuat jadwal kerja dan memperkirakan biaya kerja.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Prasyarat untuk membuat jadwal kerja

Untuk menggunakan kemampuan penjadwalan penuh fitur WBS, selesaikan konfigurasi berikut:

1.  Atur kalender default dan kalender proyek:
    1.  Klik **manajemen proyek dan akuntansi** &gt; **Konfigurasi** &gt; **manajemen proyek dan parameter akuntansi** &gt; **Penjadwalan**. Di bidang **kalender kerja default**, tentukan kalender default. Ini akan menjadi kalender kerja default untuk proyek baru yang dibuat.
    2.  Anda dapat mengubah kalender default untuk proyek tertentu. Klik halaman rincian proyek, lalu di fasttab **tim proyek dan penjadwalan**, perbarui bidang **kalender penjadwalan** dengan memilih kalender lainnya.

2.  Konfigurasikan hari kerja standar dan jam kerja. Kalender yang Anda tetapkan sebagai kalender kerja untuk proyek Anda akan digunakan di WBS untuk menentukan informasi berikut:

-   Hari kerja dan hari libur
-   Jumlah jam kerja dalam sehari

Untuk mengatur hari kerja dan jam kerja untuk kalender, atau membuat kalender baru, klik **Administrasi organisasi** &gt; **Umum** &gt; **Kalender**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Prasyarat untuk memperkirakan biaya pekerjaan

Untuk menggunakan kemampuan estimasi biaya penuh WBS, Anda harus menetapkan biaya dan harga penjualan untuk pekerja, kategori tenaga kerja, pengeluaran dan ongkos, dan item.

-   Untuk mengkonfigurasi biaya dan harga penjualan tenaga kerja, biaya, dan kategori biaya, klik **manajemen proyek dan akuntansi** &gt; **konfigurasi** &gt; **Harga**.
-   Untuk mengkonfigurasi biaya dan harga penjualan item, gunakan halaman **Perjanjian Dagang** untuk setiap item di halaman daftar **produk yang dirilis** dalam manajemen informasi produk.

## <a name="creating-a-wbs"></a>Membuat WBS
Membuat WBS melibatkan tiga aktivitas:

1.  **Dekomposisi kerja** -membuat rincian pekerjaan menjadi potongan atau tugas yang dapat dikelola.
2.  **Jadwal kerja** – memperkirakan waktu yang diperlukan untuk menyelesaikan tugas, mengatur interdependensi tugas, dan memilih tanggal mulai dan berakhir untuk tugas.
3.  **Estimasi biaya** -Estimasi biaya untuk setiap tugas.

Bagian berikut ini membahas bagaimana kemampuan WBS dapat membantu setiap aktivitas ini.

### <a name="work-decomposition"></a>Dekomposisi kerja

Membuat perincian atau dekomposisi pekerjaan biasanya merupakan langkah pertama dalam proses pembuatan WBS. Fungsi WBS mendukung konstruksi dasar berikut untuk perincian atau penguraian pekerjaan. 

**Tugas akar proyek** Tugas akar proyek adalah tugas Rangkuman tingkat atas untuk proyek. Semua tugas-tugas proyek lain yang dibuat di bawahnya. Nama tugas akar selalu diatur menjadi nama proyek. Upaya, tanggal, dan durasi node akar meringkas nilai untuk tugas di bawah tugas akar. Anda tidak dapat memodifikasi properti node akar atau menghapusnya.

**Ringkasan atau tugas kontainer** tugas Rangkuman adalah tugas yang memiliki sub-tugas atau tugas konstituen di bawahnya. Ringkasan tugas tidak memiliki usaha kerja atau biaya sendiri. Sebaliknya, upaya kerja dan biaya tugas Rangkuman adalah jumlah dari upaya kerja dan biaya tugas konstituennya. Tanggal mulai terawal dari tugas konstituen digunakan sebagai tanggal mulai dari tugas rangkuman, dan tanggal akhir terakhir dari tugas konstituen digunakan sebagai tanggal akhir. Anda dapat memodifikasi nama tugas ringkasan, tetapi tidak dapat memodifikasi properti penjadwalan untuk upaya, tanggal, dan durasi. Jika Anda menghapus tugas ringkasan, Anda juga akan menghapus semua tugas konstituennya. 

**Tugas node leaf** tugas node leaf merupakan paket kerja yang paling rinci pada proyek. node leaf memiliki upaya perkiraan, jumlah sumber daya yang direncanakan, rencana tanggal akhir dan awal, dan durasi. 

Anda dapat menyelesaikan operasi hierarki berikut untuk memungkinkan pembuatan hierarki kerja atau penguraian untuk proyek. 

**Tugas baru** setiap tugas baru yang Anda buat secara otomatis ditambahkan di bawah node akar, dan nomor WBS secara otomatis ditetapkan ke tugas. Nomor WBS mewakili tingkat tugas dalam hierarki. Untuk tugas di tingkat pertama di bawah tugas root proyek, skema penomoran 1, 2, 3, dan sebagainya, digunakan. Untuk tugas yang ada di bawah tingkat pertama, skema penomoran 1.1, 1.2, 1.3, dan sebagainya, digunakan. Untuk setiap tingkat yang ditambahkan di bawah tingkat sebelumnya, rangkaian angka bertitik baru ditambahkan. 

Saat ini, Anda tidak dapat menyesuaikan penomoran WBS. 

**Indentasi tugas** saat Anda menginden tugas, ia menjadi anak dari tugas yang mendahului. Nomor WBS tugas anak baru secara otomatis dihitung ulang berdasarkan jumlah WBS induk barunya. Tugas induk sekarang adalah tugas ringkasan atau kontainer, dan karena itu menjadi akumulasi dari tugas konstituennya. 

> [!NOTE] 
> Bila Anda mengindentasi tugas dalam tugas yang merupakan node daun sebelum operasi indentasi, tugas ringkasan baru dibuat kehilangan tanggal, upaya, dan jumlah sumber dayanya sendiri. Ia sekarang menggunakan ringkasan dari nilai tugas konstituennya yang baru. 

**Tugas outdent** ketika Anda meng-outdent tugas, itu tidak lagi merupakan tugas konstituen dari induknya. Nomor WBS tugas ini secara otomatis dihitung ulang untuk mencerminkan tingkat baru tugas dalam hirarki. Upaya, biaya, dan tanggal tugas induk sebelumnya dari tugas dihitung ulang untuk mengeluarkan tugas itu. 

**Pindahkan ke atas dan ke bawah** saat Anda mengeklik **Pindahkan ke atas** dan **Pindahkan ke bawah**, Anda mengubah posisi tugas dalam hirarki induknya. Posisi tugas tidak mempengaruhi upaya, biaya, tanggal, atau durasi tugas. Namu, nomor WBS tugas ini secara otomatis dihitung ulang untuk mencerminkan posisi baru tugas.

### <a name="schedule-estimation"></a>Estimasi Jadwal

Estimasi jadwal biasanya adalah langkah kedua dalam membuat WBS. Sebagai praktik terbaik, Anda harus menyelesaikan estimasi jadwal setelah membuat tugas. Halaman **struktur rincian kerja** di Finance memiliki dua bagian. Panel atas ditujukan untuk estimasi jadwal, dan panel bawah mencakup tab **Estimasi biaya dan pendapatan** yang dapat Anda gunakan untuk estimasi biaya. 
**Dependensi tugas** di WBS, Anda dapat membuat relasi pendahulu antara tugas. Bila Anda menetapkan tugas pendahulu ke tugas, tugas itu hanya dapat mulai ketika menyelesaikan semua tugas-tugas pendahulunya. Tanggal mulai yang direncanakan untuk tugas secara otomatis diatur ke tanggal terbaru dari semua pendahulunya. 

**Penjadwalan tugas** faktor berikut menentukan penjadwalan tugas node leaf:

-   Pendahulu
-   Usaha
-   Jumlah sumber daya
-   Tanggal Mulai dan Berakhir

Tanggal mulai tugas node leaf yang tidak memiliki pendahulu otomatis diatur ke tanggal mulai penjadwalan proyek. Masa tugas node leaf selalu dihitung sebagai jumlah hari kerja antara tanggal yang awal dan akhir. 

*<strong><em>Aturan penjadwalan</em></strong>* bila bantuan penjadwalan otomatis diaktifkan, aturan berikut berlaku untuk tugas penjadwalan untuk tugas node leaf:

-   Tanggal mulai dan akhir dari tugas yang harus hari kerja menurut kalender penjadwalan proyek.
-   Tanggal mulai tugas yang pendahulunya otomatis diatur ke tanggal akhir terbaru dari pendahulunya.
-   Upaya untuk tugas secara otomatis dihitung sebagai berikut:

Jumlah orang × durasi × jam × Jumlah jam dalam hari kerja standar dalam kalendar proyek. 

Dalam beberapa kasus, Anda mungkin ingin menyimpang dari aturan-aturan ini. Anda dapat menonaktifkan penjadwalan otomatis untuk mencegah Finance secara otomatis mengatur atau mengoreksi properti dari tugas node leaf. Bila Anda memasukkan informasi untuk tugas yang menyebabkan pelanggaran aturan penjadwalan, ikon kesalahan penjadwalan ditampilkan untuk tugas. Jika Anda tidak ingin penjadwalan kesalahan ditampilkan, klik **kesalahan penjadwalan ditampilkan** untuk menonaktifkan fitur. 

> [!NOTE] 
> Nilai untuk tugas ringkasan atau kontainer akan dihitung sebagai jumlah nilai tugas konstituen, terlepas dari Apakah bantuan penjadwalan otomatis diaktifkan atau dinonaktifkan. 

**Memperbaiki kesalahan penjadwalan** bila bantuan penjadwalan otomatis diaktifkan, kesalahan penjadwalan tidak mungkin terjadi. Namun, jika Anda menonaktifkan bantuan penjadwalan otomatis dan kemudian mengaktifkannya kembali nanti, ikon kesalahan penjadwalan mungkin muncul di WBS. 

**Memperbaiki kesalahan penjadwalan berdasarkan tugas** saat Anda mengeklik dua kali ikon kesalahan jadwal untuk tugas tertentu, kotak dialog menampilkan semua kesalahan penjadwalan untuk tugas tersebut. Anda dapat memutuskan kesalahan penjadwalan yang akan diperbaiki untuk tugas. 

**Memperbaiki semua kesalahan penjadwalan** jika Anda ingin Finance untuk memperbaiki semua kesalahan penjadwalan di WBS, di panel tindakan, klik **Perbaiki semua perbedaan penjadwalan**. 

> [!NOTE] 
> Fitur ini dapat menyebabkan modifikasi signifikan pada WBS. Kesalahan dikoreksi dalam urutan berikut:

1.  Estimasi upaya pada semua tugas diubah sehingga sama dengan kapasitas yang ditentukan dalam kalender proyek.
2.  Tanggal mulai setiap tugas dimodifikasi sehingga tugas dimulai setelah semua tugas pendahulunya selesai.
3.  Tanggal mulai dari setiap tugas dimodifikasi untuk menghilangkan kesenjangan di tanggal mulai tugas pendahulunya.

### <a name="cost-estimation"></a>Perkiraan biaya

Seperti disebutkan sebelumnya dalam dokumen ini, Anda memasukkan perkiraan biaya untuk setiap tugas node leaf dengan menggunakan tab **estimasi biaya dan pendapatan** di panel bawah dari halaman **struktur rincian kerja**. 

> [!NOTE] 
> Anda tidak dapat mengubah perkiraan biaya untuk tugas ringkasan atau penampung. Estimasi biaya untuk tugas Rangkuman sama dengan jumlah Estimasi biaya dari tugas node leaf. Estimasi total biaya untuk setiap tugas dihitung sebagai jumlah Estimasi jumlah biaya untuk jenis transaksi berikut:

-   Tugas
-   Item atau material
-   Pengeluaran

Jenis transaksi **Ongkos** digunakan untuk memperkirakan pendapatan berbasis ongkos. Jenis transaksi ini tidak memiliki komponen biaya dan karena itu tidak dipertimbangkan saat biaya diperkirakan. 

Jenis transaksi **pada akun** digunakan untuk merekam nilai penjualan yang dikontrak dalam jenis proyek dengan nilai tetap. Jenis transaksi ini juga tidak dipertimbangkan saat biaya diperkirakan. 

Bila Anda memperkirakan biaya untuk tenaga kerja, material, dan biaya untuk setiap tugas, Anda harus menetapkan kategori proyek ke estimasi biaya. 

**Estimasi biaya tenaga kerja** untuk setiap tugas node leaf, Anda menetapkan upaya kerja dalam jam dan kategori default. Oleh karena itu, bila Anda mengkonfigurasi jadwal untuk tugas, perkiraan biaya tenaga kerja untuk tugas tersebut ditambahkan secara otomatis dalam kategori default untuk tenaga kerja. Estimasi biaya ini akan ditampilkan pada tab **Estimasi biaya dan pendapatan** di kisi **rincian baris** untuk tugas tersebut. Jika Anda memerlukan perkiraan biaya tenaga kerja lainnya, Anda dapat menambahkannya di tab ini. Jika Anda menambah atau mengurangi jam pada perkiraan biaya tenaga kerja, jadwal untuk tugas tersebut akan secara otomatis dihitung ulang. 

**Estimasi biaya pengeluaran dan material** Tab **Estimasi biaya dan pendapatan** juga memungkinkan Anda memperkirakan biaya pengeluaran dan material untuk tugas, jika Anda memerlukan estimasi. 

Biaya dan harga penjualan untuk setiap baris perkiraan tenaga kerja atau pengeluaran didasarkan pada konfigurasi yang ditentukan untuk setiap kategori dalam tabel harga di **manajemen proyek dan akuntansi** &gt; **konfigurasi** &gt; **harga**. Untuk item, biaya dan harga ditambahkan secara default dari item atau perjanjian perdagangan di halaman daftar **produk yang dirilis** dalam manajemen informasi produk.

## <a name="tracking-progress-on-the-wbs"></a>Melacak kemajuan di WBS
Beberapa industri melacak kemajuan proyek terhadap WBS pada tingkat yang sangat rinci, sedangkan yang lain melacak kemajuan pada tingkat yang lebih tinggi dari WBS. Bagian ini menjelaskan bagaimana Anda dapat menggunakan pelacakan WBS untuk kebutuhan proyek Anda. 

Finance memiliki tiga tampilan untuk WBS suatu proyek: tampilan perencanaan, tampilan pelacakan upaya, dan tampilan pelacakan biaya.

### <a name="planning-view"></a>Tampilan perencanaan

Tampilan perencanaan menampilkan perkiraan terencana atau garis dasar dari informasi jadwal dan biaya. Meskipun tidak ada fitur untuk melacak versi dan garis dasar untuk WBS proyek, nilai dalam tampilan ini ditujukan untuk menunjukkan versi garis dasar. Bagian estimasi jadwal dan estimasi biaya topik ini menjelaskan tampilan ini dan cara menggunakannya untuk membuat wbs.

### <a name="effort-tracking-view"></a>Tampilan Pelacakan Upaya

Tampilan pelacakan upaya menampilkan pelacakan kemajuan tugas dalam WBS. Ini membandingkan akumulasi waktu kerja yang sebenarnya dengan tugas jam upaya yang direncanakan. Rumus berikut memberikan nilai dalam tampilan pelacakan upaya:

-   Persentase kemajuan = upaya aktual hingga sekarang ÷ upaya yang direncanakan untuk tugas
-   Upaya yang tersisa (juga dikenal sebagai estimasi menyelesaikan \[ETC\]) = rencana upaya – upaya aktual hingga saat ini
-   Perkiraan saat selesai (EAC) = usaha tersisa + upaya yang sebenarnya sampai saat ini
-   Diproyeksikan variance usaha = usaha yang direncanakan – EAC

Tampilan pelacakan upaya menampilkan proyeksi varians upaya untuk tugas, berdasarkan Apakah EAC lebih atau kurang dari upaya yang direncanakan:

-   Jika EAC lebih dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih banyak waktu daripada yang direncanakan dan terlambat dari jadwal.
-   Jika EAC lebih sedikit dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih sedikit waktu daripada yang direncanakan dan maju dari jadwal.

**Proyeksi upaya ulang manajer proyek** sesekali waktu, manajer proyek atau persona lain yang melacak kemajuan proyek harus merevisi estimasi asli pada tugas. Tugas mungkin akan bergerak lebih cepat atau lebih lambat dari yang awalnya diantisipasi karena berbagai alasan. Misalnya, cakupan telah dikurangi, atau pekerja kurang pengalaman daripada yang direncanakan. Proyeksi adalah persepsi manajer proyek tentang perkiraan, berdasarkan status proyek saat ini. Umumnya, Anda tidak boleh mengubah angka dasar Anda, karena garis dasar proyek mewakili dokumen yang diterbitkan dengan baik untuk jadwal proyek dan estimasi biaya yang mana semua stakeholder pada proyek telah setuju. 

Ada dua cara manajer proyek dapat memodifikasi upaya pada tugas:

-   Modifikasi upaya lainnya yang diatur secara otomatis untuk memperbarui upaya tersisa aktual pada tugas.
-   Modifikasi persentase kemajuan yang diatur secara otomatis untuk memperbarui kemajuan sebenarnya pada tugas.

Kedua pendekatan ini menyebabkan penghitungan ulang dari ETC, EAC tugas, dan persentase progres, serta proyeksi varians upaya pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan varians upaya yang diproyeksikan diperbarui. 

**Upaya yang dimodifikasi pada tugas ringkasan** Anda dapat memodifikasi upaya pada ringkasan atau tugas kontainer. Terlepas dari Anda memodifikasi nilai ini dengan menggunakan usaha yang tersisa atau persentase kemajuan pada tugas ringkasan, perhitungan terjadi otomatis dalam urutan berikut ini:

1.  EAC, ETC, dan persentase kemajuan tugas dihitung.
2.  EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti jumlah EAC asli.
3.  EAC baru pada setiap tugas node leaf dihitung.
4.  Persentase upaya dan progres yang tersisa akan dihitung ulang untuk semua tugas anak yang terpengaruh, berdasarkan nilai EAC yang baru. Varians upaya dari tugas juga dihitung ulang.
5.  EAC tugas ringkasan juga dihitung ulang dari node leaf.

Klik **Perluas ke tingkat** di tampilan pelacakan upaya untuk mengatur tingkat untuk melacak dan mempertahankan WBS Anda. WBS akan secara otomatis diperluas ke tingkat tersebut dalam tampilan pelacakan upaya saat Anda membukanya.

### <a name="cost-tracking-view"></a>Tampilan Pelacakan Biaya

Tampilan pelacakan biaya menampilkan pelacakan konsumsi biaya untuk tugas. Dalam tampilan ini, biaya aktual yang telah dihabiskan terhadap tugas hingga saat ini dibandingkan dengan biaya yang direncanakan untuk tugas. Rumus berikut memberikan nilai dalam tampilan pelacakan Biaya:

-   Persentase dari biaya yang dihabiskan = biaya aktual hingga sekarang ÷ rencana biaya untuk tugas
-   Biaya untuk menyelesaikan (CTC) = rencana biaya – biaya sebenarnya sampai saat ini
-   Estimasi saat selesai (EAC) = CTC + biaya aktual hingga saat ini
-   varians Biaya diproyeksikan = biaya direncanakan - EAC

Tampilan pelacakan Biaya menampilkan proyeksi varians biaya untuk tugas, berdasarkan Apakah EAC lebih atau kurang dari biaya yang direncanakan:

-   Jika EAC lebih dari biaya yang direncanakan, tugas diproyeksikan untuk menggunakan lebih banyak uang daripada yang direncanakan dan berada di atas anggaran.
-   Jika EAC lebih sedikit dari biaya yang direncanakan, tugas diproyeksikan untuk menggunakan lebih sedikit uang daripada yang direncanakan dan berada di bawah anggaran.

**Proyeksi ulang manajer proyek atas biaya** manajer proyek harus menggunakan CTC untuk merevisi perkiraan biaya awal pada tugas. Manajer proyek dapat memodifikasi nilai CTC dengan biaya yang diperlukan untuk menyelesaikan tugas. Jika Anda memodifikasi nilai CTC, CTC tugas, EAC, dan persentase biaya yang dikonsumsi, dan variasi biaya yang diproyeksikan pada tugas, akan dihitung ulang. EAC, ETC, dan persentase biaya yang dikonsumsi pada ringkasan tugas juga dihitung ulang, dan varians biaya yang diproyeksikan diperbarui. 

> [!NOTE] 
> Bila Anda merevisi upaya untuk tugas WBS dalam tampilan pelacakan upaya, CTC tugas, EAC, persentase biaya yang dikonsumsi, dan varians biaya yang diproyeksikan semuanya dihitung ulang dalam tampilan pelacakan biaya. Namun, revisi biaya tidak mempengaruhi nilai dalam tampilan pelacakan upaya, karena jenis biaya berdasarkan transaksi (tenaga kerja, material, atau pengeluaran) atau kategori proyek tidak direvisi. 

**Revisi proyeksi untuk biaya pada tugas ringkasan** Anda dapat merevisi biaya pada tugas ringkasan, dan penghitungan terjadi secara otomatis dalam urutan berikut:

1.  EAC, CTC dan persentase biaya yang dikonsumsi pada tugas akan dihitung ulang.
2.  EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti EAC asli pada tugas.
3.  EAC baru untuk setiap tugas dihitung.
4.  CTS dan persentase biaya yang dikonsumsi akan dihitung ulang untuk tugas anak yang terpengaruh, berdasarkan nilai EAC. Varians biaya dari tugas juga dihitung ulang.
5.  EAC untuk semua tugas Rangkuman dihitung ulang berdasarkan perubahan ini.

Klik **Perluas ke tingkat** di tampilan pelacakan biaya untuk mengatur tingkat untuk melacak dan mempertahankan WBS Anda. WBS akan diperluas ke tingkat tersebut dalam tampilan pelacakan biaya saat Anda membukanya.

### <a name="earned-value-management"></a>Manajemen nilai perolehan

Anda dapat menggunakan metode nilai perolehan (EVM) untuk melacak kemajuan proyek. Anda dapat melihat metrik nilai yang diperoleh di pusat peran manajer proyek. Komponen diagram nilai yang diperoleh menampilkan nilai berdasar waktu dari nilai yang direncanakan dan biaya aktual. Nilai yang diperoleh pada tanggal saat ini ditampilkan sebagai sebuah titik. Data berdasar waktu untuk nilai yang diperoleh saat ini tidak tersedia. 

Fase waktu pada diagram nilai yang diperoleh ditampilkan berdasarkan minggu atau bulan. Bagian ini menjelaskan tiga pilar EVM: nilai yang direncanakan, nilai perolehan, dan biaya aktual. 

**Nilai yang direncanakan** Teori EVM menyatakan bahwa plot nilai yang direncanakan menunjukkan tingkat rencana tim proyek untuk mendapatkan nilai pada proyek. 

Finance menggunakan aturan perolehan 0:100 saat merencanakan nilai yang direncanakan. Di dalam aturan ini, nilai tugas diposting ke tugas saat tanggal akhirnya. Tidak ada nilai yang diposting hingga tugas 100 persen selesai. 

Dalam manajemen proyek dan akuntansi, Anda memasukkan tanggal akhir node leaf dan biaya yang direncanakan untuknya. Bila grafik nilai yang direncanakan ditampilkan dalam seminggu, nilai yang direncanakan diringkas per minggu untuk semua tugas node leaf selama durasi proyek. 

**Nilai perolehan** Teori EVM menyatakan bahwa plot nilai perolehan menunjukkan tingkat tim proyek benar-benar mendapatkan nilai pada proyek. 

Finance menggunakan aturan perolehan 0:100 saat memplot nilai perolehan. Di dalam aturan ini, nilai tugas diposting ke tugas saat tanggal akhirnya. Tidak ada nilai yang diposting hingga tugas 100 persen selesai. 

Bila nilai yang diperoleh dihitung, persentase progres setiap tugas akan dipertimbangkan. Di dalam aturan perolehan 0:100, hanya tugas yang diselesaikan dalam periode tertentu yang dipertimbangkan untuk penghitungan nilai yang diperoleh pada akhir periode tersebut. Nilai yang diperoleh pada proyek dihitung untuk semua tugas yang telah diselesaikan saat grafik dibuat. 

> [!NOTE] 
> Saat ini, sistem untuk pelacakan WBS tidak memiliki struktur data untuk menyimpan persentase kemajuan historis pada setiap tugas. Oleh karena itu, nilai yang diperoleh hanya dapat dilaporkan pada waktu saat kubus diproses. Proses kubus secara teratur untuk memperbarui data nilai yang diperoleh yang ditampilkan pada pusat peran. 

**Biaya aktual** Teori EVM menyatakan bahwa plot biaya aktual menunjukkan tingkat di mana uang dibelanjakan pada proyek. 

Transaksi yang diposting ke proyek digunakan untuk merencanakan baris biaya aktual. Biaya diringkas berdasarkan tanggal. Data ini kemudian digunakan untuk grafik biaya aktual menurut minggu atau bulan pada diagram nilai yang diperoleh.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Cara menggunakan konsep nilai yang direncanakan, nilai perolehan, dan biaya aktual

**Varians jadwal** selama perencanaan, Anda membuat perkiraan untuk bekerja pada Timeline. Oleh karena itu, nilai yang direncanakan adalah tingkat penyelesaian proyek menurut perencana proyek. Setelah proyek berlangsung, pekerjaan selesai, dan proyek menghasilkan nilai. Dengan membandingkan nilai yang direncanakan dengan nilai yang diperoleh, Anda dapat melihat kemajuan kerja proyek. Hasil dari perbandingan ini disebut varians jadwal. 

Jika nilai yang direncanakan untuk suatu periode melebihi nilai yang diperoleh, jumlah pekerjaan yang telah dilakukan pada suatu proyek kurang dari yang direncanakan. Oleh karena itu, proyek terlambat dari jadwal. Karena nilai yang direncanakan dan nilai yang diperoleh dinyatakan dalam istilah moneter, waktu jeda pada proyek juga diberikan nilai moneter. 

Jika nilai yang direncanakan untuk suatu periode kurang dari nilai yang diperoleh, jumlah pekerjaan yang telah dilakukan pada suatu proyek melebihi yang direncanakan. Oleh karena itu, proyek maju dari jadwal. Waktu tunggu ini juga diberikan nilai moneter.

**Varians biaya** karena nilai yang diperoleh menggunakan harga biaya sebagai nilai pengali, nilai perolehan menunjukkan biaya pekerjaan yang dilakukan pada proyek. Saat proyek berlangsung, log transaksi memberikan rekaman uang yang sebenarnya dihabiskan pada proyek tersebut. Dengan membandingkan nilai yang diperoleh dengan biaya aktual, Anda dapat melihat jumlah uang yang dibelanjakan versus nilai yang diperoleh. Hasil dari perbandingan ini disebut varians biaya. 

Jika biaya aktual yang dihabiskan untuk periode lebih dari nilai yang diperoleh, lebih banyak uang yang dibelanjakan dari yang diperoleh. Oleh karena itu, proyek lebih dari anggaran. 

Jika biaya aktual yang dihabiskan untuk periode kurang dari nilai yang diperoleh, lebih banyak uang yang diperoleh daripada yang dibelanjakan. Oleh karena itu, proyek di bawah anggaran.

## <a name="wbs-templates"></a>Template WBS
Anda dapat menggunakan fungsi Template WBS untuk membuat template standar untuk proyek. Jika proyek yang ditawarkan perusahaan Anda melibatkan banyak pekerjaan yang dapat diulang, Anda harus mempertimbangkan untuk membuat template WBS. 

Anda dapat membuat template WBS dari WBS dari proyek yang ada, sehingga pengetahuan dan praktik terbaik yang Anda kumpulkan selama perencanaan proyek dapat digunakan kembali pada proyek serupa di masa mendatang. Namun, terkadang, mungkin tidak masuk akal untuk menyimpan seluruh WBS sebagai template. Oleh karena itu, Anda juga dapat membuat template dari bagian WBS untuk proyek.

### <a name="saving-a-projects-wbs-as-a-template"></a>Menyimpan WBS proyek sebagai template

Setelah membuat template, Anda dapat mengimpornya ke WBS proyek baru di node akar, atau dalam tugas apa pun di WBS proyek.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Mengimpor template WBS ke dalam WBS proyek

Bila Anda mengimpor tugas, tugas di template diatur berdasarkan tanggal mulai tugas yang diimpor. Selama impor, Relasi pendahulu pada tugas template digunakan untuk menghitung tanggal mulai untuk tugas yang diimpor. Kalender kerja standar proyek tujuan diterapkan untuk menghitung tanggal akhir dari tugas yang diimpor, sehingga hari kerja dan jam kerja standar yang ditentukan dalam kalender kerja proyek saat ini dipertahankan. 

Jumlah biaya dan harga penjualan pada baris estimasi diterapkan untuk menjamin bahwa harga yang spesifik untuk proyek atau kontrak proyek memiliki tanggal yang valid.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Perbedaan antara WBS proyek dan template WBS

-   Tugas di template WBS tidak memiliki tanggal mulai dan tanggal berakhir.

Hari kerja dan non-kerja tidak diatur untuk template WBS.

-   Template WBS selalu menggunakan kalender penjadwalan yang diatur sebagai kalender default untuk semua proyek.

Kalender penjadwalan default hanya digunakan untuk mencari tahu jam dalam hari kerja standar.

-   Relasi pendahulu tidak disalin ke template wbs.

Karena template WBS tidak memiliki tanggal, logika tanggal mulai yang didasarkan pada tanggal akhir pendahulunya tidak diperlukan.

-   Baris estimasi biaya tenaga kerja secara otomatis dibuat saat tugas dibuat di template WBS. Harga penjualan dan jumlah biaya disalin dari pekerja yang dipilih.

Biaya dan biaya item dapat dibuat secara manual, sama seperti yang dapat mereka lakukan pada WBS proyek.

-   Kesalahan penjadwalan ditampilkan saat terdapat penyimpangan dari rumus berikut:

Upaya = jumlah sumber daya × durasi × jumlah jam dalam hari kerja standar 

Anda dapat mengoreksi semua kesalahan penjadwalan pada waktu yang sama dengan mengeklik **Perbaiki semua kesalahan penjadwalan**. 

Atau, Anda dapat mengoreksi kesalahan penjadwalan secara individual dengan mengklik ikon peringatan untuk setiap tugas.





[!INCLUDE[footer-include](../includes/footer-banner.md)]