---
title: Perbarui atribut plug-in untuk menyertakan dimensi harga baru
description: Topik ini menyediakan informasi tentang memperbarui atribut plug-in untuk dimensi harga.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281797"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Perbarui atribut plug-in untuk menyertakan dimensi harga baru

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Jika Anda tidak menggunakan fitur kuotasi dan kontrak Project Service Automation (PSA), Anda dapat melewati topik ini.

Topik ini mengasumsikan bahwa anda telah menyelesaikan prosedur dalam topik, [membuat bidang kustom dan entitas](create-custom-fields-entities.md), [menambahkan bidang kustom untuk penyiapan harga dan entitas transaksi](field-references.md) serta [Mengonfigurasikan bidang kustom sebagai dimensi harga](set-up-pricing-dimensions.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan selesaikan dan kemudian kembali ke topik ini.

Bila detail baris kuotasi dibuat pada halaman **baris kuotasi** untuk baris kuotasi proyek, sistem membuat dua baris perkiraan di background--satu baris untuk sisi biaya perkiraan dan satu untuk sisi penjualan. Ini sama untuk baris kontrak proyek.

Bila Anda membuat perubahan pada kuantitas atau bidang pada sisi biaya, perubahan tersebut disebarkan ke sisi penjualan. Hal ini dimungkinkan karena plug-in berikut yang harus didaftarkan ulang setelah perubahan pada dimensi harga.

- PreOperationContractLineDetailUpdate - Pembaruan **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Pembaruan **msdyn_quotelinetransaction**.

Langkah-langkah berikut menjelaskan proses pendaftaran plug-in.

1. Buka **PluginRegistrationTool** dan Sambungkan ke instans online Anda.
2. Klik **pencarian**, dan Cari plug-in untuk diperbarui.

 ![Tangkapan layar dari pohon pencarian](media/PRT-1.png)

3. Setelah plug-in ditemukan, pilih dan kemudian klik **pilih formulir utama**.

4. Pilih langkah plug-in untuk diperbarui, klik kanan, lalu pilih **Perbarui**.

 ![Tangkapan layar plug-in yang akan diperbarui](media/PRT-2.png)
 
5. Di jendela pembaruan, klik elipsis (**...**) di atribut pemfilteran.

 ![Tangkapan layar pembaruan informasi konfigurasi langkah yang ada](media/PRT-3.png)
 
6. Pilih kotak centang atribut penetapan harga.

 ![Screenshot menampilkan pemilihan kotak centang untuk atribut harga](media/PRT-4.png)

7. Klik **OK** untuk menutup halaman, lalu pilih **Perbarui langkah**.

 ![Screenshot menampilkan tombol "Perbarui langkah"](media/PRT-5.png)
 
8. Ulangi proses ini untuk plug-in kedua, **PreOperationQuoteLineDetail - Pembaruan msdyn_quotelinetransaction**.

9. Tutup alat registrasi plug-in.



[!INCLUDE[footer-include](../includes/footer-banner.md)]