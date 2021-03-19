---
title: Kontrak Proyek
description: Topik ini memberikan contoh tentang kontrak proyek yang dapat anda buat untuk berbagai jenis proyek dan sumber pendanaan, dan bagaimana anda dapat mengelola kontrak dan faktur pelanggan proyek.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289553"
---
# <a name="project-contracts"></a>Kontrak Proyek

[!include [banner](../includes/banner.md)]

Artikel ini memberikan contoh tentang kontrak proyek yang dapat anda buat untuk berbagai jenis proyek dan sumber pendanaan, dan bagaimana anda dapat mengelola kontrak dan faktur pelanggan proyek.

Jenis proyek yang Anda buat untuk kontrak proyek menentukan metode yang digunakan untuk menagih pelanggan proyek. Anda dapat mengubah kontrak proyek dan proyek terkait, namun Anda tidak dapat mengubah jenis proyek. 

Dengan menggunakan kontrak proyek, Anda dapat menagih satu atau beberapa proyek pada waktu yang sama. Kontrak proyek juga membantu menjamin prosedur faktur konsisten untuk setiap subproyek dalam struktur proyek. 

Setiap proyek yang akan ditagih harus terkait dengan kontrak proyek. Pengaturan untuk kontrak proyek berlaku untuk semua proyek dan subproyek yang terkait dengan kontrak proyek tersebut. 

Kontrak proyek dapat menyebutkan satu atau beberapa sumber pendanaan. Oleh karena itu, Anda dapat membagi tagihan di antara beberapa penyandang dana, mengatur batas pendanaan sehingga sumber pendanaan tidak ditagih lebih dari jumlah tertentu, dan mengkonfigurasikan aturan pendanaan untuk menagih pengeluaran.

## <a name="funding-for-project-contracts"></a>Pendanaan untuk kontrak proyek
Beberapa kontrak proyek menentukan bahwa beberapa pihak berbagi tanggung jawab untuk mendanai biaya proyek. Berikut adalah beberapa contoh:

-   Pelanggan besar yang memiliki beberapa divisi meminta pendanaan proyek dapat dibagi menurut Divisi.
-   Perusahaan Anda berbagi biaya proyek besar dengan organisasi eksternal.
-   Sebuah proyek jalan didanai oleh dua pemerintah kota.
-   Sebuah proyek jembatan didanai oleh hibah pemerintah dan perusahaan swasta.

Di Dynamics 365 Finance, Anda dapat membagi penagihan untuk satu transaksi atau seluruh proyek di antara beberapa pelanggan, hibah, atau organisasi. 

Dalam proyek yang memiliki beberapa penyandang dana, semua pihak yang berkontribusi pada pendanaan proyek pendanaan tingkat lanjut disebut sumber pendanaan. Setelah pelanggan, organisasi, atau hibah didefinisikan sebagai sumber pendanaan, ia dapat ditetapkan ke satu atau beberapa aturan pendanaan. Aturan pendanaan berisi kriteria yang menentukan cara biaya dialokasikan ke berbagai sumber pendanaan untuk proyek. 

Karena item dalam stok, seperti yang muncul pada rekusisi pembelian dan pesanan pembelian, tidak dapat dibagi, jumlah biaya tidak dapat dibagi antara beberapa sumber pendanaan pada saat distribusi. Oleh karena itu, nilai sumber dana tetap 0 (nol) hingga masalah inventaris diposting. Bila masalah inventaris diposting, jumlah biaya akan didistribusikan berdasarkan aturan distribusi akun untuk proyek.

Berikut adalah beberapa langkah yang dapat Anda lakukan agar lebih mudah membagi tagihan di antara beberapa sumber pendanaan:

-   Tentukan bahwa semua transaksi yang dimasukkan untuk proyek menggunakan mata uang penjualan yang sama dengan kontrak proyek.
-   Mengatur batas pendanaan, sehingga sumber pendanaan tidak ditagih lebih dari jumlah tertentu pada proyek.
-   Konfigurasikan aturan pendanaan dan batas pendanaan untuk setiap pekerja, item, kategori, grup kategori, dan jenis transaksi (atau untuk semua jenis transaksi).
-   Pilih tanggal mulai dan akhir opsional untuk menentukan periode saat setiap aturan pendanaan valid.
-   Tentukan persentase tanggung jawab setiap sumber pendanaan.
-   Tentukan sumber pendanaan yang bertanggung jawab atas pembulatan selisih yang disebabkan oleh penghitungan alokasi pendanaan.
-   Konfigurasikan aturan yang menentukan cara biaya proyek ditagih ke pelanggan eksternal dan dibebankan ke organisasi internal.
-   Catat transaksi di akun pendanaan yang ditahan hingga dana tambahan dapat diperoleh, atau hingga Anda memutuskan menanggung biaya secara internal.

Untuk menentukan grup pajak yang akan dikaitkan dengan transaksi, proyek dicari tugas grup pajaknya. Jika tugas grup pajak tidak dibuat di tingkat proyek, kontrak proyek akan dicari.

### <a name="example-multiple-funding-sources-simple"></a>Contoh: beberapa sumber pendanaan (sederhana)

Tabel berikut menyediakan skenario untuk mengelola alokasi dana di antara beberapa sumber pendanaan. Skenario ini didasarkan pada asumsi berikut:

-   Pengaturan prioritas diperhitungkan dalam alokasi dana sebelum kriteria aturan pendanaan lainnya diterapkan.
-   Rentang tanggal tidak ditentukan untuk menentukan periode saat aturan pendanaan valid.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Skenario</strong></td>
<td><strong>Sumber pendanaan</strong></td>
<td><strong>Persentase alokasi</strong></td>
<td><strong>Prioritas alokasi</strong></td>
</tr>
<tr class="even">
<td>Anda ingin mengalokasikan biaya ke satu sumber pendanaan hingga dananya habis, alokasikan biaya ke sumber dana kedua hingga dananya habis, dan akhirnya alokasikan sisa biaya ke sumber dana ketiga.</td>
<td><ul>
<li>Sumber pendanaan 1</li>
<li>Sumber pendanaan 2</li>
<li>Sumber pendanaan 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anda ingin mengalokasikan 75 persen dari biaya ke salah satu sumber pendanaan dan 25 persen ke sumber dana kedua. Bila salah satu dari sumber pendanaan tersebut habis, Anda ingin membayar sisa biaya dari sumber pendanaan ketiga.</td>
<td><ul>
<li>Sumber pendanaan 1</li>
<li>Sumber pendanaan 2</li>
<li>Sumber pendanaan 3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Anda ingin mengalokasikan 75 persen dari biaya ke salah satu sumber pendanaan dan 25 persen ke sumber dana kedua. Bila salah satu dari sumber pendanaan tersebut habis, Anda ingin memecah sisa biaya antara sumber pendanaan ketiga dan sumber dana keempat.</td>
<td><ul>
<li>Sumber pendanaan 1</li>
<li>Sumber pendanaan 2</li>
<li>Sumber pendanaan 3</li>
<li>Sumber pendanaan 4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anda ingin mengalokasikan 25 persen dari biaya pertama ke salah satu sumber pendanaan dan sisanya ke sumber dana kedua.</td>
<td><ul>
<li>Sumber pendanaan 1</li>
<li>Sumber pendanaan 2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Contoh: beberapa sumber pendanaan (kompleks)

Anda memiliki tiga sumber pendanaan yang ingin Anda gunakan dalam urutan berikut:

1.  Gunakan pendanaan sumber 2 dan pendanaan sumber 3 sama hingga dana sumber 2 habis.
2.  Terus gunakan dana sumber 3 hingga habis.
3.  Gunakan dana sumber 1 setelah sumber dana 3 habis.

Untuk mencapai sasaran ini, pertama-tama Anda harus melakukan langkah berikut:

-   Mengatur batas pendanaan untuk mendanai sumber 2 dan mendanai sumber 3, untuk jumlah masing-masing.
-   Buat aturan pendanaan berikut:
    -   Aturan 1 (Prioritas 1): mengalokasikan 50 persen dari transaksi ke sumber dana 2 dan 50 persen ke dana sumber 3.
    -   Aturan 2 (Prioritas 2): mengalokasikan 100 persen dari transaksi ke sumber dana 3.
    -   Aturan 3 (Prioritas 3): mengalokasikan 100 persen dari transaksi ke sumber dana 1.

Konfigurasi ini berfungsi karena transaksi diperiksa terhadap aturan dan batas untuk menentukan apakah salah satu dari mereka berlaku untuk transaksi. Jika tidak ada aturan atau batas tertentu berlaku untuk transaksi, semua aturan transaksi berlaku. Aturan semua transaksi cocok dengan semua transaksi. 

Jika aturan ditemukan sesuai dengan transaksi, maka persentase yang telah dialokasikan pada aturan tersebut akan diterapkan terlebih dulu, namun hanya setelah kecocokan diperiksa terhadap batas yang telah diatur. Jika batas telah terpenuhi, dan dana sumber pendanaan habis, aturan pendanaan yang terkait dengan batas pendanaan diabaikan, dan program akan memeriksa aturan berikutnya yang berlaku. 

Dalam kasus tertentu, hanya sebagian dari transaksi yang dapat dialokasikan berdasarkan aturan. Hal ini mungkin terjadi karena batas tercapai bila transaksi dialokasikan. Dalam kasus ini, hanya jumlah tertentu yang dialokasikan berdasarkan aturan tersebut, seperti 50 persen ke setiap sumber pendanaan. Ini adalah kasus di aturan 1, yang dijelaskan sebelumnya di bagian ini. Sisanya dialokasikan menurut aturan berikutnya dalam urutan. 

Tabel berikut ini akan memeriksa skenario ini secara lebih rinci.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Rincian</strong></td>
</tr>
<tr class="even">
<td>Aturan pendanaan</td>
<td><ul>
<li>Aturan 1 (Prioritas 1): semua transaksi. Mengalokasikan dana sumber 2 pada 50% dan mendanai sumber 3 di 50%.</li>
<li>Aturan 2 (Prioritas 2): semua transaksi. Mengalokasikan dana sumber 3 di 100%.</li>
<li>Aturan 3 (Prioritas 2): semua transaksi. Mengalokasikan dana sumber 1 di 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Batas pendanaan</td>
<td><ul>
<li>batas Sumber pendanaan 1 = 10.000,00</li>
<li>batas Sumber pendanaan 2 = 500,00</li>
<li>batas Sumber pendanaan 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaksi 1</td>
<td><strong>Jumlah transaksi:</strong> 100,00<strong>pendanaan:</strong> transaksi dibayar berdasarkan aturan 1 saja, karena transaksi dibayar penuh setelah aturan 1 diterapkan. Transaksi ini didanai secara merata antara sumber pendanaan 2 dan sumber pendanaan 3.
<ul>
<li>Sumber pendanaan 2: 50,00</li>
<li>Sumber pendanaan 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaksi 2</td>
<td><strong>Jumlah transaksi:</strong> 5.000,00<strong>pendanaan:</strong> transaksi dibayar sesuai dengan ketiga aturan. <strong>Aturan 1</strong>
<ul>
<li>Sumber pendanaan 2: 450,00</li>
<li>Sumber pendanaan 3: 450,00</li>
</ul>
<strong>Aturan 2</strong>
<ul>
<li>Sumber pendanaan 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Aturan 3</strong>
<ul>
<li>Sumber pendanaan 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Total dana yang didistribusikan untuk setiap sumber pendanaan</td>
<td><ul>
<li>Sumber pendanaan 1: 3.850,00</li>
<li>Sumber pendanaan 2: 500,00</li>
<li>Sumber pendanaan 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Aturan penagihan
Ketika Anda menegosiasikan kontrak proyek dengan pelanggan, Anda menentukan bagaimana dan Kapan Anda dapat menagih pelanggan untuk bekerja pada suatu proyek. Setelah Anda mengkonfigurasi kontrak proyek dan proyek, Anda dapat mengkonfigurasi aturan penagihan untuk proyek. Aturan penagihan didasarkan pada persyaratan proyek yang ditentukan dalam kontrak proyek. Aturan penagihan yang dapat Anda buat tergantung pada persyaratan kontrak proyek dan jenis proyek, seperti waktu dan material atau harga tetap, yang Anda kaitkan dengan aturan penagihan. Anda dapat membuat lebih dari satu aturan penagihan untuk kontrak proyek. Anda juga dapat menetapkan aturan penagihan ke beberapa proyek yang terkait dengan kontrak proyek yang sama dan memiliki syarat penagihan yang serupa. 

Anda dapat mengkonfigurasi jenis aturan penagihan berikut:

-   **Unit pengiriman** – tagih pelanggan saat Anda menyelesaikan unit pengiriman. Anda menentukan unit pengiriman dalam kontrak.
-   **Progres** – menagih pelanggan saat Anda menyelesaikan persentase tertentu dari proyek. Anda dapat mengkonfigurasi aturan penagihan untuk menghitung secara otomatis persentase pekerjaan yang diselesaikan, atau Anda dapat secara manual menghitung persentase pekerjaan yang diselesaikan dan jumlah yang akan ditagih ke pelanggan.
-   **Tonggak pencapaian** –-tagih pelanggan untuk jumlah penuh tonggak pencapaian proyek saat tonggak tercapai.
-   **Ongkos** – tagih pelanggan untuk layanan Anda ditambah biaya manajemen, yang biasanya merupakan persentase dari biaya layanan.
-   **Waktu dan material** – tagih pelanggan untuk nilai waktu dan bahan yang digunakan pada proyek.

Untuk semua jenis aturan penagihan, Anda dapat menentukan persentase retensi yang dipotong dari faktur pelanggan hingga proyek mencapai tahapan yang disepakati. Persentase retensi pembayaran ditentukan dalam kontrak proyek. Jumlah dihitung berdasarkan, dan dikurangi dari, nilai total baris di faktur pelanggan. 

Untuk aturan penagihan **waktu dan material** dan **progres**, Anda dapat menetapkan kategori yang dikenakan biaya. Kategori yang dibebankan menunjukkan transaksi yang harus disertakan dalam faktur pelanggan. 

Ketika Anda siap untuk faktur pelanggan, jumlah faktur untuk proyek dihitung berdasarkan aturan penagihan, dan proposal proyek faktur dibuat. 

Bagian berikut menyediakan contoh yang menunjukkan cara mengkonfigurasi dan mengelola aturan penagihan untuk proyek.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Contoh: Buat aturan penagihan yang didasarkan pada jumlah unit yang dikirim

Organisasi Anda menandatangani perjanjian untuk menyediakan total lima sesi pelatihan kepada karyawan pelanggan dengan biaya 10.000 per sesi pelatihan. Anda menagih pelanggan setelah setiap sesi pelatihan. 

Saat mengkonfigurasi aturan penagihan untuk kontrak, Anda menggunakan nilai berikut:

-   Unit pengiriman adalah satu sesi pelatihan.
-   Harga unit adalah 10.000 per sesi pelatihan.
-   Jumlah total unit adalah lima sesi pelatihan.

Setelah menyelesaikan satu sesi pelatihan, Anda dapat membuat faktur untuk 10.000, untuk unit pertama yang dikirim, dan mengirim faktur kepada pelanggan.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Contoh: Buat aturan penagihan yang didasarkan pada persentase penyelesaian proyek yang ditentukan (penghitungan manual)

Organisasi Anda, sebuah firma konsultasi perangkat lunak, memasuki perjanjian dengan pelanggan untuk mengembangkan bagian dari produk yang sedang dikembangkan pelanggan. Organisasi Anda setuju untuk memberikan kode perangkat lunak selama periode enam bulan. Pelanggan setuju untuk membayar organisasi Anda Total 100.000 untuk pekerjaan. Anda membuat aturan penagihan untuk menagih pelanggan berdasarkan persentase pekerjaan yang diselesaikan pada proyek, sebagaimana ditentukan dalam kontrak.

-   Pada akhir bulan pertama, Anda bertemu dengan pelanggan untuk menentukan persentase pekerjaan yang diselesaikan. Setelah Anda dan pelanggan meninjau proyek, Anda memutuskan bahwa proyek 15 persen selesai.
-   Anda membuat faktur 15.000 (15 persen dari 100.000) dan mengirimkannya ke pelanggan.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Contoh: Buat aturan penagihan yang didasarkan pada persentase penyelesaian proyek yang ditentukan (penghitungan otomatis)

Organisasi Anda, firma pengembangan perangkat lunak, setuju untuk mengembangkan paket akuntansi penggajian untuk pelanggan senilai 30.000. Pelanggan setuju untuk membayar organisasi Anda berdasarkan persentase pekerjaan yang selesai. Anda memperkirakan bahwa biaya proyek adalah 20.000. Kontrak proyek menentukan kategori pekerjaan yang Anda gunakan dalam proses penagihan. Anda menyiapkan aturan penagihan yang menghitung jumlah faktur secara otomatis untuk persentase pekerjaan yang diselesaikan untuk setiap kategori. Anda mengkonfigurasi anggaran untuk setiap kategori:

-   **Pengembangan** – biaya 15.000 dan pendapatan 20.000
-   **Instalasi** – biaya 5.000 dan pendapatan 10.000

Bila Anda membuat faktur pelanggan untuk pertama kalinya, jumlah faktur akan dihitung secara otomatis berdasarkan informasi berikut:

-   Setelah sebulan, pekerja di proyek mengirimkan lembar waktu untuk proyek. Biaya pekerja jam adalah 5.000 untuk pengembangan dan 1.000 untuk penginstalan. Pekerjaan pembangunan 33 persen selesai (5.000 biaya aktual/15000 biaya anggaran), dan pekerjaan penginstalan 20 persen selesai (1.000 biaya aktual/5000 biaya anggaran).
-   Jumlah faktur 8.667 secara otomatis dihitung (33 persen dari 20.000 + 20 persen dari 10.000).
-   Anda membuat faktur 8.667 dan mengirimkannya ke pelanggan.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Contoh: Buat aturan penagihan yang didasarkan pada tonggak prestasi yang disepakati

Organisasi Anda, perusahaan konsultan manajemen, setuju untuk melakukan riset pasar untuk produk konsumen yang akan dijual pelanggan. Pelanggan setuju untuk menggunakan layanan selama periode tiga bulan, mulai Maret, dan setuju untuk membayar 50.000 organisasi Anda. Proyek ini memiliki tiga tonggak:

-   Tonggak 1: mengumpulkan data pelanggan – 31 Maret
-   Tonggak 2: analisis data konsumen – 30 April
-   Tonggak 3: proposal kelayakan produk – 31 Mei

Pelanggan setuju untuk membayar 10.000 organisasi Anda untuk tonggak pertama, 20.000 untuk tonggak kedua, dan 20.000 untuk tonggak ketiga. 

Saat Anda menyiapkan kontrak proyek, Anda setuju untuk menagih pelanggan berdasarkan tonggak yang telah diselesaikan. Penyiapan aturan penagihan mencakup langkah-langkah berikut:

-   Tentukan tonggak proyek.
-   Tentukan jumlah faktur pelanggan saat setiap tonggak selesai.

Ketika tonggak pertama selesai pada tanggal 31 Maret, Anda menandai tonggak prestasi sebagai selesai, dan kemudian membuat faktur untuk 10.000 dan mengirimkannya ke pelanggan. Anda tidak dapat membuat faktur untuk tonggak hingga Anda telah menandai tonggak prestasi sebagai selesai.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Contoh: Buat aturan penagihan yang didasarkan pada layanan ditambah biaya manajemen

Organisasi Anda, perusahaan konsultan manajemen, setuju untuk melakukan riset pasar untuk mengevaluasi kelangsungan hidup produk yang sedang dikembangkan oleh pelanggan, perusahaan ritel. Persyaratan perjanjian menentukan bahwa Anda akan memberikan layanan dari tiga konsultan manajemen teratas, yang akan melakukan penelitian berdasarkan waktu dan bahan. Pelanggan setuju untuk membayar 100 per jam, ditambah biaya 10 persen manajemen untuk jam konsultasi yang dibebankan ke proyek. 

Saat Anda menyiapkan kontrak proyek, buat aturan penagihan untuk menambahkan biaya manajemen 10 persen ke jam konsultasi yang dibebankan ke proyek. 

Bila Anda membuat faktur untuk pelanggan, pelanggan ditagih biaya manajemen 10 persen ditambah biaya jam konsultasi. Misalnya, jika tiga konsultan bekerja Total 200 jam pada proyek, faktur untuk 22.000 dibuat berdasarkan perhitungan berikut:

-   200 jam pada 100 per jam = 20.000
-   10 persen biaya manajemen = 2.000
-   Jumlah total faktur = 22.000

Jika biaya dapat dikenai pajak untuk pelanggan, dan Anda memilih grup pajak penjualan dalam kontrak proyek, grup pajak penjualan akan secara otomatis dimasukkan dalam aturan penagihan untuk biaya.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Contoh: Buat aturan penagihan untuk nilai waktu dan material

Organisasi Anda, sebuah firma konsultasi perangkat lunak, setuju untuk menyediakan lima konsultan teknis untuk mengerjakan proyek pengembangan perangkat lunak untuk pelanggan selama enam bulan berikutnya. Pelanggan setuju untuk membayar 150 untuk setiap jam konsultasi, ditambah biaya perlengkapan kantor. Organisasi Anda mengirimkan faktur kepada pelanggan pada akhir setiap bulan. 

Saat Anda menyiapkan kontrak proyek, Anda setuju untuk menagih pelanggan setiap bulan untuk waktu dan bahan pada proyek. Anda membuat aturan penagihan yang mencakup informasi berikut:

-   Periode kontrak adalah enam bulan.
-   Waktu konsultasi dihitung pada tingkat 150 per jam.
-   Persediaan kantor ditagih pada biaya, dan total biaya untuk proyek tidak boleh melebihi 10.000.
-   Anda membuat faktur pelanggan di akhir setiap bulan kalender selama proyek.

Selama bulan pertama, Total 800 jam dicatat dicatat oleh konsultan pada proyek. Biaya perlengkapan kantor yang dibebankan pada proyek adalah 2.000. Oleh karena itu, pada akhir bulan, Anda membuat faktur untuk 122.000, yang dihitung sebagai 800 jam di 150 per jam, plus 2.000 untuk perlengkapan kantor.





[!INCLUDE[footer-include](../includes/footer-banner.md)]