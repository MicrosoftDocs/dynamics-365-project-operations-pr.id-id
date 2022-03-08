---
title: Sekilas faktur antarperusahaan
description: Topik ini berisi informasi dan contoh tentang membuat faktur antarperusahaan untuk berbagai proyek.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002645"
---
# <a name="intercompany-invoicing-overview"></a>Sekilas faktur antarperusahaan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Organisasi Anda mungkin memiliki beberapa divisi, anak perusahaan, dan entitas hukum lainnya yang mentransfer produk dan layanan satu sama lain untuk proyek. Entitas hukum yang menyediakan layanan atau produk disebut *entitas hukum pemberi pinjaman*. Entitas hukum yang menerima layanan atau produk disebut *entitas hukum peminjam*.

Ilustrasi berikut menampilkan skenario umum, yakni dua entitas hukum, Contoso Robotics USA (entitas hukum peminjam) dan Robotics Contoso UK (entitas hukum pemberia pinjaman) berbagi sumber daya untuk melaksanakan proyek untuk pelanggan, Adventure Works. Untuk skenario ini, Contoso Robotics USA dikontrak untuk memberikan pekerjaan ke Adventure Works.

![Faktur antarperusahaan](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations menggunakan aliran berikut ini untuk memproses transaksi antarperusahaan:

1. Sumber daya dari record entitas hukum pemberi pinjaman untuk transaksi pengeluaran atau waktu antarperusahaan berdasarkan waktu dan biaya pemesanan proyek di entitas hukum peminjam.
2. Biaya waktu dan pengeluaran dicatat di perusahaan pemberi pinjaman dengan menggunakan daftar harga biaya unit perusahaan peminjam.
3. Transaksi penjualan antarperusahaan yang belum ditagihkan dicatat di perusahaan pemberi pinjaman dengan menggunakan daftar harga biaya unit perusahaan peminjam.
4. Pendapatan yang belum ditagih tercatat di perusahaan peminjam menggunakan daftar harga penjualan kontrak proyek. Pelanggan dapat ditagih apabila pendapatan yang belum ditagih tercatat. Pelanggan tidak perlu menunggu hingga pemrosesan faktur antarperusahaan selesai.
5. Faktur pelanggan antarperusahaan dibuat secara berkala di perusahaan pemberi pinjaman. Faktur dibuat secara manual atau dengan menggunakan proses otomatis berkala. Faktur tunggal dapat dibuat untuk setiap entitas hukum peminjam atau faktur terpisah dapat dibuat berdasarkan proyek.
6. Saat faktur pelanggan antarperusahaan diposting di entitas hukum pemberi pinjaman, faktur tertunda vendor yang terkait dibuat di entitas hukum peminjam. Biaya di faktur tertunda vendor akan dicatat di subbuku besar proyek saat faktur diposting.

Diagram berikut menunjukkan faktur antarperusahaan yang terkait dengan aktivitas akuntansi dan posting yang diharapkan ke buku besar.

![Alur antarperusahaan](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Sumber daya tambahan

- [Mengonfigurasikan faktur antarperusahaan](configure-intercompany-invoicing.md)
- [Mencatat transaksi antarperusahaan](create-intercompany-transactions.md)
- [Membuat faktur vendor dan pelanggan antarperusahaan](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]