---
title: Uang muka
description: Topik ini menyediakan informasi tentang kasbon.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078367"
---
# <a name="cash-advance"></a>Uang muka

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

kasbon memungkinkan karyawan untuk meminjam uang dari perusahaan mereka sebelum menimbulkan pengeluaran. Bila kasbon yang diminta disetujui dan dibayar, karyawan dapat menggunakan uang untuk pengeluaran bisnis yang mungkin akan segera timbul. 

## <a name="create-and-submit-a-cash-advance-request"></a>Membuat dan mengirimkan permintaan kasbon

1. Dalam **pengeluaran saya** , pilih **kasbon** > **baru** untuk membuat kasbon baru. 
2. Pada halaman **permintaan kasbon baru** , masukkan tujuan pengeluaran dan pilih lokasi dengan pengeluaran yang akan dikeluarkan.
3. Masukkan jumlah dan mata uang yang diminta, lalu pilih **Simpan**. 
4. Setelah Anda siap mengirimkan permintaan kasbon, pada halaman **permintaan kasbon** , pilih **alur kerja** > **Ajukan**.

## <a name="modify-a-cash-advance-request"></a>Memodifikasi permintaan kasbon

Anda dapat memodifikasi permintaan kasbon jika belum diajukan untuk disetujui.

1. Di dalam **pengeluaran saya: kasbon** mencari dan memilih kasbon yang ingin Anda edit.
2. Pilih **Edit** , dan buat perubahan yang diperlukan untuk permintaan kasbon. 
3. Pilih **Simpan dan Tutup**.


## <a name="view-cash-advance-requests"></a>Lihat Permintaan kasbon
Anda dapat meninjau daftar semua uang tunai yang ada dalam draf, diajukan, dalam peninjauan, atau dibayar berdasarkan **pengeluaran saya: kasbon**. 

## <a name="approve-cash-advance-requests"></a>Setujui Permintaan kasbon

Manajer atau pengguna yang dikonfigurasi sebagai pemberi persetujuan dalam alur kerja akan dapat menyetujui kasbon yang dikirim kepada mereka untuk ditinjau. 

1. Untuk menyetujui kasbon, dalam **proses kasbon** , pilih **kasbon untuk saya tinjau**.
2. Pilih kasbon yang perlu Anda tinjau dan pilih **setujui**.  

## <a name="pay-cash-advances"></a>Bayar kasbon 
Prosedur berikut biasanya diselesaikan oleh akuntan atau pengguna dengan izin akuntansi.

1. Untuk memposting uang tunai yang disetujui, pilih **uang tunai yang disetujui** , lalu pilih **bayar dan transfer**.  
2. Berikan rincian jurnal untuk kasbon, lalu pilih **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Ajukan laporan pengeluaran terhadap kasbon yang telah dibayar 

Bila Anda membuat dan mengirimkan laporan pengeluaran untuk kasbon yang telah Anda terima, pengeluaran akan disesuaikan secara otomatis dengan sebelumnya. Jika kasbon lebih besar dari jumlah yang dikeluarkan, Anda harus mengembalikan saldo ke perusahaan menggunakan kategori pengeluaran **uang tunai dikembalikan**. Jika kasbon perusahaan yang dibayar kurang dari jumlah yang Anda belanjakan, perusahaan harus mengganti saldo Anda. 

### <a name="example"></a>Contoh
Anda berencana untuk melakukan perjalanan konferensi dari Seattle ke New York City. Anda membuat permintaan kasbon 3000,00 USD karena Anda telah memperkirakan biaya tiket konferensi, penerbangan, Hotel, makan, dan taksi untuk menjadi sekitar jumlah ini. Anda tidak akan dibayar kecuali manajer menyetujui permintaan ini. Setelah manajer menyetujui, kasbon yang diminta akan dibayarkan sebagai 3000,00 USD ke rekening bank Anda. Anda kemudian menghadiri konferensi. Setelah menyelesaikan perjalanan, Anda mendapati bahwa Total pengeluaran hanya 2790,00 USD. Pilih **Kas** di bidang **metode pembayaran** , dan ajukan pengeluaran 2790,00 USD. Jumlah pengeluaran yang dikirim akan disesuaikan secara otomatis dengan 3000,00 USD kasbon yang dipinjamkan kepada Anda. Anda sekarang berutang saldo 210,00 USD (3000,00-2790,00) ke perusahaan, yang dapat Anda kembali ke perusahaan menggunakan kategori pengeluaran **pengembalian uang tunai**. 
