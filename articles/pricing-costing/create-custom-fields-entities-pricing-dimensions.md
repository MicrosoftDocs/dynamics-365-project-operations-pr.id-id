---
title: Membuat entitas dan bidang kustom sebagai dimensi harga
description: Topik ini menyediakan informasi tentang cara membuat rangkaian pilihan kustom atau entitas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078522"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Membuat entitas dan bidang kustom sebagai dimensi harga

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Selesaikan langkah-langkah berikut saat anda ingin membuat rangkaian pilihan kustom atau entitas.

> [!IMPORTANT]
> Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah. Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya. Setelah anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Membuat solusi kustom untuk dimensi harga
1. Buka **pengaturan** > **solusi** , lalu pilih **baru** untuk membuat solusi baru. 
2. Namai solusi, **\<your organization name> dimensi harga** , masukkan informasi yang diperlukan lainnya, lalu pilih **Simpan**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga

Dimensi harga dapat berupa rangkaian pilihan atau entitas. Keduanya harus dibuat dalam solusi harga. Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.

### <a name="entity-based-dimensions"></a>Dimensi berdasarkan entitas

1. Buka **pengaturan** > **solusi** , lalu klik dua kali **\<your organization name> dimensi harga**.
2. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas**.
3. Pilih **baru** untuk membuat entitas baru yang disebut **judul standar**. 
4. Masukkan informasi tersisa yang diperlukan dan kemudian pilih **Simpan**.


### <a name="option-set-based-dimensions"></a>Dimensi berbasis rangkaian pilihan 
Anda dapat membuat dua dimensi berbasis rangkaian pilihan. Gunakan **lokasi kerja sumber daya** untuk melacak harga lokasi kerja **Awal** dan pekerjaan **di lokasi** serta gunakan **jam kerja sumber daya** dengan nilai **reguler** dan **lembur** untuk menerapkan markup saat pekerjaan selesai.


1. Buka **pengaturan** > **solusi** , dan klik dua kali  **\<your organization name> dimensi harga**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih  **rangkaian pilihan**. 
3. Pilih **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu pilih **simpan**.

## <a name="create-data-for-entity-based-dimensions"></a>Membuat data untuk dimensi berbasis entitas

Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan. Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**. Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.

1. Pilih **pencarian tingkat lanjut** , pilih **judul standar** entitas, lalu pilih **hasil**. Semua baris di entitas **judul standar** akan ditampilkan.
2. Pilih **Baru** , Di bidang **Nama** , masukkan "Systems Engineer", lalu pilih **Simpan**.
3. Tutup formulir. 
4. Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tambahkan semua entitas yang diperlukan dan komponen terkait ke solusi dimensi harga
Anda harus menambahkan entitas berikut ke solusi harga. Gunakan langkah-langkah dalam prosedur ini untuk membuat beberapa perubahan skema penting dalam solusi harga sehingga entitas mengetahui dimensi harga baru.

1. Pilih **pengaturan** > **solusi** , dan klik dua kali **\<your organization name> dimensi harga**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.
3. Di kotak dialog **komponen solusi** , pilih entitas berikut:

  - Aktual
  - Sumber Daya yang Dapat Dipesan
  - Baris Perkiraan
  - Rincian Baris Faktur
  - Lini Jurnal
  - Rincian Baris Kontrak Proyek
  - Anggota Tim Proyek
  - Detail Baris Kuotasi
  - Markup Harga Peran
  - Harga Peran 
  - Entri Waktu 


> [!NOTE]
> Pastikan untuk menyertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.

4. Bila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih di atas, pilih **tidak**.

