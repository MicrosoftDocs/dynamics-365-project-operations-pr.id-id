---
title: Jurnal integrasi dalam Project Operations
description: Topik ini memberikan informasi tentang bekerja dengan jurnal Integrasi dalam Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ebdb543560027d223715d0e5c70c864b706cb2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007145"
---
# <a name="integration-journal-in-project-operations"></a>Jurnal integrasi dalam Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Entri waktu dan pengeluaran membuat transaksi **Aktual** yang mewakili tampilan operasional pekerjaan yang diselesaikan terhadap proyek. Dynamics 365 Project Operations menyediakan alat kepada akuntan untuk meninjau transaksi dan menyesuaikan atribut akuntansi sesuai kebutuhan. Setelah peninjauan dan penyesuaian selesai, transaksi diposting ke buku besar pembantu proyek dan buku besar Umum. Akuntan dapat melakukan kegiatan ini menggunakan jurnal **Integrasi Project Operations** jurnal(**Dynamics 365 Finance** > **Manajemen proyek dan akuntansi** > **Jurnal** > **Integrasi Project Operations**.

![Alur jurnal integrasi](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Membuat rekaman dalam Jurnal integrasi Project Operations

Rekaman dalam jurnal Integrasi Project Operations dibuat menggunakan proses berkala, **Impor dari tabel penahapan**. Anda dapat menjalankan proses ini dengan masuk ke **Dynamics 365 Finance** > **Manajemen proyek dan akuntansi** > **Berkala** > **Integrasi Project Operations** > **Impor dari tabel penahapan**. Anda dapat menjalankan proses secara interaktif atau mengonfigurasi proses untuk berjalan di latar belakang sesuai kebutuhan.

Ketika proses berkala berjalan, setiap aktual yang belum ditambahkan ke jurnal Integrasi Project Operations ditemukan. Baris jurnal untuk setiap transaksi aktual dibuat.
Sistem ini mengelompokkan baris jurnal ke dalam jurnal terpisah berdasarkan nilai yang dipilih dalam bidang **Unit periode di jurnal Integrasi Project Operations Integration** tab (**Keuangan** > **Manajemen proyek dan akuntansi** > **Konfigurasi** > **Parameter manajemen proyek dan akuntansi**, **Project Operations di Dynamics 365 Customer Engagement**). Nilai yang mungkin untuk bidang ini meliputi:

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
    - Jika **kategori transaksi** tidak diatur dalam aktual proyek, sistem menggunakan nilai pada bidang **default kategori proyek** pada tab **Project Operations pada Dynamics 365 Customer Engagement** pada halaman **parameter manajemen proyek dan akuntansi**.
  - Bidang **sumber daya** mewakili sumber daya proyek yang terkait dengan transaksi ini. Sumber daya digunakan sebagai referensi dalam proposal faktur proyek untuk pelanggan.
  - Bidang **nilai tukar** di-default dari **nilai tukar mata uang** yang ditetapkan di Dynamics 365 Finance. Jika konfigurasi nilai tukar tidak ada, proses periodik **impor dari penahapan** tidak akan menambahkan rekaman ke jurnal dan pesan kesalahan akan ditambahkan ke log eksekusi pekerjaan.
  - Bidang **properti baris** mewakili jenis penagihan dalam aktual proyek. Pemetaan properti baris dan jenis penagihan ditentukan pada tab **Project Operations pada Dynamics 365 Customer Engagement** pada halaman **parameter manajemen proyek dan akuntansi**.

Hanya atribut akuntansi berikut dapat diperbarui di baris jurnal integrasi Project Operations:

- **Grup pajak penjualan penagihan** dan **grup pajak penjualan item tagihan**
- **Dimensi keuangan** (menggunakan tindakan **mendistribusikan jumlah**)

Integrasi baris jurnal dapat dihapus, namun setiap baris yang belum diposting akan dimasukkan ke dalam jurnal lagi setelah Anda jalankan kembali proses periodik **impor dari penahapan**.

Ketika Anda memposting jurnal integrasi, transaksi buku besar pembantu proyek dan buku besar umum dibuat. Ini digunakan di faktur pelanggan hilir, pengakuan pendapatan dan pelaporan keuangan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]