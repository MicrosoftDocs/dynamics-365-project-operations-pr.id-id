---
title: Mengonfigurasikan integrasi Project Operations per entitas hukum
description: Topik ini menyediakan informasi tentang mengonfigurasikan integrasi per entitas hukum di Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fc3f5be1318d482ece9a6e9e4fadc3cf628ff79577776e679f32cef7c0b2fc8f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999410"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Mengonfigurasikan integrasi Project Operations per entitas hukum 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Tindakan topik akan memandu Anda melakukan langkah-langkah yang diperlukan untuk mengkonfigurasi Dynamics 365 Project Operations per entitas hukum.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktifkan kunci target di Dynamics 365 Finance

Selesaikan langkah-langkah berikut untuk mengaktifkan fitur yang diperlukan.

1. Di Dynamics 365 Finance, buka ruang kerja **manajemen fitur**.
2. Dalam **Daftar fitur**, Cari dan Aktifkan fitur berikut:
  
    - **Aktifkan beberapa baris kontrak untuk proyek**
    - **Aktifkan Project Operations di Dynamics 365 Customer Engagement**

> [!NOTE]
> Jika Anda tidak melihat **tombol fitur** yang tercantum, Verifikasikan bahwa versi keuangan Anda memenuhi persyaratan versi minimum (versi aplikasi 10.0.13 dengan semua pembaruan kualitas yang diterapkan atau lebih tinggi). Pilih **Periksa pembaruan** untuk me-refresh daftar fitur.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Menentukan skenario penyebaran Project Operations untuk entitas hukum

Anda dapat mengaktifkan Project Operations pada Dynamics 365 Customer Engagement di tingkat entitas hukum. Anda dapat memiliki satu entitas hukum menggunakan Project Operations di Dynamics 365 Customer Engagement untuk skenario berbasis sumber daya/non-stok. Di lingkungan yang sama, Anda dapat memiliki entitas hukum lain menggunakan Project Operations untuk skenario pesanan produksi/di-stok.

1. Di Dynamics 365 Finance, buka **manajemen proyek dan akuntansi** > **konfigurasi** > **parameter manajemen proyek dan akuntansi global**.
2. Dalam daftar entitas hukum yang tersedia, pilih entitas di mana beberapa baris kontrak dan Project Operations pada fitur Dynamics 365 Customer Engagement akan diaktifkan. Biarkan entitas hukum yang akan menggunakan Project Operations untuk skenario pesanan distok/produksi tidak dipilih.

> [!NOTE]
> Entitas hukum dapat dipilih hanya jika tidak memiliki proyek saat ini.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurasikan parameter akuntansi dan manajemen proyek

Setiap entitas hukum yang menggunakan Project Operations pada Dynamics 365 Customer Engagement memerlukan seperangkat parameter default. Parameter ini dikonfigurasi pada tab **Project Operations** pada halaman **parameter manajemen proyek dan akuntansi**. Parameter itu adalah:

  - **Jenis penagihan default**: Project Operations menggunakan rangkaian tetap default jenis penagihan yang harus dipetakan ke properti baris Finance. Buat rekaman untuk setiap jenis penagihan: **tidak ditentukan**, **Dikenakan biaya**, **Tidak dikenakan biaya**, **gratis**, dan **tidak tersedia**.
  - **Default kategori proyek**: Pilih kategori proyek default yang akan digunakan untuk setiap jenis transaksi. Default ini akan digunakan dalam **jurnal integrasi Project Operations** dan di perkiraan yang mana tidak ada kategori transaksi yang ditentukan untuk aktual proyek.
  - **Perkiraan**: Pilih model perkiraan yang akan digunakan untuk perkiraan waktu dan pengeluaran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]