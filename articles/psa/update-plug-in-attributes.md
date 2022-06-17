---
title: Perbarui atribut plug-in untuk menyertakan dimensi harga baru
description: Artikel ini menyediakan informasi tentang memperbarui atribut plug-in untuk dimensi harga.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
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
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913210"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Perbarui atribut plug-in untuk menyertakan dimensi harga baru

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Jika Anda tidak menggunakan fitur Project Service Automation (PSA) Quoting and Contracting, Anda dapat melewati artikel ini.

Artikel ini mengasumsikan bahwa Anda telah menyelesaikan prosedur dalam artikel, [Membuat bidang dan entitas](create-custom-fields-entities.md) kustom, [Menambahkan bidang kustom ke pengaturan harga dan entitas](field-references.md) transaksional, dan [Menyiapkan bidang kustom sebagai dimensi harga](set-up-pricing-dimensions.md). Jika Anda belum menyelesaikan prosedur tersebut, kembali dan selesaikan dan kemudian kembali ke artikel ini.

Bila detail baris kuotasi dibuat pada halaman **baris kuotasi** untuk baris kuotasi proyek, sistem membuat dua baris perkiraan di background--satu baris untuk sisi biaya perkiraan dan satu untuk sisi penjualan. Ini sama untuk baris kontrak proyek.

Bila Anda membuat perubahan pada kuantitas atau bidang pada sisi biaya, perubahan tersebut disebarkan ke sisi penjualan. Hal ini dimungkinkan karena plug-in berikut yang harus didaftarkan ulang setelah perubahan pada dimensi harga.

- PreOperationContractLineDetailUpdate - Pembaruan **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Pembaruan **msdyn_quotelinetransaction**.

Langkah-langkah berikut menjelaskan proses pendaftaran plug-in.

1. Buka **PluginRegistrationTool** dan Sambungkan ke instans online Anda.
2. Klik **pencarian**, dan Cari plug-in untuk diperbarui.

 ![Tangkapan layar dari pohon pencarian.](media/PRT-1.png)

3. Setelah plug-in ditemukan, pilih dan kemudian klik **pilih formulir utama**.

4. Pilih langkah plug-in untuk diperbarui, klik kanan, lalu pilih **Perbarui**.

 ![Tangkapan layar plug-in yang akan diperbarui.](media/PRT-2.png)
 
5. Di jendela pembaruan, klik elipsis (**...**) di atribut pemfilteran.

 ![Tangkapan layar pembaruan informasi konfigurasi langkah yang ada.](media/PRT-3.png)
 
6. Pilih kotak centang atribut penetapan harga.

 ![Screenshot menampilkan pemilihan kotak centang untuk atribut harga.](media/PRT-4.png)

7. Klik **OK** untuk menutup halaman, lalu pilih **Perbarui langkah**.

 ![Screenshot menampilkan tombol "Perbarui langkah".](media/PRT-5.png)
 
8. Ulangi proses ini untuk plug-in kedua, **PreOperationQuoteLineDetail - Pembaruan msdyn_quotelinetransaction**.

9. Tutup alat registrasi plug-in.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
