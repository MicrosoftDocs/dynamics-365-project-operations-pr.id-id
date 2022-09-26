---
title: Membayar saat pembayaran vendor berbayar
description: Ini topik menjelaskan cara menggunakan skenario bayar saat dibayar (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Membayar saat pembayaran vendor berbayar

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Ini topik menjelaskan cara menggunakan skenario bayar saat dibayar (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Membuat pesanan pembelian yang memiliki persyaratan PWP

Saat Anda memposting faktur dari vendor, jika vendor tunduk pada persyaratan PWP, persyaratan tersebut ditampilkan pada baris pesanan pembelian (PO). Untuk membuat PO yang memiliki persyaratan PWP, ikuti langkah berikut.

1. Di Microsoft Dynamics 365 Finance, ikuti salah satu langkah berikut:

    - Buka **pengadaan dan pembekalan** \> **pesanan pembelian** \> **semua pesanan pembelian**. Pada panel tindakan, pilih **Baru**. Dalam kotak **dialog Buat pesanan** pembelian, pilih vendor tempat persyaratan PWP disiapkan pada proyek, masukkan informasi lain yang diperlukan, lalu pilih **OK**.
    - Buka **manajemen proyek dan akuntansi** \> **proyek** \> **Semua proyek**. Pada Panel Tindakan, pada tab **Kelola**, pilih **tugas Item**. Pilih pesanan pembelian. Pilih vendor tempat persyaratan PWP disiapkan pada proyek, lalu pilih **OK**.

2. Pada halaman **Pesanan pembelian**, pada **tab Cepat baris** Pesanan pembelian, pilih **Tambahkan baris** untuk membuat baris pesanan pembelian.
3. Pilih nomor item atau kategori pengadaan, dan masukkan detail lain yang diperlukan. Tinjau detail jalur PO untuk vendor.

    Pilihan **bayar saat berbayar** dipilih secara otomatis, dan nilai di bidang **persentase ambang PWP** secara otomatis disalin dari bidang **persentase ambang PWP** di halaman **proyek**.

4. Jika Anda tidak ingin menerapkan persyaratan PWP ke vendor untuk baris PO, kosongkan pilihan **bayar saat berbayar**. Dalam hal ini, **bidang persentase** ambang batas PWP untuk garis PO akan diatur ulang **menjadi 0** (nol).
5. **Pada halaman Pesanan pembelian**, pada Panel Tindakan, pada tab **Pembelian**, pilih **Konfirmasi** untuk mengonfirmasi pesanan pembelian.
6. Pada Panel Tindakan, pada tab **Faktur**, pilih **Faktur** untuk membuat faktur untuk pesanan pembelian.

## <a name="create-a-project-invoice-proposal"></a>Membuat proposal faktur proyek

Proposal faktur proyek digunakan untuk membuat faktur proyek untuk pelanggan. Dalam skenario PWP, pembayaran vendor bergantung pada pembayaran pelanggan sesuai dengan pengaturan PWP. Namun, ada opsi yang memungkinkan Anda melepaskan pembayaran tanpa pembayaran pelanggan sesuai kebutuhan Anda. Untuk membuat faktur proyek bagi pelanggan, ikuti langkah-langkah berikut.

1. Di aplikasi keterlibatan pelanggan, buka **Proyek Proyek** \> **·**, dan pilih proyek.
2. Pada tab **Aktual**, pilih baris aktual yang dihasilkan oleh PO yang memiliki **jenis transaksi penjualan** Tidak Ditagih. Kemudian pilih **Siap untuk faktur**.
3. Buka **kontrak** Proyek Penjualan \>**Penjualan** \>**·**, dan pilih kontrak proyek.
4. Pada Panel Tindakan, pilih **Faktur** untuk membuat faktur pelanggan.
5. Di Keuangan, buka **Manajemen proyek dan akuntansi** \> **Impor Berkala** \> **dari tabel** pementasan, dan pilih **OK** untuk menghasilkan jurnal integrasi operasi Proyek.
6. Buka **Manajemen proyek dan akuntansi** \> **Faktur** \> **proyek Proposal faktur proyek**, dan pilih **Posting** untuk memposting proposal faktur yang dihasilkan untuk proyek.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Memperbarui pembayaran pelanggan dan membayar vendor

Ketika vendor menyelesaikan pekerjaannya pada suatu proyek dan mengirimi Anda faktur, Anda harus meninjau status proyek dan faktur pelanggan untuk menentukan apakah persyaratan PWP terpenuhi untuk proyek tersebut. Jika persyaratan PWP untuk vendor terpenuhi, Anda dapat menentukan baris pada faktur vendor untuk membayar, berdasarkan pembayaran pelanggan untuk proyek. Jika Anda memutuskan untuk membayar vendor meskipun persyaratan PWP tidak terpenuhi, Anda dapat menimpa persyaratan PWP pada halaman **faktur vendor dengan bayar saat dibayar**.

1. Di Keuangan, buka **Proyek manajemen dan akuntansi** \> **Proyek** \> **Semua proyek**, dan pilih proyek.
2. Pada Panel Tindakan, pilih **Kontrol**, lalu pilih **Faktur vendor** untuk memperlihatkan semua faktur vendor yang telah dibuat untuk proyek tersebut.
3. Pada halaman **faktur vendor dengan bayar saat dibayar**, di bidang pencarian, masukkan nilai untuk menemukan faktur vendor yang ingin Anda tinjau, lalu pilih **Cari**.
4. **Pilih opsi Bayar saat dibayar** untuk hanya melihat faktur PWP.
5. **Pada tab Cepat baris** faktur Vendor, pilih baris yang ingin Anda rilis untuk pembayaran.
6. Pilih **Rilis pembayaran** vendor. Opsi **bayar saat dibayar** dikosongkan, dan nilai bidang **siap untuk pembayaran** diubah ke **ya**.
