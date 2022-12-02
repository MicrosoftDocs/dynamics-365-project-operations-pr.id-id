---
title: Jurnal integrasi dalam Project Operations
description: Artikel ini memberikan informasi tentang bekerja dengan jurnal Integrasi dalam Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541081"
---
# <a name="integration-journal-in-project-operations"></a>Jurnal integrasi dalam Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Entri waktu, pengeluaran, biaya, dan materi membuat transaksi **Aktual** yang mewakili tampilan operasional pekerjaan yang diselesaikan terhadap proyek. Dynamics 365 Project Operations menyediakan alat kepada akuntan untuk meninjau transaksi dan menyesuaikan atribut akuntansi sesuai kebutuhan. Setelah peninjauan dan penyesuaian selesai, transaksi diposting ke buku besar pembantu proyek dan buku besar Umum. Akuntan dapat melakukan aktivitas ini menggunakan jurnal **Integrasi Project Operations** (**Dynamics 365 Finance** > **Manajemen dan akuntansi proyek** > **Jurnal** > **junal Integrasi Project Operations**.

![Alur jurnal integrasi.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Membuat rekaman dalam Jurnal integrasi Project Operations

Rekaman dalam jurnal Integrasi Project Operations dibuat menggunakan proses berkala, **Impor dari tabel penahapan**. Anda bisa menjalankan proses ini dengan membuka **Dynamics 365 Finance** > **Manajemen dan akuntansi proyek** > **Periodik** > **Integrasi Project Operations** > **Impor dari tabel penahapan**. Anda dapat menjalankan proses secara interaktif atau mengonfigurasi proses untuk berjalan di latar belakang sesuai kebutuhan.

Ketika proses berkala berjalan, setiap aktual yang belum ditambahkan ke jurnal Integrasi Project Operations ditemukan. Baris jurnal untuk setiap transaksi aktual dibuat.
Sistem ini mengelompokkan baris jurnal ke dalam jurnal terpisah berdasarkan nilai yang dipilih dalam bidang **Unit periode di jurnal Integrasi Project Operations** (tab **Finance** > **Manajemen dan akuntansi proyek** > **Pengaturan** > **Parameter manajemen proyek dan akuntansi**, **Project Operations pada Dynamics 365 Customer Engagement**). Nilai yang mungkin untuk bidang ini meliputi:

  - **Hari**: Aktual dikelompokkan menurut tanggal transaksi. Jurnal terpisah dibuat untuk setiap hari.
  - **Bulan**: Aktual dikelompokkan menurut bulan kalender. Jurnal terpisah dibuat untuk setiap bulan.
  - **Tahun**: Aktual dikelompokkan menurut bulan tahun. Jurnal terpisah dibuat untuk setiap tahun.
  - **Semua**: Semua transaksi aktual disertakan dalam jurnal integrasi yang sama. Jika jurnal tidak tersedia ketika proses berkala berjalan, misalnya jika jurnal sedang dalam proses memposting transaksi, jurnal baru dibuat.

Baris jurnal dibuat berdasarkan aktual proyek. Daftar berikut ini mencakup beberapa aturan default dan transformasi yang lebih penting:

  - Setiap transaksi aktual proyek memiliki baris dalam jurnal Integrasi Project Operations. Biaya dan transaksi penjualan yang tidak tertagih untuk jenis penagihan waktu dan material ditampilkan pada baris terpisah.
  - Bidang **Tanggal** menunjukkan tanggal transaksi. Bidang **Tanggal akuntansi** menunjukkan tanggal di mana transaksi dicatat ke buku besar. Jika tanggal akuntansi berada dalam [periode keuangan tertutup](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), dan parameter **secara otomatis menetapkan tanggal akuntansi ke periode buku besar terbuka** ditetapkan pada tab **Keuangan** dari halaman parameter **manajemen proyek dan akuntansi**, sistem akan menyesuaikan tanggal akuntansi transaksi ke tanggal pertama dalam periode buku besar terbuka berikutnya.
  - Kolom **Voucher** menunjukkan nomor voucher untuk setiap transaksi aktual. Urutan nomor voucher didefinisikan pada tab **Urutan angka**, pada halaman parameter **manajemen Proyek dan akuntansi**. Setiap baris diberi nomor baru. Setelah voucher diposting, Anda dapat melihat bagaimana biaya dan transaksi penjualan yang belum ditagih terkait dengan memilih **voucher terkait** pada halaman **transaksi voucher**.
  - Bidang **kategori** mewakili transaksi proyek dan di-default berdasarkan Kategori transaksi untuk aktual proyek terkait.
    - Jika **kategori transaksi** diatur dalam aktual proyek dan **kategori proyek** ada di entitas hukum tertentu, kategori di-default ke kategori proyek ini.
    - Jika **Kategori transaksi** tidak diatur dalam aktual Proyek, sistem menggunakan nilai dalam bidang **Default kategori proyek** pada tab **Project Operations pada Dynamics 365 Customer Engagement** di halaman **Parameter manajemen dan akuntansi proyek**.
  - Bidang **sumber daya** mewakili sumber daya proyek yang terkait dengan transaksi ini. Sumber daya digunakan sebagai referensi dalam proposal faktur proyek untuk pelanggan.
  - Default bidang **Tarif penukaran** dari **Tarif penukaran mata uang** diatur dalam Dynamics 365 Finance. Jika konfigurasi nilai tukar tidak ada, proses periodik **impor dari penahapan** tidak akan menambahkan rekaman ke jurnal dan pesan kesalahan akan ditambahkan ke log eksekusi pekerjaan.
  - Bidang **properti baris** mewakili jenis penagihan dalam aktual proyek. Pemetaan baris properti dan jenis tagihan ditentukan dalam tab **Project Operations pada Dynamics 365 Customer Engagement** di halaman **Parameter manajemen dan akuntansi proyek**.

Hanya atribut akuntansi berikut dapat diperbarui di baris jurnal integrasi Project Operations:

- **Grup pajak penjualan penagihan** dan **grup pajak penjualan item tagihan**
- **Dimensi keuangan** (menggunakan tindakan **mendistribusikan jumlah**)

Baris jurnal integrasi bisa dihapus. Namun, setip baris yang belum diposting akan dimasukkan ke dalam jurnal lagi setelah Anda menjalankan ulang proses periodik **Impor dari penahapan**.

### <a name="post-the-project-operations-integration-journal"></a>Posting jurnal Integrasi Project Operations

Ketika Anda memposting jurnal integrasi, transaksi buku besar pembantu proyek dan buku besar umum dibuat. Ini digunakan di faktur pelanggan hilir, pengakuan pendapatan dan pelaporan keuangan.

Jurnal integrasi Project Operations yang dipilih dapat diposting menggunakan **Posting** pada halaman jurnal integrasi Project Operations. Semua jurnal dapat secara otomatis diposting dengan menjalankan proses di **Periodik** > **Integrasi Project Operations** > **Posting jurnal integrasi Project Operations**.

Memposting dapat dilakukan secara interaktif atau dalam batch. Perlu diketahui bahwa semua jurnal yang memiliki lebih dari 100 baris akan secara otomatis diposting dalam batch. Untuk kinerja yang lebih baik bila jurnal yang memiliki banyak baris diposting dalam batch, aktifkan fitur **Posting jurnal integrasi Project Operations menggunakan beberapa tugas bacth** di dalam ruang kerja **Manajemen Fitur**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Mengalihkan semua baris yang memiliki kesalahan posting ke jurnal baru

> [!NOTE]
> Untuk menggunakan kemampuan ini, aktifkan fitur **Transfer semua baris dengan kesalahan posting ke fitur jurnal integrasi Project Operations baru** di ruang ruang kerja **Manajemen Fitur**.

Fitur ini akan membantu meningkatkan pengalaman dengan jurnal integrasi Project Operations. Bila diaktifkan, masalah penentuan waktu menulis dua kali dan masalah pengaturan tidak lagi mencegah jurnal yang valid untuk diposting. Selama memposting ke jurnal integrasi Project Operations, sistem memvalidasi setiap baris di jurnal. Ini memposting semua baris yang tidak memiliki kesalahan dan membuat jurnnal baru untuk semua baris yang memiliki keselahan memposting.

Untuk meninjau jurnal yang memiliki baris kesalahan memposting, buka **Manajeman dan akuntansi proyek** \> **Jurnal** \> **Jurnal Project Operations**, dan filter daftar jurnal menggunakan bidang **Jurnal asli**. Ilustrasi berikut menunjukkan contoh di mana jurnal pada halaman jurnal integrasi **Project Operations** telah difilter dengan cara ini.

![Jurnal asli ditampilkan pada halaman jurnal integrasi Project Operations.](./media/transferLines-originalJournal.png)

Jika pekerjaan batch periodik dikonfigurasi untuk memposting jurnal integrasi, akan dicoba memposting lagi, dan jurnal akan diposting jika masalah waktu sudah diperbaiki. Setiap jurnal yang tersisa harus diselidiki secara manual dengan meninjau catatan dan melakukan tindakan apa pun yang diperlukan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
