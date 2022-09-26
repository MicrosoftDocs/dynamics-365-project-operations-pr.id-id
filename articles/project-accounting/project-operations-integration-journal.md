---
title: Jurnal integrasi dalam Project Operations
description: Artikel ini menyediakan informasi tentang bekerja dengan jurnal Integrasi dalam Operasi Proyek.
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

Waktu, pengeluaran, biaya, dan entri material membuat **Transaksi aktual** yang mewakili pandangan operasional pekerjaan yang diselesaikan terhadap suatu proyek. Dynamics 365 Project Operations menyediakan alat kepada akuntan untuk meninjau transaksi dan menyesuaikan atribut akuntansi sesuai kebutuhan. Setelah peninjauan dan penyesuaian selesai, transaksi diposting ke buku besar pembantu proyek dan buku besar Umum. Seorang akuntan dapat melakukan kegiatan ini menggunakan **jurnal Project Operations Integration** (**Dynamics 365 Finance** > **Project management and accounting** > **Journals** > **Project Operations Integration** journal.

![Alur jurnal integrasi.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Membuat rekaman dalam Jurnal integrasi Project Operations

Rekaman dalam jurnal Integrasi Project Operations dibuat menggunakan proses berkala, **Impor dari tabel penahapan**. Anda dapat menjalankan proses ini dengan masuk ke **Dynamics 365 Finance** > **Project manajemen dan akuntansi** > **Impor Integrasi** > **Operasi Proyek Berkala** > **dari tabel** pementasan. Anda dapat menjalankan proses secara interaktif atau mengonfigurasi proses untuk berjalan di latar belakang sesuai kebutuhan.

Ketika proses berkala berjalan, setiap aktual yang belum ditambahkan ke jurnal Integrasi Project Operations ditemukan. Baris jurnal untuk setiap transaksi aktual dibuat.
Sistem mengelompokkan baris jurnal ke dalam jurnal terpisah berdasarkan nilai yang dipilih dalam **unit Periode pada bidang jurnal** Integrasi Operasi Proyek (**Manajemen Proyek Keuangan** > **dan akuntansi** > **Pengaturan** > **Manajemen proyek dan parameter** akuntansi, **Operasi Proyek pada tab Dynamics 365 Customer Engagement**). Nilai yang mungkin untuk bidang ini meliputi:

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
    - Jika **kategori** Transaksi tidak diatur dalam Project actual, sistem menggunakan nilai di **bidang default** kategori Project pada **tab Project Operations on Dynamics 365 Customer Engagement** pada **halaman Project management and accounting parameters**.
  - Bidang **sumber daya** mewakili sumber daya proyek yang terkait dengan transaksi ini. Sumber daya digunakan sebagai referensi dalam proposal faktur proyek untuk pelanggan.
  - Bidang **Nilai tukar** default dari **nilai tukar** Mata Uang yang ditetapkan dalam Dynamics 365 Finance. Jika konfigurasi nilai tukar tidak ada, proses periodik **impor dari penahapan** tidak akan menambahkan rekaman ke jurnal dan pesan kesalahan akan ditambahkan ke log eksekusi pekerjaan.
  - Bidang **properti baris** mewakili jenis penagihan dalam aktual proyek. Properti baris dan pemetaan jenis penagihan ditentukan pada **tab Operasi Proyek pada Dynamics 365 Customer Engagement** pada **halaman Manajemen proyek dan parameter** akuntansi.

Hanya atribut akuntansi berikut dapat diperbarui di baris jurnal integrasi Project Operations:

- **Grup pajak penjualan penagihan** dan **grup pajak penjualan item tagihan**
- **Dimensi keuangan** (menggunakan tindakan **mendistribusikan jumlah**)

Baris jurnal integrasi dapat dihapus. Namun, setiap baris yang tidak diposting akan dimasukkan ke dalam jurnal lagi setelah Anda menjalankan **kembali Proses periodik Impor dari pementasan**.

### <a name="post-the-project-operations-integration-journal"></a>Posting jurnal integrasi Operasi Proyek

Ketika Anda memposting jurnal integrasi, transaksi buku besar pembantu proyek dan buku besar umum dibuat. Ini digunakan di faktur pelanggan hilir, pengakuan pendapatan dan pelaporan keuangan.

Jurnal integrasi Operasi Proyek yang dipilih dapat diposting dengan menggunakan **Post** di halaman jurnal integrasi Operasi Proyek. Semua jurnal dapat diposting secara otomatis dengan menjalankan proses di **jurnal integrasi Integrasi** > **Operasi Proyek Berkala** > **Pasca** Operasi Proyek.

Posting dapat dilakukan secara interaktif atau dalam batch. Perhatikan bahwa semua jurnal yang memiliki lebih dari 100 baris akan secara otomatis diposting dalam satu batch. Untuk kinerja yang lebih baik ketika jurnal yang memiliki banyak baris diposting dalam satu batch, aktifkan **jurnal integrasi Pasca Operasi Proyek menggunakan fitur beberapa tugas** batch di **ruang kerja Manajemen** fitur. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Mentransfer semua baris yang memiliki kesalahan posting ke jurnal baru

> [!NOTE]
> Untuk menggunakan kemampuan ini, aktifkan **Fitur Transfer semua baris dengan kesalahan posting ke jurnal integrasi** Operasi Proyek baru di **ruang kerja Manajemen** fitur.

Fitur ini membantu meningkatkan pengalaman dengan jurnal integrasi Operasi Proyek. Saat diaktifkan, masalah waktu tulis ganda dan masalah penyiapan tidak lagi mencegah jurnal yang valid diposting. Selama posting ke jurnal integrasi Operasi Proyek, sistem memvalidasi setiap baris dalam jurnal. Ini memposting semua baris yang tidak memiliki kesalahan dan membuat jurnal baru untuk semua baris yang memiliki kesalahan posting.

Untuk meninjau jurnal yang memiliki baris kesalahan posting, buka **Jurnal** integrasi Operasi Proyek manajemen dan akuntansi \>**Jurnal** \>**·**, dan filter daftar jurnal dengan **menggunakan bidang Jurnal** asli. Ilustrasi berikut menunjukkan contoh di mana jurnal di **halaman jurnal** integrasi Operasi Proyek telah difilter dengan cara ini.

![Jurnal asli ditampilkan di halaman jurnal integrasi Project Operations.](./media/transferLines-originalJournal.png)

Jika pekerjaan batch berkala dikonfigurasi untuk memposting jurnal integrasi, posting akan di-reattempted, dan jurnal akan diposting jika masalah waktu telah diperbaiki. Setiap jurnal yang tersisa harus diselidiki secara manual dengan meninjau log dan mengambil tindakan yang diperlukan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
