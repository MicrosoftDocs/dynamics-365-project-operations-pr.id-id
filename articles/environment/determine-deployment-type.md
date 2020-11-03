---
title: Menentukan jenis penyebaran Anda
description: Topik ini memberikan informasi untuk membantu Anda menentukan jenis penyebaran Project operations yang benar untuk perusahaan Anda.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078488"
---
# <a name="determine-your-deployment-type"></a>Menentukan jenis penyebaran Anda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

> [!IMPORTANT]
> Setelah Anda membeli lisensi, mulai di sini untuk menentukan model penyebaran terbaik dari Dynamics 365 Project Operations menggunakan [alur penginstalan terpandu](https://aka.ms/provisionprojectoperations).
> Setelah Anda menyelesaikan alur penginstalan terpandu, Anda akan diarahkan ke Portal manajemen yang benar untuk menyelesaikan penginstalan. Lihat rincian penyebaran untuk menyelesaikan penginstalan.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Pelanggan Dynamics yang lama menggunakan Dynamics 365 Project Service Automation
Project Operations mencakup kemampuan yang disertakan dengan Project Service Automation. Jalur peningkatan akan dirilis untuk pelanggan ini di masa mendatang.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Pelanggan lama Dynamics 365 Finance menggunakan manajemen proyek dan akuntansi 

Pelanggan Finance yang ada yang menggunakan fungsi manajemen proyek dan akuntansi dapat terus menggunakan ini sebagaimana adanya. Lihat [Project Operations untuk skenario pesanan dengan stok/produksi](#pma).


## <a name="deployment-types"></a>Jenis Penyebaran
Project Operations mendukung beberapa pilihan penyebaran agar sesuai dengan kebutuhan Anda. Apakah Anda adalah pelanggan Dynamics 365 baru atau lama, Project Operations dapat mendukung kebutuhan Anda.

[Kuesioner penyebaran](https://aka.ms/provisionprojectoperations) kami akan membantu Anda menentukan penyebaran yang tepat. Hasil akan memandu Anda menuju salah satu jenis penyebaran berikut:

- [Penyebaran sederhana – menangani faktur proforma](#lite)
- [Project Operations untuk skenario sumber daya/tanpa stok](#integrated)
- [Project Operations untuk skenario pesanan dengan stok/produksi](#pma)

Project Operations mendukung skenario pesanan dengan stok/produksi dan skenario non-stok/berbasis sumber daya pada lingkungan yang sama melalui konfigurasi tingkat entitas hukum. Misalnya, Aswono dapat menggunakan kemampuan pesanan produksi/penuh di fasilitas produksi AS (entitas hukum = Aswono Manufacturing Indonesia). Aswono dapat menggunakan kemampuan berbasis sumber daya/non-stok di fasilitas layanan Aswono Lengan Robotika di Inggris (entitas hukum = Aswono Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Penyebaran sederhana - menangani faktur proforma

Penyebaran sederhana mencakup kemampuan berikut:

- Perencanaan proyek menggunakan Microsoft Project untuk web
- Harga multidimensi
- Manajemen sumber daya terpadu
- Pelacakan Waktu
- Pengeluaran dasar
- Proposal faktur

#### <a name="deployment-steps"></a>Langkah-langkah penyebaran
Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).

Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](lite-preview-subscription-sign-up.md) dan [penyediaan lingkungan baru](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations untuk skenario sumber daya/tanpa stok
Project Operations untuk skenario sumber daya/non-stok mencakup kemampuan berikut:
  
- Perencanaan proyek menggunakan Microsoft Project untuk web
- Harga multidimensi
- Manajemen sumber daya terpadu
- Pelacakan Waktu
- Pengeluaran dasar
- Pengeluaran Penuh
- OCR Tanda Terima
- Faktur Lengkap
- Pengakuan pendapatan

#### <a name="deployment-steps"></a>Langkah-langkah penyebaran
Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).

Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](resource-sign-up-preview-subscription.md) dan [penyediaan lingkungan baru](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations untuk skenario pesanan dengan stok/produksi

- Perencanaan proyek dengan WBS
- Manajemen sumber daya
- Pelacakan Waktu
- Pengeluaran Penuh
- OCR Tanda Terima
- Faktur Lengkap
- Pengakuan pendapatan
- Pesanan Produksi
- Dukungan material

#### <a name="deployment-steps"></a>Langkah-langkah penyebaran
Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).

Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) dan [penyediaan lingkungan baru](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

