---
title: Subkontrak di rilis Akses Awal Oktober 2021
description: Topik ini memberikan ikhtisar kemampuan subkontrak dalam Project Operations yang merupakan bagian dari rilis akses awal Oktober 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383699"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subkontrak di rilis Akses Awal Oktober 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Topik ini memberikan ikhtisar kemampuan subkontrak dalam Dynamics 365 Project Operations yang merupakan bagian dari rilis akses awal Oktober 2021. Rangkaian fitur ini tidak siap untuk produksi atau lingkungan langsung, sehingga fitur ini akan tetap dalam rilis akses awal hingga rangkaian fitur lengkap dirilis. Kami sangat menyarankan agar Anda tidak menggunakan rangkaian fitur subkontrak untuk skenario produksi langsung hingga banner pratinjau dihilangkan. 

Daftar berikut memberikan garis besar tentang informasi yang saat ini tersedia di rilis Akses Awal Oktober 2021:

1. Manajer proyek membuat subkontrak dengan vendor. Secara default, daftar harga yang dilampirkan ke rekaman vendor digunakan untuk subkontrak. Akun vendor memiliki jenis relasi **Vendor** atau **Pemasok**.

2. Manajer proyek dapat memerinci semua pembelian sebagai item baris pada subkontrak. Baris subkontrak dapat untuk waktu, pengeluaran, atau produk. Kelas transaksi baris subkontrak menentukan tujuan baris tersebut.

3. Manajer akun vendor dan manajer proyek dapat mengulang proses subkontrak. Harga dapat disesuaikan dalam daftar harga Pembelian yang dilampirkan ke Subkontrak.

4. Pada titik ini atau versi yang lebih baru dalam proses, jika baris subkontrak adalah untuk waktu, manajer akun vendor mengaitkan kontak vendor dengan setiap baris subkontrak. Keterkaitan ini memberikan informasi kepada manajer proyek yang sedang mengerjakan subkontrak. Bila kontak vendor dikaitkan dengan baris subkontrak, sistem secara otomatis membuat sumber daya yang dapat dipesan dari kontak, jika sumber daya yang dapat dipesan belum ada.

5. Metode penagihan di setiap baris subkontrak dapat adalah **Harga Tetap** atau **Waktu dan Bahan**. Untuk baris subkontrak harga tetap, jadwal faktur berbasis pencapaian dikonfigurasikan.

Langkah-langkah lainnya dalam alur proses bisnis untuk subkontrak yang diuraikan dalam Ikhtisar saat ini tidak tersedia. Saat fungsi baru ditambahkan, topik ini akan diperbarui. 

Ilustrasi berikut menunjukkan rilis Akses Awal Subkontrak dibandingkan dengan proses bisnis end-to-end.

![Mensubkontrak alur proses](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Rilis Akses Awal baris subkontrak berbasis kuantitas dan berbasis kerja
Di rilis Akses Awal Oktober 2021, hanya baris subkontrak berbasis kuantitas yang didukung. Ini berarti bahwa baris subkontrak dapat digunakan untuk membeli waktu, pengeluaran, atau bahan dari vendor tetapi bukan seluruh badan kerja. Ini juga berarti bahwa kuantitas yang dibeli (unit waktu, pengeluaran, atau kuantitas bahan) pada baris subkontrak dapat digunakan pada proyek apa pun dalam sistem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
