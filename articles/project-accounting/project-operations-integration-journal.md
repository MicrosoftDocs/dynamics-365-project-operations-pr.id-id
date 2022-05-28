---
title: Jurnal integrasi dalam Project Operations
description: Topik ini memberikan informasi tentang bekerja dengan jurnal Integrasi dalam Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5e1a455d055fe562a1946cc3b90c8274ef1a4b12
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582438"
---
# <a name="integration-journal-in-project-operations"></a>Jurnal integrasi dalam Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Entri waktu dan pengeluaran membuat transaksi **Aktual** yang mewakili tampilan operasional pekerjaan yang diselesaikan terhadap proyek. Dynamics 365 Project Operations menyediakan alat kepada akuntan untuk meninjau transaksi dan menyesuaikan atribut akuntansi sesuai kebutuhan. Setelah peninjauan dan penyesuaian selesai, transaksi diposting ke buku besar pembantu proyek dan buku besar Umum. Seorang akuntan dapat melakukan kegiatan ini menggunakan **jurnal Project Operations Integration** (**Dynamics 365 Finance** > **Project management and accounting** > **Journals** > **Project Operations Integration** journal.

![Alur jurnal integrasi.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Membuat rekaman dalam Jurnal integrasi Project Operations

Rekaman dalam jurnal Integrasi Project Operations dibuat menggunakan proses berkala, **Impor dari tabel penahapan**. Anda dapat menjalankan proses ini dengan membuka **Dynamics 365 Finance** > **Project management and accounting** > **Periodic** > **Project Operations Integration** > **Import dari staging table**. Anda dapat menjalankan proses secara interaktif atau mengonfigurasi proses untuk berjalan di latar belakang sesuai kebutuhan.

Ketika proses berkala berjalan, setiap aktual yang belum ditambahkan ke jurnal Integrasi Project Operations ditemukan. Baris jurnal untuk setiap transaksi aktual dibuat.
Sistem mengelompokkan baris jurnal ke dalam jurnal terpisah berdasarkan nilai yang dipilih di **unit Periode pada bidang jurnal** Integrasi Operasi Proyek (**manajemen Proyek Keuangan** > **dan pengaturan** > **akuntansi** > **Manajemen proyek dan parameter** akuntansi, **Operasi Proyek pada tab Dynamics 365 Customer Engagement**). Nilai yang mungkin untuk bidang ini meliputi:

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
    - Jika **kategori** Transaksi tidak diatur dalam Aktual proyek, sistem menggunakan nilai dalam **bidang default** kategori Proyek pada **operasi proyek pada** Dynamics 365 Customer Engagement tab pada **halaman Parameter** manajemen proyek dan akuntansi.
  - Bidang **sumber daya** mewakili sumber daya proyek yang terkait dengan transaksi ini. Sumber daya digunakan sebagai referensi dalam proposal faktur proyek untuk pelanggan.
  - Bidang **Nilai tukar** default dari **nilai tukar Mata Uang yang** ditetapkan dalam Dynamics 365 Finance. Jika konfigurasi nilai tukar tidak ada, proses periodik **impor dari penahapan** tidak akan menambahkan rekaman ke jurnal dan pesan kesalahan akan ditambahkan ke log eksekusi pekerjaan.
  - Bidang **properti baris** mewakili jenis penagihan dalam aktual proyek. Properti baris dan pemetaan tipe penagihan didefinisikan pada **operasi proyek pada tab Dynamics 365 Customer Engagement** pada **halaman Parameter** manajemen dan akuntansi proyek.

Hanya atribut akuntansi berikut dapat diperbarui di baris jurnal integrasi Project Operations:

- **Grup pajak penjualan penagihan** dan **grup pajak penjualan item tagihan**
- **Dimensi keuangan** (menggunakan tindakan **mendistribusikan jumlah**)

Integrasi baris jurnal dapat dihapus, namun setiap baris yang belum diposting akan dimasukkan ke dalam jurnal lagi setelah Anda jalankan kembali proses periodik **impor dari penahapan**.

Ketika Anda memposting jurnal integrasi, transaksi buku besar pembantu proyek dan buku besar umum dibuat. Ini digunakan di faktur pelanggan hilir, pengakuan pendapatan dan pelaporan keuangan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
