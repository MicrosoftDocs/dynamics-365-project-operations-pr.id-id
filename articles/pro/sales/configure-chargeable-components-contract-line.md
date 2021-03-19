---
title: Mengonfigurasikan komponen yang dikenakan biaya di baris kontrak berbasis proyek - lite
description: Topik ini memberikan informasi tentang cara menambahkan komponen yang dikenakan biaya ke lini kontrak dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf3f2a28fc992d6444b35d6ffa0c3f6cadcf16ea
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273922"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Mengonfigurasikan komponen yang dikenakan biaya di baris kontrak berbasis proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Baris kontrak berbasis proyek telah *menyertakan* komponen dan komponen *yang dapat dikenakan biaya*.

Komponen yang disertakan adalah komponen yang tunduk pada:

  - Metode penagihan dan pemisahan pelanggan
  - Batas Jangan terlampaui 
  - Pengaturan frekuensi faktur yang didefinisikan pada baris kontrak berbasis proyek

Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya menggunakan bidang **Tipe Penagihan**. Bidang **Tipe Penagihan** adalah kumpulan opsi yang memungkinkan nilai berikut dalam konteks baris kontrak:

  - Dikenakan biaya
  - Tidak Dikenakan Biaya

Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori tugas, peran, dan transaksi.

Dapat dikenakan Biaya didefinisikan pada tugas untuk baris kontrak proyek dan berlaku untuk semua kelas transaksi yang disertakan di baris. Jika bidang **Sertakan Tugas** pada baris kontrak kosong atau diatur ke **Seluruh proyek**, tab **Tugas yang dapat dikenakan biaya** tidak akan tersedia.

Bisa dikenakan biaya yang didefinisikan pada peran untuk baris kontrak proyek hanya berlaku untuk kelas transaksi **waktu**. Jika bidang **Sertakan waktu** pada baris kontrak diatur ke **Tidak**, tab **Peran yang dapat dikenakan biaya** tidak akan tersedia.

Bisa dikenakan biaya yang didefinisikan pada kategori transaksi untuk baris kontrak proyek hanya berlaku untuk kelas transaksi **Pengeluaran**. Jika bidang **Sertakan Pengeluaran** pada diatur ke **Tidak**, tab **Kategori yang dapat dikenakan biaya** tidak akan tersedia.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Memperbarui tugas proyek sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Tugas proyek dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu yang memungkinkan pengaturan berikut:

Jika baris kontrak berbasis proyek mencakup **Waktu** dan tugas tertentu, **T1** dikaitkan dengannya sebagai dikenakan biaya. Jika ada baris kontrak kedua yang mencakup **Pengeluaran**, Anda dapat mengaitkan tugas T1 di baris kontrak sebagai tidak dikenakan biaya. Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran tidak dikenakan biaya.

Jenis penagihan tugas dapat dikonfigurasi pada tab **tugas kena biaya** pada baris kontrak dengan memperbarui bidang **jenis penagihan** pada subkisi tugas baris kontrak. Atau, Anda dapat memperbarui bidang **jenis penagihan** pada subkisi dari konfigurasi penagihan tugas proyek yang menunjukkan baris kontrak yang terkait dengan tugas.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Peran dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu.

Jenis penagihan peran dapat dikonfigurasi pada tab **Peran Kena Biaya** dari baris kontrak. Untuk melakukannya, perbarui bidang **jenis penagihan** pada subkisi **peran kena biaya**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya

Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu.

Jenis penagihan transaksi dapat dikonfigurasi pada tab **Kategori Kena Biaya** dari baris kontrak berbasis proyek. Untuk melakukannya, perbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**.

### <a name="resolve-chargeability"></a>Menangani pengenaan biaya

Perkiraan atau aktual yang dibuat untuk waktu hanya akan dianggap dikenakan biaya jika **Waktu** disertakan pada baris kontrak, dan jika **Tugas** dan **Peran** dikonfigurasi sebagai dikenakan biaya pada baris kontrak.

Perkiraan atau aktual yang dibuat untuk pengeluaran hanya akan dianggap dikenakan biaya jika **Pengeluaran** disertakan pada baris kontrak, dan jika **Tugas** dan kategori **Transaksi** dikonfigurasi sebagai dikenakan biaya pada baris kontrak.


| Mencakup Waktu | Mencakup Pengeluaran | Mencakup Tugas | Peran           | Kategori       | Tugas                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ya           | Ya              | Keseluruhan proyek | Dikenakan biaya     | Dikenakan biaya     | Penagihan pada aktual Waktu: **Dikenakan Biaya** </br> Jenis penagihan pada aktual Pengeluaran: **Dikenakan biaya**           |
| Ya           | Ya              | Tugas yang dipilih | Dikenakan biaya     | Dikenakan biaya     | Penagihan pada aktual Waktu: **Dikenakan Biaya** </br> Jenis penagihan pada aktual Pengeluaran: **Dikenakan biaya**           |
| Ya           | Ya              | Tugas yang dipilih | Tidak Dikenakan Biaya | Dikenakan biaya     | Penagihan pada aktual Waktu: **Tidak Dikenakan Biaya** </br> Jenis penagihan pada aktual Pengeluaran: **Dikenakan biaya**       |
| Ya           | Ya              | Tugas yang dipilih | Dikenakan biaya     | Dikenakan biaya     | Penagihan pada aktual Waktu: **Tidak Dikenakan Biaya** </br> Jenis penagihan pada aktual Pengeluaran:   **Tidak Dikenakan biaya** |
| Ya           | Ya              | Tugas yang dipilih | Tidak Dikenakan Biaya | Dikenakan biaya     | Penagihan pada aktual Waktu: **Tidak Dikenakan Biaya** </br> Jenis penagihan pada aktual Pengeluaran:   **Tidak Dikenakan biaya** |
| Ya           | Ya              | Tugas yang dipilih | Tidak Dikenakan Biaya | Tidak Dikenakan Biaya | Penagihan pada aktual Waktu: **Tidak Dikenakan Biaya** </br> Jenis penagihan pada aktual Pengeluaran:   **Tidak Dikenakan biaya** |
| No            | Ya              | Keseluruhan proyek | Tidak dapat diatur   | Dikenakan biaya     | Penagihan pada aktual Waktu: **Tidak tersedia**</br>Jenis penagihan pada aktual Pengeluaran: **Dikenakan biaya**          |
| No            | Ya              | Keseluruhan proyek | Tidak dapat diatur   | Tidak Dikenakan Biaya | Penagihan pada aktual Waktu: **Tidak tersedia**</br> Jenis penagihan pada aktual Pengeluaran: **Tidak Dikenakan biaya**     |
| Ya           | No               | Keseluruhan proyek | Dikenakan biaya     | Tidak dapat diatur   | Penagihan pada aktual Waktu: **Dikenakan Biaya** </br> Jenis penagihan pada aktual Pengeluaran: **Tidak tersedia**        |
| Ya           | No               | Keseluruhan proyek | Tidak Dikenakan Biaya | Tidak dapat diatur   | Penagihan pada aktual Waktu: **Tidak Dikenakan Biaya** </br>Jenis penagihan pada aktual Pengeluaran: **Tidak tersedia**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]