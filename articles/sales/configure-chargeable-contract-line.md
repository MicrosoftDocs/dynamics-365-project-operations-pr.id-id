---
title: Mengonfigurasi komponen yang dikenakan biaya dari baris kontrak berbasis proyek
description: Topik ini menyediakan informasi tentang komponen dikenakan biaya dan yang tidak dikenakan yang disertakan di baris kontrak.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2266d8e0fe998e7161ede4cb4eaf7d3c70c54f71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278692"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Mengonfigurasi komponen yang dikenakan biaya dari baris kontrak berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Baris kontrak berbasis proyek memiliki konsep komponen yang dikenakan dan tidak dikenakan biaya yang disertakan.

Komponen yang disertakan diatur dalam metode penagihan, pemisahan pelanggan, batas yang tidak boleh dilebihi, dan pengaturan frekuensi faktur yang ditentukan pada baris kontrak berbasis proyek.

Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya dengan memperbarui bidang **Tipe Penagihan**.

Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori peran dan transaksi.

Untuk baris kontrak proyek, Bisa dikenakan biaya yang didefinisikan pada peran hanya berlaku untuk kelas transaksi **waktu**. Jika **Sertakan waktu** diatur ke **Tidak** di baris kontrak proyek, tab **Peran yang dapat dikenakan biaya** tidak tersedia.

Bisa dikenakan biaya yang didefinisikan pada kategori transaksi untuk baris kontrak proyek hanya berlaku untuk kelas transaksi **Pengeluaran**. Jika **Sertakan Pengeluaran** diatur ke **Tidak** di baris kontrak proyek, tab **Kategori yang dapat dikenakan biaya** tidak tersedia.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Peran dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak berbasis proyek tertentu.

Di tab **Peran kena biaya** pada baris kontrak berbasis proyek, di sub kisi **Kategori kena biaya** pada bidang **Jenis penagihan**, perbarui jenis penagihan untuk peran.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya

Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak berbasis proyek tertentu.

Di tab **Kategori kena biaya** pada baris kontrak berbasis proyek, di sub kisi **Kategori kena biaya** pada bidang **Jenis penagihan**, perbarui jenis penagihan untuk transaksi.

### <a name="resolve-chargeability"></a>Menangani pengenaan biaya

Perkiraan atau aktual yang dibuat untuk waktu hanya akan dianggap dikenakan biaya jika waktu disertakan pada baris kontrak, dan jika peran dikonfigurasi sebagai dikenakan biaya pada baris kontrak.

Perkiraan atau aktual yang dibuat untuk pengeluaran hanya akan dianggap dikenakan biaya jika Pengeluaran disertakan pada baris kontrak, dan jika kategori Transaksi dikonfigurasi sebagai dikenakan biaya pada baris kontrak.

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