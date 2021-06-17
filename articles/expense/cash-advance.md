---
title: Uang muka
description: Topik ini menyediakan informasi tentang kasbon.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c610fdda8f337e0c16fe5010770aca678201c328
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002150"
---
# <a name="cash-advance"></a>Uang muka

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

kasbon memungkinkan karyawan untuk meminjam uang dari perusahaan mereka sebelum menimbulkan pengeluaran. Bila kasbon yang diminta disetujui dan dibayar, karyawan dapat menggunakan uang untuk pengeluaran bisnis yang mungkin akan segera timbul. 

## <a name="create-and-submit-a-cash-advance-request"></a>Membuat dan mengirimkan permintaan kasbon
Untuk membuat kasbon baru dan mengajukan permintaan uang tunai, lakukan langkah berikut: 

1. Dalam **Pengeluaran Saya**, pilih **kasbon** > **Baru**. 
2. Pada halaman **permintaan kasbon baru**, masukkan tujuan pengeluaran dan pilih lokasi dengan pengeluaran yang akan dikeluarkan.
3. Masukkan jumlah dan mata uang yang diminta, lalu pilih **Simpan**. 
4. Setelah Anda siap mengirimkan permintaan kasbon, pada halaman **permintaan kasbon**, pilih **alur kerja** > **Ajukan**.

## <a name="modify-a-cash-advance-request"></a>Memodifikasi permintaan kasbon

Anda dapat memodifikasi permintaan kasbon jika belum diajukan untuk disetujui.

1. Dalam **Pengeluaran Saya: kasbon** cari dan pilih kasbon yang akan diedit.
2. Pilih **Edit**, dan buat perubahan yang diperlukan untuk permintaan kasbon. 
3. Pilih **Simpan dan Tutup**.


## <a name="view-cash-advance-requests"></a>Lihat Permintaan kasbon
Anda dapat meninjau daftar semua uang tunai yang ada dalam draf, diajukan, dalam peninjauan, atau dibayar berdasarkan **pengeluaran saya: kasbon**. 

## <a name="approve-cash-advance-requests"></a>Setujui Permintaan kasbon

Manajer atau pengguna yang dikonfigurasi sebagai pemberi persetujuan dalam alur kerja akan dapat menyetujui kasbon yang dikirim kepada mereka untuk ditinjau. 

1. Untuk menyetujui kasbon, dalam **proses kasbon**, pilih **kasbon untuk saya tinjau**.
2. Pilih kasbon yang perlu Anda tinjau dan pilih **setujui**.  

## <a name="pay-cash-advances"></a>Bayar kasbon 
Prosedur berikut biasanya diselesaikan oleh akuntan atau pengguna dengan izin akuntansi.

1. Untuk memposting uang tunai yang disetujui, pilih **uang tunai yang disetujui**, lalu pilih **bayar dan transfer**.  
2. Berikan rincian jurnal untuk kasbon, lalu pilih **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Ajukan laporan pengeluaran terhadap kasbon yang telah dibayar 

Saat Anda membuat dan mengirimkan laporan pengeluaran untuk kasbon yang telah Anda terima, pengeluaran akan secara otomatis disesuaikan dengan kasbon tersebut. Jika kasbon lebih besar dari jumlah yang dikeluarkan, Anda harus mengembalikan saldo ke perusahaan menggunakan kategori pengeluaran **uang tunai dikembalikan**. Jika kasbon yang dibayar perusahaan kurang dari jumlah yang Anda keluarkan, perusahaan harus mengganti selisihnya. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Pilih uang muka tunai yang berlaku untuk pengeluaran Anda
Sebelum mengajukan laporan pengeluaran, Anda dapat memilih uang muka yang sesuai dengan transaksi pengeluaran pada laporan. Untuk menggunakan fungsi ini, dua fitur berikut harus diaktifkan dari ruang kerja **manajemen Fitur**:

  - Laporan pengeluaran model baru
  - Kemampuan untuk memetakan uang muka tunai ke baris pengeluaran
 
 Bila fitur ini diaktifkan:
 
  - Anda dapat menambahkan satu atau lebih uang muka untuk setiap baris pengeluaran.
  - Saldo uang muka yang tersedia dapat dilihat secara real time saat laporan pengeluaran disimpan. Langkah ini memungkinkan Anda memproses transaksi pengeluaran dan menghasilkan transaksi tunai pada waktu yang sama.
  - Anda dapat memilih beberapa uang muka untuk satu transaksi pengeluaran.
  - Data rekonsiliasi tunai muka tersedia menggunakan kueri. 
 
Jika Anda tidak menggunakan fitur ini, fungsi akan tetap sama, dengan uang muka yang ada akan dikurangi secara otomatis setelah pengeluaran diajukan.

### <a name="example"></a>Contoh 
Anda berencana melakukan perjalanan dari Seattle ke New York City untuk konferensi. Anda membuat permintaan kasbon untuk 3000,00 USD berdasarkan perkiraan biaya tiket konferensi, penerbangan, hotel, makan siang, dan taksi. Anda tidak akan dibayar, kecuali manajer Anda menyetujui permintaan ini. Setelah manajer menyetujui, kasbon yang diminta akan dibayarkan sebagai 3000,00 USD ke rekening bank Anda. Anda kemudian menghadiri konferensi. Setelah menyelesaikan perjalanan, Anda mendapati bahwa Total pengeluaran hanya 2790,00 USD. Pilih **Kas** pada bidang **metode Pembayaran**, lalu kirim pengeluaran untuk 2790,00 USD. Jumlah pengeluaran yang dikirim akan disesuaikan secara otomatis dengan 3000,00 USD kasbon yang dipinjamkan kepada Anda. Anda sekarang berutang selisih 210,00 USD (3000,00 - 2790,00), yang dapat Anda kembalikan ke perusahaan menggunakan kategori Pengeluaran **Kas kembali**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
