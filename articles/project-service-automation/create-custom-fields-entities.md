---
title: Membuat bidang dan entitas kustom
description: Topik ini menjelaskan cara membuat rangkaian pilihan dan entitas dalam solusi anda sendiri di platform Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752501"
---
# <a name="create-custom-fields-and-entities"></a>Membuat bidang dan entitas kustom 

Selesaikan langkah-langkah berikut saat anda ingin membuat rangkaian pilihan kustom atau entitas pada platform Power Apps.  
Prosedur dalam topik ini harus diselesaikan menggunakan antarmuka web dari Project Service Automation (PSA).

> [!IMPORTANT]
> Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah. Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya. Setelah anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Membuat solusi kustom untuk dimensi harga
1. Dalam PSA, klik **pengaturan** > **solusi**, lalu klik **baru** untuk membuat solusi baru. 
2. Namai solusi, **\<nama organisasi Anda >dimensi harga**, masukkan informasi yang diperlukan lainnya, lalu klik **Simpan**.

> ![Membuat solusi kustom untuk dimensi harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga

Dimensi harga dapat berupa rangkaian pilihan atau entitas. Keduanya harus dibuat dalam solusi harga. Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.

### <a name="entity-based-dimensions"></a>Dimensi berdasarkan entitas

1. Dalam PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **\<nama organisasi > dimensi harga**.
2. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas**.
3. Klik **baru** untuk membuat entitas baru yang disebut **judul standar**. Masukkan informasi tersisa yang diperlukan dan kemudian klik **Simpan**.

> ![Definisi entitas judul standar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensi berbasis rangkaian pilihan 
Anda dapat membuat dua dimensi berbasis rangkaian pilihan. Gunakan **lokasi kerja sumber daya** untuk melacak harga lokasi kerja **Awal** dan pekerjaan **di lokasi** serta gunakan **jam kerja sumber daya** dengan nilai **reguler** dan **lembur** untuk menerapkan markup saat pekerjaan selesai.


1. Dalam PSA, klik **pengaturan** > **solusi**, lalu klik dua kali  **\<nama organisasi > dimensi harga**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih  **rangkaian pilihan**. 
3. Klik **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu klik **simpan**.

> ![Dimensi harga berdasarkan rangkaian pilihan disebut lokasi kerja sumber daya ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensi harga berdasarkan rangkaian pilihan disebut jam kerja sumber daya ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Membuat data untuk dimensi berbasis entitas

Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan. Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**. Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.

1. Di PSA, Klik **Pencarian Tingkat Lanjut**. Pilih entitas **judul standar**, lalu klik **hasil**. Semua baris di entitas **judul standar** akan ditampilkan.
2. Klik **Baru**. Di bidang **Nama**, masukkan "Systems Engineer", lalu klik **Simpan**.
3. Tutup formulir. 
4. Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".

> ![Data sampel untuk entitas judul standar ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tambahkan semua entitas PSA yang diperlukan dan komponen terkait ke solusi dimensi harga
Anda harus menambahkan entitas Project Service berikut ke solusi harga. Gunakan langkah-langkah dalam prosedur ini untuk membuat beberapa perubahan skema penting dalam solusi harga sehingga entitas mengetahui dimensi harga baru.

1. Dalam PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **\<nama organisasi > dimensi harga**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.
3. Di kotak dialog **komponen solusi**, pilih entitas berikut:

- Aktual
- Sumber Daya yang Dapat Dipesan
- Baris Perkiraan
- Rincian Baris Faktur
- Lini Jurnal
- Rincian Baris Kontrak Proyek
- Anggota Tim Proyek
- Rincian Baris Kuotasi
- Markup Harga Peran
- Harga Peran 
- Entri Waktu 

> ![Menambahkan entitas yang ada ke solusi dimensi harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen solusi](media/Dimension-Components.png)

> [!NOTE]
> Pastikan untuk menyertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.

4. Bila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih di atas, klik **tidak**.

> ![Jangan sertakan semua komponen terkait](media/Do-not-include-required.png)


