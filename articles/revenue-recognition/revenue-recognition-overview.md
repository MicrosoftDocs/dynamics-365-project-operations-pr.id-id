---
title: Sekilas pengakuan pendapatan
description: Topik ini berisi informasi tentang pengakuan pendapatan dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278872"
---
# <a name="revenue-recognition-overview"></a>Sekilas pengakuan pendapatan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Di Dynamics 365 Project Operations, prinsip pengakuan pendapatan bervariasi berdasarkan pada metode penagihan yang dipilih untuk proyek atau bagian dari proyek. Topik ini berisi informasi tentang pengakuan pendapatan dalam Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transaksi yang dihitung menggunakan metode penagihan waktu dan material

- Pengakuan biaya dan pendapatan terhubung. Biaya transaksi dan penjualan yang belum ditagih diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).
- Biaya proyek dan profil pendapatan menentukan apakah transaksi penjualan yang belum ditagih diposting di buku besar. Jika **Pendapatan yang terkumpul** dipilih, sistem menggunakan **Nilai penjualan WIP** dan akun **Nilai penjualan pendapatan yang terkumpul** saat posting dilakukan. Berikut adalah contoh dari metode ini.  

  | Jenis transaksi | Debit/Kredit | Jumlah |
  | --- | --- | --- |
  | Nilai Penjualan WIP | Debit | 100 |
  | pendapatan akrual - nilai penjualan | Kredit | 100 |

- Pendapatan direkognisi pada saat pembuatan faktur. Sistem menggunakan akun **Pendapatan tertagih** pada saat diposting. Berikut adalah contoh dari metode ini.  

  | Jenis transaksi | Debit/Kredit | Jumlah |
  | --- | --- | --- |
  | Saldo pelanggan | Debit | 120 |
  | Pajak penjualan untuk dibayarkan | Kredit | 20 |
  | Pendapatan Tertagih | Kredit | 100 |

- Jika pendapatan diperoleh saat penjualan yang belum ditagih diposting, sistem akan membalikkan pendapatan yang diperoleh pada faktur.

  | Jenis transaksi | Debit/Kredit | Jumlah |
  | --- | --- | --- |
  | Nilai Penjualan WIP | Kredit | 100 |
  | pendapatan akrual - nilai penjualan | Debit | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transaksi yang dihitung menggunakan metode penagihan harga tetap

- Pengakuan biaya dan pendapatan terpisah. Biaya transaksi diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Transaksi penjualan yang belum ditagih tidak dibuat.
- Pendapatan dapat direkognisi saat pembuatan faktur jika biaya proyek dan profil pendapatan memiliki **Prinsip yang digunakan untuk penghitungan penyelesaian proyek** yang diatur ke **Tanpa WIP**. Hanya gunakan metode ini untuk proyek jangka pendek dan sederhana.
- Pendapatan dapat direkognisi menggunakan estimasi pendapatan harga tetap, baik dengan metode **Kontrak yang selesai** maupun **Persen penyelesaian pengakuan pendapatan**.

## <a name="additional-resources"></a>Sumber daya tambahan
[Mengonfigurasikan akuntansi untuk artikel yang bisa ditagih](../project-accounting/configure-accounting-billable-projects.md)

[Proyek estimasi pendapatan harga tetap](rev-rec-percentage-completion-method.md)

[Mengelola estimasi pendapatan](rev-rec-completed-contract-method.md)

[Metode biaya penyelesaian](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]