---
title: Mengonfigurasi kategori pengeluaran
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi kategori pengeluaran dan kategori bersama untuk laporan pengeluaran.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 925c0894616df587b8a749bc00ea52ed06672827
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577010"
---
# <a name="set-up-expense-categories"></a>Mengonfigurasi kategori pengeluaran

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Bila karyawan membuat laporan pengeluaran, setiap biaya yang direkam harus dikaitkan dengan kategori pengeluaran. Kategori pengeluaran berasal dari kategori bersama yang dapat dibagikan di seluruh entitas hukum di organisasi Anda. Tergantung pada bagaimana organisasi Anda didefinisikan, kategori pengeluaran ini juga dapat dibagikan di area lain. Berdasarkan definisi organisasi dan panduan dari tim penerapan, Anda harus menentukan apakah kategori yang digunakan dalam manajemen pengeluaran hanya akan digunakan di manajemen pengeluaran atau harus dibagikan di area lain.

> [!NOTE]
> Kategori ini dapat dibagi antara manajemen proyek dan manajemen akuntansi dan pengeluaran, atau antara manajemen proyek dan akuntansi dan produksi. Namun, mereka tidak dapat dibagi antara manajemen pengeluaran dan produksi.

Sebelum Anda dapat memulai proses konfigurasi, keputusan berikut harus dibuat untuk setiap kategori pengeluaran:

- Apa itu kategori pengeluaran? Contohnya mencakup kategori untuk penerbangan, Hotel, atau jarak tempuh.
- Dapatkah kategori pengeluaran juga dapat digunakan dalam manajemen proyek dan akuntansi? Jika bisa, Anda juga harus membuat keputusan berikut:

    - Biaya akun apa yang akan digunakan untuk biaya berikut?

        - Biaya
        - Alokasi penggajian
        - WIP-Nilai biaya
        - Item biaya
        - Item-Nilai biaya-WIP
        - Rugi akrual
        - Rugi akrual-WIP

    - Akun pendapatan apa yang akan digunakan untuk sumber pendapatan berikut?

        - Pendapatan yang ditagih
        - pendapatan akrual – nilai penjualan
        - WIP-nilai penjualan
        - Pendapatan akrual-produksi
        - WIP-Produksi
        - Pendapatan akrual-laba
        - WIP-Laba
        - Pendapatan akrual-langganan
        - WIP-Langganan

- Apa itu jenis pengeluaran?
- Apa yang dimaksud dengan metode pembayaran default untuk kategori pengeluaran?
- Apakah pengeluaran dalam kategori pengeluaran harus diitemkan?
- Apa yang dimaksud akun default utama untuk kategori pengeluaran?
- Apa yang dimaksud dengan grup pajak penjualan item default untuk kategori pengeluaran?
- Apakah metode pembayaran tambahan diizinkan untuk kategori pengeluaran? Jika demikian, apa saja?
- Apakah ada subkategori dalam kategori pengeluaran ini? Jika ada subkategori, Anda juga harus membuat keputusan berikut:

    - Apakah ada subkategori yang dikecualikan dari pemulihan pajak?
    - Apa yang dimaksud dengan grup pajak penjualan item dari subkategori?


[!INCLUDE[footer-include](../includes/footer-banner.md)]