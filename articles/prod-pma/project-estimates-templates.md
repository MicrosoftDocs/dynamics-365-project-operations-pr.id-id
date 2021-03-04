---
title: Sinkronisasikan estimasi proyek secara langsung dari Project Service Automation ke Finance and Operations
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan estimasi jam proyek dan estimasi pengeluaran proyek secara langsung dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078612"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sinkronisasikan estimasi proyek secara langsung dari Project Service Automation ke Finance and Operations

[!include[banner](../includes/banner.md)]

Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan estimasi jam proyek dan estimasi pengeluaran proyek secara langsung dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.

> [!NOTE]
> - Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.
> - Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation ke Finance

Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance. Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang estimasi jam proyek dan estimasi pengeluaran proyek dari Project Service Automation ke Finance.

Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimasi jam proyek

### <a name="template-and-tasks"></a>Template dan tugas

Untuk mengakses template yang tersedia, di Pusat admin Microsoft Power Apps, pilih **proyek** , lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan estimasi jam proyek dari Project Service Automation ke Finance:

- **Nama template di integrasi data:** estimasi jam proyek (PSA ke Fin and Ops)
- **Nama tugas dalam proyek**

    - Relasi transaksi
    - Perkiraan pengeluaran

### <a name="entity-set"></a>Rangkaian Entitas

| Project Service Automation | Keuangan                                       |
|----------------------------|-----------------------------------------------|
| Tugas Proyek              | Entitas integrasi untuk estimasi jam proyek |

### <a name="entity-flow"></a>Alur entitas

Estimasi jam proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai perkiraan jam proyek.

### <a name="prerequisites"></a>Prasyarat

Sebelum sinkronisasi perkiraan jam proyek dapat terjadi, Anda harus mensinkronisasikan proyek, tugas proyek, dan kategori transaksi pengeluaran proyek.

### <a name="power-query"></a>Power Query

Di template estimasi jam proyek, anda harus menggunakan Microsoft Power Query untuk Excel untuk menyelesaikan tugas ini:

- Atur ID model perkiraan default yang akan digunakan saat integrasi membuat perkiraan jam baru.
- Filter rekaman khusus sumber daya dalam tugas yang akan gagal dalam integrasi ke perkiraan jam.
- Filter setiap baris kategori transaksi kosong. Kegagalan untuk menyelesaikan tugas ini dapat mengakibatkan perkiraan jam salah.

#### <a name="set-the-default-forecast-model-id"></a>Mengatur ID model default perkiraan

Untuk memperbarui ID model perkiraan default dalam template, klik panah **peta** untuk membuka pemetaan. Lalu pilih tautan **kueri lanjutan dan filter**.

- Jika anda menggunakan estimasi jam proyek default (PSA ke Fin and Ops), pilih **kondisi dimasukkan** di daftar **langkah yang diterapkan**. Di entri **fungsi** , ganti **O\_forecast** dengan nama ID model perkiraan yang harus digunakan dengan integrasi. Template default memiliki ID model perkiraan dari data demo.
- Jika Anda membuat template baru, Anda harus menambahkan kolom ini. Di Power Query, pilih **Tambah kolom kondisional** , dan masukkan nama untuk kolom baru, misalnya **ModelID**. Masukkan kondisi untuk kolom, di mana, jika tugas proyek tidak null, maka \<enter the forecast model ID\>; jika tidak maka null.

#### <a name="filter-out-resource-specific-records"></a>Memfilter rekaman khusus sumber daya

Estimasi jam proyek (PSA ke Fin and Ops) memiliki filter default yang menghilangkan rekaman khusus sumber daya apa pun. Jika Anda membuat template sendiri, Anda harus menambahkan filter ini. Pilih tautan **kueri lanjutan dan filter** untuk memfilter pada kolom **msdyn\_islinetask** agar hanya rekaman yang **salah** yang disertakan.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filter baris kategori transaksi kosong

Anda harus menambahkan filter untuk menghapus setiap baris yang memiliki kategori transaksi kosong. Tugas ini diperlukan, terlepas dari Apakah Anda menggunakan template default atau membuat template Anda sendiri. Filter ini menghilangkan baris ringkasan apa pun dari Project Service Automation yang mungkin menyebabkan perkiraan jam di Finance menjadi tidak benar. Pilih tautan **kueri lanjutan dan filter** untuk memfilter rekaman null di kolom **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.

[![Pemetaan tugas template dalam integrasi data](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Estimasi pengeluaran proyek

### <a name="template-and-tasks"></a>Template dan tugas

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan estimasi pengeluaran proyek dari Project Service Automation ke Finance:

- **Nama template di integrasi data:** estimasi pengeluaran proyek (PSA ke Fin and Ops)
- **Nama tugas dalam proyek**

    - Relasi transaksi 
    - Perkiraan pengeluaran

### <a name="entity-set"></a>Rangkaian Entitas

| Project Service Automation | Keuangan                                                  |
|----------------------------|----------------------------------------------------------|
| Koneksi Transaksi    | Entitas integrasi untuk Relasi transaksi proyek |
| Baris Perkiraan             | Entitas integrasi untuk estimasi proyek         |

### <a name="entity-flow"></a>Alur entitas

Estimasi pengeluaran proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai perkiraan pengeluaran proyek.

### <a name="prerequisites"></a>Prasyarat

Sebelum sinkronisasi perkiraan pengeluaran proyek dapat terjadi, Anda harus mensinkronisasikan proyek, tugas proyek, dan kategori transaksi pengeluaran proyek.

### <a name="power-query"></a>Power Query

Di template estimasi pengeluaran proyek, anda harus menggunakan Power Query untuk menyelesaikan tugas berikut ini:

- Filter untuk menyertakan hanya rekaman baris estimasi pengeluaran.
- Atur ID model perkiraan default yang akan digunakan saat integrasi membuat perkiraan jam baru.
- Ubah jenis penagihan.
- Ubah jenis transaksi.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filter untuk menyertakan hanya baris estimasi pengeluaran

Template perkiraan pengeluaran proyek (PSA ke Fin and Ops) memiliki filter default yang mencakup hanya baris pengeluaran di integrasi. Jika Anda membuat template sendiri, Anda harus menambahkan filter ini. Pilih tugas **Relasi transaksi** , lalu klik panah **peta** untuk membuka pemetaan. Pilih tautan **kueri lanjutan dan filter**. Filter kolom **msdyn\_transactiontype1** sehingga mencakup hanya **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Mengatur ID model default perkiraan

Untuk memperbarui ID model perkiraan default dalam template, pilih tugas **Estimasi pengeluaran** , lalu klik panah **peta** untuk membuka pemetaan. Pilih tautan **kueri lanjutan dan filter**.

- Jika anda menggunakan template estimasi pengeluaran proyek default (PSA ke Fin and Ops), di Power Query, pilih **kondisi dimasukkan** pertama dari bagian **langkah yang diterapkan**. Di entri **fungsi** , ganti **O\_forecast** dengan nama ID model perkiraan yang harus digunakan dengan integrasi. Template default memiliki ID model perkiraan dari data demo.
- Jika Anda membuat template baru, Anda harus menambahkan kolom ini. Di Power Query, pilih **Tambah kolom kondisional** , dan masukkan nama untuk kolom baru, misalnya **ModelID**. Masukkan kondisi untuk kolom, di mana, jika ID baris estimasi tidak null, maka \<enter the forecast model ID\>; jika tidak maka null.

#### <a name="transform-the-billing-types"></a>Ubah jenis penagihan

Template perkiraan pengeluaran proyek (PSA ke Fin and Ops) mencakup bidang kondisional yang digunakan untuk mengubah jenis penagihan yang diterima dari Project Service Automation selama integrasi. Jika Anda membuat template sendiri, Anda harus menambahkan kolom bersyarat ini. Pilih tautan **kueri lanjutan dan pemfilteran** , lalu pilih **Tambah kolom kondisional**. Masukkan nama untuk kolom baru, seperti **billingtype**. Lalu masukkan kondisi berikut:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Ubah jenis transaksi

Template perkiraan pengeluaran proyek (PSA ke Fin and Ops) mencakup bidang kondisional yang digunakan untuk mengubah jenis transaksi yang diterima dari Project Service Automation selama integrasi. Jika Anda membuat template sendiri, Anda harus menambahkan kolom bersyarat ini. Pilih tautan **kueri lanjutan dan pemfilteran** , lalu pilih **Tambah kolom kondisional**. Masukkan nama untuk kolom baru, seperti **TransactionType**. Lalu masukkan kondisi berikut:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.

[![Pemetaan template transaksi estimasi pengeluaran](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Pemetaan template estimasi pengeluaran](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]