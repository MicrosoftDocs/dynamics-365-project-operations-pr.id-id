---
title: Mengonfigurasikan komponen yang dikenakan biaya pada baris kuotasi - lite
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi komponen dikenakan biaya dan yang tidak dikenakan biaya pada baris kuotasi berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177110"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Mengonfigurasikan komponen yang dikenakan biaya pada baris kuotasi - lite

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

Jika baris kuotasi berbasis proyek mencakup **waktu** dan tugas **T1**, tugas dikaitkan ke baris kuotasi sebagai dikenakan biaya. Jika ada baris kuotasi kedua yang mencakup **Pengeluaran**, Anda dapat mengaitkan tugas **T1** di baris kuotasi sebagai tidak dikenakan biaya. Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran yang dicatat di tugas adalah tidak dikenakan biaya.

Jenis penagihan tugas dapat dikonfigurasi pada tab **tugas kena biaya** pada baris kuotasi berbasis proyek dengan memperbarui bidang **jenis penagihan** pada subkisi **tugas tugas baris kuotasi**. Atau, Anda dapat memperbarui jenis penagihan untuk tugas proyek di bidang **jenis penagihan** pada subkisi dari konfigurasi penagihan tugas proyek yang menunjukkan baris kuotasi yang terkait dengan tugas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Peran dapat dikenakan atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu.

Jenis penagihan peran dapat dikonfigurasi pada tab **Peran kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **peran kena biaya**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya

Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kuotasi tertentu.

Jenis penagihan transaksi dapat dikonfigurasi pada tab **Kategori kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]