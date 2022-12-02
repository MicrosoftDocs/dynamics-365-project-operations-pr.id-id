---
title: Menentukan jenis penyebaran Anda
description: artikel ini memberikan informasi untuk membantu Anda menentukan jenis penyebaran Project operations yang benar untuk perusahaan Anda.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912198"
---
# <a name="determine-your-deployment-type"></a>Menentukan jenis penyebaran Anda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

> [!IMPORTANT]
> Setelah Anda membeli lisensi, mulai di sini untuk menentukan model penyebaran Dynamics 365 Project Operations terbaik menggunakan [alur penginstalan Terpandu](https://aka.ms/provisionprojectoperations).
> Setelah Anda menyelesaikan alur penginstalan terpandu, Anda akan diarahkan ke Portal manajemen yang benar untuk menyelesaikan penginstalan. Lihat rincian penyebaran untuk menyelesaikan penginstalan.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Pelanggan Dynamics yang lama menggunakan Dynamics 365 Project Service Automation
Project Operations mencakup kemampuan yang disertakan dengan Project Service Automation. Jalur peningkatan akan dirilis untuk pelanggan ini di rilis 2021 gelombang 1.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Pelanggan lama Dynamics 365 Finance menggunakan manajemen proyek dan akuntansi 

Pelanggan Finance yang ada yang menggunakan fungsi manajemen proyek dan akuntansi dapat terus menggunakannya sebagaimana adanya. Lihat [Project Operations untuk skenario pesanan dengan stok/produksi](#pma).


## <a name="deployment-regions"></a>Wilayah Penyebaran
Untuk menentukan kawasan yang mendukung penyebaran Project Operations, lihat [ketersediaan geografis untuk Dynamics 365 dan laporan Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Pilih **Lihat Laporan**, lalu perluas **Dynamics 365 > Aplikasi Operasi > Dynamics 365 Project Operations** untuk melihat kawasan yang didukung.

## <a name="deployment-types"></a>Jenis Penyebaran
Project Operations mendukung beberapa pilihan penyebaran agar sesuai dengan kebutuhan Anda. Apakah Anda adalah pelanggan Dynamics 365 baru atau lama, Project Operations dapat mendukung kebutuhan Anda.

[Kuesioner penyebaran](https://aka.ms/provisionprojectoperations) kami akan membantu Anda menentukan penyebaran yang tepat. Hasil akan memandu Anda menuju salah satu jenis penyebaran berikut:

- [Penyebaran sederhana – menangani faktur proforma](#lite)
- [Project Operations untuk skenario sumber daya/tanpa stok](#integrated)
- [Project Operations untuk skenario pesanan dengan stok/produksi](#pma)

Project Operations mendukung skenario pesanan dengan stok/produksi dan skenario non-stok/berbasis sumber daya pada lingkungan yang sama melalui konfigurasi tingkat entitas hukum. Misalnya, Aswono dapat menggunakan kemampuan pesanan produksi/penuh di fasilitas produksi AS (entitas hukum = Aswono Manufacturing Indonesia). Aswono dapat menggunakan kemampuan berbasis sumber daya/non-stok di fasilitas layanan Aswono Lengan Robotika di Inggris (entitas hukum = Aswono Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Penyebaran sederhana - menangani faktur proforma

Penyebaran sederhana mencakup kemampuan berikut:

- Proses penjualan untuk proyek yang memperluas pengalaman aplikasi Dynamics 365 Sales
- Perencanaan proyek menggunakan Microsoft Project untuk web
- Harga multidimensi
- Manajemen sumber daya terpadu
- Pelacakan Waktu
- Pengeluaran dasar
- Faktur proforma untuk tinjauan dan edit manajer proyek 

#### <a name="deployment-steps"></a>Langkah-langkah penyebaran
Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).

Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](lite-preview-subscription-sign-up.md) dan [penyediaan lingkungan baru](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations untuk skenario sumber daya/tanpa stok
Project Operations untuk skenario sumber daya/non-stok mencakup kemampuan berikut:
 
- Proses penjualan untuk proyek yang memperluas aplikasi Dynamics 365 Sales
- Perencanaan proyek menggunakan Microsoft Project untuk web
- Harga multidimensi
- Manajemen sumber daya terpadu
- Pelacakan Waktu
- Pengeluaran dasar
- Pengeluaran penuh
- OCR Tanda Terima
- faktur Proforma dan sisi pelanggan 
- Pengakuan pendapatan untuk proyek

#### <a name="deployment-steps"></a>Langkah-langkah penyebaran
Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).

Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](resource-sign-up-preview-subscription.md) dan [penyediaan lingkungan baru](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations untuk skenario pesanan dengan stok/produksi

- Perencanaan proyek dengan WBS
- Manajemen sumber daya
- Pelacakan Waktu
- Pengeluaran penuh
- OCR Tanda Terima
- Faktur Lengkap
- Pengakuan pendapatan
- Pesanan Produksi
- Dukungan bahan ber-stok dengan inventaris

#### <a name="deployment-steps"></a>Langkah-langkah penyebaran
Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).

Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) dan [penyediaan lingkungan baru](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]