---
title: Mengonfigurasikan integrasi Project Operations per entitas hukum
description: Topik ini menyediakan informasi tentang mengonfigurasikan integrasi per entitas hukum di Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585842"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Mengonfigurasikan integrasi Project Operations per entitas hukum 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Tindakan topik akan memandu Anda melakukan langkah-langkah yang diperlukan untuk mengkonfigurasi Dynamics 365 Project Operations per entitas hukum.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Mengaktifkan tombol fitur di Dynamics 365 Finance

Selesaikan langkah-langkah berikut untuk mengaktifkan fitur yang diperlukan.

1. Di Dynamics 365 Finance, buka **ruang kerja Manajemen** Fitur.
2. Dalam **Daftar fitur**, Cari dan Aktifkan fitur berikut:
  
    - **Aktifkan beberapa baris kontrak untuk proyek**
    - **Aktifkan Operasi Proyek di Dynamics 365 Customer Engagement**

> [!NOTE]
> Jika Anda tidak melihat **tombol fitur** yang tercantum, Verifikasikan bahwa versi keuangan Anda memenuhi persyaratan versi minimum (versi aplikasi 10.0.13 dengan semua pembaruan kualitas yang diterapkan atau lebih tinggi). Pilih **Periksa pembaruan** untuk me-refresh daftar fitur.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Menentukan skenario penyebaran Project Operations untuk entitas hukum

Anda dapat mengaktifkan Operasi Proyek di Dynamics 365 Customer Engagement pada tingkat badan hukum. Anda dapat memiliki satu badan hukum menggunakan Operasi Proyek di Dynamics 365 Customer Engagement untuk skenario berbasis sumber daya/non-stok. Di lingkungan yang sama, Anda dapat memiliki entitas hukum lain menggunakan Project Operations untuk skenario pesanan produksi/di-stok.

1. Di Dynamics 365 Finance, buka **Manajemen proyek dan pengaturan** > **akuntansi** > **Parameter manajemen proyek dan akuntansi global**.
2. Dalam daftar badan hukum yang tersedia, pilih entitas di mana beberapa jalur kontrak dan Operasi Proyek pada fitur Dynamics 365 Customer Engagement akan diaktifkan. Biarkan entitas hukum yang akan menggunakan Project Operations untuk skenario pesanan distok/produksi tidak dipilih.

> [!NOTE]
> Entitas hukum dapat dipilih hanya jika tidak memiliki proyek saat ini.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurasikan parameter akuntansi dan manajemen proyek

Setiap badan hukum yang menggunakan Operasi Proyek di Dynamics 365 Customer Engagement memerlukan serangkaian parameter default. Parameter ini dikonfigurasi pada tab **Project Operations** pada halaman **parameter manajemen proyek dan akuntansi**. Parameter itu adalah:

  - **Jenis penagihan default**: Project Operations menggunakan rangkaian tetap default jenis penagihan yang harus dipetakan ke properti baris Finance. Buat rekaman untuk setiap jenis penagihan: **tidak ditentukan**, **Dikenakan biaya**, **Tidak dikenakan biaya**, **gratis**, dan **tidak tersedia**.
  - **Default kategori proyek**: Pilih kategori proyek default yang akan digunakan untuk setiap jenis transaksi. Default ini akan digunakan dalam **jurnal integrasi Project Operations** dan di perkiraan yang mana tidak ada kategori transaksi yang ditentukan untuk aktual proyek.
  - **Perkiraan**: Pilih model perkiraan yang akan digunakan untuk perkiraan waktu dan pengeluaran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]