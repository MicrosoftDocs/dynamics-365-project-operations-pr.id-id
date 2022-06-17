---
title: Integrasi manajemen pengeluaran
description: Artikel ini menyediakan informasi tentang integrasi laporan pengeluaran dalam Operasi Proyek menggunakan penulisan ganda.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64c318dc1915a9a87b6ae3c6b8a2aa6d3c9cd36
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924618"
---
# <a name="expense-management-integration"></a>Integrasi manajemen pengeluaran

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini menyediakan informasi tentang integrasi laporan pengeluaran dalam penyebaran [biaya penuh Operasi](../expense/expense-overview.md) Proyek menggunakan penulisan ganda.

## <a name="expense-categories"></a>Kategori Pengeluaran

Dalam penyebaran pengeluaran penuh, kategori pengeluaran dibuat dan dikelola di aplikasi Keuangan dan Operasi. Untuk membuat kategori pengeluaran baru, selesaikan langkah-langkah berikut:

1. Di Microsoft Dataverse, buat **Kategori Transaksi**. Integrasi tulis ganda akan menyinkronkan kategori transaksi ini ke aplikasi Keuangan dan Operasi. Untuk informasi lebih lanjut, lihat [Mengkonfigurasi kategori proyek](/dynamics365/project-operations/project-accounting/configure-project-categories) dan [integrasi data konfigurasi serta pengaturan Project Operations](resource-dual-write-setup-integration.md). Sebagai hasil dari integrasi ini, sistem membuat empat catatan kategori bersama di aplikasi Keuangan dan Operasi.
2. Di Finance, buka **manajemen pengeluaran** > **Pengaturan** > **kategori bersama** dan pilih kategori bersama dengan dengan kelas transaksi **Pengeluaran**. Atur parameter **Dapat digunakan dalam Pengeluaran** ke **Benar** dan tentukan jenis pengeluaran yang akan digunakan.
3. Menggunakan rekaman kategori bersama ini, buat kategori pengeluaran baru dengan masuk ke **manajemen pengeluaran** > **Konfigurasi** > **Kategori baru** dan memilih **Baru**. Ketika rekaman disimpan, penulisan ganda menggunakan peta tabel, **entitas ekspor kategori pengeluaran proyek integrasi Project Operations (msdyn\_expensecategories)** untuk mensinkronisasi rekaman ini ke Dataverse.

  ![Integrasi kategori pengeluaran.](./media/DW6ExpenseCategories.png)

Kategori pengeluaran dalam aplikasi Keuangan dan Operasi adalah khusus untuk perusahaan atau badan hukum. Ada rekaman khusus entitas hukum yang terpisah dan terkait di Dataverse. Bila manajer proyek mengestimasi pengeluaran, mereka tidak dapat memilih kategori pengeluaran yang dibuat untuk proyek yang dimiliki oleh perusahaan lain daripada perusahaan yang memiliki proyek yang sedang mereka kerjakan. 

## <a name="expense-reports"></a>Laporan pengeluaran

Laporan pengeluaran dibuat dan disetujui di aplikasi Keuangan dan Operasi. Untuk informasi lebih lanjut, lihat [Membuat dan memproses laporan pengeluaran di Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Setelah laporan pengeluaran disetujui oleh manajer Proyek, laporan tersebut diposting ke buku besar umum. Di Project Operations, baris laporan pengeluaran terkait proyek diposting menggunakan aturan posting khusus:

  - Biaya terkait proyek (termasuk pajak yang tidak dapat dipulihkan) tidak dengan segera diposting ke akun biaya proyek pada buku besar umum, namun diposting ke akun integrasi pengeluaran. Akun ini dikonfigurasi dalam **Manajemen proyek dan akuntansi** > **Konfigurasi** > **Parameter manajemen proyek dan akuntansi**, tab **Project Operations di Dynamics 365 Customer Engagement**.
  - Sinkronisasi penulisan ganda ke Dataverse menggunakan peta tabel **entitas ekspor pengeluaran proyek integrasi Project Operations (msdyn\_expenses)**.
  - Buku besar pembantu pajak, buku besar pembantu vendor, dan posting keuangan lainnya dicatat sebagai berlaku pada saat posting laporan pengeluaran.

  ![Integrasi laporan pengeluaran.](./media/DW6ExpenseReports.png)

Bila rekaman ditulis ke entitas **Pengeluaran** dalam Dataverse, sistem akan memicu proses persetujuan rekaman otomatis. Jika diperlukan, status proses persetujuan otomatis dapat ditinjau di Dataverse dengan masuk ke **Pengaturan tingkat lanjut** > **Sistem** > **Pekerjaan sistem**. Setelah persetujuan selesai, rekaman kelas transaksi pengeluaran dibuat di entitas **Aktual**.

Aktual terkait pengeluaran kemudian diproses menggunakan peta tabel dua ganda **aktual integrasi Project Operations (msdyn\_actuals)**. Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md).

Proses periodik, **Impor dari penahapan** membuat baris jurnal yang terkait dengan laporan Pengeluaran di jurnal Integrasi Project Operations. Akun pengimbang di-default ke akun integrasi pengeluaran. Jurnal integrasi Posting menghapus saldo akun untuk transaksi pengeluaran dan memindahkan jumlah pengeluaran ke akun biaya proyek. Sistem juga membuat transaksi buku besar pembantu proyek untuk tujuan faktur hilir dan pengakuan pendapatan.
