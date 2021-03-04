---
title: Faktur Antarperusahaan
description: Artikel ini menyediakan informasi dan contoh tentang faktur antarperusahaan untuk proyek.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078510"
---
# <a name="intercompany-invoicing"></a>Faktur Antarperusahaan

[!include [banner](../includes/banner.md)]

Artikel ini menyediakan informasi dan contoh tentang faktur antarperusahaan untuk proyek.

Organisasi Anda mungkin memiliki beberapa divisi, anak perusahaan, dan entitas hukum lainnya yang mentransfer produk dan layanan satu sama lain untuk proyek. Badan hukum yang menyediakan layanan atau produk disebut *entitas hukum yang meminjamkan* , dan entitas hukum yang menerima layanan atau produk disebut *entitas hukum yang meminjam*. 

Ilustrasi berikut menunjukkan skenario umum di mana dua entitas hukum, SI FR (entitas hukum yang meminjam) dan SI USA (entitas hukum yang meminjam) berbagi sumber daya untuk memberikan proyek untuk pelanggan A. Untuk skenario ini, SI FR dikontrak untuk memberikan pekerjaan kepada pelanggan A. 

[![Contoh Faktur Antarperusahaan](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Tujuannya adalah untuk membuat kontrol biaya, pengakuan pendapatan, pajak, dan harga transfer untuk transaksi proyek antarperusahaan lebih fleksibel dan bertenaga. Selain itu, kemampuan berikut diberikan:

-   Membuat faktur pelanggan terhadap proyek di entitas hukum yang meminjam dengan menggunakan lembar waktu antarperusahaan, pengeluaran, dan faktur vendor di entitas hukum yang meminjamkan.
-   Mendukung penghitungan pajak dan biaya tidak langsung.
-   Menunda pengakuan pendapatan dalam entitas hukum yang meminjamkan dan bila entitas hukum yang meminjam harus mengakui biaya.
-   Mengakumulasikan pendapatan pekerjaan dalam proses (WIP) dalam entitas hukum yang meminjamkan.
-   Mengatur transfer harga yang dapat didasarkan pada berbagai model harga. Berikut adalah beberapa contoh:
    -   **Kuantitas** – jumlah yang Anda masukkan di bidang **harga** adalah biaya aktual per kuantitas atau unit.
    -   **Jumlah Tagihan** -harga/biaya per transaksi ditambah jumlah biaya yang Anda masukkan pada bidang **harga**.
    -   **Persentase biaya** – harga transfer adalah harga/biaya per transaksi dikalikan dengan persentase biaya yang Anda masukkan dalam bidang **harga**.
    -   **Persentase harga penjualan** – persentase dari harga penjualan yang ditransfer ke entitas hukum yang meminjamkan.
    -   **Jumlah di bawah harga penjualan** -jumlah yang ditahan entitas hukum yang meminjam dari harga penjualan sebelum transfer ke entitas hukum yang meminjamkan.
    -   **Rasio kontribusi** – jumlah yang Anda masukkan dalam bidang **harga** adalah rasio kontribusi, yang dinyatakan sebagai persentase dari harga penjualan.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Contoh 1: Konfigurasikan parameter untuk faktur Antarperusahaan
Dalam contoh ini, USSI adalah entitas hukum yang meminjamkan, dan sumber dayanya melaporkan waktu terhadap entitas hukum yang meminjam, FRSI, yang memiliki kontrak dengan pelanggan akhir. Jam dan biaya yang dapat dimasukkan oleh laporan karyawan USSI dalam faktur proyek yang dihasilkan FRSI. Selain itu, ada sumber ketiga transaksi yang bisa berasal dari entitas hukum yang meminjamkan (USSI dalam contoh ini) saat menyediakan layanan vendor bersama ke anak perusahaan (seperti FRSI) dan kemudian meneruskan biaya tersebut ke proyek dalam anak perusahaan tersebut. Semua dokumen faktur yang cocok dan penghitungan pajak diselesaikan oleh keuangan. 

Untuk contoh ini, FRSI harus pelanggan di entitas hukum USSI, dan USSI harus vendor di entitas hukum FRSI. Selanjutnya, Anda dapat mengkonfigurasi relasi antarperusahaan di antara dua entitas hukum. Prosedur berikut menunjukkan cara mengkonfigurasi parameter sehingga entitas hukum dapat berpartisipasi dalam faktur antarperusahaan.

1. Mengkonfigurasi FRSI sebagai pelanggan di entitas hukum USSI, dan mengatur USSI sebagai vendor di entitas hukum FRSI. Terdapat tiga titik masuk untuk langkah yang diperlukan untuk tugas ini.

   | Langkah |                                                       Titik Masuk                                                        |                                                                                                                                                                                               Deskripsi                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Di USSI, klik <strong>piutang</strong> &gt; <strong>Pelanggan</strong> &gt; <strong>semua pelanggan</strong>. |                                                                                                                                                                  Buat rekaman pelanggan baru untuk FRSI, dan pilih grup pelanggan.                                                                                                                                                                  |
   |  B   |    Di FRSI, klik <strong>Hutang Dagang</strong> &gt; <strong>vendor</strong> &gt; <strong>semua vendor</strong>.     |                                                                                                                                                                    Buat rekaman vendor baru untuk USSI, dan pilih grup vendor.                                                                                                                                                                    |
   |  C   |                                  Di FRSI, buka rekaman vendor yang baru saja Anda buat.                                  | Pada panel tindakan, pada tab <strong>Umum</strong>, di grup <strong>Konfigurasi</strong>, klik <strong>Antarperusahaan</strong>. Pada halaman <strong>antarperusahaan</strong>, pada tab <strong>relasi perdagangan</strong>, atur penggeser <strong>aktif</strong> ke <strong>ya</strong>. Di bidang <strong>perusahaan pelanggan</strong>, pilih rekaman Pelanggan yang Anda buat di langkah A. |


2. Klik **manajemen proyek dan akuntansi** &gt; **Konfigurasi** &gt; **parameter akuntansi manajemen proyek** , dan kemudian klik tab **antarperusahaan**. Cara Anda mengkonfigurasi parameter tergantung pada apakah Anda adalah entitas hukum yang meminjam atau entitas hukum yang meminjamkan.
   -   Jika Anda entitas hukum yang meminjam, pilih kategori pengadaan yang harus digunakan untuk mencocokkan faktur vendor, yang dihasilkan secara otomatis.
   -   Jika Anda adalah badan hukum yang meminjamkan, untuk setiap entitas yang meminjam, pilih kategori proyek default untuk setiap jenis transaksi. Kategori proyek digunakan untuk konfigurasi pajak bila kategori yang ditagih dalam transaksi antarperusahaan hanya ada di entitas hukum yang meminjam. Anda dapat memilih untuk mengakumulasikan pendapatan untuk transaksi antarperusahaan. Akrual ini dilakukan saat transaksi dikirim, dan kemudian dibalik saat faktur antarperusahaan dikirim.

3. Klik **manajemen proyek dan akuntansi** &gt; **konfigurasi** &gt; **Harga** &gt; **harga transfer**.
4. Pilih mata uang, jenis transaksi, dan model transfer harga. Mata uang yang digunakan pada faktur adalah mata uang yang dikonfigurasi dalam rekaman pelanggan untuk entitas hukum yang meminjam di entitas hukum yang meminjamkan. Mata uang digunakan untuk mencocokkan entri dalam tabel transfer harga.
5. Klik **Buku besar umum** &gt; **penataan posting** &gt; **akuntansi antarperusahaan** , dan atur hubungan untuk USSI dan FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Contoh 2: membuat dan memposting lembar waktu Antarperusahaan
USSI, entitas hukum yang meminjamkan, harus membuat dan memposting lembar waktu untuk proyek dari FRSI, entitas hukum yang meminjam. Terdapat dua titik masuk untuk langkah yang diperlukan untuk tugas ini.

| Langkah | Titik Masuk                                                                       | Deskripsi                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Manajemen proyek dan akuntansi** &gt; **lembar waktu** &gt; **Semua lembar waktu** | Membuat lembar waktu baru. Pada baris lembar waktu, di bidang **entitas hukum** , pilih **FRSI**. Di bidang **id proyek** , pilih proyek di FRSI. Masukkan jam untuk setiap hari dalam seminggu. |
| B    | Halaman **lembar waktu**                                                                | Setelah alur kerja berjalan, posting lembar waktu, dan buat catatan nomor voucher.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Contoh 3: membuat dan memposting faktur vendor Antarperusahaan
USSI, entitas hukum yang meminjamkan, harus membuat dan memposting faktur vendor antarperusahaan untuk proyek dari FRSI, entitas hukum yang meminjam. Faktur vendor ini menunjukkan tenaga kerja alihdaya dan pengeluaran yang dilakukan oleh vendor yang dibayar oleh USSI. Terdapat dua titik masuk untuk langkah yang diperlukan untuk tugas ini.

| Langkah | Titik Masuk                                                                                      | Deskripsi                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **utang dagang** &gt; **faktur** &gt; **buka vendor faktur** &gt; **Faktur vendor baru** | Buat faktur vendor baru, dan masukkan layanan yang diperoleh atas nama proyek FRSI.                                                                                                                                                                                  |
| B    | Halaman **faktur vendor**                                                                      | Masukkan baris yang menunjukkan layanan alihdaya atas nama FRSI. Pada fasttab **rincian baris** , pada tab **proyek** untuk baris faktur, di bidang **perusahaan proyek** , masukkan **FRSI**. Masukkan proyek dan informasi yang terkait. Kemudian posting faktur vendor. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Contoh 4: membuat dan memposting faktur Antarperusahaan
USSI, entitas hukum pinjaman, harus membuat dan memposting faktur antarperusahaan. Terdapat dua titik masuk untuk langkah yang diperlukan untuk tugas ini.

| Langkah | Titik Masuk                                                                                             | Deskripsi                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Manajemen proyek dan akuntansi** &gt; **faktur proyek** &gt; **faktur pelanggan antarperusahaan**  | Klik **baru** untuk membuka halaman **Buat faktur antarperusahaan**.                                                                                  |
| B    | **Manajemen proyek dan akuntansi** &gt; **faktur proyek** &gt; **faktur pelanggan antarperusahaan** | Pada halaman **Buat faktur antarperusahaan** , masukkan entitas hukum, tentukan transaksi yang harus disertakan, lalu klik **Cari**. |
| C    | **Manajemen proyek dan akuntansi** &gt; **faktur proyek** &gt; **faktur pelanggan antarperusahaan** | Pilih transaksi untuk faktur, atau klik **Pilih Semua** untuk menagih semua transaksi dalam daftar, lalu klik **OK**.                  |
| D    | Halaman **faktur antarperusahaan**                                                                       | Proposal faktur pelanggan antarperusahaan ditampilkan.                                                                                             |
| E    | Halaman **faktur antarperusahaan**                                                                       | Klik **posting**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Contoh 5: posting faktur vendor dan tagih pelanggan
Ketika entitas hukum yang meminjamkan, USSI, memposting faktur pelanggan antarperusahaan, yang faktur vendor tertunda yang cocok dibuat di entitas hukum yang meminjamkan, FRSI. Setelah faktur vendor ini dikirim, FRSI juga menagih pelanggan proyek selama jam-jam yang USSI masukkan. Terdapat tiga titik masuk untuk langkah yang diperlukan untuk tugas ini.

| Langkah | Titik Masuk                                                                                        | Deskripsi                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **utang dagang** &gt; **faktur** &gt; **faktur vendor tertunda**                            | Periksa faktur untuk memverifikasi bahwa nilai lembar waktu disertakan, dan kemudian posting faktur vendor.                  |
| B    | **Manajemen proyek dan akuntansi** &gt; **faktur proyek** &gt; **proposal faktur proyek** | Buat faktur proyek baru untuk proyek, dan Verifikasikan bahwa transaksi jam yang diposting ditampilkan.            |
| C    | Halaman **faktur proyek**                                                                       | Pilih faktur proyek, lalu klik **Lihat rincian** untuk meninjau jumlah biaya dan penjualan. Kemudian posting faktur. |


Untuk informasi lebih lanjut, lihat [konfigurasi faktur proyek antarperusahaan](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]