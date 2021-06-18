---
title: Membuat solusi untuk dimensi harga kustom
description: Topik ini berisi informasi tentang cara membuat solusi untuk dimensi harga kustom.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010340"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Membuat solusi untuk dimensi harga kustom

 _**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_ 

>[!IMPORTANT]
>Semua perubahan dimensi harga kustom harus dalam solusi terpisah. Praktik terbaik yang penting ini memberikan fleksibilitas untuk memperbarui atau menghapus perubahan yang diperlukan, sehingga membantu dalam menggunakan kembali karya Anda, dan akan lebih memudahkan saat memindahkan perubahan ke berbagai instans lainnya. Setelah Anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai solusi **Terkelola**, dan kemudian impor ke instans lain untuk digunakan kembali.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Membuat solusi untuk dimensi harga kustom

1.  Pilih **Pengaturan** > **Solusi**, lalu pilih **Baru**.
2.  Beri nama untuk solusi tersebut, *dimensi harga <your organization name>*.
3. Masukkan informasi tersisa yang diperlukan dan kemudian pilih **Simpan**.

  ![Membuat solusi untuk dimensi harga kustom](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tambahkan semua entitas yang diperlukan dan komponen terkait ke solusi dimensi harga

Tambahkan entitas Project Service berikut ke solusi harga Anda untuk membuat perubahan skema yang penting dalam solusi harga. Setelah Anda menyelesaikan prosedur ini, entitas akan mengenali dimensi harga yang baru.

1.  Pilih **Pengaturan** > **Solusi**, lalu klik dua kali **<*nama organisasi Anda*> dimensi harga**.
2.  Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.
3.  Di kotak dialog **komponen solusi**, pilih entitas berikut:
 
   - **Aktual**
   - **Sumber Daya Dapat Dipesan**
   - **Baris Perkiraan**
   - **Tugas Proyek**
   - **Rincian Baris Faktur**
   - **Lini Jurnal**
   - **Rincian Baris Kontrak Proyek**
   - **Anggota Tim Proyek**
   - **Rincian Baris Kuotasi**
   - **Markup Harga Peran**
   - **Harga Peran**
   - **Entri Waktu**
 
   ![Menambahkan solusi dimensi harga kustom berbagai entitas yang ada](./media/Existing-entities-to-PD-solution.png)
 
 4. Untuk setiap entitas, tinjau komponen yang ditambahkan dan daftar akhir aset entitas untuk setiap entitas. 

   >[!NOTE]
   > Sertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.

  ![Entitas ditambahkan](./media/solution-component-selection.png)


5.  Apabila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih, pilih **Tidak, jangan sertakan komponen yang diperlukan.**

    ![Termasuk entitas dependen](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]