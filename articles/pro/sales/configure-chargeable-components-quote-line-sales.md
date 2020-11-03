---
title: Konfigurasikan komponen yang dikenakan biaya pada baris kuotasi
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi komponen dikenakan biaya dan yang tidak dikenakan biaya pada baris kuotasi berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078605"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurasikan komponen yang dikenakan biaya pada baris kuotasi

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Baris kuotasi berbasis proyek memiliki konsep *menyertakan* komponen dan komponen *yang dapat dikenakan biaya*.

Komponen yang tergantung pada:

  - Metode penagihan dan pemisahan pelanggan
  - Batas Jangan terlampaui 
  - Pengaturan frekuensi faktur yang didefinisikan pada baris kuotasi berbasis proyek

Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya menggunakan bidang **Tipe Penagihan**. Bidang **Tipe Penagihan** adalah kumpulan opsi yang memungkinkan nilai berikut dalam konteks baris kuotasi:

  - Dikenakan biaya
  - Tidak Dikenakan Biaya

Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori tugas, peran, dan transaksi.

Dapat dikenakan Biaya didefinisikan pada tugas untuk baris kuotasi dan berlaku untuk semua kelas transaksi yang disertakan di baris itu. Jika bidang **Sertakan Tugas** diatur ke **Seluruh proyek** atau dibiarkan kosong, tab **Tugas yang dapat dikenakan biaya** tidak tersedia.

Bisa dikenakan biaya didefinisikan pada peran untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **waktu**. Jika bidang, **Sertakan waktu** diatur ke **Tidak** di baris kuotasi proyek, tab **Peran yang dapat dikenakan biaya** tidak tersedia.

Bisa dikenakan biaya didefinisikan pada kategori transaksi untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **Pengeluaran**. Jika bidang, **Sertakan Pengeluaran** diatur ke **Tidak** di baris kuotasi proyek, tab **Kategori yang dapat dikenakan biaya** tidak tersedia.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Memperbarui tugas proyek yang akan dikenakan biaya atau tidak dapat dikenakan biaya

Tugas proyek dapat dikenakan biaya atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu yang memungkinkan pengaturan berikut:

Jika baris kuotasi berbasis proyek mencakup **waktu** dan tugas **T1** , tugas dikaitkan ke baris kuotasi sebagai dikenakan biaya. Jika ada baris kuotasi kedua yang mencakup **Pengeluaran** , Anda dapat mengaitkan tugas **T1** di baris kuotasi sebagai tidak dikenakan biaya. Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran yang dicatat di tugas adalah tidak dikenakan biaya.

Tipe tagihan tugas dapat dikonfigurasi pada tab **Tugas yang Dikenakan Biaya** dari baris kuotasi berbasis proyek dengan memperbarui bidang **Tipe Penagihan** pada subkisi **tugas baris kuotasi**. Atau, Anda dapat memperbarui tipe penagihan untuk tugas proyek di bidang **Tipe Penagihan** pada subkisi di konfigurasi Penagihan tugas proyek yang memperlihatkan baris kuotasi yang terkait dengan tugas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Peran dapat dikenakan atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu.

Tipe tagihan peran dapat dikonfigurasi pada tab **Peran yang Dikenakan Biaya** dari baris kuotasi dengan memperbarui bidang **Tipe Penagihan** pada subkisi **peran yang dikenakan Biaya**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya

Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kuotasi tertentu.

Tipe tagihan transaksi dapat dikonfigurasi pada tab **Kategori yang Dikenakan Biaya** dari baris kuotasi dengan memperbarui bidang **Tipe Penagihan** pada subkisi **Kategori yang dikenakan Biaya**.

### <a name="resolve-chargeability"></a>Menangani pengenaan biaya
Perkiraan atau aktual yang dibuat untuk waktu hanya akan dianggap dikenakan biaya jika **Waktu** disertakan pada baris kuotasi, dan jika **Tugas** dan **Peran** dikonfigurasi sebagai dikenakan biaya pada baris kuotasi.

Perkiraan atau aktual yang dibuat untuk pengeluaran hanya akan dianggap dikenakan biaya jika **Pengeluaran** disertakan pada baris kuotasi, dan jika **Tugas** dan kategori **Kategori Transaksi** dikonfigurasi sebagai dikenakan biaya pada baris kuotasi.

| Mencakup Waktu | Mencakup Pengeluaran | Tugas Disertakan | Peran | Kategori | Tugas | Penagihan |
| --- | --- | --- | --- | --- | --- | --- |
| Ya | Ya | Keseluruhan proyek | Dikenakan biaya | Dikenakan biaya | Tidak dapat diatur | Penagihan pada aktual Waktu: Dikenakan Biaya </br>Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya |
| Ya | Ya | Hanya tugas yang dipilih | Dikenakan biaya | Dikenakan biaya | Dikenakan biaya | Penagihan pada aktual Waktu: Dikenakan Biaya</br>Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya |
| Ya | Ya | Hanya tugas yang dipilih | Tidak Dikenakan Biaya | Dikenakan biaya | Dikenakan biaya | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya</br>Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya |
| Ya | Ya | Hanya tugas yang dipilih | Dikenakan biaya | Dikenakan biaya | Tidak Dikenakan Biaya | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya</br> Jenis penagihan pada aktual Pengeluaran: Tidak Dikenakan biaya |
| Ya | Ya | Hanya tugas yang dipilih | Tidak Dikenakan Biaya | Dikenakan biaya | Tidak Dikenakan Biaya | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya</br> Jenis penagihan pada aktual Pengeluaran: Tidak Dikenakan biaya |
| Ya | Ya | Hanya tugas yang dipilih | Tidak Dikenakan Biaya | Tidak Dikenakan Biaya | Dikenakan biaya | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya</br> Jenis penagihan pada aktual Pengeluaran: Tidak Dikenakan biaya |
| No | Ya | Keseluruhan proyek | Tidak dapat diatur | Dikenakan biaya | Tidak dapat diatur | Penagihan pada aktual Waktu: Tidak tersedia </br>Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya |
| No | Ya | Keseluruhan proyek | Tidak dapat diatur | Tidak Dikenakan Biaya | Tidak dapat diatur | Penagihan pada aktual Waktu: Tidak tersedia </br>Jenis penagihan pada aktual Pengeluaran: Tidak Dikenakan biaya |
| Ya | No | Keseluruhan proyek | Dikenakan biaya | Tidak dapat diatur | Tidak dapat diatur | Penagihan pada aktual Waktu: Dikenakan Biaya</br>Jenis penagihan pada aktual Pengeluaran: Tidak tersedia |
| Ya | No | Keseluruhan proyek | Tidak Dikenakan Biaya | Tidak dapat diatur | Tidak dapat diatur | Penagihan pada aktual Waktu: Tidak Dikenakan Biaya </br>Jenis penagihan pada aktual Pengeluaran: Tidak tersedia |
