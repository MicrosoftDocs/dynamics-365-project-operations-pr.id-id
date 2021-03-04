---
title: Membuat entitas dan bidang kustom sebagai dimensi harga
description: Topik ini menyediakan informasi tentang cara membuat rangkaian pilihan kustom atau entitas.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642817"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Membuat entitas dan bidang kustom sebagai dimensi harga

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Lakukan langkah-langkah berikut apabila Anda ingin membuat rangkaian pilihan kustom atau entitas untuk menggunakannya sebagai dimensi harga. Untuk informasi lebih lanjut, lihat [Ringkasan dimensi harga](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah. Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan. Hal ini juga akan membantu untuk menggunakan kembali karya Anda dan lebih memudahkan untuk memindahkan perubahan tersebut ke instans lain. Setelah Anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **Solusi terkelola** dan impor ke instans lain untuk menggunakan kembali pengaturan harga Anda.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga

Dimensi harga dapat berupa rangkaian pilihan atau entitas. Keduanya harus dibuat dalam solusi harga. Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.

### <a name="entity-based-dimensions"></a>Dimensi berdasarkan entitas
Untuk membuat dimensi berbasis entitas, ikuti langkah-langkah berikut:

1. Buka **pengaturan** > **solusi**, lalu klik dua kali **\<your organization name> dimensi harga**.
2. Di Penelusur Solusi, di panel navigasi kiri, pilih **Entitas**.
3. Pilih **baru** untuk membuat entitas baru yang disebut **judul standar**. 
4. Masukkan informasi tersisa yang diperlukan dan kemudian pilih **Simpan**.

> ![Definisi entitas judul standar](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensi berbasis rangkaian pilihan 
Anda dapat membuat dua dimensi berbasis rangkaian pilihan. 

- Gunakan **Lokasi Kerja Sumber Daya** untuk melacak harga pekerjaan lokasi **Rumah** dan pekerjaan **Di Tempat Kerja**. 
- Gunakan **Jam Kerja Sumber Daya** dengan nilai **Reguler** dan **Lembur** untuk menerapkan markup saat pekerjaan selesai.

Grafik berikut memberikan tampilan dimensi **Lokasi Kerja Sumber Daya**. 

> ![Dimensi harga berdasarkan rangkaian pilihan disebut lokasi kerja sumber daya](media/Option-set-PD-called-Resource-Work-Location.png)

Grafik berikut memberikan tampilan dimensi **Jam Kerja Sumber Daya**. 

> ![Dimensi harga berdasarkan rangkaian pilihan disebut jam kerja sumber daya](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Buka **pengaturan** > **solusi**, dan klik dua kali  **\<your organization name> dimensi harga**. 
2. Di Penelusur Solusi, pada panel navigasi kiri, pilih **Rangkaian Pilihan**. 
3. Pilih **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu pilih **simpan**.

## <a name="create-data-for-entity-based-dimensions"></a>Membuat data untuk dimensi berbasis entitas

Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan. Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**. Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.

1. Pilih **Pencarian Tingkat Lanjut**.
2. Pilih entitas **Judul Standar**, lalu pilih **Hasil**. Semua baris di entitas **judul standar** akan ditampilkan.
3. Pilih **Baru**, Di bidang **Nama**, masukkan "Systems Engineer", lalu pilih **Simpan**.
4. Tutup halaman. 
5. Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".

> ![Data sampel untuk entitas Judul Standar](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]