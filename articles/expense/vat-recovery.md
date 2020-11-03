---
title: Pemulihan PPN di manajemen pengeluaran
description: Topik ini menjelaskan cara menerima pengembalian dana pada transaksi pajak pertambahan nilai (ppn) yang memenuhi syarat.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078352"
---
# <a name="vat-recovery-in-expense-management"></a>Pemulihan PPN di manajemen pengeluaran

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menerima pengembalian dana pada transaksi pajak pertambahan nilai (PPN) yang memenuhi syarat, perusahaan atau organisasi harus mengidentifikasi, mengumpulkan, memverifikasi, dan mengirimkan informasi yang akurat. Proses ini mencakup beberapa tugas dan, tergantung pada ukuran perusahaan Anda, dapat mencakup beberapa karyawan atau peran.

Untuk memulihkan PPN di modul **manajemen pengeluaran** , prasyarat berikut harus diselesaikan:

- Kode pajak harus dibuat untuk negara/wilayah yang dialokasikan untuk kategori pengeluaran.
- Grup pajak penjualan harus dibuat untuk setiap kode pajak.
- Kode pajak penjualan item harus dibuat untuk setiap grup pajak penjualan.

Setelah prasyarat selesai, langkah-langkah berikut harus diselesaikan untuk meminta pengembalian dana untuk transaksi PPN.

1. Pada laporan pengeluaran, masukkan informasi pajak tentang transaksi kartu kredit untuk mengidentifikasi pengembalian dana PPN yang memenuhi syarat.
2. Verifikasi bahwa semua informasi pajak lengkap, dan kemudian posting laporan pengeluaran.
3. Biaya proses yang memenuhi syarat untuk pemulihan PPN internasional.
4. Kirim data pemulihan PPN ke vendor pihak ketiga untuk mengajukan pengembalian pemulihan internasional.
5. Proses pengeluaran untuk pemulihan PPN dalam negeri.

Bagian berikut ini memberikan contoh yang menunjukkan cara Aswono menyelesaikan setiap langkah.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Masukkan informasi pajak tentang transaksi kartu kredit untuk mengidentifikasi pengembalian dana PPN yang memenuhi syarat

Bunga, perwakilan penjualan Aswono yang berbasis di Amerika Serikat, baru-baru ini kembali dari perjalanan penjualan ke Inggris. Selama perjalanan, Bunga mengeluarkan biaya kartu kredit pribadi untuk makanan. Bunga sekarang harus membuat laporan pengeluaran untuk merekonsiliasi pengeluaran.

Saat Bunga memasukkan informasi tentang laporan pengeluaran, ia memilih **Inggris Raya** di bidang **negara/kawasan** di halaman **edit laporan pengeluaran**. Daftar grup pajak penjualan kemudian difilter sehingga hanya menampilkan grup yang berlaku untuk Inggris. Bunga memilih grup pajak penjualan **Inggris 001** dan kemudian memilih grup pajak penjualan item **makan**. Selanjutnya, Bunga menambahkan transaksi baru untuk penginapan. Karena hanya ada satu grup pajak penjualan dan satu grup pajak penjualan item untuk menginap di Inggris Raya, informasi ini akan secara otomatis diisi pada laporan biaya Bunga.

Sesuai kebijakan Aswono, semua pengeluaran harus memiliki tanda terima yang sesuai. Oleh karena itu, ketika Bunga menyimpan laporan pengeluaran, dia menerima pesan yang menyatakan bahwa dia harus melampirkan tanda terima untuk setiap transaksi yang dia Daftarkan pada laporan pengeluarannya. Bunga memverifikasi bahwa dia telah melampirkan gambar digital dari setiap penerimaan transaksi ke laporan pengeluarannya dan kemudian mengajukan laporannya untuk disetujui. Dia kemudian mengirimkan tanda terima kertas ke tim pemrosesan Back-Office. Tim ini akan mengirimkan data pemulihan PPN ke vendor pihak ketiga yang mengembalikan file pemulihan PPN internasional untuk Aswono.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Verifikasi informasi pajak dan posting laporan pengeluaran

Sebelum April, Koordinator utang dagang untuk Aswono, dapat memposting laporan pengeluaran, ia harus memasukkan informasi pajak apa pun yang tidak ada. Dia membuka halaman **rincian laporan pengeluaran** dan melihat laporan pengeluaran Bunga yang disetujui. April kemudian membuka laporan biaya untuk melihat rincian transaksi. Dia melihat bahwa Nancy tidak memasukkan grup pajak penjualan item untuk salah satu transaksi. Karena informasi ini tidak tersedia, April tidak dapat memposting laporan pengeluaran. Oleh karena itu, ia melihat pada halaman **konfigurasi pajak** dalam manajemen pengeluaran, dan menemukan grup pajak penjualan item yang sesuai untuk negara/kawasan dan jenis transaksi. April sekarang dapat memposting laporan pengeluaran ke buku besar.

Ketika April memposting laporan pengeluaran, item kerja dipulihkan PPN dibuat. Item pekerjaan ini ditetapkan ke anggota tim pemrosesan Back-Office. April menerima pesan yang menegaskan bahwa posting berhasil. Pesan ini juga mencantumkan jumlah transaksi PPN yang diidentifikasi untuk pemulihan.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Biaya proses yang memenuhi syarat untuk pemulihan PPN internasional

Arnie, anggota tim pemrosesan Back-Office Aswono, bertanggung jawab untuk memverifikasi bahwa semua informasi yang diperlukan untuk pemulihan PPN tercakup dalam laporan pengeluaran. Dia membuka halaman **pemulihan pajak pengeluaran** dan memilih laporan pengeluaran yang disampaikan Bunga. Arnie kemudian memverifikasi bahwa semua tanda terima yang diperlukan dilampirkan, dan grup pajak penjualan benar dan kode pajak penjualan item dimasukkan.

Ketika Arnie menerima tanda terima kertas dari Bunga, ia memverifikasi mereka terhadap tanda terima digital dan kemudian mengubah status laporan pengeluaran ke **siap untuk pemulihan**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Mengirim data pemulihan PPN ke vendor pihak ketiga

Ketika Arnie siap mengirim data laporan pengeluaran ke vendor pihak ketiga yang akan mengajukan pengembalian pemulihan PPN, ia membuka halaman **pemulihan pajak pengeluaran**. Dia memfilter halaman sehingga hanya menampilkan laporan pengeluaran yang ditandai sebagai **siap untuk pemulihan**. Arnie kemudian memilih **File** &gt; **ekspor ke Excel**. Informasi PPN dari laporan pengeluaran diekspor ke lembar kerja Microsoft Excel. Arnie mengirimkan lembar kerja ini ke vendor pihak ketiga dan menyertakan pesan yang menyatakan bahwa tanda terima kertas telah dikirim melalui kurir.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Proses pengeluaran untuk pemulihan PPN dalam negeri

Arnie harus memverifikasi bahwa transaksi laporan pengeluaran memenuhi syarat untuk pemulihan PPN, dan bahwa kuitansi digital dilampirkan ke laporan. Untuk mulai memproses pengeluaran yang memenuhi syarat untuk pemulihan dalam negeri, Arnie membuka halaman **pemulihan pajak pengeluaran** dan memilih laporan pengeluaran yang memerlukan verifikasi. Dia memverifikasi bahwa tanda terima adalah atas nama perusahaan, bukan karyawan. (Untuk pemulihan PPN, tanda terima harus nama perusahaan.) Arnie kemudian memverifikasi bahwa grup pajak penjualan benar dan kode pajak penjualan item dimasukkan.

Ketika Arnie menerima tanda terima kertas, ia akan mengubah status laporan pengeluaran ke **siap untuk pemulihan**. Dia kemudian dapat mengajukan pengembalian dengan otoritas pajak yang sesuai. Dalam kasus ini, otoritas pajak yang sesuai di Amerika Serikat adalah Internal Revenue Service (IRS).
