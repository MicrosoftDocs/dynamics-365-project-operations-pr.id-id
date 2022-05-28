---
title: Integrasi faktur vendor
description: Laporan topik memberikan informasi tentang integrasi faktur vendor di Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8650eed2230b99b821c1635fdc88252bb65c5583
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591179"
---
# <a name="vendor-invoice-integration"></a>Integrasi faktur vendor

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Pengadaan terkait proyek di Dynamics 365 Project Operations dapat direkam dengan masuk ke **utang dagang** > **Faktur** > **Faktur vendor Tertunda** dan menggunakan dokumen faktur vendor yang tertunda. Untuk informasi lebih lanjut, lihat [Beli bahan non-stok dengan faktur vendor tertunda](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Sebelum Anda menggunakan fungsi yang dijelaskan di topik ini, lihat dan terapkan konfigurasi yang diperlukan. Untuk informasi lebih lanjut, lihat [Mengaktifkan materi non-stok dan faktur vendor yang tertunda](../procurement/configure-materials-nonstocked.md).

Di Project Operations, faktur vendor terkait proyek diposting menggunakan aturan posting khusus:

- Biaya terkait proyek (termasuk pajak yang tidak dapat dipulihkan) tidak segera diposting ke akun biaya proyek dalam buku besar umum. Sebagai gantinya, biaya akan diposting ke **akun integrasi pengadaan**. Akun ini dikonfigurasi dalam **Manajemen proyek dan akuntansi** > **Konfigurasi** > **Parameter manajemen proyek dan akuntansi**, di tab **Project Operations di Dynamics 365 Customer Engagement**.
- Penulisan ganda mensinkronisasikan rincian faktur vendor ke Microsoft Dataverse menggunakan peta tabel berikut:

     - **Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices)**: Peta tabel ini mensinkronisasikan informasi header faktur vendor. Hanya faktur vendor dengan sekurangnya satu baris yang berisi ID proyek yang disinkronisasi ke Dataverse.
     - **Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoicelines)**: Peta tabel ini mensinkronisasikan informasi baris faktur vendor. Hanya baris yang berisi ID proyek yang akan disinkronisasi ke Dataverse.

     > [!NOTE]
     > Rincian faktur vendor di Dataverse tidak dapat diedit.

Subledger pajak, subledger vendor, dan posting keuangan lainnya dicatat sebagai berlaku di Dynamics 365 Finance ketika faktur vendor diposting.

![Integrasi faktur vendor.](media/DW7VendorInvoice.png)

Ketika rekaman ditulis ke entitas **faktur Vendor** di Dataverse, proses persetujuan otomatis rekaman dimulai. Jika diperlukan, status proses persetujuan otomatis dapat ditinjau di Dataverse dengan masuk ke **Pengaturan tingkat lanjut** > **Sistem** > **Pekerjaan sistem**. Setelah persetujuan selesai, sistem membuat rekaman kelas transaksi bahan dalam entitas **Aktual**.

Aktual terkait bahan kemudian diproses menggunakan peta tabel penulisan ganda, **Aktual integrasi Project Operations (msdyn_actuals)**. Untuk informasi lebih lanjut, Lihat [aktual dan estimasi proyek](resource-dual-write-estimates-actuals.md).

Proses periodik, **Impor dari penahapan** membuat baris jurnal integrasi Project Operations terkait faktur vendor. Akun pengimbang di-default ke akun integrasi pengadaan. Ketika jurnal integrasi diposting, saldo akun dihapus untuk transaksi faktur vendor dan jumlah baris dipindahkan ke akun biaya proyek. Transaksi buku besar pembantu proyek juga dibuat untuk tujuan faktur hilir dan pengakuan pendapatan.
