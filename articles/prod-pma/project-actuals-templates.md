---
title: Mensinkronisasikan aktual proyek secara langsung dari Project Service Automation ke jurnal integrasi proyek untuk posting di Finance and Operations
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan aktual proyek secara langsung dari Microsoft Dynamics 365 Project Service Automation ke Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 11ccbd64c37341b2969e10e9a737f1aa4b4a61f9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289688"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Mensinkronisasikan aktual proyek secara langsung dari Project Service Automation ke jurnal integrasi proyek untuk posting di Finance and Operations

[!include[banner](../includes/banner.md)]

Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan aktual proyek secara langsung dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.

Template akan mensinkronisasi transaksi dari Project Service Automation ke dalam tabel penahapan di Finance. Setelah sinkronisasi selesai, Anda **harus** mengimpor data dari tabel penahapan ke jurnal integrasi.

> [!NOTE]
> - Integrasi aktual proyek tersedia mulai versi 8.0.1.
> - Jika Anda menggunakan Enterprise Edition 7.3.0 setelah menginstal 4132657 KB dan 4132660 KB, Anda dapat menggunakan template untuk mengintegrasikan tugas proyek, kategori transaksi pengeluaran, perkiraan jam, perkiraan biaya, dan aktual, serta untuk mengkonfigurasi penguncian fungsionalitas. Jika Anda harus me-reset distribusi akuntansi, kami sarankan Anda juga menginstal 4131710 KB.
> - Jika Anda menggunakan versi 7.3.0, dan Anda membawa transaksi biaya melalui dari Project Service Automation, Anda harus menginstal 4345320 KB agar dapat mencakup biaya tersebut dalam faktur proyek.
> - Jika Anda memasukkan jumlah pajak penjualan pada transaksi waktu atau pengeluaran dalam Project Service Automation, Anda harus menginstal Project Service Automation update 7. Jika tidak, aktual pajak tidak akan ditautkan ke aktual terkait waktu atau biaya, dan tidak akan disinkronisasikan ke Finance. Hubungi Dukungan untuk informasi lebih lanjut.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation ke Finance

Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance. Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang aktual proyek dari Project Service Automation ke Finance.

Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Aktual proyek dari Project Service Automation

### <a name="template-and-tasks"></a>Template dan tugas

Untuk mengakses template yang tersedia, di Pusat admin Microsoft Power Apps, pilih **proyek**, lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan aktual proyek dari Project Service Automation ke Finance:

- **Nama template di integrasi data:** aktual proyek (PSA ke Fin and Ops)
- **Nama tugas dalam proyek**

    - Aktual
    - TransactionConnections

### <a name="entity-set"></a>Rangkaian Entitas

| Project Service Automation | Keuangan                                   |
|----------------------------|----------------------------------------------------------|
| Aktual                    | Entitas integrasi untuk aktual proyek                   |
| Koneksi Transaksi    | Entitas integrasi untuk Relasi transaksi proyek |

### <a name="entity-flow"></a>Alur entitas

Aktual proyek dikelola dalam Project Service Automation, dan disinkronisasi ke jurnal integrasi proyek di Finance. Akuntansi akan diterapkan berdasarkan dimensi keuangan default dan konfigurasi posting.

### <a name="prerequisites"></a>Prasyarat

Sebelum sinkronisasi aktual dapat terjadi, Anda harus mengkonfigurasikan parameter integrasi Project Service Automation dan mensinkronisasikan proyek, tugas proyek, dan kategori transaksi pengeluaran proyek.

### <a name="power-query"></a>Power Query

Di template proyek aktual, anda harus menggunakan Microsoft Power Query untuk Excel untuk menyelesaikan tugas ini:

- Ubah jenis transaksi di Project Service Automation ke jenis transaksi yang benar di Finance. Transformasi ini sudah ditentukan dalam template proyek aktual (PSA ke Fin and Ops).
- Ubah jenis penagihan di Project Service Automation ke jenis penagihan yang benar di Finance. Transformasi ini sudah ditentukan dalam template proyek aktual (PSA ke Fin and Ops). Jenis penagihan kemudian dipetakan ke properti baris, berdasarkan konfigurasi pada halaman **parameter integrasi Project Service Automation**.
- Filter ke unit organisasi sumber daya tertentu yang harus disinkronisasikan dengan template ini.
- Jika aktual antarperusahaan atau biaya antarperusahaan tidak akan disinkronisasi dengan Finance, Anda harus mengubah unit organisasi kontrak menjadi entitas hukum yang benar di Finance. Di template proyek aktual (PSA ke Fin and Ops), kolom kondisional ditentukan berdasarkan data demo. Anda harus memperbarui kolom kondisional yang terakhir dimasukkan ke entitas hukum yang benar. Jika tidak, kesalahan integrasi mungkin terjadi, atau transaksi aktual yang salah dapat diimpor ke Finance.
- Jika aktual waktu antarperusahaan atau pengeluaran antar perusahaan tidak akan disinkronisasikan ke Finance, Anda harus menghapus kolom kondisional terakhir yang disisipkan dari template Anda. Jika tidak, kesalahan integrasi mungkin terjadi, atau transaksi aktual yang salah dapat diimpor ke Finance.

#### <a name="contract-organizational-unit"></a>Unit organisasi kontrak
Untuk memperbarui kolom kondisional yang disisipkan dalam template, klik panah **peta** untuk membuka pemetaan. Pilih tautan **kueri lanjutan dan filter** untuk membuka Power query.

- Jika anda menggunakan template default proyek aktual (PSA ke Fin and Ops), di Power Query, pilih **kondisi dimasukkan** terakhir dari bagian **langkah yang diterapkan**. Di entri **fungsi**, ganti **USSI** dengan nama entitas hukum yang harus digunakan dengan integrasi. Tambahkan kondisi tambahan ke entri **fungsi** sesuai kebutuhan Anda, dan perbarui kondisi **else** dari **usmf** ke entitas hukum yang benar.
- Jika Anda membuat template baru, Anda harus menambahkan kolom untuk mendukung waktu dan pengeluaran antarperusahaan. Pilih **Tambah kolom kondisional**, dan masukkan nama untuk kolom, misalnya **LegalEntity**. Masukkan kondisi untuk kolom, di mana, jika **msdyn\_contractorganizationalunitid.msdyn\_name** adalah \<organizational unit\>, maka \<enter the legal entity\>; jika tidak maka null.

### <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.

[![Pemetaan template-aktual](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Pemetaan template-sambungan transaksi](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Impor dari tabel pementasan setelah integrasi dari Project Service Automation

Impor dari proses periodik tabel penahapan harus dijalankan setelah sinkronisasi aktual dari Project Service Automation ke Finance. Proses ini akan mengimpor transaksi proyek dari tabel penahapan ke jurnal integrasi Project Service Automation, di mana akuntansi diterapkan, dan transaksi impor dapat diposting. Sebaiknya jalankan proses ini dalam mode batch; secara opsional dapat diatur untuk dijalankan sebagai batch berulang.

## <a name="update-actuals-from-finance"></a>Memperbarui aktual dari Finance

### <a name="template-and-tasks"></a>Template dan tugas

Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasi nomor voucher dan pajak penjualan untuk transaksi proyek yang dikirim dari Finance ke Project Service Automation:

- **Nama template di integrasi data:** pembaruan aktual proyek (Fin Ops ke PSA)
- **Nama tugas dalam proyek**

    - Aktual 
    - TransactionConnections

### <a name="entity-set"></a>Rangkaian Entitas

| Keuangan                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entitas integrasi untuk aktual proyek                   | Aktual                    |
| Entitas integrasi untuk Relasi transaksi proyek | Koneksi Transaksi    |

### <a name="entity-flow"></a>Alur entitas

Aktual proyek dikelola dalam Project Service Automation, dan disinkronisasi ke jurnal integrasi proyek di Finance. Setelah aktual diposting di Finance, mereka diperbarui dalam Project Service Automation dengan nomor voucher dari Finance. Jika pajak penjualan ditambahkan pada Finance, aktual pajak baru dibuat di Project Service Automation.

### <a name="power-query"></a>Power Query

Di template pembaruan aktual proyek, anda harus menggunakan Power Query untuk menyelesaikan tugas ini:

- Ubah jenis transaksi di Finance ke jenis transaksi yang benar di Project Service Automation. Transformasi ini sudah ditentukan dalam template pembaruan aktual proyek (Fin Ops ke PSA).
- Ubah jenis penagihan di Finance ke jenis penagihan yang benar di Project Service Automation. Transformasi ini sudah ditentukan dalam template pembaruan aktual proyek (Fin Ops ke PSA).

### <a name="template-mapping-in-data-integration"></a>Pemetaan template di integrasi data

Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data. Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Finance ke Project Service Automation.

[![Pemetaan template-pembaruan aktual](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Pemetaan template-pembaruan transaksi](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]