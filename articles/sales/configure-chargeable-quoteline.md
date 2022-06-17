---
title: Mengonfigurasikan komponen kena biaya pada baris kuotasi berbasis proyek
description: Artikel ini memberikan informasi tentang komponen yang disertakan, dikenakan biaya, dan tidak dikenakan biaya pada baris kutipan berbasis proyek.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff409132ef9103641578f9c94f8ea1ff56738a71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915556"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Mengonfigurasikan komponen kena biaya pada baris kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Baris kuotasi berbasis proyek dapat mencakup komponen dan komponen yang dapat dikenai biaya.

Komponen yang disertakan diatur dalam metode penagihan, pemisahan pelanggan, tidak melebihi batas, dan pengaturan frekuensi faktur yang ditentukan pada baris kuotasi berbasis proyek.
Subset komponen yang disertakan dapat ditandai sebagai dapat dikenai biaya menggunakan **Jenis Penagihan**. Anda dapat memilih salah satu pilihan berikut di bidang **Jenis Penagihan** dalam konteks baris kuotasi:

   - Dikenakan biaya
   - Tidak Dikenakan Biaya

Komponen kena biaya dapat didefinisikan pada kategori peran dan transaksi.

Pengenaan biaya yang ditentukan pada peran untuk baris kuotasi proyek hanya berlaku untuk kelas transaksi **Waktu**. Jika baris kuotasi proyek memiliki tab **Sertakan Waktu** = **Tidak**, tab **Peran Kena Biaya** tidak tersedia.

Pengenaan biaya yang ditentukan pada kategori transaksi untuk baris kuotasi proyek hanya berlaku untuk kelas transaksi **Pengeluaran**. Jika baris kuotasi proyek memiliki tab **Sertakan Pengeluaran** = **Tidak**, tab **Kategori Kena Biaya** tidak tersedia.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya
Peran dapat dikenakan biaya atau tidak dikenakan biaya pada baris kuotasi berbasis proyek. Jenis penagihan pada peran dapat dikonfigurasi di tab **Peran Kena Biaya** di baris kuotasi berbasis proyek. Untuk melakukannya, perbarui **Jenis Penagihan** pada subkisi **Peran Kena Biaya**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya
Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kuotasi berbasis proyek. Jenis penagihan pada transaksi dapat dikonfigurasi di tab **Kategori Kena Biaya** di baris kuotasi berbasis proyek. Untuk melakukannya, perbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**. 

## <a name="resolve-chargeability"></a>Menangani pengenaan biaya

Nilai estimasi atau aktual yang dibuat untuk waktu hanya akan dianggap kena biaya jika waktu disertakan pada baris kuotasi dan jika peran dikonfigurasi sebagai kena biaya.
Nilai estimasi atau aktual yang dibuat untuk pengeluaran hanya akan dianggap kena biaya jika pengeluaran disertakan pada baris kuotasi dan jika kategori transaksi dikonfigurasi sebagai kena biaya pada baris kuotasi. Tabel berikut menunjukkan cara default pengenaan biaya pada setiap nilai aktual. Nilai default berdasarkan pada komponen yang disertakan dan jenis penagihan yang diatur pada baris kuotasi.

| Mencakup Waktu | Mencakup Pengeluaran | Peran | Kategori | Tugas |
| --- | --- | --- | --- | --- |
| Ya | Ya | Dikenakan biaya | Dikenakan biaya | Penagihan pada aktual Waktu: Dikenakan Biaya </br>Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya |
| Ya | Ya | Tidak Dikenakan Biaya | Dikenakan biaya | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya </br>Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya |
| Ya | Ya | Tidak Dikenakan Biaya | Tidak Dikenakan Biaya | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya </br>Jenis penagihan pada aktual Pengeluaran: Tidak Dikenakan biaya |
| No | Ya | Tidak dapat diatur | Dikenakan biaya | Penagihan pada aktual Waktu: Tidak tersedia </br>Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya |
| No | Ya | Tidak dapat diatur | Tidak Dikenakan Biaya | Penagihan pada aktual Waktu: Tidak tersedia </br>Jenis penagihan pada aktual Pengeluaran: Tidak Dikenakan biaya |
| Ya | No | Dikenakan biaya | Tidak dapat diatur | Penagihan pada aktual Waktu: Dikenakan Biaya </br>Jenis penagihan pada aktual Pengeluaran: Tidak tersedia |
| Ya | No | Tidak Dikenakan Biaya | Tidak dapat diatur | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya </br> Jenis penagihan pada aktual Pengeluaran: Tidak tersedia |


[!INCLUDE[footer-include](../includes/footer-banner.md)]