---
title: Membuat dan menerapkan persyaratan retensi pembayaran vendor
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi dan memelihara persyaratan retensi untuk pembayaran vendor.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078621"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Membuat dan menerapkan persyaratan retensi pembayaran vendor

[!include [banner](../includes/banner.md)] 

Mengatur persyaratan retensi pembayaran vendor untuk proyek berguna bila organisasi Anda ingin mempertahankan bagian dari pembayaran yang dilakukan ke vendor. Misalnya, bila Anda ingin menyimpan pembayaran ke vendor hingga produk yang dikirim memenuhi harapan Anda. Persyaratan retensi pembayaran vendor dapat ditentukan saat Anda menegosiasikan kontrak vendor.

## <a name="create-vendor-payment-retention-terms"></a>Membuat persyaratan retensi pembayaran vendor

Anda dapat memasukkan persentase pembayaran vendor untuk retensi dan persentase dari jumlah disimpan sebelumnya yang akan dirilis. Jumlah akan disimpan secara otomatis pada faktur vendor hingga kontrak mencapai status penyelesaian yang ditentukan. Setelah mengkonfigurasi persyaratan retensi, Anda dapat menerapkannya ke proyek apa pun untuk vendor tersebut.

Gunakan langkah-langkah berikut untuk mengkonfigurasi dan memelihara persyaratan retensi untuk pembayaran vendor. 

1. Buka **manajemen proyek dan akuntansi** > **Retensi** > **persyaratan retensi pembayaran vendor**.
2. Pilih **baru** untuk menambahkan persyaratan retensi vendor baru. Nilai **id aturan** untuk persyaratan baru akan dimasukkan secara otomatis. 
3. Masukkan deskripsi singkat di bidang **deskripsi** , dan pada fasttab **persyaratan** , pilih **Tambah baris** untuk memasukkan nilai persyaratan untuk berikut ini:

   - **Persentase unit yang dikirim** : masukkan persentase penyelesaian untuk persyaratan. Jumlah akan ditahan secara otomatis pada faktur vendor hingga tahapan penyelesaian proyek setara dengan persentase yang ditentukan. Misalnya, jika Anda memasukkan 50,00, jumlah ditahan hingga proyek 50 persen selesai.
   - **Persentase untuk ditahan** : masukkan persentase jumlah faktur vendor yang akan ditahan. Misalnya, jika Anda memasukkan 10,00, maka 10 persen dari jumlah faktur vendor ditahan hingga proyek mencapai persentase Penyelesaian sebagaimana diatur dalam **bidang persentase unit yang dikirim**.
   - **Persentase untuk rilis** : Pilih **Tambah baris** untuk memasukkan persentase dari jumlah yang sebelumnya ditahan akan dirilis untuk tingkat penyelesaian proyek yang dipilih.

> [!NOTE]
> Jika Anda memiliki lebih dari satu tonggak untuk tingkat penyelesaian proyek yang berbeda, masukkan baris persyaratan retensi vendor terpisah untuk setiap aturan retensi. Setiap baris dapat menentukan persentase retensi berbeda dan persentase rilis berbeda untuk setiap tingkat penyelesaian proyek yang ditentukan.

Setelah Anda membuat persyaratan retensi vendor, Anda dapat menerapkannya persyaratan tersebut ke sebuah proyek.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Terapkan persyaratan retensi vendor ke proyek

1. Buka **Management Proyek dan Akuntansi** > **Proyek** > **semua proyek** dan buka proyek dari halaman daftar proyek.
2. Pada fasttab **perjanjian vendor** , pilih **Tambah baris**.
3. Di **bidang kode akun** , pilih salah satu pilihan berikut: 

   - **Tabel** : persyaratan retensi vendor berlaku untuk satu vendor.
   - **Grup** : persyaratan retensi vendor berlaku untuk semua vendor dalam grup vendor.
   - **Semua** : persyaratan retensi vendor berlaku untuk semua vendor.

4. Di **bidang vendor/grup vendor** , pilih vendor atau grup vendor yang menerapkan persyaratan retensi vendor. Jika Anda memilih **semua** di langkah sebelumnya, bidang ini tidak tersedia.
5. Di bidang **persyaratan retensi vendor** , pilih persyaratan retensi yang Anda buat di prosedur sebelumnya.
6. Jika proyek juga memiliki persyaratan bayar-saat-dibayar (PWP) yang diatur untuk vendor, masukkan persentase ambang batas untuk proyek di bidang **persentase ambang PWP**.

Persyaratan retensi vendor juga ditampilkan pada pesanan pembelian yang Anda buat untuk vendor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]