---
title: Mengkonfigurasi akuntansi untuk proyek internal
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi praktik akuntansi untuk proyek internal dalam Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597848"
---
# <a name="configure-accounting-for-internal-projects"></a>Mengkonfigurasi akuntansi untuk proyek internal

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Proyek internal memungkinkan perusahaan melacak biaya yang terkait dengan aktivitas yang tidak ditagihkan kepada pelanggan. Contoh proyek internal mencakup:

- Mengembangkan produk, seperti aplikasi seluler, dan melacak biaya yang terkait dengan pengembangan.
- Mengelola waktu dan pengeluaran pra-penjualan. Proyek internal pra-penjualan ini dapat dikonversi nanti ke proyek yang dapat ditagih jika kuotasi dimenangkan.

Proyek apa pun yang tidak terkait dengan kontrak di Dynamics 365 Project Operations ditangani sebagai internal. Profil biaya dan pendapatan proyek tidak digunakan untuk menentukan aturan akuntansi untuk proyek. Biaya proyek internal selalu diposting menggunakan prinsip laba-rugi. Akun buku besar untuk posting ditetapkan pada halaman **penataan posting buku besar**.

- Transaksi waktu diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **alokasi gaji**.
- Transaksi pengeluaran diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **akun pengimbang untuk pengeluaran**.
- Transaksi item diposting dengan mendebit akun **Biaya** dan mengkredit akun **biaya - Item**.

Setelah transaksi diposting ke proyek, jika proyek terkait dengan kontrak proyek, sistem akan membalikkan semua transaksi yang terkumpul dan membuat transaksi yang dapat ditagih baru. Transaksi yang dapat ditagih mengikuti aturan akuntansi yang ditentukan di profil biaya dan pendapatan proyek masing-masing.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
