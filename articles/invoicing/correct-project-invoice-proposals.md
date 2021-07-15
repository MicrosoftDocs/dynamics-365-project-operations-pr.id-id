---
title: Memperbaiki akuntansi pada draf proposal faktur proyek
description: Topik ini menjelaskan cara menyesuaikan informasi yang terkait dengan akuntansi pada draf proposal faktur.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251228"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Memperbaiki akuntansi pada draf proposal faktur proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

*Rincian operasional* untuk faktur proyek dikelola oleh manajer proyek pada faktur pro forma. Rincian ini mencakup keputusan tentang jam, pengeluaran, bahan, atau tahapan yang harus ditagihkan, tarif, serta penerapan jumlah uang muka dan panjar. Setelah mengkonfirmasikan faktur pro forma asli, Anda dapat menyesuaikan rincian operasional dengan membuat dan mengkonfirmasikan [faktur pro forma perbaikan](../proforma-invoicing/corrective-invoices.md).

*Rincian akuntansi* untuk faktur proyek dikelola di dokumen faktur untuk pelanggan. Rincian ini mencakup perhitungan pajak penjualan dan dimensi keuangan yang diterapkan ke faktur. Laporan topik ini memberikan rincian tentang penyesuaian rincian akuntansi ini pada draf proposal faktur proyek.

## <a name="adjust-sales-tax"></a>Menyesuaikan Pajak Penjualan

Grup pajak penjualan penagihan default dan grup pajak penjualan item dapat disesuaikan secara langsung pada dokumen proposal faktur. Untuk menyesuaikan grup ini, pilih **Edit**, lalu di setiap baris proposal faktur proyek, masukkan nilai baru di bidang **grup pajak penjualan** atau **grup pajak penjualan Item**.

## <a name="adjust-financial-dimensions"></a>Menyesuaikan dimensi keuangan

Dimensi keuangan tidak dapat diedit secara langsung pada baris proposal faktur proyek. Melainkan, ikuti langkah-langkah ini untuk menyesuaikan dimensi keuangan pada proposal faktur proyek.

1. Pada proposal faktur proyek, pilih **Hapus semua** untuk menghilangkan baris proposal faktur proyek.

    > [!NOTE]
    > Tombol **Hapus semua** tersedia hanya setelah administrator sistem mengaktifkan fitur **Hapus baris proposal faktur saat menggunakan Project Operations untuk skenario berbasis sumber daya/non-stok** di ruang kerja **manajemen Fitur**.

2. Menyesuaikan dimensi keuangan:

    - **Transaksi cicilan (tahapan penagihan):** Buka **Semua proyek** \> **Kelola** \> **transaksi cicilan**, dan pilih tahapan yang memerlukan penyesuaian. Kemudian, pada tab **Dimensi keuangan**, perbarui nilai jika diperlukan.
    - **Waktu, pengeluaran, dan transaksi bahan**: Pada halaman **Transaksi proyek yang diposting**, pilih **Sesuaikan akuntansi** untuk memperbarui dimensi keuangan.

3. Setelah selesai menyesuaikan nilai dimensi keuangan, buka **manajemen proyek dan akuntansi** \> **Berkala** \> **Integrasi Project Operations**, dan pilih **Impor dari tabel penahapan** untuk menjalankan proses berkala. Proses tersebut menggunakan nilai dimensi keuangan yang diperbarui untuk membuat ulang baris proposal faktur proyek. Nilai yang diperbarui kemudian digunakan dalam buku besar umum dan buku besar pembantu proyek ketika faktur proyek diposting.
