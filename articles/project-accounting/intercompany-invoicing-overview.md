---
title: Sekilas faktur antarperusahaan
description: Artikel ini menyediakan informasi dan contoh tentang faktur antarperusahaan untuk proyek.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913578"
---
# <a name="intercompany-invoicing-overview"></a>Sekilas faktur antarperusahaan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Organisasi Anda mungkin memiliki beberapa divisi, anak perusahaan, dan entitas hukum lainnya yang mentransfer produk dan layanan satu sama lain untuk proyek. Entitas hukum yang menyediakan layanan atau produk disebut *entitas hukum pemberi pinjaman*. Entitas hukum yang menerima layanan atau produk disebut *entitas hukum peminjam*.

Ilustrasi berikut menunjukkan skenario umum di mana dua entitas hukum, Contoso Robotics USA (entitas hukum peminjam) dan Contoso Robotics UK (entitas hukum pemberi pinjaman) berbagi sumber daya untuk menyediakan proyek bagi pelanggan, Adventure works. Untuk skenario ini, Contoso Robotics USA dikontrak untuk memberikan pekerjaan kepada Adventure Works.

![Faktur antarperusahaan.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations menggunakan aliran berikut ini untuk memproses transaksi antarperusahaan:

1. Sumber daya dari record entitas hukum pemberi pinjaman untuk transaksi pengeluaran atau waktu antarperusahaan berdasarkan waktu dan biaya pemesanan proyek di entitas hukum peminjam.
2. Biaya waktu dan pengeluaran dicatat di perusahaan pemberi pinjaman dengan menggunakan daftar harga biaya unit perusahaan peminjam.
3. Transaksi penjualan antarperusahaan yang belum ditagihkan dicatat di perusahaan pemberi pinjaman dengan menggunakan daftar harga biaya unit perusahaan peminjam.
4. Pendapatan yang belum ditagih tercatat di perusahaan peminjam menggunakan daftar harga penjualan kontrak proyek. Pelanggan dapat ditagih apabila pendapatan yang belum ditagih tercatat. Pelanggan tidak perlu menunggu hingga pemrosesan faktur antarperusahaan selesai.
5. Faktur pelanggan antarperusahaan dibuat secara berkala di perusahaan pemberi pinjaman. Faktur dibuat secara manual atau dengan menggunakan proses otomatis berkala. Faktur tunggal dapat dibuat untuk setiap entitas hukum peminjam atau faktur terpisah dapat dibuat berdasarkan proyek.
6. Saat faktur pelanggan antarperusahaan diposting di entitas hukum pemberi pinjaman, faktur tertunda vendor yang terkait dibuat di entitas hukum peminjam. Biaya di faktur tertunda vendor akan dicatat di subbuku besar proyek saat faktur diposting.

Diagram berikut menunjukkan faktur antarperusahaan yang terkait dengan aktivitas akuntansi dan posting yang diharapkan ke buku besar.

![Alur antarperusahaan.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Sumber daya tambahan

- [Mengonfigurasikan faktur antarperusahaan](configure-intercompany-invoicing.md)
- [Mencatat transaksi antarperusahaan](create-intercompany-transactions.md)
- [Membuat faktur vendor dan pelanggan antarperusahaan](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]