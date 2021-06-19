---
title: Membuat solusi kustom untuk dimensi harga
description: Topik ini menjelaskan cara membuat solusi kustom saat membuat dimensi harga kustom.
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
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012320"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Membuat solusi kustom untuk dimensi harga

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Semua perubahan dimensi harga kustom harus dalam solusi terpisah. Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya. Setelah anda membuat perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.

1. Pilih **Pengaturan** > **Solusi**, lalu pilih **Baru**. 
2. Namai solusi, **\<your organization name> dimensi harga**, masukkan informasi yang diperlukan lainnya, lalu pilih **Simpan**.

> ![Membuat solusi kustom untuk dimensi harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tambahkan semua entitas yang diperlukan dan komponen terkait ke solusi dimensi harga
Anda harus menambahkan entitas Project Service berikut ke solusi harga. Selesaikan langkah-langkah dalam prosedur ini untuk membuat beberapa perubahan skema penting dalam solusi harga sehingga entitas mengetahui dimensi harga baru.

1. Pilih **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.
3. Di kotak dialog **komponen solusi**, pilih entitas berikut:

- Aktual
- Sumber Daya Dapat Dipesan
- Baris Perkiraan
- Tugas Proyek
- Detail Baris Faktur
- Lini Jurnal
- Detail Baris Kontrak Proyek
- Anggota Tim Proyek
- Rincian Baris Kuotasi
- Markup Harga Peran
- Harga Peran 
- Entri Waktu 

> ![Menambahkan entitas yang ada ke solusi dimensi harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen solusi](media/Dimension-Components.png)

> [!NOTE]
> Pastikan untuk menyertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.

4. Bila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih, pilih **tidak**.

> ![Jangan sertakan semua komponen terkait](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]