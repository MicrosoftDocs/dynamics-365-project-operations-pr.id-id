---
title: Mengkonfigurasi akuntansi untuk proyek internal
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi praktik akuntansi untuk proyek internal dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132382"
---
# <a name="configure-accounting-for-internal-projects"></a>Mengkonfigurasi akuntansi untuk proyek internal

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Proyek internal memungkinkan perusahaan melacak biaya yang terkait dengan aktivitas yang tidak ditagihkan kepada pelanggan. Contoh proyek internal mencakup:

- Mengembangkan produk, seperti aplikasi seluler, dan melacak biaya yang terkait dengan pengembangan.
- Mengelola waktu dan pengeluaran pra-penjualan. Proyek internal pra-penjualan ini dapat dikonversi nanti ke proyek yang dapat ditagih jika kuotasi dimenangkan.

Setiap proyek yang tidak terkait dengan kontrak dalam Dynamics 365 Project Operations diperlakukan sebagai internal. Profil biaya dan pendapatan proyek tidak digunakan untuk menentukan aturan akuntansi untuk proyek. Biaya proyek internal selalu diposting menggunakan prinsip laba-rugi. Akun buku besar untuk posting ditetapkan pada halaman **penataan posting buku besar**.

- Transaksi waktu diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **alokasi gaji**.
- Transaksi pengeluaran diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **akun pengimbang untuk pengeluaran**.

Setelah transaksi diposting ke proyek, jika proyek terkait dengan kontrak proyek, sistem akan membalikkan semua transaksi yang terkumpul dan membuat transaksi yang dapat ditagih baru. Transaksi yang dapat ditagih mengikuti aturan akuntansi yang ditentukan di profil biaya dan pendapatan proyek masing-masing.




[!INCLUDE[footer-include](../includes/footer-banner.md)]