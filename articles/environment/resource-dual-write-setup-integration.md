---
title: Konfigurasi Project Operations dan integrasi data konfigurasi
description: Artikel ini menyediakan informasi tentang menyiapkan dan mengonfigurasi peta tulis ganda Operasi Proyek.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914544"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Konfigurasi Project Operations dan integrasi data konfigurasi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini menyediakan informasi tentang integrasi penulisan ganda Operasi Proyek untuk entitas penyiapan dan konfigurasi.

## <a name="project-contracts-contract-lines-and-projects"></a>Kontrak Proyek, Baris Kontrak, dan Proyek

Kontrak proyek, jalur kontrak, dan proyek dibuat dan Dataverse disinkronkan ke aplikasi Keuangan dan Operasi untuk akuntansi tambahan. Rekaman di entitas ini dapat dibuat dan dihapus hanya dalam Dataverse. Namun, atribut akuntansi seperti default grup pajak penjualan dan dimensi keuangan dapat ditambahkan ke catatan ini di aplikasi Keuangan dan Operasi.

  ![Konsep integrasi kontrak proyek.](./media/1ProjectContract.jpg)

Prospek, peluang, dan kutipan aktivitas penjualan dilacak Dataverse dan tidak disinkronkan ke aplikasi Keuangan dan Operasi karena tidak ada akuntansi hilir yang terkait dengan aktivitas ini.

Fungsionalitas kontrak proyek dalam Dataverse membuat catatan kontrak proyek di aplikasi Keuangan dan Operasi menggunakan **peta tabel Header kontrak proyek (salesorders**). Menyimpan kontrak proyek di Dataverse juga memulai pembuatan rekaman entitas pelanggan kontrak proyek. Catatan ini disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peta tabel Sumber pendanaan proyek (msdyn\_ projectcontractssplitbillingrules**). Peta ini juga mensinkronisasikan penambahan pelanggan, pembaruan, dan penghapusan kontrak proyek. Persentase penagihan terpisah antara pelanggan kontrak proyek hanya dikuasai dan Dataverse tidak disinkronkan ke aplikasi Keuangan dan Operasi.

Setelah kontrak proyek dibuat, Dataverse akuntan proyek dapat memperbarui atribut akuntansi untuk kontrak proyek ini di aplikasi Keuangan dan Operasi dengan **membuka Manajemen proyek dan akuntansi** > **Kontrak** > **proyek Siapkan Tampilkan** > **akuntansi** default. Akuntan dapat meninjau atribut kontrak proyek operasional, seperti tanggal pengiriman yang diminta dan jumlah kontrak dengan memilih ID kontrak proyek di aplikasi Keuangan dan Operasi yang membuka catatan kontrak proyek terkait di Dataverse.

Entitas proyek disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peta tabel Proyek V2 (proyek\_ msdyn**). Akuntan proyek dapat:

  - Tinjau proyek di aplikasi Keuangan dan Operasi dengan membuka **Manajemen proyek dan akuntansi** > **Semua proyek**. 
  - Perbarui atribut akuntansi untuk proyek di aplikasi Keuangan dan Operasi dengan **membuka Manajemen proyek dan akuntansi** > **Semua proyek** > **Siapkan** > **Tampilkan akuntansi** default.  
  - Tinjau atribut proyek operasional, seperti perkiraan tanggal mulai dan berakhir, dengan memilih ID proyek di aplikasi Keuangan dan Operasi yang membuka rekaman proyek terkait di Dataverse.

Proyek dikaitkan dengan kontrak proyek melalui entitas **baris kontrak Proyek**.

Garis kontrak proyek dalam Dataverse membuat aturan penagihan kontrak proyek di aplikasi Keuangan dan Operasi menggunakan **peta tabel Jalur kontrak proyek (salesorderdetails**). Metode penagihan menentukan jenis aturan penagihan kontrak proyek di aplikasi Keuangan dan Operasi:

  - Baris kontrak proyek dengan metode penagihan waktu dan bahan membuat aturan penagihan waktu dan jenis bahan.
  - Baris kontrak metode penagihan harga tetap membuat aturan penagihan bertahap.

Garis kontrak proyek dapat ditinjau oleh akuntan proyek di aplikasi Keuangan dan Operasi dengan membuka **Manajemen proyek dan akuntansi** > **Kontrak** > **proyek Siapkan Tampilkan** > **akuntansi** default, dan tinjau detail pada **tab Garis kontrak** . Akuntan juga dapat mengatur dimensi keuangan default untuk garis kontrak metode penagihan harga tetap pada tab ini.

## <a name="billing-milestones"></a>Tahap Penagihan

Baris kontrak proyek dengan menggunakan metode penagihan harga tetap ditagihkan melalui tahapan penagihan. Tonggak penagihan disinkronkan ke transaksi akun proyek di aplikasi Keuangan dan Operasi dengan menggunakan **peta tabel pencapaian jalur kontrak integrasi Operasi Proyek (msdyn\_ contractlinescheduleofvalues**).

  ![Integrasi Tahap Penagihan.](./media/2Milestones.jpg)

Akuntan dapat memeriksa transaksi cicilan dan menyesuaikan atribut akuntansi untuk transaksi tersebut dengan masuk ke **manajemen proyek dan akuntansi** > **Kontrak proyek** > **Kelola** > **Transaksi cicilan** atau **Manajemen proyek dan akuntansi** > **Semua proyek** > **Kelola** > **transaksi cicilan**.

Saat pertama kali membuat tahap penagihan untuk baris kontrak proyek tertentu, sistem secara otomatis membuat proyek estimasi pendapatan harga tetap untuk proyek yang terkait dengan baris kontrak ini. Proyek estimasi pendapatan harga tetap dapat ditinjau dengan masuk ke **Manajemen proyek dan akuntansi** > **Proyek estimasi pendapatan harga tetap**.

### <a name="project-tasks"></a>Tugas Proyek

Tugas proyek disinkronkan ke aplikasi Keuangan dan Operasi melalui **peta tabel Tugas proyek (msdyn\_ projecttasks)** hanya untuk tujuan referensi. Membuat, memperbarui, dan menghapus operasi tidak didukung melalui aplikasi Keuangan dan Operasi.

  ![Integrasi tugas proyek.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Sumber daya proyek

Entitas **Peran** sumber daya proyek disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peta tabel Peran sumber daya proyek untuk semua perusahaan (bookableresourcecategories)** hanya untuk tujuan referensi. Karena peran sumber daya tidak Dataverse spesifik untuk perusahaan, sistem secara otomatis membuat catatan peran sumber daya khusus perusahaan masing-masing di aplikasi Keuangan dan Operasi secara otomatis untuk semua badan hukum yang disertakan ke dalam cakupan integrasi tulis ganda.

![Integrasi peran sumber daya.](./media/5Resources.jpg)

Sumber daya proyek dalam Operasi Proyek dipertahankan Dataverse dan tidak disinkronkan ke aplikasi Keuangan dan Operasi.

### <a name="transaction-categories"></a>Kategori Transaksi

Kategori transaksi dipertahankan dan Dataverse disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peta tabel Kategori transaksi proyek (msdyn\_ transactioncategories**). Setelah rekaman kategori transaksi disinkronisasi, sistem secara otomatis membuat empat rekaman kategori bersama. Setiap data sesuai dengan jenis transaksi di aplikasi Keuangan dan Operasi dan menautkannya ke catatan kategori transaksi.

![Integrasi Kategori Transaksi.](./media/4TransactionCategories.jpg)

Menggunakan kategori transaksi untuk estimasi dan aktual memerlukan akuntan proyek atau administrator sistem agar dapat membuat kategori proyek yang sesuai di setiap entitas hukum. Untuk informasi selengkapnya, lihat [Mengonfigurasi kategori proyek](../project-accounting/configure-project-categories.md).
