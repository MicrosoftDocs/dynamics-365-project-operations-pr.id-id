---
title: Laman beranda harga dan dimensi biaya
description: Topik ini memberikan ikhtisar tentang dimensi harga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 137fee27dd2302d47ae12faccde1682cff43db93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284137"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Laman beranda harga dan dimensi biaya

[!include [banner](../includes/psa-now-project-operations.md)]

Dimensi yang digunakan untuk menetapkan harga tenaga kerja dan penetapan biaya dalam organisasi berbasis proyek dipengaruhi oleh atribut berikut:

- Orang yang bekerja sama dengan pengalaman, peran, atau geografi mereka
- Pekerjaan yang akan dilakukan mirip dalam hal kompleksitas atau waktu dalam sehari

Mengingat sifat umum atribut ini dari pekerjaan dan orang-orang yang diperlukan untuk melakukan pekerjaan, ada dua jenis nilai dimensi harga yang tersedia di Project Service Automation: 

- **Rangkaian pilihan** - Atribut yang merupakan enumerasi tetap untuk rangkaian nilai.
- **Nilai berdasarkan entitas** -atribut yang dapat memiliki rangkaian nilai bervariasi yang terbatas namun dapat berubah seiring waktu.

## <a name="pricing-dimensions"></a>Dimensi harga

PSA dikirim dengan seperangkat dimensi harga default. Anda dapat melihat ini dengan membuka **Project Service** > **Parameter**. Pada rekaman parameter, pada tab **Dimensi harga berbasis jumlah**, Verifikasikan bahwa peran , **msdyn_resourcecategory**, dan unit organisasi sumber daya, **msdyn_organizationalunit** memiliki bidang **Berlaku untuk penjualan** dan **berlaku untuk biaya** yang ditetapkan ke **ya**. Ini akan memungkinkan Anda mengkonfigurasi harga dan biaya untuk setiap peran dan kombinasi unit organisasi.

![Tangkapan layar dari parameter Project Service dengan "berlaku for penjualan" disorot](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Jika Anda telah menggunakan bidang bawaan peran dan unit organisasi sebagai dimensi harga sebelum versi 3 dari PSA, tidak akan ada perubahan yang dapat diamati. Anda dapat terus menggunakan project service seperti biasa. 

Jika Anda perlu harga atau biaya untuk sumber daya menggunakan atribut tambahan, Anda dapat membuat bidang kustom, entitas, dan dimensi. Untuk informasi lebih lanjut, lihat topik berikut, Namun perhatikan bahwa Anda harus menyelesaikan prosedur dalam urutan yang tercantum di bawah ini:

- [Membuat bidang dan entitas kustom](create-custom-fields-entities.md)
- [Menambahkan bidang kustom ke pengaturan harga dan entitas transaksi](field-references.md)
- [Mengonfigurasikan bidang kustom sebagai dimensi harga ](set-up-pricing-dimensions.md)
- [Perbarui atribut plug-in untuk menyertakan dimensi harga baru](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Waktu sumber daya manusia
Bagaimana organisasi menghargai waktu sumber daya manusia sering merupakan pertimbangan strategis penting yang secara langsung mempengaruhi profitabilitas organisasi. Bekerja dengan tim keuangan dan pimpinan praktik ketika organisasi Anda siap untuk mengidentifikasi bagaimana cara mengkonfigurasi tagihan dan tarif biaya untuk waktu sumber daya manusia.

Pertimbangan lain untuk harga mencakup apakah akan menggunakan ulang bidang atau entitas yang tidak memiliki dimensi harga namun berlaku sebagai dimensi harga untuk organisasi Anda. Bidang seperti **kategori transaksi** (**msdyn_transactioncategory**) dan **sumber daya dapat dipesan** (**bookableresource**) adalah contoh dimensi kandidat. 

Bayangkan apakah dimensi harga anda harus berupa tabel atau rangkaian pilihan. Jika anda memperkirakan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, buat entitas dan bukan rangkaian pilihan. Mengelola rangkaian pilihan, seperti menambah atau menghilangkan nilai, memerlukan admin atau pengembang sedangkan menambahkan baris baru ke tabel dapat dilakukan oleh sebagian besar pengguna bisnis.

Contoh berikut menunjukkan tarif tagihan yang diatur berdasarkan peran dan unit organisasi sumber daya yang dimiliki sumber daya. Tarif biaya biasanya didasarkan pada kisaran gaji karyawan dan unit organisasi milik mereka. Dalam contoh ini, tabel tingkat tagihan dan tingkat biaya akan terlihat seperti berikut ini.

**Tarif tagihan sampel**

| Peran        | Unit Organisasi    |Unit      |Harga      |Mata Uang  |
| ------------|-------------|----------|----------:|----------|
| Pengembang   | Contoso AS  |Hour | 200|USD     |
| Pengembang   | Aswono India |Hour|   112|USD     |


**Sampel tarif biaya**

| Kisaran gaji     | Unit Organisasi    |Unit      |Harga      |Mata Uang  |
| ----------------|-------------|----------|----------:|----------|
| Perusahaan saya_Band1 | Contoso AS  |Hour | 145|USD     |
| Perusahaan saya_Band2 | Aswono India |Hour|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]