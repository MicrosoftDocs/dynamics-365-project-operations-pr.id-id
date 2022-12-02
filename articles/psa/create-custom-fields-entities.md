---
title: Membuat bidang dan entitas kustom
description: Artikel ini menjelaskan cara membuat rangkaian pilihan dan entitas dalam solusi anda sendiri di platform Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926918"
---
# <a name="create-custom-fields-and-entities"></a>Membuat bidang dan entitas kustom 

[!include [banner](../includes/psa-now-project-operations.md)]

Selesaikan langkah-langkah berikut saat anda ingin membuat rangkaian pilihan kustom atau entitas pada platform Power Apps.  
Prosedur dalam artikel ini harus diselesaikan menggunakan antarmuka web dari Project Service Automation (PSA).

> [!IMPORTANT]
> Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah. Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya. Setelah anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga

Dimensi harga dapat berupa rangkaian pilihan atau entitas. Keduanya harus dibuat dalam solusi harga. Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.

### <a name="entity-based-dimensions"></a>Dimensi berdasarkan entitas

1. Di PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**.
2. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas**.
3. Klik **baru** untuk membuat entitas baru yang disebut **judul standar**. Masukkan informasi tersisa yang diperlukan dan kemudian klik **Simpan**.

> ![Definisi entitas judul standar.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensi berbasis rangkaian pilihan 
Anda dapat membuat dua dimensi berbasis rangkaian pilihan. Gunakan **lokasi kerja sumber daya** untuk melacak harga lokasi kerja **Awal** dan pekerjaan **di lokasi** serta gunakan **jam kerja sumber daya** dengan nilai **reguler** dan **lembur** untuk menerapkan markup saat pekerjaan selesai.


1. Di PSA, klik **pengaturan** > **solusi**, lalu klik dua kali  **dimensi harga \<your organization name>**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih  **rangkaian pilihan**. 
3. Klik **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu klik **simpan**.

> ![Dimensi harga berdasarkan rangkaian pilihan disebut lokasi kerja sumber daya.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensi harga berdasarkan rangkaian pilihan disebut jam kerja sumber daya.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Membuat data untuk dimensi berbasis entitas

Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan. Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**. Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.

1. Di PSA, Klik **Pencarian Tingkat Lanjut**. Pilih entitas **judul standar**, lalu klik **hasil**. Semua baris di entitas **judul standar** akan ditampilkan.
2. Klik **Baru**. Di bidang **Nama**, masukkan "Systems Engineer", lalu klik **Simpan**.
3. Tutup formulir. 
4. Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".

> ![Data sampel untuk entitas Judul Standar.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
