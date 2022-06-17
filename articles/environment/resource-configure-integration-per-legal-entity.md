---
title: Mengonfigurasikan integrasi Project Operations per entitas hukum
description: Artikel ini menyediakan informasi tentang menyiapkan integrasi oleh badan hukum dalam Operasi Proyek.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914682"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Mengonfigurasikan integrasi Project Operations per entitas hukum 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini memandu Anda melalui langkah-langkah yang diperlukan untuk mengonfigurasi Dynamics 365 Project Operations per badan hukum.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktifkan tombol fitur di Dynamics 365 Finance

Selesaikan langkah-langkah berikut untuk mengaktifkan fitur yang diperlukan.

1. Di Dynamics 365 Finance, buka ruang **kerja Manajemen** Fitur.
2. Dalam **Daftar fitur**, Cari dan Aktifkan fitur berikut:
  
    - **Aktifkan beberapa baris kontrak untuk proyek**
    - **Mengaktifkan Operasi Proyek di Dynamics 365 Customer Engagement**

> [!NOTE]
> Jika Anda tidak melihat **tombol fitur** yang tercantum, Verifikasikan bahwa versi keuangan Anda memenuhi persyaratan versi minimum (versi aplikasi 10.0.13 dengan semua pembaruan kualitas yang diterapkan atau lebih tinggi). Pilih **Periksa pembaruan** untuk me-refresh daftar fitur.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Menentukan skenario penyebaran Project Operations untuk entitas hukum

Anda dapat mengaktifkan Operasi Proyek di Dynamics 365 Customer Engagement di tingkat badan hukum. Anda dapat memiliki satu badan hukum menggunakan Operasi Proyek pada Dynamics 365 Customer Engagement untuk skenario berbasis sumber daya/non-stok. Di lingkungan yang sama, Anda dapat memiliki entitas hukum lain menggunakan Project Operations untuk skenario pesanan produksi/di-stok.

1. Di Dynamics 365 Finance, buka **Manajemen proyek dan akuntansi** > **Setup** > **Manajemen proyek global dan parameter akuntansi**.
2. Dalam daftar badan hukum yang tersedia, pilih entitas di mana beberapa jalur kontrak dan Operasi Proyek pada fitur Dynamics 365 Customer Engagement akan diaktifkan. Biarkan entitas hukum yang akan menggunakan Project Operations untuk skenario pesanan distok/produksi tidak dipilih.

> [!NOTE]
> Entitas hukum dapat dipilih hanya jika tidak memiliki proyek saat ini.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurasikan parameter akuntansi dan manajemen proyek

Setiap badan hukum yang menggunakan Operasi Proyek pada Dynamics 365 Customer Engagement memerlukan serangkaian parameter default. Parameter ini dikonfigurasi pada tab **Project Operations** pada halaman **parameter manajemen proyek dan akuntansi**. Parameter itu adalah:

  - **Jenis penagihan default**: Project Operations menggunakan rangkaian tetap default jenis penagihan yang harus dipetakan ke properti baris Finance. Buat rekaman untuk setiap jenis penagihan: **tidak ditentukan**, **Dikenakan biaya**, **Tidak dikenakan biaya**, **gratis**, dan **tidak tersedia**.
  - **Default kategori proyek**: Pilih kategori proyek default yang akan digunakan untuk setiap jenis transaksi. Default ini akan digunakan dalam **jurnal integrasi Project Operations** dan di perkiraan yang mana tidak ada kategori transaksi yang ditentukan untuk aktual proyek.
  - **Perkiraan**: Pilih model perkiraan yang akan digunakan untuk perkiraan waktu dan pengeluaran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]