---
title: Merekam penggunaan bahan pada proyek dan tugas proyek
description: Artikel ini memberikan informasi tentang cara mencatat penggunaan materi terhadap proyek dan tugas proyek.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eeb8303821bc4c246e37333ddbcb77ca798d2e8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920064"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Merekam penggunaan bahan pada proyek dan tugas proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Seiring tim proyek yang bekerja melalui tugas pada proyek, mereka menggunakan atau menggunakan bahan. Log penggunaan bahan memberikan cara untuk merekam penggunaan ini sehingga dapat disetujui oleh manajer proyek dan akhirnya ditagih kepada pelanggan. 

Untuk merekam penggunaan bahan katalog atau pilihan dan mengirimkannya kepada pemberi izin, ikuti langkah-langkah berikut: 

1. Di panel navigasi, pilih **Penggunaan bahan**, lalu pilih **Baru**.
2. Pada halaman **Penggunaan bahan Baru**, masukkan informasi penggunaan materi yang diperlukan, lalu pilih **Simpan**.

Tabel berikut memberikan informasi tentang bidang pada halaman **log penggunaan bahan**. 

| **Bidang** | **Deskripsi** | **Dampak hilir** |
| --- | --- | --- |
| KETERANGAN | Deskripsi tentang penggunaan bahan khusus. | Tidak ada dampak hilir untuk bidang ini. |
| Tanggal | Tanggal untuk digunakannya bahan. | Tidak ada dampak hilir untuk bidang ini. |
| Project | Daftar proyek yang aktif. | Memilih proyek untuk log penggunaan bahan akan mempengaruhi bidang **Tugas** untuk menunjukkan hanya tugas yang ada pada proyek. |
| Tugas | Daftar tugas untuk proyek termasuk tugas node leaf dan ringkasan. | Memilih tugas untuk log penggunaan bahan mempengaruhi biaya bahan aktual dan penjualan bahan aktual untuk tugas. Jika bidang ini kosong, penjualan dan biaya penggunaan bahan terkait dilacak dan diringkas hanya pada tingkat proyek. |
| Pilih Produk | Tentukan apakah penggunaan bahan adalah untuk produk **yang Ada** (katalog) atau produk **pilihan**. | Bidang ini menentukan jenis produk. |
| Produk | ID produk dari katalog produk. Bila Anda memilih ID produk, bidang **Pilih Produk** akan secara otomatis diperbarui ke **produk yang ada**. ID tersebut digunakan untuk mengambil harga biaya dan penjualan dari daftar harga. | Tidak ada dampak hilir untuk bidang ini. |
| Deskripsi Produk Pilihan | Bidang teks untuk menulis nama produk. Bidang ini tersedia bila Anda memilih produk **Pilihan** dalam bidang **pilih Produk**.| Tidak ada dampak hilir untuk bidang ini. |
| Sumber Daya yang Dapat Dipesan| Sumber daya yang menggunakan bahan ini pada proyek. Default untuk bidang ini adalah sumber daya yang dapat dipesan dari pengguna yang masuk, tetapi dapat diubah untuk mencatat penggunaan atas nama anggota lain dalam tim proyek. | Tidak ada dampak hilir untuk bidang ini. |
| Grup Unit | Nilai default pada bidang ini berasal dari grup unit yang disiapkan sebagai default pada produk katalog. Anda dapat memperbarui bidang ini untuk memilih grup unit lain. | Tidak ada dampak hilir untuk bidang ini. |
| Unit | Nilai default di bidang ini adalah unit default dari produk yang dipilih. Anda dapat memperbarui bidang ini untuk memilih unit lain. | Mengubah unit menghasilkan biaya dan harga per unit default yang berbeda. |
| Quantity | Kuantitas produk yang telah digunakan pada proyek atau tugas proyek. | Tidak ada dampak hilir untuk bidang ini. |
| Biaya Unit | Biaya per unit dari kombinasi produk dan unit yang dipilih sebagaimana diatur dalam daftar harga biaya yang berlaku. | Biaya unit selalu ditampilkan dalam mata uang biaya proyek. Jika tidak ada biaya per unit untuk kombinasi produk dan unit dalam daftar harga, maka biaya unit akan diatur default ke 0,00. |
| Biaya Total | Jumlah biaya yang dihitung sebagai kuantitas \* biaya per unit.| Jumlah Biaya selalu ditampilkan dalam mata uang biaya proyek. |


## <a name="submit-material-usage-for-review-and-approval"></a>Ajukan penggunaan bahan untuk ditinjau dan disetujui 
Setelah mengambil semua penggunaan bahan dan Anda siap menyetujuinya, Anda harus mengirimkan informasi penggunaan untuk ditinjau.

1. Buka **Log Penggunaan Bahan**, lalu pilih satu atau beberapa entri. Atau, pilih semua rekaman penggunaan bahan menggunakan kotak centang pada header.
2. Pilih **kirim**. Sistem akan memproses entri yang dipilih, lalu membuat permintaan persetujuan penggunaan bahan.

## <a name="recall-a-material-usage-log"></a>Tarik Kembali log Penggunaan bahan

Bila perlu, Anda dapat menarik penggunaan bahan yang diajukan. Waktu yang diperlukan untuk menarik entri penggunaan bahan tergantung pada tahapan persetujuan.  Jika pemberi izin belum menyetujui entri, penarikan dapat terjadi segera. Namun, jika entri telah disetujui, pemberi izin diminta untuk menyetujui penarikan dan membalikkan transaksi.

1. Buka **Penggunaan bahan**, dan dalam daftar log penggunaan bahan, pilih penggunaan bahan untuk mengingatnya.
2. Pilih **Tarik**. Jika entri penggunaan bahan belum disetujui, sistem akan segera menariknya. Jika entri bahan telah disetujui, permintaan penarikan dibuat untuk memberitahukan pemberi izin bahwa Anda ingin menarik penggunaan bahan. Pemberi persetujuan kemudian akan mengkonfirmasi bahwa pembalikan dapat dilakukan, dan entri akan dikembalikan.

## <a name="delete-a-material-usage-log"></a>Hapus log Penggunaan bahan

Anda dapat menghapus log penggunaan bahan yang belum diajukan. Untuk menghapus log penggunaan bahan yang telah diajukan, Anda harus menariknya terlebih dulu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
