---
title: Konfigurasi Project Operations dan integrasi data konfigurasi
description: Informasi topik tentang pengaturan dan konfigurasi peta penulisan ganda Project Operations.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939000"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Konfigurasi Project Operations dan integrasi data konfigurasi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Informasi topik tentang integrasi penulisan ganda Project Operations untuk entitas konfigurasi dan pengaturan.

## <a name="project-contracts-contract-lines-and-projects"></a>Kontrak Proyek, Baris Kontrak, dan Proyek

Kontrak proyek, baris kontrak, dan proyek dibuat di Dataverse dan disinkronisasikan ke aplikasi Finance and Operations untuk akuntansi tambahan. Rekaman di entitas ini dapat dibuat dan dihapus hanya dalam Dataverse. Namun, atribut akuntansi seperti default grup pajak penjualan dan dimensi keuangan dapat ditambahkan ke rekaman tersebut di aplikasi Finance and Operations.

  ![Konsep integrasi kontrak proyek](./media/1ProjectContract.jpg)

Prospek, peluang, dan kuotasi aktivitas penjualan dilacak di Dataverse dan tidak disinkronisasi ke aplikasi Finance and Operations karena tidak ada akuntansi hilir yang terkait dengan aktivitas ini.

Fungsi kontrak proyek dalam Dataverse membuat rekaman kontrak proyek di aplikasi Finance and Operations menggunakan peta tabel **Header kontrak proyek (salesorders)**. Menyimpan kontrak proyek di Dataverse juga memulai pembuatan rekaman entitas pelanggan kontrak proyek. Rekaman ini disinkronisasi ke aplikasi Finance and Operations menggunakan peta tabel **sumber dana Proyek (msdyn\_projectcontractssplitbillingrules)**. Peta ini juga mensinkronisasikan penambahan pelanggan, pembaruan, dan penghapusan kontrak proyek. Persentase penagihan terpisah antara pelanggan kontrak proyek diolah hanya dalam Dataverse dan tidak disinkronisasi ke aplikasi Finance and Operations.

Setelah kontrak proyek dibuat dalam Dataverse, akuntan proyek dapat memperbarui atribut akuntansi untuk kontrak proyek ini di aplikasi Finance and Operations dengan membuka **manajemen proyek dan akuntansi** > **Kontrak proyek** > **Konfigurasi** > **Tampilkan akuntansi default**. Akuntan dapat memeriksa atribut kontrak proyek operasional, seperti tanggal pengiriman yang diminta dan jumlah kontrak dengan memilih ID kontrak proyek di aplikasi Finance and Operations yang membuka rekaman kontrak proyek terkait di Dataverse.

Entitas proyek disinkronisasi ke aplikasi Finance and Operations menggunakan peta tabel **Proyek V2 (msdyn\_projects)**. Akuntan proyek dapat:

  - Meninjau proyek di aplikasi Finance and Operations dengan masuk ke **Manajemen proyek dan akuntansi** > **Semua proyek**. 
  - Perbarui atribut akuntansi untuk proyek dalam aplikasi Finance and Operations dengan membuka **Manajemen proyek dan akuntansi** > **Semua proyek** > **Konfigurasi** > **Tampilkan akuntansi default**.  
  - Periksa atribut proyek operasional, seperti perkiraan tanggal mulai dan berakhir, dengan memilih ID proyek dalam aplikasi Finance and Operations yang membuka rekaman proyek terkait dalam Dataverse.

Proyek dikaitkan dengan kontrak proyek melalui entitas **baris kontrak Proyek**.

Baris kontrak proyek dalam Dataverse membuat aturan penagihan kontrak proyek di aplikasi Finance and Operations menggunakan peta tabel **Baris kontrak proyek (salesorderdetails)**. Metode penagihan menentukan jenis aturan penagihan kontrak proyek di aplikasi Finance and Operations:

  - Baris kontrak proyek dengan metode penagihan waktu dan bahan membuat aturan penagihan waktu dan jenis bahan.
  - Baris kontrak metode penagihan harga tetap membuat aturan penagihan bertahap.

Baris kontrak proyek dapat ditinjau oleh akuntan proyek dalam aplikasi Finance and Operations dengan membuka **Manajemen Proyek dan akuntansi** > **Kontrak Proyek** > **Konfigurasi** > **Tampilkan akuntansi default**, dan meninjau rincian pada tab **Baris kontrak**. Akuntan juga dapat mengatur dimensi keuangan default untuk baris kontrak metode penagihan harga tetap pada tab ini.

## <a name="billing-milestones"></a>Tahap Penagihan

Baris kontrak proyek dengan menggunakan metode penagihan harga tetap ditagihkan melalui tahapan penagihan. Tahapan penagihan disinkronisasi ke transaksi cicilan proyek di aplikasi Finance and Operations menggunakan peta tabel **tahapan baris kontrak integrasi Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrasi Tahap Penagihan](./media/2Milestones.jpg)

Akuntan dapat memeriksa transaksi cicilan dan menyesuaikan atribut akuntansi untuk transaksi tersebut dengan masuk ke **manajemen proyek dan akuntansi** > **Kontrak proyek** > **Kelola** > **Transaksi cicilan** atau **Manajemen proyek dan akuntansi** > **Semua proyek** > **Kelola** > **transaksi cicilan**.

Saat pertama kali membuat tahap penagihan untuk baris kontrak proyek tertentu, sistem secara otomatis membuat proyek estimasi pendapatan harga tetap untuk proyek yang terkait dengan baris kontrak ini. Proyek estimasi pendapatan harga tetap dapat ditinjau dengan masuk ke **Manajemen proyek dan akuntansi** > **Proyek estimasi pendapatan harga tetap**.

### <a name="project-tasks"></a>Tugas Proyek

Tugas proyek disinkronisasi ke aplikasi Finance and Operations melalui peta tabel **Tugas proyek (msdyn\_projecttasks)** hanya untuk tujuan referensi. Operasi buat, perbarui, dan hapus tidak didukung melalui aplikasi Finance and Operations.

  ![Integrasi tugas proyek](./media/3Tasks.jpg)

## <a name="project-resources"></a>Sumber daya proyek

Entitas **peran sumber daya proyek** disinkronisasi ke aplikasi Finance and Operations menggunakan peta tabel **peran sumber daya Proyek untuk semua perusahaan (bookableresourcecategories)** hanya untuk tujuan referensi. Karena peran sumber daya di Dataverse tidak spesifik perusahaan, sistem secara otomatis membuat rekaman peran sumber daya khusus perusahaan masing-masing dalam aplikasi Finance and Operations secara otomatis untuk semua entitas hukum yang tercakup dalam cakupan integrasi penulisan ganda.

![Integrasi peran sumber daya](./media/5Resources.jpg)

Sumber daya proyek dalam Project Operations dikelola dalam Dataverse dan tidak disinkronisasikan ke aplikasi Finance and Operations.

### <a name="transaction-categories"></a>Kategori Transaksi

Kategori transaksi dikelola di Dataverse dan disinkronisasi ke aplikasi Finance and Operations menggunakan peta tabel **Kategori transaksi Proyek (msdyn\_transactioncategories)**. Setelah rekaman kategori transaksi disinkronisasi, sistem secara otomatis membuat empat rekaman kategori bersama. Setiap rekaman terkait dengan jenis transaksi di aplikasi Finance and Operations dan menautkannya ke rekaman kategori transaksi.

![Integrasi Kategori Transaksi](./media/4TransactionCategories.jpg)

Menggunakan kategori transaksi untuk estimasi dan aktual memerlukan akuntan proyek atau administrator sistem agar dapat membuat kategori proyek yang sesuai di setiap entitas hukum. Untuk informasi selengkapnya, lihat [Mengonfigurasi kategori proyek](../project-accounting/configure-project-categories.md).