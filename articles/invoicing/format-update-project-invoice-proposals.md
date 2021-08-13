---
title: Mengelola proposal faktur proyek
description: Laporan topik ini memberikan rincian tentang memproses faktur yang dihadapi pelanggan dengan Project Operations untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989915"
---
# <a name="manage-project-invoice-proposals"></a>Mengelola proposal faktur proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Proposal faktur proyek dapat diproses oleh departemen penagihan Anda bila dua kondisi berikut terpenuhi:

  - Manajer proyek mengkonfirmasikan faktur proforma dalam Microsoft Dataverse.
  - Semua transaksi penjualan belum tertagih waktu dan material yang tercakup dalam faktur proforma diposting menggunakan jurnal Integrasi Dynamics 365 **Project Operations**.

Gunakan langkah-langkah berikut untuk menyelesaikan proposal faktur proyek di Dynamics 365 Finance.

1. Periksa informasi penagihan untuk transaksi waktu dan material, lalu posting jurnal **Integrasi Project Operations**.
2. Periksa informasi penagihan untuk tahapan penagihan harga tetap.
3. Tinjau dan format proposal faktur proyek.
4. Posting dan cetak faktur proyek.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Mengelola informasi penagihan di jurnal Integrasi Project Operations

Aktual proyek yang dibuat Dataverse ditinjau dan diposting di Finance oleh akuntan Proyek. Untuk informasi lebih lanjut tentang bekerja dengan jurnal Integrasi, lihat [jurnal integrasi dalam Project Operations](../project-accounting/project-operations-integration-journal.md).

Aktual biaya dan aktual penjualan belum tertagih ditambahkan ke jurnal Integrasi sebagai baris terpisah:

  - Harga biaya unit dan jumlah biaya pada aktual Biaya di-default dari transaksi biaya aktual proyek di Dataverse.
  - Harga penjualan unit dan jumlah penjualan pada default transaksi penjualan Belum tertagih dari transaksi penjualan aktual proyek belum tertagih dalam Dataverse.

### <a name="billing-sales-tax"></a>Pajak penjualan penagihan

Penghitungan pajak penjualan untuk penagihan ditentukan oleh kombinasi bidang **grup pajak penjualan penagihan** dan **grup pajak penjualan item penagihan** di rekaman penjualan belum tertagih di baris jurnal **Integrasi Project Operations**. Sistem di-default terhadap nilai bidang ini berdasarkan pengaturan pada tab **Keuangan** pada halaman **parameter manajemen proyek dan akuntansi**.

- **Metode grup pajak penjualan** menentukan logika default grup pajak penjualan penagihan:
  
  - **Proyek**: Akan selalu men-default grup pajak penjualan penagihan dari proyek. Anda dapat memeriksa atau mengubah grup pajak penjualan penagihan default pada proyek dengan memilih **Tampilkan akuntansi default** pada halaman **Semua Proyek**.
  - **Kontrak Proyek**: Akan selalu men-default grup pajak penjualan penagihan dari kontrak proyek. Anda dapat memeriksa atau mengubah grup pajak penjualan default pada kontrak proyek dengan memilih **Tampilkan akuntansi default** pada halaman **Kontrak Proyek**.
  - **Pelanggan**: Akan selalu men-default grup pajak penjualan penagihan dari pelanggan.
  - **Pencarian**: Akan mencari di semua entitas di atas dan memilih nilai pertama yang tersedia. Pencarian dimulai dengan entitas **Proyek**, kemudian entitas **kontrak Proyek**, dan akhirnya entitas **Pelanggan**.

- **Metode grup pajak penjualan item** menentukan logika default grup pajak penjualan item penagihan:
  
  - Untuk waktu, pengeluaran, dan jenis transaksi biaya, grup pajak penjualan item penagihan akan selalu default dari entitas **kategori Proyek**.
  - Untuk jenis transaksi material, grup pajak penjualan item penagihan di-default berdasarkan pengaturan **metode grup pajak penjualan Item** di **parameter manajemen proyek dan akuntansi**. Nomor item men-default grup pajak penjualan item dari entitas **produk yang dirilis**. Nomor kategori men-default grup pajak penjualan item dari entitas **Kategori proyek**.

### <a name="financial-dimensions"></a>Dimensi keuangan

Dimensi keuangan untuk rekaman penjualan yang belum tertagih dalam **jurnal Integrasi Project Operations** di-default dari entitas **Proyek**. Dimensi keuangan dapat ditinjau dan disesuaikan dengan memilih **Jumlah Distribusi**. Jika Anda perlu mengubah dimensi keuangan rekaman penjualan belum tertagih setelah faktur Integrasi diposting, namun sebelum faktur Proforma dikonfirmasi, buka **Semua Proyek** > **Kelola** > **Transaksi yang Diposting**, pilih transaksi, lalu pilih **Proses** > **Penyesuaian akuntansi**.

### <a name="exchange-rates"></a>Kurs

Mata uang transaksi belum tertagih di Dataverse digunakan sebagai mata uang transaksi di Finance dan dikonversi ke mata uang akuntansi perusahaan menggunakan nilai tukar yang ditentukan di Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Mengelola atribut keuangan tahapan penagihan 

Baris kontrak proyek yang menggunakan metode penagihan harga tetap ditagihkan melalui [tahapan harga tetap](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Akuntan proyek dapat meninjau tahapan penagihan di Finance dengan membuka **manajemen proyek dan akuntansi** > **Semua proyek** > **Kelola** > **transaksi kredit**.

### <a name="billing-sales-tax"></a>Pajak penjualan penagihan

**Grup pajak penjualan** dan nilai **grup pajak penjualan Item**  di-default dari pengaturan saat tahapan penagihan baru dibuat di Dataverse. Sistem men-default nilai-nilai tersebut ke bidang ini berdasarkan pengaturan pada tab **Keuangan** pada halaman **parameter manajemen proyek dan akuntansi**.

- **Metode grup pajak penjualan** menentukan logika default **grup pajak penjualan penagihan**:

    - **Proyek** akan selalu men-default grup pajak penjualan penagihan dari proyek. Anda dapat memeriksa atau mengubah grup pajak penjualan default pada proyek dengan memilih **Tampilkan akuntansi default** pada halaman **Semua Proyek**.
    - **Kontrak Proyek** Akan selalu men-default grup pajak penjualan penagihan dari kontrak proyek. Anda dapat memeriksa atau mengubah grup pajak penjualan default pada kontrak proyek dengan memilih **Tampilkan akuntansi default** pada halaman **Kontrak Proyek**.
    - **Pelanggan** Akan selalu di-default ke grup pajak penjualan penagihan dari pelanggan.
    - **Pencarian** Akan mencari di semua entitas di daftar ini dan memilih nilai pertama yang tersedia. Pencarian dimulai dengan entitas **Proyek**, kemudian entitas **kontrak Proyek**, dan kemudian entitas **Pelanggan**.

- **Grup pajak penjualan item tahapan harga tetap** digunakan sebagai nilai default pada bidang **grup pajak penjualan Item** untuk tahapan penagihan. Akuntan dapat memeriksa dan memodifikasi nilai ini pada halaman **transaksi Cicilan**. Sistem menggunakan nilai dari transaksi cicilan saat membuat baris proposal faktur proyek.
 

### <a name="financial-dimensions"></a>Dimensi keuangan

Dimensi keuangan default untuk tahapan penagihan harga tetap diatur pada baris kontrak Proyek. Buka **Kontrak proyek** > **Tampilkan akuntansi default** dan pada tab **Baris kontrak**, pilih **baris kontrak harga**, lalu atur nilai dimensi keuangan yang ingin Anda gunakan sebagai default.

Akuntan proyek dapat mengedit informasi dimensi keuangan dan pajak penjualan pada tahapan faktur hingga proposal faktur Proyek dibuat.


## <a name="create-project-invoice-proposals"></a>Buat proposal faktur proyek

Proposal faktur proyek dapat ditinjau dalam modul **manajemen Proyek dan akuntansi** dengan masuk ke proposal **faktur Proyek** > **Proposal faktur proyek**.

Header proposal faktur proyek dibuat di Finance saat faktur Proforma dikonfirmasi di Dataverse. Untuk rekonsiliasi yang lebih mudah, sistem menetapkan nomor proposal faktur proyek di finance ke nomor yang sama dengan ID faktur Proforma dalam Dataverse. Karena faktur Proforma tidak terkonfirmasi dalam urutan yang sama saat pembuatannya, urutan nomor proposal faktur proyek di Keuangan harus memungkinkan perubahan pada angka yang lebih rendah dan lebih tinggi. Konfigurasikan urutan angka menggunakan langkah-langkah berikut:

1. Di Finance,, buka urutan **Administrasi Organisasi** > **Urutan Nomor** > **Urutan nomor**.
2. Dalam Filter **Area**, pilih **Proyek**.
3. Dalam filter **Referensi**, pilih **proposal faktur**.
4. Gunakan bidang **Perusahaan** untuk memfilter setiap entitas hukum dengan integrasi Dataverse Project Operations diaktifkan.
5. Buka **rincian Urutan Nomor** dan pada rangkaian tab **Umum**:

    - **izinkan perubahan pengguna: Ke nomor yang lebih rendah** = **Ya**
    - **izinkan perubahan pengguna: Ke nomor yang lebih tinggi** = **Ya**

Baris proposal faktur proyek ditambahkan oleh sistem menggunakan proses periodik **Impor dari tabel penahapan** (**Manajemen proyek dan akuntansi** > **Berkala** > **integrasi Project Operations** > **Impor dari tabel penahapan**). Proses ini dapat dijalankan secara manual maupun menggunakan jadwal berkala. Sistem tidak akan menambahkan baris ke dokumen proposal faktur hingga semua baris siap ditagih. Transaksi waktu dan material siap ditagihkan hanya bila dikirim menggunakan jurnal **Integrasi Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Memformat dan mencetak proposal faktur

Akuntan proyek dapat menyesuaikan hasil cetak faktur proyek dengan menggunakan halaman **format proposal faktur** dan kemampuan manajemen cetak.

### <a name="format-invoice-proposals"></a>Memformat proposal faktur

Halaman **Format proposal faktur** memungkinkan mengelompokkan transaksi kustom untuk ditampilkan di faktur proyek pelanggan.

1. Pada halaman **proposal faktur proyek**, pilih **Cetak** > **Format Proposal faktur**.
2. Pilih **Baru** untuk membuat pengelompokan baru untuk printout faktur Proyek.
3. Pada bidang **Rincian/Ringkasan**, pilih pilihan untuk pengelompokan ini:

    - Pilih **Rincian** untuk mencetak rincian transaksi faktur pelanggan.
    - Pilih **Ringkasan** untuk mencetak ringkasan transaksi faktur pelanggan.

> [!NOTE]
> Pilihan pada bidang **Rincian/Ringkasan** pada halaman **Format proposal faktur** mengesampingkan pilihan yang dipilih di bidang **Format faktur** pada halaman **Proposal faktur** untuk mencetak faktur rinci atau faktur yang diringkas.

- Pilih baris transaksi yang akan disertakan di bagian ini pada tab **Transaksi yang Tersedia** dan pilih **Sertakan transaksi** untuk memindahkannya ke tab **Transaksi yang Dipilih**.
- Pilih **Pindahkan ke atas** dan **Pindahkan ke bawah** untuk mengubah urutan bagian.
- Pilih **Pratinjau cetak** untuk mempratinjau faktur berformat.

### <a name="print-management"></a>Manajemen cetak

Manajemen cetak menggunakan file laporan yang berbeda untuk dicetak, menentukan tujuan, dan menyesuaikan teks footer untuk faktur. Manajemen cetak dapat diatur pada tingkat modul, namun pengaturan ini dapat ditimpa untuk pelanggan, kontrak, atau proposal faktur tertentu. Untuk mengakses fungsi ini pada halaman **proposal faktur proyek**, pilih **Cetak** > **manajemen Cetak**.

Konfigurasi manajemen cetak ditampilkan sebagai tampilan pohon, dengan setiap tingkat node menampilkan dokumen yang tersedia untuk disesuaikan. Anda dapat menetapkan hasil cetak kustom pada tingkat dokumen proposal faktur, modul, pelanggan, atau kontrak. Untuk memodifikasi hasil cetak dokumen asli, perluas node yang diinginkan dan pilih **item Asli**. Pada bidang **Format laporan**, pilih format laporan yang akan digunakan untuk cetak. Anda dapat menggunakan format laporan kustom menggunakan [kerangka kerja Manajemen Dokumen Bisnis](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>posting proposal faktur

Setelah faktur ditinjau dan diedit, dan baris proposal faktur sangat memuaskan, periksa total faktur dan pajak penjualan. Di grup **Rincian**, pilih **Total**, lalu pilih **Posting** untuk memposting faktur.

Untuk melihat faktur sebelum posting, kosongkan kotak centang **Posting**. **Pro forma** akan dicetak pada faktur untuk menandakan bahwa ini adalah faktur sampel. Untuk mencetak faktur, centang kotak **Cetak faktur**.

Selain halaman **Proposal faktur**, proposal faktur juga dapat diposting dengan menjalankan pekerjaan berkala, **Posting proposal faktur**. Untuk menemukan pekerjaan ini, buka **Manajemen proyek dan akuntansi** > **Berkala** > **Faktur Proyek** > **Proposal faktur berkala**.

Halaman ini menampilkan semua proposal faktur yang siap diposting. Anda dapat menjadwalkan posting proposal faktur dengan memilih **Kumpulan**. Atur **parameter Pemrosesan kumpulan** ke **Ya** dan atur pengulangan pemrosesan kumpulan dengan memilih **Pengulangan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
