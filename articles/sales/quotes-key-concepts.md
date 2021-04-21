---
title: Kuotasi - Konsep utama
description: Topik ini memberikan informasi tentang kuotasi proyek dan kuotasi penjualan yang tersedia dalam Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 488c57527e6cc153093014438453001170f311dc
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663697"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Konsep unik untuk kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Di Dynamics 365 Project Operations, ada dua jenis kuotasi: proyek dan penjualan. Kedua jenis kuotasi ini berbeda dalam hal berikut:

- **Kisi untuk item baris**: Pada kuotasi penjualan, hanya ada satu kisi untuk item baris. Di kuotasi proyek, ada dua kisi untuk item baris. Satu kisi adalah untuk baris proyek dan lainnya adalah untuk baris produk.
- **Aktivasi dan revisi**: kuotasi penjualan mendukung aktivasi dan revisi. Proses ini tidak didukung pada kuotasi proyek.
- **Pesanan yang dilampirkan**: Anda dapat melampirkan beberapa pesanan ke kuotasi penjualan. Hanya satu kontrak proyek dapat dilampirkan ke kuotasi proyek.
- **Memenangkan kuotasi**: bila Anda memenangkan kuotasi penjualan, peluang terkait dapat tetap terbuka. Setelah kuotasi proyek dimenangkan, peluang terkait ditutup.
- **Bidang dan konsep**: Kuotasi penjualan tidak mencakup beberapa bidang dan konsep yang disertakan dalam kuotasi proyek. Bidang mencakup **unit kontrak**, **manajer akun**, dan **nama tagihan ke kontak**.  
- **Jenis**: Kuotasi penjualan dan kuotasi proyek juga diidentifikasi berdasarkan bidang berbasis rangkaian pilihan, **jenis**. Untuk kuotasi penjualan, bidang ini memiliki nilai **berbasis item**. Untuk kuotasi proyek, ia memiliki nilai **berbasis kerja**.

Topik ini berfokus pada rincian kuotasi proyek.

Kuotasi proyek dalam Project Operations dapat memiliki beberapa item baris atau baris kuotasi. Bahkan, kuotasi proyek memiliki dua kisi untuk item baris. Satu kisi adalah untuk baris berbasis proyek yang memungkinkan perkiraan rinci. Kisi lainnya adalah untuk lini berbasis produk menggunakan harga satuan sederhana dan pendekatan berbasis kuantitas.

- **Berbasis proyek**: nilai kuotasi ditentukan setelah Anda memperkirakan berapa banyak pekerjaan yang diperlukan. Anda dapat memperkirakan kerja pada tingkat tinggi, langsung sebagai rincian baris di bawah setiap baris kuotasi, atau berdasarkan perkiraan dari awal, dengan menggunakan proyek dan rencana proyek. Baris kuotasi berbasis proyek hanya ditemukan dalam kuotasi berbasis proyek yang dibuat menggunakan Project Operations. Baris kuotasi jenis ini adalah formulir kustom baris kuotasi tulis yang tersedia dalam Microsoft Dynamics 365 Sales.

- **Berbasis produk**: jumlah (nilai yang dikutip) ditentukan berdasarkan kuantitas unit yang terjual dan harga penjualan unit. Produk pada baris berbasis produk dapat berasal dari Katalog Produk dalam Sales, atau dapat berupa produk yang Anda tentukan. Baris kuotasi jenis ini juga tersedia pada kuotasi berbasis proyek yang dibuat menggunakan Project Operations.

Jumlah pada kuotasi adalah total di seluruh baris berbasis produk dan baris berbasis proyek.

> [!NOTE]
> Kuotasi dan baris kuotasi tidak diperlukan di Project Operations. Anda dapat memulai proses proyek dengan kontrak proyek (proyek yang dijual). Namun, peluang selalu diperlukan, terlepas dari Apakah Anda mulai dengan kuotasi atau kontrak proyek.

## <a name="project-based-quote-lines"></a>Baris kuotasi berbasis proyek

Baris kuotasi berbasis proyek dalam Project Operations memiliki metode penagihan berikut:

- Waktu dan bahan
- Harga Tetap

### <a name="time-and-material"></a>Waktu dan Material

Metode penagihan waktu dan material didasarkan pada konsumsi. Bila Anda memilih metode penagihan ini, pelanggan ditagih saat proyek menyebabkan biaya. Faktur dibuat pada frekuensi periodik berbasis tanggal. Selama proses penjualan, nilai yang dikutip dari komponen waktu dan material hanya memberikan perkiraan biaya akhir kepada pelanggan. Vendor tidak melakukannya sendiri untuk menyelesaikan proyek tepat pada nilai yang dikutip. Komponen waktu dan material meningkatkan risiko pelanggan. Pelanggan mungkin ingin menegosiasikan klausa tambahan yang tidak melebihi batas untuk meminimalkan risiko. Project Operations tidak mendukung pengaturan klausul yang tidak melebihi batas.

### <a name="fixed-price"></a>Harga Tetap

Pada metode penagihan harga tetap, vendor berkomitmen untuk memberikan proyek dengan biaya tetap kepada pelanggan. Pelanggan ditagih nilai yang dikutip dari baris kuotasi harga tetap, terlepas dari biaya yang ditimbulkan vendor untuk memberikan baris kuotasi tersebut. Nilai baris kuotasi harga tetap ditagih dengan salah satu cara berikut: 

- Sebagai jumlah bulat pada awal atau akhir proyek, atau saat tonggak waktu proyek tercapai. 
- Pada frekuensi berdasarkan tanggal dari angsuran yang sama dari nilai tetap pada baris kuotasi. Angsuran ini dikenal sebagai tonggak waktu periodik.
- Dengan angsuran yang memiliki nilai moneter yang selaras dengan kemajuan pekerjaan atau tonggak waktu tertentu yang dicapai dalam proyek. Dalam kasus ini, nilai masing-masing angsuran dapat berbeda, tetapi jumlah mereka semua harus sama dengan nilai tetap pada baris kuotasi.

Project Operations mendukung ketiga jenis jadwal faktur untuk baris kuotasi harga tetap.

## <a name="transaction-classification"></a>Klasifikasi Transaksi

Organisasi layanan profesional biasanya mengutip dan menagih pelanggan mereka berdasarkan klasifikasi biaya. Biaya diwakili oleh klasifikasi transaksi berikut:

- **Waktu**: klasifikasi ini mewakili biaya tenaga kerja atau waktu sumber daya manusia pada suatu proyek.
- **Pengeluaran**: klasifikasi ini mewakili semua jenis pengeluaran lain pada suatu proyek. Karena biaya dapat dikelompokkan secara luas, sebagian besar organisasi membuat subkategori, seperti perjalanan, Penyewaan Mobil, Hotel, atau perlengkapan kantor.
- **Biaya**: klasifikasi ini mewakili biaya tetap lain-lain, denda, dan item lainnya yang dibebankan kepada pelanggan. 
- **Pajak**: klasifikasi ini menunjukkan jumlah pajak yang ditambahkan pengguna saat mereka memasukkan pengeluaran.
- **Transaksi material**: klasifikasi ini merupakan aktual dari lini produk pada faktur proyek yang telah dikonfirmasi.
- **Tonggak waktu**: klasifikasi ini digunakan oleh logika penagihan harga tetap.

Satu atau lebih klasifikasi transaksi ini dapat diasosiasikan dengan masing-masing baris kuotasi. Setelah kuotasi dimenangkan, pemetaan antara klasifikasi transaksi dan baris kuotasi ditransfer ke baris kontrak.
  
Misalnya, kuotasi mungkin berisi dua baris kuotasi berikut: 

- Di sini berlaku pekerjaan konsultasi yang menggunakan metode penagihan waktu dan bahan serta klasifikasi waktu dan transaksi biaya. Misalnya, Semua transaksi waktu dan biaya untuk proyek contoh **penerapan Dynamics AX** ditagih pada pelanggan berdasarkan waktu dan materi yang digunakan. 
- Biaya perjalanan terkait yang menggunakan metode penagihan harga tetap. Misalnya, Semua biaya perjalanan untuk proyek contoh **penerapan Dynamics AX** ditagih pada nilai uang tetap.

> [!NOTE]
> Kombinasi dari proyek dan klasifikasi transaksi **waktu**, **pengeluaran**, dan **biaya** yang terkait dengan baris kuotasi atau baris kontrak harus unik. Jika kombinasi yang sama antara proyek dan kelas transaksi dikaitkan dengan lebih dari satu baris kontrak atau baris kuotasi, Project Operations tidak akan berfungsi dengan benar.

## <a name="billing-types"></a>Jenis Penagihan

Bidang **jenis penagihan** menentukan konsep ketertagihan. Ini adalah rangkaian pilihan yang memiliki nilai yang mungkin berikut:

- **Dikenakan biaya**: biaya yang Diperoleh dari peran/kategori ini adalah biaya langsung yang mendorong eksekusi proyek, dan pelanggan akan membayar untuk pekerjaan ini. Pembayaran dapat diberikan sebagai pengaturan waktu dan material atau harga tetap. Namun, karyawan yang menghabiskan waktu ini akan menerima kredit yang sesuai untuk pemanfaatan yang dapat ditagih.
- **Tidak dikenakan biaya**: biaya yang Diperoleh dari peran/kategori ini dianggap biaya langsung yang mendorong eksekusi proyek, meskipun pelanggan tidak menyadari fakta ini dan tidak akan membayar untuk pekerjaan ini. Karyawan yang menghabiskan waktu ini tidak akan dikreditkan dengan pemanfaatan yang dapat ditagih.
- **Gratis**: biaya yang diperoleh dari peran/kategori ini dianggap biaya langsung yang mendorong eksekusi proyek, dan pelanggan mengakui fakta ini. Karyawan yang menghabiskan waktu ini akan dikreditkan untuk pemanfaatan yang dapat ditagih. Namun, biaya ini tidak dibebankan kepada pelanggan.
- **Tidak tersedia**: biaya yang dikeluarkan pada proyek internal yang tidak memerlukan pelacakan pendapatan dilacak dengan menggunakan pilihan ini.

## <a name="invoice-schedule"></a>Jadwal faktur

Jadwal faktur adalah rangkaian tanggal saat pemfakturan untuk proyek terjadi. Anda dapat memilih untuk membuat jadwal faktur pada baris kuotasi. Setiap baris kuotasi dapat memiliki jadwal faktur tersendiri. Untuk membuat jadwal faktur, Anda harus menyediakan nilai atribut berikut:

- Tanggal mulai penagihan 
- Tanggal pengiriman yang menunjukkan tanggal berakhir penagihan pada proyek
- Frekuensi faktur

Ketiga nilai atribut ini digunakan untuk membuat rangkaian tanggal tentatif untuk membuat faktur.

## <a name="invoice-frequency"></a>Frekuensi faktur

Frekuensi faktur adalah entitas yang menyimpan nilai atribut yang membantu mengekspresikan frekuensi pembuatan faktur. Atribut berikut mengekspresikan atau menentukan entitas frekuensi faktur:

- **Periode**: bulanan, dua mingguan, dan periode mingguan didukung. 
- **Berjalan per periode**: untuk periode mingguan dan dua mingguan, Anda hanya dapat menentukan satu operasi per periode. Untuk periode bulanan, Anda dapat menentukan antara satu hingga empat operasi per periode. 
- **Hari berjalan**: hari saat faktur harus dijalankan. Anda dapat mengonfigurasikan atribut ini dengan dua cara:
  - **Hari kerja**: misalnya, Anda dapat menentukan bahwa faktur dijalankan setiap hari Senin atau setiap hari Senin kedua. Pelanggan yang harus menetapkan faktur untuk dijalankan pada hari kerja mungkin lebih suka konfigurasi semacam ini. 
  - **Hari Kalender**: misalnya, Anda dapat menentukan bahwa faktur dijalankan pada hari ketujuh dan dua puluh satu setiap bulan. Beberapa organisasi mungkin memilih konfigurasi semacam ini, karena membantu menjamin bahwa faktur di dijalankan pada jadwal tetap setiap bulan.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Jadwal faktur untuk baris kuotasi harga tetap

Untuk baris kuotasi harga tetap, Anda dapat menggunakan kisi **jadwal faktur** untuk membuat tonggak waktu penagihan yang sama dengan nilai baris kuotasi.

- Untuk membuat tonggak waktu penagihan yang terbagi rata, pilih frekuensi faktur, masukkan tanggal mulai penagihan pada baris kuotasi, dan pilih **tanggal selesai yang diminta** untuk kuotasi di bagian **ringkasan** header kuotasi. Kemudian pilih **Buat tonggak waktu periodik** untuk membuat tonggak waktu terpisah yang sama berdasarkan frekuensi faktur yang dipilih. 
- Untuk membuat tonggak penagihan Total, buat tonggak waktu, lalu masukkan nilai baris kuotasi sebagai jumlah tonggak waktu.
- Untuk membuat tonggak waktu penagihan yang didasarkan pada tugas tertentu dalam rencana proyek, buat tonggak waktu, dan Petakan ke elemen jadwal proyek dalam UI tonggak waktu penagihan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
