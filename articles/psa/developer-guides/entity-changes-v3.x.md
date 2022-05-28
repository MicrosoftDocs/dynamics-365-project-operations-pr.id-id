---
title: Perubahan entitas, kontrol, dan antarmuka pengguna (Project Service Automation 3.x)
description: Topik ini menjelaskan perubahan solusi untuk Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: da43e0d15e655977c0c1be7348192a0189a56a6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597572"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Perubahan entitas, kontrol, dan antarmuka pengguna (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Dengan dirilisnya Microsoft Dynamics Project Service Automation (PSA) 3. x, banyak perubahan yang telah dilakukan pada entitas, kontrol, tampilan, dan antarmuka pengguna. topik berikut berisi informasi penting tentang perubahan penting.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relasi induk-anak untuk dokumen penjualan, baris dokumen penjualan, entitas detail baris dokumen penjualan
Dalam versi Dynamics 365 Project Service Automation (PSA) yang dirilis sebelum versi 3,0, beberapa Relasi antara dokumen penjualan, baris dokumen penjualan, dan entitas rincian baris dokumen penjualan diterapkan melalui bidang string yang akan memiliki representasi string GUID entitas terkait. Hal ini dikarenakan keterbatasan platform yang memerlukan kode kustom yang signifikan pada server dan sisi klien solusi untuk membuat Relasi tersebut bekerja seperti Relasi entitas Dynamics CRM tipikal dan untuk membuat bidang string bertindak seperti bidang pencarian.

PSA 3.0 telah diperbarui memanfaatkan Relasi entitas baru antara entitas penjualan dan baris entitas dokumen penjualan.

Karena bidang pencarian sekarang dapat digunakan untuk menunjukkan referensi ke entitas, bidang yang menampung nilai string GUID entitas yang terkait di versi sebelumnya tidak lagi diperlukan dan karena itu telah ditolak. Klien kustom dan kode sisi server yang menangani Relasi yang didefinisikan oleh bidang string lama juga telah ditolak.

### <a name="entity-schema-changes"></a>Perubahan skema entitas
Tabel berikut ini berisi daftar satu-satu dari bidang string yang ditolak dan bidang pencarian baru untuk entitas. 

 Entitas |   Bidang ditolak (string) | Bidang baru (Pencarian)
--- | --- | ---
invoicedetail (Baris Faktur) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (aktual) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Jadwal Faktur baris kontrak Proyek) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Tonggak Waktu baris kontrak) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (fakta) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (detail baris faktur) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (baris jurnal) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Kategori Sumber daya baris kontrak Proyek) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Rincian baris kontrak proyek) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Kategori Transaksi baris kontrak Proyek) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Klasifikasi Transaksi Baris Kontrak Proyek) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (jadwal faktur baris kuotasi) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Kategori Sumber Daya Baris Kuotasi) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Milestone baris kuotasi) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (detail baris kuotasi) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Kategori Transaksi Baris Kuotasi) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Klasifikasi Transaksi Baris Kuotasi) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (baris pesanan) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Tampilan dan kontrol kustom yang ditolak
Tampilan dan kontrol kustom berikut, serta artefak terkaitnya, telah ditolak.

- Tampilan ketertagihan.
- Kontrol kisi kustom untuk menampilkan detail baris kuotasi di halaman **informasi proyek** untuk baris kuotasi.
- Kontrol kisi kustom untuk menampilkan detail baris kontrak proyek di halaman **informasi proyek** untuk baris pesanan penjualan.

> [!NOTE]
> Untuk daftar lengkap sumber daya yang ditolak, lihat [sumber daya web yang ditolak dalam Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Modul aplikasi antarmuka klien terpadu
Dengan pengenalan modul aplikasi Unified client Interface (UCI), entri peta situs PSA telah dihapus dari sistem.  
Fungsi yang terkait dengan peralihan formulir untuk peluang, kuotasi, pesanan, faktur telah ditolak karena tidak lagi diperlukan karena modul aplikasi UCI hanya mencakup versi PSA dari formulir.  

Sumber daya web berikut ini ditolak:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Untuk daftar lengkap sumber daya yang ditolak, lihat [sumber daya web yang ditolak dalam Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
