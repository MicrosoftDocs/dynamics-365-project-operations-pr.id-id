---
title: Ikhtisar dimensi harga
description: Topik ini menyediakan informasi tentang dimensi harga di Dynamics 365 Project operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898220"
---
# <a name="pricing-dimensions-overview"></a>Ikhtisar dimensi harga

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dimensi yang digunakan dalam sumber daya manusia untuk mengatur harga dan biaya jatuh ke dalam dua Kategori:

- Sosial
- Pekerjaan Terencana

Oleh karena itu, ada dua jenis nilai dimensi harga yang tersedia:

- **Rangkaian pilihan**: dimensi yang merupakan enumerasi tetap untuk rangkaian nilai.
- **Nilai berdasarkan entitas**: dimensi yang dapat berupa rangkaian nilai bervariasi.

## <a name="pricing-dimensions"></a>Dimensi harga

Dynamics 365 Project Operations dikirim dengan seperangkat default dimensi harga. Anda dapat melihat dimensi harga ini dengan membuka **Project Operations** > **Parameter**. Pada rekaman parameter, pada tab **Dimensi harga berbasis jumlah**, Verifikasikan bahwa peran , **msdyn_resourcecategory**, dan unit organisasi sumber daya, **msdyn_organizationalunit** memiliki bidang **Berlaku untuk penjualan** dan **berlaku untuk biaya** yang ditetapkan ke **ya**. Dengan mengaktifkan bidang ini, Anda dapat mengkonfigurasi harga dan biaya untuk setiap peran dan kombinasi unit organisasi.

Jika Anda perlu harga atau biaya untuk sumber daya menggunakan atribut tambahan, Anda dapat membuat bidang kustom, entitas, dan dimensi.

## <a name="pricing-human-resource-time"></a>Waktu sumber daya manusia
Bagaimana organisasi menghargai waktu sumber daya manusia sering merupakan pertimbangan strategis penting yang secara langsung mempengaruhi profitabilitas organisasi. Bekerja dengan tim keuangan dan pimpinan praktik ketika organisasi Anda siap untuk mengidentifikasi bagaimana cara mengkonfigurasi tagihan dan tarif biaya untuk waktu sumber daya manusia.

Pertimbangan lain untuk harga mencakup apakah akan menggunakan ulang bidang atau entitas yang tidak memiliki dimensi harga namun berlaku sebagai dimensi harga untuk organisasi Anda. Bidang seperti **kategori transaksi** (**msdyn_transactioncategory**) dan **sumber daya dapat dipesan** (**bookableresource**) adalah contoh dimensi kandidat. 

Bayangkan apakah dimensi harga anda harus berupa tabel atau rangkaian pilihan. Jika anda memperkirakan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda dapat membuat entitas dan bukan rangkaian pilihan. Mengelola rangkaian pilihan, seperti menambah atau menghilangkan nilai, memerlukan admin atau pengembang sedangkan menambahkan baris baru ke tabel dapat dilakukan oleh sebagian besar pengguna.

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
