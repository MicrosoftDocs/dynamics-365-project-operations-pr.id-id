---
title: Memperbarui atribut plug-in dengan menyertakan dimensi harga baru
description: Topik ini berisi informasi tentang cara memperbarui atribut plug-in untuk dimensi harga.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3b441b9ea0418e10db80a86613b2c41ea2c4673
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575032"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Memperbarui atribut plug-in dengan menyertakan dimensi harga baru

Topik ini berisi informasi tentang cara memperbarui atribut plug-in untuk dimensi harga.

> [!NOTE]
> Topik ini hanya berlaku untuk fitur kuotasi dan kontrak di Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Prasyarat
Sebelum Anda menyelesaikan langkah-langkah dalam topik ini, Anda harus menyelesaikan prosedur dalam topik berikut:

  - [Membuat bidang dan entitas kustom](create-custom-fields-entities-pricing-dimensions.md) 
  - [Menambahkan bidang kustom ke pengaturan harga dan entitas transaksi ](add-custom-fields-price-setup-transactional-entities.md)
  - [Mengonfigurasikan bidang kustom sebagai dimensi harga](set-up-custom-fields-pricing-dimensions.md). 
  
Jika Anda belum menyelesaikan prosedur tersebut, selesaikan dan kemudian kembali ke topik ini.

## <a name="register-a-plug-in"></a>Mendaftarkan plug-in
Apabila rincian baris kuotasi dibuat pada halaman **Baris Kuotasi** untuk baris kuotasi proyek, sistem membuat dua baris estimasi. Satu baris adalah untuk sisi biaya estimasi dan baris lainnya adalah untuk sisi penjualan. Ini sama untuk baris kontrak proyek.

Apabila Anda membuat perubahan pada kuantitas atau bidang pada sisi biaya, perubahan tersebut juga dilakukan sisi penjualan. Hal ini dimungkinkan karena plug-in PreOperation di entitas Quotelinedetail dan rincian contractline menghubungkan atribut tertentu di sisi biaya ke sisi penjualan pada transaksi. Jika Anda memerlukan perubahan yang dibuat pada nilai dimensi harga di sisi penjualan untuk juga dibuat pada sisi biaya, plug-in berikut harus didaftarkan ulang setelah membuat perubahan pada dimensi harga.

Berikut adalah plug-in untuk memperbarui dan mendaftar ulang:

- PreOperationContractLineDetailUpdate - **Pembaruan msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Pembaruan msdyn_quotelinetransaction**

Lakukan langkah-langkah berikut untuk memperbarui dan mendaftarkan ulang plug-in.

1. Buka **PluginRegistrationTool** dan sambungkan ke lingkungan Project Operations Dataverse.
2. Pilih **Cari**, dan ketik beberapa huruf pertama plug-in yang akan diperbarui.
3. Setelah plug-in ditemukan, pilih dan kemudian pilih **Pilih Formulir Utama**.
4. Pilih langkah **Perbarui msdyn_orderlinetransaction**, klik kanan dan kemudian pilih **Perbarui**.
5. Di halaman dialog **Perbarui**, pilih elipsis (**...**) di atribut pemfilteran.
6. Jendela atribut filter akan terbuka dan menyediakan daftar semua atribut di entitas dan dimensi harga. Pilih kotak centang untuk atribut dimensi harga.
7. Pilih **OK** untuk menutup halaman, lalu pilih **Perbarui Langkah**.
8. Ulangi langkah 2-7 untuk plug-in kedua, **PreOperationQuoteLineDetail**. Untuk plug-in ini, Anda harus memperbarui langkah **Pembaruan msdyn_quotelinetransaction**.
9. Tutup **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]