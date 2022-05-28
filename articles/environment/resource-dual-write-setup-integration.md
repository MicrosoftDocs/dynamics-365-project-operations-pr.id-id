---
title: Konfigurasi Project Operations dan integrasi data konfigurasi
description: Informasi topik tentang pengaturan dan konfigurasi peta penulisan ganda Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586900"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Konfigurasi Project Operations dan integrasi data konfigurasi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Informasi topik tentang integrasi penulisan ganda Project Operations untuk entitas konfigurasi dan pengaturan.

## <a name="project-contracts-contract-lines-and-projects"></a>Kontrak Proyek, Baris Kontrak, dan Proyek

Kontrak proyek, jalur kontrak, dan proyek dibuat Dataverse dan disinkronkan ke aplikasi Keuangan dan Operasi untuk akuntansi tambahan. Rekaman di entitas ini dapat dibuat dan dihapus hanya dalam Dataverse. Namun, atribut akuntansi seperti default grup pajak penjualan dan dimensi keuangan dapat ditambahkan ke catatan ini di aplikasi Keuangan dan Operasi.

  ![Konsep integrasi kontrak proyek.](./media/1ProjectContract.jpg)

Prospek, peluang, dan kutipan aktivitas penjualan dilacak Dataverse dan tidak disinkronkan ke aplikasi Keuangan dan Operasi karena tidak ada akuntansi hilir yang terkait dengan aktivitas ini.

Fungsionalitas kontrak proyek dalam Dataverse membuat catatan kontrak proyek di aplikasi Keuangan dan Operasi menggunakan **peta tabel Header kontrak proyek (salesorders**). Menyimpan kontrak proyek di Dataverse juga memulai pembuatan rekaman entitas pelanggan kontrak proyek. Catatan ini disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peta tabel Sumber pendanaan Proyek (msdyn\_ projectcontractssplitbillingrules**). Peta ini juga mensinkronisasikan penambahan pelanggan, pembaruan, dan penghapusan kontrak proyek. Persentase penagihan terpisah antara pelanggan kontrak proyek hanya Dataverse dikuasai dan tidak disinkronkan ke aplikasi Keuangan dan Operasi.

Setelah kontrak proyek dibuat pada Dataverse tahun 2010, akuntan proyek dapat memperbarui atribut akuntansi untuk kontrak proyek ini di aplikasi Keuangan dan Operasi dengan membuka **manajemen proyek dan kontrak** > **proyek akuntansi** > **.** > **·** Akuntan dapat meninjau atribut kontrak proyek operasional, seperti tanggal pengiriman yang diminta dan jumlah kontrak dengan memilih ID kontrak proyek di aplikasi Keuangan dan Operasi yang membuka catatan kontrak proyek terkait di Dataverse.

Entitas proyek disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peta tabel Proyek V2 (proyek\_ msdyn**). Akuntan proyek dapat:

  - Tinjau proyek di aplikasi Keuangan dan Operasi dengan membuka **Manajemen proyek dan akuntansi** > **Semua proyek**. 
  - Perbarui atribut akuntansi untuk proyek di aplikasi Keuangan dan Operasi dengan membuka **Manajemen proyek dan akuntansi** > **Semua proyek** > **Siapkan** > **Tampilkan akuntansi** default.  
  - Tinjau atribut proyek operasional, seperti perkiraan tanggal mulai dan akhir, dengan memilih ID proyek di aplikasi Keuangan dan Operasi yang membuka catatan proyek terkait di Dataverse.

Proyek dikaitkan dengan kontrak proyek melalui entitas **baris kontrak Proyek**.

Garis kontrak proyek dalam Dataverse membuat aturan penagihan kontrak proyek di aplikasi Keuangan dan Operasi menggunakan **peta tabel Jalur kontrak proyek (salesorderdetails**). Metode penagihan menentukan jenis aturan penagihan kontrak proyek di aplikasi Keuangan dan Operasi:

  - Baris kontrak proyek dengan metode penagihan waktu dan bahan membuat aturan penagihan waktu dan jenis bahan.
  - Baris kontrak metode penagihan harga tetap membuat aturan penagihan bertahap.

Jalur kontrak proyek dapat ditinjau oleh akuntan proyek di aplikasi Keuangan dan Operasi dengan membuka **manajemen proyek dan kontrak** > **Proyek akuntansi** > **Set up** > **Show default accounting**, dan meninjau detail pada **tab Garis** kontrak. Akuntan juga dapat mengatur dimensi keuangan default untuk jalur kontrak metode penagihan harga tetap pada tab ini.

## <a name="billing-milestones"></a>Tahap Penagihan

Baris kontrak proyek dengan menggunakan metode penagihan harga tetap ditagihkan melalui tahapan penagihan. Tonggak penagihan disinkronkan untuk memproyeksikan transaksi akun di aplikasi Keuangan dan Operasi dengan menggunakan **peta tabel tonggak garis kontrak integrasi Operasi Proyek (msdyn\_ contractlinescheduleofvalues**).

  ![Integrasi Tahap Penagihan.](./media/2Milestones.jpg)

Akuntan dapat memeriksa transaksi cicilan dan menyesuaikan atribut akuntansi untuk transaksi tersebut dengan masuk ke **manajemen proyek dan akuntansi** > **Kontrak proyek** > **Kelola** > **Transaksi cicilan** atau **Manajemen proyek dan akuntansi** > **Semua proyek** > **Kelola** > **transaksi cicilan**.

Saat pertama kali membuat tahap penagihan untuk baris kontrak proyek tertentu, sistem secara otomatis membuat proyek estimasi pendapatan harga tetap untuk proyek yang terkait dengan baris kontrak ini. Proyek estimasi pendapatan harga tetap dapat ditinjau dengan masuk ke **Manajemen proyek dan akuntansi** > **Proyek estimasi pendapatan harga tetap**.

### <a name="project-tasks"></a>Tugas Proyek

Tugas proyek disinkronkan ke aplikasi Keuangan dan Operasi melalui **peta tabel Tugas proyek (msdyn\_ projecttasks)** hanya untuk tujuan referensi. Membuat, memperbarui, dan menghapus operasi tidak didukung melalui aplikasi Keuangan dan Operasi.

  ![Integrasi tugas proyek.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Sumber daya proyek

Entitas **peran** sumber daya Proyek disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peran sumber daya Proyek untuk semua peta tabel perusahaan (bookableresourcecategories)** hanya untuk tujuan referensi. Karena peran sumber daya tidak Dataverse spesifik perusahaan, sistem secara otomatis membuat catatan peran sumber daya khusus perusahaan masing-masing di aplikasi Keuangan dan Operasi secara otomatis untuk semua badan hukum yang termasuk dalam cakupan integrasi dual-write.

![Integrasi peran sumber daya.](./media/5Resources.jpg)

Sumber daya proyek dalam Operasi Proyek dipertahankan Dataverse dan tidak disinkronkan ke aplikasi Keuangan dan Operasi.

### <a name="transaction-categories"></a>Kategori Transaksi

Kategori transaksi dipertahankan Dataverse dan disinkronkan ke aplikasi Keuangan dan Operasi menggunakan **peta tabel Kategori transaksi Proyek (kategori\_ transaksi msdyn**). Setelah rekaman kategori transaksi disinkronisasi, sistem secara otomatis membuat empat rekaman kategori bersama. Setiap catatan sesuai dengan jenis transaksi di aplikasi Keuangan dan Operasi dan menautkannya ke catatan kategori transaksi.

![Integrasi Kategori Transaksi.](./media/4TransactionCategories.jpg)

Menggunakan kategori transaksi untuk estimasi dan aktual memerlukan akuntan proyek atau administrator sistem agar dapat membuat kategori proyek yang sesuai di setiap entitas hukum. Untuk informasi selengkapnya, lihat [Mengonfigurasi kategori proyek](../project-accounting/configure-project-categories.md).
