---
title: Penyediaan lingkungan baru
description: Topik ini menyediakan informasi tentang bagaimana menyediakan lingkungan Project Operations baru.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949366"
---
# <a name="provision-a-new-environment"></a>Penyediaan lingkungan baru

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini memberikan informasi tentang cara penyediaan lingkungan Dynamics 365 Project Operations baru untuk skenario berbasis sumber daya/non-stok.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Aktifkan penetapan otomatis Project Operations dalam proyek LCS

Gunakan langkah-langkah berikut untuk mengaktifkan alur penyediaan otomatis Project Operations untuk proyek LCS Anda.

1. Buka [LCS](https://lcs.dynamics.com/v2), lalu pilih ubin **manajemen fitur pratinjau**.
2. Dalam Daftar **fitur pratinjau**, pilih **Project Operations** dan pilih fitur **pratinjau yang diaktifkan** untuk mengaktifkan Project Operations.

> [!NOTE]
> Langkah ini dilakukan hanya satu kali per proyek LCS.

## <a name="provision-a-project-operations-environment"></a>Penyediaan lingkungan Project Operations

1. Buka Dynamics 365 Finance [lingkungan demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) baru atau penyebaran [lingkungan produksi/Sandbox](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Lalui Wizard **penyediaan lingkungan**. 

> [!IMPORTANT]
> Pastikan versi aplikasi yang dipilih adalah 10.0.13 atau lebih tinggi.

3. Untuk menyediakan Project Operations, di dalam **pengaturan lanjutan**, pilih **Common Data Service**. 
4. Aktifkan **pengaturan Common Data Service** dengan memilih **ya**, lalu masukkan informasi di bidang wajib:

  - Nama
  - Wilayah
  - Bahasa
  - Mata uang
 
5. Di bidang **template Common Data Service**, pilih **Project Operations** 

6. Pilih jenis lingkungan untuk penyebaran Anda. Uji coba berbasis langganan akan memungkinkan Anda menyebarkan lingkungan CDS selama 30 hari. 

![Pengaturan penyebaran](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Pilih **setuju** untuk menyetujui persyaratan layanan, lalu pilih **selesai** untuk kembali ke pengaturan penyebaran.

![Persetujuan Penyebaran](./media/2DeploymentConsent.png)

7. Lengkapi bidang yang diperlukan yang tersisa di Wizard dan konfirmasikan penyebaran. Waktu penyediaan lingkungan bervariasi berdasarkan jenis lingkungan. Penyediaan mungkin memerlukan waktu hingga enam jam.

  Setelah penyebaran berhasil diselesaikan, lingkungan akan ditampilkan sebagai **disebarkan**.

8. Untuk mengonfirmasi bahwa lingkungan telah berhasil disebarkan, pilih **masuk** dan masuk ke lingkungan untuk mengonfirmasi.

![Rincian lingkungan ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Terapkan data demo Project Operations Finance (langkah opsional)

Terapkan data demo Project Operations Finance ke lingkungan host cloud rilis Layanan 10.0.13 seperti dijelaskan dalam [artikel ini](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Terapkan pembaruan ke lingkungan Finance

Project Operations memerlukan lingkungan Finance dengan versi aplikasi **10.0.13 (10.0.569.20009)** atau lebih tinggi.

Anda mungkin perlu menerapkan pembaruan kualitas ke lingkungan Finance Anda untuk menerima versi ini.

1. Di LCS, di halaman **rincian lingkungan**, di Bagian **pembaruan yang tersedia**, pilih **Lihat pembaruan**.

![Lihat pembaruan](./media/5ViewUpdates.png)

2. Pada halaman **pembaruan biner**, pilih **Simpan paket.**

![Simpan paket](./media/6SavePackage.png)

3. Klik **pilih semua**, lalu pilih **Simpan paket**.

![Tinjau dan simpan pembaruan](./media/7ReviewAndSaveUpdates.png)

4. Masukkan nama dan Deskripsi paket, lalu pilih **Simpan**. Tergantung pada koneksi internet, proses ini mungkin akan memakan waktu.

![Mengunggah paket ke pustaka aset](./media/8UploadPackageToAssetsLibrary.png)

5. Setelah paket disimpan, pilih **selesai** dan Simpan paket ini ke pustaka aset dalam proyek LCS Anda.

Menyimpan dan memvalidasi paket mungkin memerlukan waktu ~ 15 menit.

6. Untuk menerapkan pembaruan, navigasi ke halaman **rincian lingkungan** di lcs dan pilih **memelihara** > **menerapkan pembaruan**.

![Memelihara lingkungan](./media/9MaintainEnvironment.png)

7. Dalam daftar pembaruan, pilih paket yang Anda buat, lalu pilih **Terapkan**.

![Menerapkan pembaruan](./media/10ApplyUpdates.png)

Layanan lingkungan akan memakan waktu. Setelah selesai, lingkungan akan kembali ke keadaan disebarkan.

![Lingkungan Disebarkan](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Membuat sambungan tulis ganda 

1. Di proyek LCS, buka halaman **rincian lingkungan**.
2. Di dalam **informasi lingkungan Common Data Service**, pilih **tautkan ke CDS for Apps**.
3. Setelah tautan selesai, pilih **tautkan ke CDS for Apps** lagi. Anda akan diarahkan ke Tulis Ganda di Finance.

![Tautan ke CDS](./media/12LinktoCDS.png)

4. Pilih **Terapkan solusi** untuk mengakses entitas yang akan dipetakan dalam integrasi.

![Terapkan solusi](./media/13ApplySolutions.png)

5. Pilih kedua solusi, **peta entitas tulis ganda Dynamics 365 Finance and Operations** dan **peta entitas tulis ganda Dynamics 365 Project Operations**, lalu pilih **Terapkan**.

![Konfirmasi Solusi](./media/14ConfirmSolutions.png)

Setelah solusi diterapkan, entitas tulis ganda diterapkan ke lingkungan.

![Menerapkan solusi](./media/15ApplyingSolutions.png)

Setelah entitas diterapkan, Semua pemetaan yang tersedia didaftarkan di lingkungan.

![Peta Tulis Ganda](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Segarkan entitas data setelah pembaruan

1. Di Finance, buka ruang kerja **manajemen data**.

![Ruang kerja manajemen data](./media/16DataManagement.png)

2. Pilih ubin **parameter kerangka**.

![Parameter kerangka](./media/17FrameworkParameters.png)

3. Pada halaman **pengaturan entitas**, pilih **segarkan daftar entitas**.

![Segarkan daftar entitas](./media/18RefreshEntityList.png)

Penyegaran akan berlangsung sekitar 20 menit. Anda akan menerima pemberitahuan setelah selesai.

![Segarkan Konfirmasi](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Jalankan peta Tulis Ganda Project Operations

1. Di proyek LCS, buka halaman **rincian lingkungan**.
2. Di dalam **informasi lingkungan Common Data Service**, pilih **tautkan ke CDS for Apps**. Setelah memilih tautan, Anda akan diarahkan ke daftar entitas di pemetaan.
3. Mulai peta seperti yang dijelaskan dalam tabel berikut. Pastikan untuk mengikuti urutan yang tercantum.

| **Peta Entitas** | **Refresh Entitas** | **Sinkronisasi awal** | **Master untuk sinkronisasi awal** | **Prasyarat menjalankan** | **Sinkronisasi awal prasyarat** |
| --- | --- | --- | --- | --- | --- |
| **Peran sumber daya proyek untuk semua perusahaan (bookableresourcecategories)** | No | Ya | Common Data Service | No | N\A |
| **Entitas hukum (cdm\_companies)** | No | Ya | Aplikasi Finance and Operations | No | N\A |
| **Aktual Integrasi Project Operations (msdyn\_actuals)** | No | No | N\A | Ya | No |
| **Baris kontrak proyek (salesorderdetails)** | No | No | N\A | No | No |
| **Entitas integrasi untuk Relasi transaksi proyek (msdyn\_transactionconnections)** | No | No | N\A | No | N\A |
| **Baris kontrak integrasi Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | N\A | No | N\A |
| **Entitas integrasi Project Operations untuk estimasi pengeluaran (msdyn\_estimateslines)** | No | No | N\A | No | N\A |
| **Entitas integrasi Project Operations untuk estimasi jam (msdyn\_resourceassignments)** | No | No | N\A | No | N\A |
| **Entitas ekspor pengeluaran proyek integrasi Project Operations (msdyn\_expenses)** | Ya | No | N\A | No | N\A |
| **Entitas integrasi Project Operations untuk estimasi jam (msdyn\_resourceassignments)** | Ya | No | N\A | No | N\A |

4. Untuk me-refresh entitas, pilih nama peta, lalu pilih **refresh entitas**. 
5. Lanjutkan dengan menjalankan peta setelah penyegaran selesai.

![Segarkan Peta](./media/20RefreshMapping.png)

Sebelum Anda mengaktifkan peta berikutnya, Verifikasikan bahwa peta dalam tabel dalam status **berjalan**. Menjalankan peta dengan sejumlah besar prasyarat mungkin akan memakan waktu.

Untuk menjalankan peta dengan prasyarat, Aktifkan pengalih **Tampilkan peta entitas yang terkait**. Jika tabel menunjukkan **sinkronisasi awal prasyarat** adalah **Tidak**, Verifikasikan bahwa tanda **sinkronisasi awal** **dinonaktifkan** di semua peta prasyarat sebelum Anda menjalankannya.

![Jalankan Peta](./media/21RunMap.png)

6. Validasi semua peta terkait proyek berada dalam status berjalan.

![Semua peta berjalan](./media/22AllMapsRunning.png)

Lingkungan Project Operations Anda sekarang telah disediakan dan dikonfigurasi.
