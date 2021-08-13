---
title: Manajemen subkontrak dalam Project Operations
description: Topik ini memberikan ikhtisar proses manajemen subkontrak komprehensif di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994235"
---
# <a name="subcontract-management-in-project-operations"></a>Manajemen subkontrak dalam Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Subkontrak di Microsoft Dynamics 365 Project Operations mendukung alur proses bisnis berikut ini.

![Mensubkontrak alur proses](../media/SubcontractingProcessFlow.png)

Berikut adalah deskripsi langkah demi langkah tentang proses subkontrak.

1. Manajer proyek membuat subkontrak dengan vendor. Secara default, daftar harga yang dilampirkan ke rekaman vendor digunakan untuk subkontrak. Akun vendor memiliki jenis relasi **Vendor** atau **Pemasok**.
2. Manajer proyek dapat memerinci semua pembelian sebagai item baris pada subkontrak. Baris subkontrak dapat untuk waktu, pengeluaran, atau produk. Kelas transaksi yang dipilih di setiap baris subkontrak menentukan tujuan baris tersebut.
3. Manajer akun vendor dan manajer proyek dapat mengulang proses subkontrak. Harga dapat disesuaikan dalam daftar harga Pembelian yang dilampirkan ke Subkontrak.
4. Pada titik ini atau versi yang lebih baru dalam proses, jika baris subkontrak adalah untuk waktu, manajer akun vendor mengaitkan kontak dengan setiap baris subkontrak. Keterkaitan ini memberikan informasi kepada manajer proyek yang sedang mengerjakan subkontrak. Bila kontak dikaitkan dengan baris subkontrak, sistem secara otomatis membuat sumber daya yang dapat dipesan dari kontak, jika sumber daya yang dapat dipesan belum ada.
5. Metode penagihan di setiap baris subkontrak dapat adalah **Harga Tetap** atau **Waktu dan Bahan**. Untuk baris subkontrak harga tetap, Anda dapat mengkonfigurasi jadwal faktur berbasis pencapaian.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
