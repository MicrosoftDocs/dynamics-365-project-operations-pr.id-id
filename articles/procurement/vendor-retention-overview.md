---
title: Ikhtisar retensi vendor
description: Topik ini memberikan ikhtisar kemampuan retensi vendor.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588464"
---
# <a name="vendor-retention-overview"></a>Ikhtisar retensi vendor

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Organisasi Anda mungkin ingin mempertahankan sebagian pembayaran kepada vendor yang mengerjakan proyek untuk organisasi Anda. Misalnya, sebelum membayar vendor, Anda dapat memastikan bahwa item dan layanan yang mereka berikan telah memenuhi kebutuhan Anda.

Saat menegosiasikan pembelian untuk proyek dengan vendor, Anda dapat menentukan persyaratan retensi vendor yang mencakup persentase atau jumlah yang akan dipertahankan. Saat vendor mengirimkan item dan layanan, Anda mengurangi persentase atau jumlah retensi yang ditentukan dari pembayaran Anda ke vendor. Setelah proyek selesai atau mencapai tahapan interim sebagaimana ditentukan dalam kontrak vendor, Anda melepas jumlah yang dipertahankan dan membuat pembayaran ke vendor.

## <a name="vendor-retention-example"></a>Contoh retensi vendor

Contoh berikut menunjukkan bagaimana persentase jumlah faktur vendor dipertahankan berdasarkan persentase yang selesai untuk proyek.

Contoso Robotics USA telah berkontrak dengan vendor Fabrikam untuk memberikan pelatihan selama 100 jam untuk proyek pembaruan perlengkapan. Nilai kontrak total adalah USD 30.000 dengan harga pembelian yang disetujui sebesar USD 300 per jam.

Pelatihan akan dilakukan dalam tiga fase dengan jadwal berikut:

- Fase 1: 50 jam, atau 50 persen dari proyek
- Fase 2: 30 jam, atau 80 persen dari proyek dalam total
- Fase 3: 20 jam, atau 100 persen dari proyek

Tabel berikut berisi daftar istilah retensi.

| **Persentase unit yang dikirim** | **Persentase untuk dipertahankan** | **Persentase untuk dilepas** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Transaksi mengakibatkan jumlah berikut:

- Fase 1:
  - Jumlah yang harus dibayar adalah 50 x 300, atau 15.000.
  - 20 persen dari jumlah tersebut, atau 3.000 akan dipertahankan dan akan dirilis di tahapan berikutnya.
  - Jumlah yang dibayar ke vendor adalah 12.000.
- Fase 2:
  - Jumlah yang harus dibayar adalah 30 x 300, atau 9.000.
  - 10 persen dari jumlah, atau 900, dipertahankan.
  - 10 persen dari 3.000 yang dipertahankan di Fase 1 atau 300 akan dirilis.
  - Jumlah yang dibayar ke vendor adalah 8.400. Jumlah ini adalah 9.000 kurang retensi 900 ditambah 300 yang dirilis dari retensi Fase 1.
- Fase 3:
  - Jumlah yang harus dibayar adalah 20 x 300, atau 6.000.
  - Tidak ada jumlah yang dipertahankan.
  - Jumlah yang dirilis adalah 3.600. Jumlah ini terdiri dari 3.000 yang dipertahankan di Fase 1, dikurang 300 dari Fase 1 yang dirilis di Fase 2, ditambah 900 yang dipertahankan di Fase 2.
  - Jumlah yang dibayar ke vendor adalah 9.600. Jumlah ini terdiri dari jumlah dipertahankan 3.600 ditambah 6.000 untuk penyelesaian Fase 3.

Jumlah total yang telah dibayar ke vendor setelah tiga fase selesai adalah 30.000, yakni jumlah total pesanan pembelian (15.000 + 9.000 + 6.000).
