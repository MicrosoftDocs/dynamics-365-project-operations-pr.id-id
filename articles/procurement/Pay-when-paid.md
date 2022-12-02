---
title: Pembayaran vendor "bayar jika dibayar"
description: Topik menjelaskan cara menggunakan skenario bayar jika dibayar (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525385"
---
# <a name="pay-when-paid-vendor-payments"></a>Pembayaran vendor "bayar jika dibayar"

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik menjelaskan cara menggunakan skenario bayar jika dibayar (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Membuat pesanan pembelian yang memiliki persyaratan PWP

Bila Anda memposting faktur dari vendor, jika vendor tunduk pada persyaratan PWP, persyaratan tersebut akan ditampilkan baris pesanan pembelian (PO). Untuk membuat PO yang memiliki persyaratan PWP, ikuti langkah berikut.

1. Dalam Microsoft Dynamics 365 Finance, ikuti langkah-langkah berikut:

    - Buka **pengadaan dan pembekalan** \> **pesanan pembelian** \> **semua pesanan pembelian**. Pada panel tindakan, pilih **Baru**. Di kotak dialog **Buat pesanan pembelian**, pilih vendor dengan persyaratan PWP yang disiapkan pada proyek, masukkan informasi yang diperlukan lainnya, lalu pilih **OK**.
    - Buka **manajemen proyek dan akuntansi** \> **proyek** \> **Semua proyek**. Pada Panel Tindakan, di tab **Atur**, pilih **Tugas item**. Pilih pesanan pembelian. Pilih vendor dengan persyaratan PWP yang disiapkan pada proyek, lalu pilih **OK**.

2. Pada halaman **Pesanan pembelian**, pada Tab Cepat **Baris pesanan Pembelian**, pilih **Tambah baris** untuk membuat baris pesanan pembelian.
3. Pilih nomor item atau kategori pengadaan, lalu masukkan rincian lainnya yang diperlukan. Lihat rincian baris PO untuk vendor.

    Pilihan **bayar saat berbayar** dipilih secara otomatis, dan nilai di bidang **persentase ambang PWP** secara otomatis disalin dari bidang **persentase ambang PWP** di halaman **proyek**.

4. Jika Anda tidak ingin menerapkan persyaratan PWP ke vendor untuk baris PO, kosongkan pilihan **bayar saat berbayar**. Dalam kasus ini, bidang **Persentase ambang bates PWP** untuk baris PO akan diatur kembali ke **0** (nol).
5. Pada halaman **Pesanan pembelian**, pada Panel Tindakan, pada tab **Pembelian**, pilih **Konfirmasi** untuk mengonfirmasi pesanan pembelian.
6. Pada Panel Tindakan, pada tab **Faktur**, pilih **Faktur** untuk membuat faktur pesanan pembelian.

## <a name="create-a-project-invoice-proposal"></a>Buat proposal faktur proyek

Proposal faktur proyek digunakan untuk membuat faktur proyek kepada pelanggan. Dalam skenario PWP, pembayaran vendor tergantung pada pembayaran pelanggan berdasarkan pengaturan PWP. Namun, ada beberapa pilihan yang memungkinkan Anda melepas pembayaran tanpa pembayaran pelanggan sesuai kebutuhan. Untuk membuat faktur proyek untuk pelanggan, ikuti langkah-langkah berikut.

1. Dalam aplikasi customer engagement, buka **Proyek** \> **Proyek**, lalu pilih proyeknya.
2. Pada tab **Aktual**, pilih baris aktual yang dihasilkan oleh PO yang memiliki jenis transaksi **Penjualan belum terbillasi**. Selanjutnya pilih **Siap untuk faktur**.
3. Bukak **Penjualan** \> **Penjualan** \> **Kontrak proyek**, dan pilih kontrak proyek.
4. Pada Panel Tindakan, pilih **Faktur** untuk membuat faktur pelanggan.
5. Pada Finance, buka **Manajemen proyek dan akuntansi** \> **Periodik** \> **Impor dari tabel penahapan**, dan pilih **OK** untuk membuat jurnal integrasi Project Operations.
6. Buka **Manajemen proyek dan akuntansi** \> **Faktur proyek** \> **Proposal faktur proyek**, dan pilih **Posting** untuk memposting proposal faktur yang dibuat untuk proyek.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Memperbarui pembayaran pelanggan dan membayar vendor

Bila vendor menyelesaikan tugasnya dalam proyek dan mengirimkan faktur, Anda harus meninjau status proyek dan faktur pelanggan untuk menentukan apakah persyaratan PWP telah dipenuhi untuk proyek. Jika persyaratan PWP untuk vendor terpenuhi, Anda dapat menentukan baris pada faktur vendor untuk membayar, berdasarkan pembayaran pelanggan untuk proyek. Jika Anda memutuskan untuk membayar vendor meskipun persyaratan PWP tidak terpenuhi, Anda dapat menimpa persyaratan PWP pada halaman **faktur vendor dengan bayar saat dibayar**.

1. Di Finance, buka **Manajemen proyek dan akuntansi** \> **Proyek** \> **Semua proyek**, lalu pilih proyek.
2. Pada Panel Tindakan, pilih **Kontrol**, lalu pilih **Vendor faktur** untuk menampilkan semua faktur vendor yang telah dibuat untuk proyek.
3. Pada halaman **faktur vendor dengan bayar saat dibayar**, di bidang pencarian, masukkan nilai untuk menemukan faktur vendor yang ingin Anda tinjau, lalu pilih **Cari**.
4. Pilih pilihan **Bayar jika dibayar** untuk melihat hanya faktur PWP.
5. Pada Fast Tab **baris faktur vendor**, pilih baris yang ingin Anda rilis untuk pembayaran.
6. Pilih **Rilis pembayaran vendor**. Opsi **bayar saat dibayar** dikosongkan, dan nilai bidang **siap untuk pembayaran** diubah ke **ya**.
