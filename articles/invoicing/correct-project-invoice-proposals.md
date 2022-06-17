---
title: Memperbaiki akuntansi pada draf proposal faktur proyek
description: Artikel ini menjelaskan cara menyesuaikan informasi terkait akuntansi pada draf proposal faktur.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921214"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Memperbaiki akuntansi pada draf proposal faktur proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

*Rincian operasional* untuk faktur proyek dikelola oleh manajer proyek pada faktur pro forma. Rincian ini mencakup keputusan tentang jam, pengeluaran, bahan, atau tahapan yang harus ditagihkan, tarif, serta penerapan jumlah uang muka dan panjar. Setelah mengkonfirmasikan faktur pro forma asli, Anda dapat menyesuaikan rincian operasional dengan membuat dan mengkonfirmasikan [faktur pro forma perbaikan](../proforma-invoicing/corrective-invoices.md).

*Rincian akuntansi* untuk faktur proyek dikelola di dokumen faktur untuk pelanggan. Rincian ini mencakup perhitungan pajak penjualan dan dimensi keuangan yang diterapkan ke faktur. Artikel ini memberikan detail tentang bagaimana detail akuntansi ini dapat disesuaikan pada draf proposal faktur proyek.

## <a name="adjust-sales-tax"></a>Menyesuaikan Pajak Penjualan

Grup pajak penjualan penagihan default dan grup pajak penjualan item dapat disesuaikan secara langsung pada dokumen proposal faktur. Untuk menyesuaikan grup ini, pilih **Edit**, lalu di setiap baris proposal faktur proyek, masukkan nilai baru di bidang **grup pajak penjualan** atau **grup pajak penjualan Item**.

## <a name="adjust-financial-dimensions"></a>Menyesuaikan dimensi keuangan

### <a name="header-dimensions"></a>Dimensi header

Secara default, dimensi keuangan faktur berasal dari catatan transaksi proyek yang tidak ditagih yang sedang ditagih. Namun, pengaturan sistem memungkinkan Anda menggunakan dimensi keuangan pada header proposal faktur proyek untuk memposting saldo pelanggan. Untuk mengaktifkan fungsi ini, pilih **Izinkan pembaruan ke dimensi proyek untuk piutang** pada tab **Keuangan** di **halaman Manajemen proyek dan parameter** akuntansi.

Dimensi keuangan pada header faktur dapat diedit sebelum faktur diposting. Pada halaman **Proposal** faktur proyek, beralihlah **ke tampilan Header**, lalu edit nilai pada tab **Dimensi** keuangan.

Tampilan **Header** hanya tersedia setelah administrator sistem mengaktifkan **proposal faktur Gunakan Proyek dan formulir jurnal faktur dengan fitur tampilan** Header dan Baris di **ruang kerja Manajemen** fitur. Fitur ini memerlukan pembaruan Keuangan 10.0.25 atau yang lebih baru.

### <a name="line-dimensions"></a>Dimensi garis

Dimensi keuangan tidak dapat diedit secara langsung pada baris proposal faktur proyek. Melainkan, ikuti langkah-langkah ini untuk menyesuaikan dimensi keuangan pada proposal faktur proyek.

1. Pada proposal faktur proyek, pilih **Hapus semua** untuk menghilangkan baris proposal faktur proyek.

    Tombol **Hapus semua** tersedia hanya setelah administrator sistem mengaktifkan fitur **Hapus baris proposal faktur saat menggunakan Project Operations untuk skenario berbasis sumber daya/non-stok** di ruang kerja **manajemen Fitur**.

2. Menyesuaikan dimensi keuangan:

    - **Transaksi cicilan (tahapan penagihan):** Buka **Semua proyek** \> **Kelola** \> **transaksi cicilan**, dan pilih tahapan yang memerlukan penyesuaian. Kemudian, pada tab **Dimensi keuangan**, perbarui nilai jika diperlukan.
    - **Waktu, pengeluaran, dan transaksi bahan**: Pada halaman **Transaksi proyek yang diposting**, pilih **Sesuaikan akuntansi** untuk memperbarui dimensi keuangan.

3. Setelah selesai menyesuaikan nilai dimensi keuangan, buka **manajemen proyek dan akuntansi** \> **Berkala** \> **Integrasi Project Operations**, dan pilih **Impor dari tabel penahapan** untuk menjalankan proses berkala. Proses tersebut menggunakan nilai dimensi keuangan yang diperbarui untuk membuat ulang baris proposal faktur proyek. Nilai yang diperbarui kemudian digunakan dalam buku besar umum dan buku besar pembantu proyek ketika faktur proyek diposting.
