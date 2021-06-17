---
title: Mensinkronisasi kontrak proyek dan proyek secara langsung dari Project Service Automation ke Finance
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan kontrak dan proyek secara langsung dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 2f5fa0143c903f08b3937426805cb43d5d6109e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999810"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Mensinkronisasi kontrak proyek dan proyek secara langsung dari Project Service Automation ke Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan kontrak dan proyek secara langsung dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.

> [!NOTE] 
> Jika Anda menggunakan Enterprise Edition 7.3.0, Anda harus menginstal KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation ke Finance

> [!NOTE]
> Sebelum Anda dapat menggunakan Project Service Automation untuk membiayai solusi integrasi, Anda harus terbiasa dengan fitur integrasi data Dynamics 365.

Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance. Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang kontrak proyek, proyek, baris kontrak proyek, dan tonggak pencapaian baris kontrak dari Project Service Automation ke Finance.

Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Template dan tugas

Untuk mengakses template yang tersedia, di Pusat admin Microsoft Power Apps, pilih **proyek**, lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan proyek dan kontrak proyek dari Project Service Automation ke Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Mengintegrasikan dengan Dynamics 365 Project Service Automation v2.x
- **Nama template dalam integrasi Data**: Proyek dan kontrak (Project Service Automation ke Finance)
- **Nama tugas dalam proyek**

    - Kontrak proyek Project Service Automation ke Finance
    - Proyek Project Service Automation ke Finance
    - Baris kontrak proyek Project Service Automation ke Finance
    - Tahapan baris kontrak proyek Project Service Automation ke Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Mengintegrasikan dengan Dynamics 365 Project Service Automation v3.x
Ada perubahan skema dalam Project Service Automation yang mempengaruhi template tonggak garis kontrak proyek dan penggunaan template versi v2 diperlukan untuk mengintegrasikan Project Service Automation v3. x dengan Dynamics 365.

- **Nama template dalam integrasi Data**: Proyek dan kontrak (Project Service Automation 3.x ke Finance) - v2
- **Nama tugas dalam proyek**

    - Kontrak proyek Project Service Automation ke Finance
    - Proyek Project Service Automation ke Finance
    - Baris kontrak proyek Project Service Automation ke Finance
    - Tahapan baris kontrak proyek Project Service Automation ke Finance

Sebelum sinkronisasi kontrak proyek dan proyek dapat terjadi, Anda harus mensinkronisasikan akun.

## <a name="entity-set"></a>Rangkaian Entitas

| Project Service Automation       | Keuangan                                                |
|----------------------------------|--------------------------------------------------------|
| Pesanan                           | Entitas integrasi untuk kontrak proyek                |
| Proyek                         | Entitas integrasi untuk proyek                         |
| Baris pesanan                      | Entitas integrasi untuk baris kontrak proyek           |
| Tahap Baris Kontrak Proyek | Entitas integrasi untuk Tonggak pencapaian baris kontrak proyek |

## <a name="entity-flow"></a>Alur entitas

Kontrak proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai kontrak proyek. Sebagai bagian dari template integrasi, Anda dapat mengatur sumber integrasi dalam Finance untuk kontrak proyek.

Proyek waktu dan material serta harga tetap dikelola di Project Service Automation dan disinkronisasikan ke Finance sebagai proyek. Sebagai bagian dari integrasi template, Anda dapat mengatur sumber integrasi untuk proyek di Finance. Saat ini, hanya proyek waktu dan material serta proyek harga tetap yang didukung.


Baris kontrak proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai aturan penagihan kontrak proyek. Jika metode penagihan berbeda dari jenis proyek default, sinkronisasi akan memperbarui jenis proyek untuk baris kontrak proyek dan grup proyek.

Tonggak pencapaian baris kontrak proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai tonggak pencapaian aturan penagihan kontrak proyek.

## <a name="project-service-automation-to-finance-integration-solution"></a>Solusi integrasi Project Service Automation ke Finance

Bidang **id kontrak proyek** tersedia di halaman **kontrak proyek**. Bidang ini telah dibuat sebagai kunci alami dan unik untuk mendukung integrasi.

Bila kontrak proyek baru dibuat, jika nilai **id kontrak proyek** belum ada, maka secara otomatis dihasilkan menggunakan urutan nomor. Nilai ini terdiri dari **ORD** yang diikuti dengan urutan nomor yang bertambah dan kemudian akhiran enam karakter. Berikut adalah contoh: **ORD-01022-Z4M9Q0**.

Bidang **Nomor proyek** tersedia di halaman **proyek**. Bidang ini telah dibuat sebagai kunci alami dan unik untuk mendukung integrasi.

Bila proyek baru dibuat, jika nilai **Nomor proyek** belum ada, maka secara otomatis dihasilkan menggunakan urutan nomor. Nilai ini terdiri dari **PRJ** yang diikuti dengan urutan nomor yang bertambah dan kemudian akhiran enam karakter. Berikut adalah contoh: **PRJ-01049-CCNID0**.

Bila solusi integrasi Project Service Automation ke Finance diterapkan, skrip peningkatan menetapkan bidang **id kontrak proyek** untuk kontrak proyek yang ada dan bidang **nomor proyek** untuk proyek yang ada di Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Prasyarat dan konfigurasi pemetaan

- Sebelum sinkronisasi kontrak proyek dan proyek dapat terjadi, Anda harus mensinkronisasikan akun.
- Di rangkaian sambungan, tambahkan pemetaan bidang kunci integrasi untuk **msdyn\_organizationalunits** menjadi **msdyn\_name \[Name\]**. Anda mungkin harus terlebih dulu menambahkan proyek ke rangkaian sambungan. Untuk informasi lebih lanjut, lihat [mengintegrasikan data ke Common Data Service for Apps](/powerapps/administrator/data-integrator).
- Di rangkaian sambungan, tambahkan pemetaan bidang kunci integrasi untuk **msdyn\_projects** ke **msdynce\_projectnumber \[Project Number\]**. Anda mungkin harus terlebih dulu menambahkan proyek ke rangkaian sambungan. Untuk informasi lebih lanjut, lihat [mengintegrasikan data ke Common Data Service for Apps](/powerapps/administrator/data-integrator).
- **SourceDataID** untuk kontrak proyek dan proyek dapat diperbarui ke nilai yang berbeda atau dihapus dari pemetaan. Nilai template default adalah **Project Service Automation**.
- Pemetaan **paymentterms** harus diperbarui sehingga mencerminkan persyaratan pembayaran yang valid di Finance. Anda juga dapat menghapus pemetaan dari tugas proyek. Peta nilai default memiliki nilai default untuk data demo. Tabel berikut Menampilkan nilai dalam Project Service Automation.

    | Nilai | KETERANGAN   |
    |-------|---------------|
    | 1     | Jatuh tempo 30 hari        |
    | 2     | Diskon 2% untuk pembayaran 10 hari setelah tanggal faktur, jatuh tempo 30 hari |
    | 3     | Jatuh tempo 45 hari        |
    | 4     | Jatuh tempo 60 hari        |

## <a name="power-query"></a>Power Query

Gunakan Microsoft Power Query untuk Excel untuk memfilter data jika kondisi berikut terpenuhi:

- Anda memiliki pesanan penjualan di Dynamics 365 Sales.
- Anda memiliki beberapa unit organisasi dalam Project Service Automation, dan unit organisasi ini akan dipetakan ke beberapa entitas hukum di keuangan.

Jika anda harus menggunakan Power Query, ikuti petunjuk berikut:

- Template proyek dan kontrak (PSA untuk Fin dan Ops) memiliki filter default yang mencakup hanya pesanan penjualan jenis **item kerja (msdyn\_ordertype = 192350001)**. Filter ini membantu menjamin bahwa kontrak proyek tidak dibuat untuk pesanan penjualan di Finance. Jika Anda membuat template sendiri, Anda harus menambahkan filter ini.
- Buat filter Power Query yang mencakup hanya organisasi kontrak yang harus disinkronisasi ke entitas hukum dari rangkaian sambungan integrasi. Contohnya, kontrak proyek yang Anda miliki dengan unit organisasional kontrak Contoso AS harus disinkronisasikan ke entitas hukum USSI, namun kontrak proyek yang Anda miliki dengan unit organisasional kontrak Contoso Global harus disinkronisasikan ke entitas hukum USMF. Jika Anda tidak menambahkan filter ini ke pemetaan tugas, Semua kontrak proyek akan disinkronisasikan ke entitas hukum yang ditentukan untuk rangkaian sambungan, terlepas dari unit organisasi kontrak.

## <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

> [!NOTE] 
> Bidang **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, dan **AddressZipCode** tidak disertakan dalam pemetaan default untuk kontrak proyek. Anda dapat menambahkan pemetaan jika Anda memerlukan data ini akan disinkronisasikan untuk kontrak proyek.
>
> Bidang **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** tidak disertakan dalam pemetaan untuk proyek. Anda dapat menambahkan pemetaan jika Anda memerlukan data ini akan disinkronisasikan untuk proyek.

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.

[![Pemetaan template kontrak proyek](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Pemetaan template proyek](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Pemetaan template baris kontrak proyek](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Pemetaan template tonggak baris kontrak proyek](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Pemetaan tonggak pencapaian baris kontrak proyek dalam proyek dan kontrak (PSA 3. x ke Dynamics)- template V2:

[![Pemetaan tonggak baris kontrak proyek dengan template versi dua](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]