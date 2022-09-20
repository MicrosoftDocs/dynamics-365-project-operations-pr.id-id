---
title: Perubahan fitur dari Project Service Automation ke Project Operations
description: Artikel ini memberikan gambaran umum tentang perubahan fitur dari Project Service Automation ke Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459930"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Perubahan fitur dari Project Service Automation ke Project Operations

Upgrade dari Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations Lite akan dikirimkan dalam tiga fase. Artikel ini memberikan informasi tentang perubahan besar yang dapat Anda harapkan untuk dilihat saat pemutakhiran selesai.

| Tingkatkan pengiriman | Tahap 1 <br>(Januari 2022) | Tahap 2 <br>(Bulan November 2022) | Tahap 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Tidak ada ketergantungan pada struktur rincian kerja (WBS) untuk proyek. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS termasuk dalam batas Operasi Proyek yang saat ini didukung. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar batas Operasi Proyek yang saat ini didukung, termasuk dukungan untuk klien desktop Proyek. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Manajemen proyek

Perubahan paling signifikan dalam pengalaman pengguna adalah di bidang perencanaan proyek. Project Operations mengadopsi pengalaman modern baru untuk mengelola struktur rincian kerja (WBS) dengan memanfaatkan kemampuan penjadwalan yang disediakan oleh [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Perbedaan dalam pengalaman penjadwalan

Tabel berikut ini meringkas perbedaan penjadwalan antara Otomatisasi Layanan Proyek dan Operasi Proyek.

|  Penjadwalan     |   Project Operations   |   Psa   |
|-----------------|------------------------|---------|
| Templat proyek - Kemampuan untuk menentukan dan menerapkan templat proyek saat proyek dibuat  |  &nbsp;    | :heavy_check_mark: |
| Integrasi struktur rincian kerja proyek (WBS) dengan klien desktop   |    &nbsp;  | :heavy_check_mark: |
| Kendala - Mulai tidak lebih awal dari, selesaikan selambat-lambatnya  | :heavy_check_mark: |   &nbsp;  |
| Milestones - Tugas dengan durasi nol   | :heavy_check_mark:  |  &nbsp;  |
| Tugas yang didorong oleh sumber daya akan menghormati ketersediaan sumber daya yang ditetapkan   | :heavy_check_mark: |  &nbsp;    |
| Pengeditan bertahap waktu - Edit paket dan bekerja setiap hari   |   &nbsp;  | :heavy_check_mark: |
| Penjadwalan otomatis/manual - Gunakan mesin penjadwalan Proyek untuk menjadwalkan tugas secara otomatis atau manual |  &nbsp; | :heavy_check_mark:  |
| Edit proyek besar langsung di antarmuka pengguna: Tidak ada batasan ukuran paket yang dapat diedit  | Batas tugas 500  | :heavy_check_mark:       |
| Persen selesai - Tandai kemajuan tugas   | :heavy_check_mark:  |  &nbsp;  |
| [Mode](../project-management/scheduling-modes.md) Jadwal Proyek - Tentukan proyek sebagai unit tetap, upaya tetap, atau durasi tetap | :heavy_check_mark: | &nbsp; |
| Linimasa - Membangun dan menyesuaikan tampilan garis waktu untuk memvisualisasikan detail jadwal dan berkomunikasi dengan pemangku kepentingan. | :heavy_check_mark:  | &nbsp; |
| Tugas yang didorong oleh upaya - Menjadwalkan dukungan mesin untuk menjadwalkan tugas sebagai upaya yang didorong oleh upaya  | :heavy_check_mark:  | &nbsp; |
| **Kotak dialog Informasi** tugas - Simpan detail tugas menggunakan kotak dialog | :heavy_check_mark:  |  &nbsp;  |
| Seret dan lepas - Multi-pilih tugas dan ubah posisinya di WBS | :heavy_check_mark: | &nbsp;  |
| Tampilan persisten yang fleksibel - Menentukan tampilan atribut tugas yang lebih terperinci   | :heavy_check_mark:  | &nbsp; |
| Mengurutkan dan memfilter WBS  | :heavy_check_mark:  | &nbsp; |
| Tampilan papan untuk pengiriman proyek non-air terjun  | :heavy_check_mark:   | &nbsp; |
| Tampilan garis waktu - Bagan Gantt interaktif yang digunakan untuk memvisualisasikan dan mengedit WBS   | :heavy_check_mark:  | &nbsp; |
| Pintasan Keyboard - Menggunakan pintasan keyboard untuk operasi umum, seperti indentasi atau sisipan  | :heavy_check_mark:  |  &nbsp; |
| Pembatalan multi-level - Lakukan analisis bagaimana-jika untuk sepenuhnya memahami dampak perubahan dengan membalikkan dan menerapkan kembali seluruh rangkaian operasi | :heavy_check_mark: | &nbsp; |
| Potong/Salin/Tempel - Berkolaborasi pada pengembangan jadwal dengan menyalin dan menempelkan detail jadwal antar aplikasi  | :heavy_check_mark: | &nbsp; |
| Daftar periksa tugas - Menambahkan hingga 20 item daftar periksa ke tugas   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Perencanaan proyek

Halaman **Proyek** dalam Operasi Proyek memiliki sejumlah besar perbedaan dibandingkan **dengan halaman Proyek** di Project Service Automation.

Tindakan berikut telah dihapus dari **halaman Proyek** sebagai bagian dari pemutakhiran Fase 1:

  - **Buka di MS Project**
  - **Buat Template**
  - **Batalkan tautan dari MS Project**

Halaman **Proyek** di Operasi Proyek mencakup tab baru berikut.

- **Perkiraan Materi**
- **Konfigurasi Penagihan Tugas**

Tab **Status** telah dihapus dan **bidang Status** sekarang berada di tab **Ringkasan** dengan mode penjadwalan proyek.

   ![Pembaruan pada halaman Proyek.](media/projectform.png)

Tab **Jadwal** telah diganti namanya menjadi tab **Tugas** dan menampilkan pengalaman perencanaan proyek baru dengan Project for the Web.

   ![Tab Tugas proyek baru.](media/tasktab.png)

## <a name="scheduling-modes"></a>Mode penjadwalan

Operasi Proyek telah memperkenalkan fitur baru, [mode](../project-management/scheduling-modes.md) Penjadwalan. Semua proyek Project Service Automation yang ada akan default ke **Fixed Duration** di Project Operations. Namun, default untuk proyek baru dapat dikelola dengan masuk ke **Pengaturan Parameter Parameter Parameter** > **·** > **Schedule Mode** > **·**.

   ![Pengaturan parameter proyek untuk mode Jadwal.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Batas perencanaan proyek

Operasi Proyek bergantung pada Project for the Web untuk semua operasi penjadwalan proyek. Project for the Web mengelola struktur rincian kerja menggunakan batas dalam tabel berikut.

| **Bidang**                                          | **Batas**             |
|----------------------------------------------------|-----------------------|
| Tugas total maksimum untuk proyek                  | 500                   |
| durasi total maksimum untuk proyek               | 3650 hari (10 tahun)  |
| Sumber daya total maksimum untuk proyek              | 300                   |
| Tautan total maksimum (hanya penerus) untuk proyek | 600                   |
| bidang kustom total maksimum untuk proyek          | 10                    |
| Tingkat hierarki maksimum                            | 10 Tingkat             |
| Tautan maksimum (penerus + pendahulu)            | 20                    |
| Durasi maksimum tugas daun                      | 1250 hari             |
| Durasi maksimum tugas ringkasan                 | 3650 hari (10 tahun)  |
| Sumber daya maksimum ditetapkan ke tugas               | 20 Sumber Daya          |
| Rentang tanggal yang didukung untuk tugas                    | 1/1/2000 - 31/12/2149 |
| Item daftar periksa                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Ekstensibilitas dan pengembangan perencanaan proyek

Setelah Anda meng-upgrade ke Project Operations, Anda harus menggunakan PROJECT Scheduling API untuk menjalankan operasi buat, perbarui, dan hapus pada entitas berikut:

|   Nama entitas           |   Nama logika entitas       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tugas Proyek            | msdyn_projecttask           |
| Dependensi Tugas Proyek | msdyn_projecttaskdependency |
| Penetapan Sumber Daya     | msdyn_resourceassignment    |
| Wadah Proyek          | msdyn_projectbucket         |
| Anggota Tim Proyek     | msdyn_projectteam           |

Jika saat ini Anda memiliki penyesuaian yang melibatkan entitas ini, lihat [Menggunakan API jadwal Proyek untuk melakukan operasi dengan entitas](../project-management/schedule-api-preview.md) Penjadwalan untuk panduan implementasi.

## <a name="data-model-changes"></a>Perubahan model data

Sebagai bagian dari Peningkatan Fase 1, ada perubahan pada model data. Perubahan ini terutama merupakan perubahan bidang pada entitas yang ada. Pada Fase 1, entitas, **msydn_project**, dan **msdyn_projectteam** adalah pemfaktoran ulang penyesuaian. 

> [!IMPORTANT]
> Bagian ini akan diperbarui dengan entitas tambahan saat fase peningkatan di masa mendatang selesai.

Bidang berikut telah diganti dengan bidang baru.

|   Entitas          |   Nama logis lama   |   Nama logis baru    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Bidang berikut telah ditambahkan.

|   Entitas          |   Nama logika                               |   Deskripsi |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Menunjukkan agregat penjualan biaya aktual pada proyek. Hanya untuk digunakan dalam Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Menunjukkan agregat biaya material aktual pada proyek. Hanya untuk digunakan dalam Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Menunjukkan agregat penjualan material aktual pada proyek. Hanya untuk digunakan dalam Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Garis kontrak yang terkait dengan proyek ini. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ini adalah bidang sistem internal yang digunakan untuk **Copy Project** yang terkait dengan Identifier Korelasi. Hanya untuk digunakan dalam Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ini adalah bidang sistem internal, yang digunakan untuk **Copy Project** yang terkait dengan Session Identifier. Hanya untuk digunakan dalam Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Sinkronisasi terakhir xRM Global Revision Token dari layanan penjadwalan Project. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokumen Microsoft Project milik proyek. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Agregat biaya material yang direncanakan pada proyek. Hanya untuk digunakan dalam Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Agregat penjualan material yang direncanakan pada proyek. Hanya untuk digunakan dalam Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program terkait proyek ini. |
| msdyn_project     | msdyn_quotelineproject                       | Baris Kutipan yang terkait dengan proyek ini. |
| msdyn_project     | msdyn_replaylogheader                        | Header untuk log replay. |
| msdyn_project     | msdyn_schedulemode                           | Mode penjadwalan default yang digunakan untuk semua tugas pada proyek.  |
| msdyn_project     | msdyn_taskearlieststart                      | Tanggal mulai paling awal untuk tugas apa pun dalam proyek.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Anggota tim proyek tempat anggota tim proyek ini disalin. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Menunjukkan apakah akan membuat persyaratan sumber daya untuk anggota tim generik yang baru dibuat.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status hapus anggota tim untuk melacak apakah ada permintaan penghapusan yang dikirim ke layanan penjadwalan Proyek dan apakah berhasil mengirimkan respons kembali dalam jangka waktu yang diharapkan. |
| msdyn_projectteam | msdyn_effortcompleted                        | Melacak upaya yang dilakukan oleh anggota tim pada tugas mereka. |
| msdyn_projectteam | msdyn_effortremaining                        | Melacak upaya yang belum diselesaikan oleh anggota tim pada tugas mereka. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Masa tunggu dari saat anggota tim mengirimkan permintaan penghapusan ke layanan penjadwalan Proyek hingga anggota tim benar-benar dihapus pada Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Stempel waktu untuk merekam saat permintaan penghapusan anggota tim dikirim ke layanan penjadwalan Proyek. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Menampilkan anggota tim proyek yang disalin anggota tim proyek ini.  |

## <a name="project-templates"></a>Template Proyek

Operasi Proyek tidak menyediakan dukungan untuk templat proyek. Namun, Anda dapat mereplikasi sebagian besar fungsionalitas inti dengan menggunakan [Project Copy API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Dukungan add-in desktop

Dukungan untuk add-in Microsoft Project Desktop tidak akan tersedia dalam 2 fase pertama pemutakhiran. Di Fase 3, pelanggan yang memiliki proyek yang lebih besar dari batas Project for the Web yang saat ini didukung akan dapat menggunakan add-in desktop.

## <a name="editing-resource-assignment-contours"></a>Mengedit kontur penugasan sumber daya

Kemampuan untuk mengedit kontur penetapan sumber daya akan tersedia saat Fase 2 peningkatan tersedia.

## <a name="billing-and-pricing"></a>Penagihan dan harga

Fitur baru berikut telah ditambahkan di Operasi Proyek. Fitur-fitur ini bersifat aditif dan tidak memengaruhi model data Project Service Automation.

- [Merekam penggunaan materi pada proyek dan tugas proyek](../material/material-usage-log.md)
- [Manajemen subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berbasis uang muka dan panjar](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan validasi kontrak tidak melebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Penagihan berbasis tugas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Komponen yang tidak digunakan lagi

Tabel berikut mendokumentasikan semua bidang yang tidak digunakan lagi yang dipindahkan ke solusi komponen yang tidak digunakan lagi setelah pemutakhiran. Untuk informasi selengkapnya dan tautan ke solusi, lihat [Dynamics 365 Project Service Automation 3x ke Operasi Proyek 4x komponen yang tidak digunakan lagi](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_persen                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_sisa jam                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_sisa jam                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Kolom                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

