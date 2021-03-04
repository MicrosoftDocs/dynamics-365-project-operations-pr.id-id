---
title: Pemulihan PPN
description: Topik ini menjelaskan cara mendapatkan pengembalian dana pada transaksi pajak pertambahan nilai (ppn).
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49397592ea002b9da872ac1aa455719b6ca2292e
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960206"
---
# <a name="vat-recovery"></a>Pemulihan PPN 

Untuk menerima pengembalian dana pada transaksi pajak pertambahan nilai (PPN) yang memenuhi syarat, perusahaan atau organisasi harus mengidentifikasi, mengumpulkan, memverifikasi, dan mengirimkan informasi yang akurat. Proses ini mencakup beberapa tugas dan, tergantung pada ukuran perusahaan Anda, dapat mencakup beberapa karyawan atau peran.

Untuk memulihkan PPN dengan manajemen pengeluaran, prasyarat berikut harus diselesaikan:

- Kode pajak harus dibuat untuk negara/wilayah yang dialokasikan untuk kategori pengeluaran.
- Grup pajak penjualan harus dibuat untuk setiap kode pajak.
- Kode pajak penjualan item harus dibuat untuk setiap grup pajak penjualan.

Setelah prasyarat selesai, karyawan mengikuti langkah-langkah berikut untuk meminta pengembalian dana untuk transaksi PPN.

1. Pada laporan pengeluaran, masukkan informasi pajak tentang transaksi kartu kredit untuk mengidentifikasi pengembalian dana PPN yang memenuhi syarat.
2. Pastikan bahwa semua informasi pajak lengkap, dan kemudian posting laporan pengeluaran.
3. Biaya proses yang memenuhi syarat untuk pemulihan PPN internasional.
4. Kirim data pemulihan PPN ke vendor pihak ketiga untuk mengajukan pengembalian pemulihan internasional.
5. Proses pengeluaran untuk pemulihan PPN dalam negeri.

Bagian berikut ini memberikan contoh yang menunjukkan cara Aswono menyelesaikan setiap langkah.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Pada laporan pengeluaran, masukkan informasi pajak tentang transaksi kartu kredit untuk mengidentifikasi pengembalian dana PPN yang memenuhi syarat

Bunga, perwakilan penjualan Aswono yang berbasis di Amerika Serikat, baru-baru ini kembali dari perjalanan penjualan ke Inggris. Selama perjalanan, dia mengeluarkan biaya kartu kredit pribadi untuk makanan. Bunga sekarang harus membuat laporan pengeluaran untuk merekonsiliasi pengeluarannya.

Saat Bunga memasukkan informasi tentang laporan pengeluaran, ia memilih **Inggris Raya** di bidang **negara/kawasan** di halaman **edit laporan pengeluaran**. Daftar grup pajak penjualan kemudian difilter sehingga hanya menampilkan grup yang berlaku untuk Inggris. Bunga memilih grup pajak penjualan **Inggris 001** dan kemudian memilih grup pajak penjualan item **makan**. Selanjutnya dia menambahkan transaksi baru untuk penginapan. Karena hanya ada satu grup pajak penjualan dan grup pajak penjualan item untuk menginap di Inggris Raya, informasi ini akan secara otomatis diisi pada laporan biaya Bunga.

Sesuai kebijakan Aswono, semua pengeluaran harus memiliki tanda terima yang sesuai. Oleh karena itu, ketika Bunga menyimpan laporan pengeluaran, dia menerima pesan yang menyatakan bahwa dia harus melampirkan tanda terima untuk setiap transaksi yang dia Daftarkan pada laporan pengeluarannya. Bunga memverifikasi bahwa dia telah melampirkan gambar digital dari setiap penerimaan transaksi ke laporan pengeluarannya dan kemudian mengajukan laporannya untuk disetujui. Dia kemudian mengirimkan tanda terima kertas ke tim pemrosesan Back-Office. Tim ini akan mengirimkan data pemulihan PPN ke vendor pihak ketiga yang mengembalikan file pemulihan PPN internasional untuk Aswono.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Pastikan bahwa semua informasi pajak lengkap, dan kemudian posting laporan pengeluaran

April, Koordinator utang dagang untuk Aswono, harus memasukkan informasi pajak apa pun yang tidak ada dari laporan pengeluaran sebelum laporan bisa diposting. Dia membuka halaman **rincian laporan pengeluaran** dan melihat laporan pengeluaran Bunga yang disetujui. April kemudian membuka laporan biaya untuk melihat rincian transaksi. Dia melihat bahwa Nancy tidak memasukkan grup pajak penjualan item untuk salah satu transaksi. Karena informasi ini tidak tersedia, April tidak dapat memposting laporan pengeluaran. Oleh karena itu, April melihat pada halaman **konfigurasi pajak** dalam manajemen pengeluaran, dan menemukan grup pajak penjualan item yang sesuai untuk negara/kawasan dan jenis transaksi. April sekarang dapat memposting laporan pengeluaran ke buku besar.

Ketika April memposting laporan pengeluaran, item kerja dipulihkan PPN dibuat. Item pekerjaan ini ditetapkan ke anggota tim pemrosesan Back-Office. April menerima pesan yang menegaskan bahwa posting berhasil. Pesan ini juga mencantumkan jumlah transaksi PPN yang diidentifikasi untuk pemulihan.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Biaya proses yang memenuhi syarat untuk pemulihan PPN internasional

Arnie, anggota tim pemrosesan Back-Office Aswono, bertanggung jawab untuk mengonfirmasikan bahwa semua informasi yang diperlukan untuk pemulihan PPN tercakup dalam laporan pengeluaran. Dia membuka halaman **pemulihan pajak pengeluaran** dan memilih laporan pengeluaran yang disampaikan Bunga. Arnie memverifikasi bahwa semua tanda terima yang diperlukan dilampirkan, dan grup pajak penjualan benar dan kode pajak penjualan item dimasukkan.

Ketika Arnie menerima tanda terima kertas dari Bunga, ia tanda terima kertas terhadap tanda terima digital dan kemudian mengubah status laporan pengeluaran ke **siap untuk pemulihan**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Kirim data pemulihan PPN ke vendor pihak ketiga untuk mengajukan pengembalian pemulihan internasional

Ketika Arnie siap mengirim data laporan pengeluaran ke vendor pihak ketiga yang akan mengajukan pengembalian pemulihan PPN, ia membuka halaman **pemulihan pajak pengeluaran**. Dia memfilter halaman sehingga hanya menampilkan laporan pengeluaran yang ditandai sebagai **siap untuk pemulihan**. Arnie kemudian memilih **File** &gt; **ekspor ke Excel**. Informasi PPN dari laporan pengeluaran diekspor ke lembar kerja Microsoft Excel. Arnie mengirimkan lembar kerja ini ke vendor pihak ketiga dan menyertakan pesan yang menyatakan bahwa tanda terima kertas telah dikirim melalui kurir.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Proses pengeluaran untuk pemulihan PPN dalam negeri

Arnie harus memverifikasi bahwa transaksi laporan pengeluaran memenuhi syarat untuk pemulihan PPN, dan bahwa kuitansi digital dilampirkan ke laporan. Untuk mulai memproses pengeluaran yang memenuhi syarat untuk pemulihan dalam negeri, Arnie membuka halaman **pemulihan pajak pengeluaran** dan memilih laporan pengeluaran yang memerlukan verifikasi. Dia memverifikasi bahwa tanda terima adalah atas nama perusahaan, bukan karyawan. Untuk pemulihan PPN, penerimaan harus atas nama perusahaan. Arnie kemudian mengkonfirmasi bahwa grup pajak penjualan yang benar dan kode pajak penjualan barang diterapkan.

Ketika Arnie menerima tanda terima kertas, ia akan mengubah status laporan pengeluaran ke **siap untuk pemulihan**. Dia kemudian dapat mengajukan pengembalian dengan otoritas pajak yang sesuai. Dalam kasus ini, otoritas pajak yang sesuai di Amerika Serikat adalah Internal Revenue Service (IRS).
