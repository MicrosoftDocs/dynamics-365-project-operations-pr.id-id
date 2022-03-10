---
title: Default dimensi keuangan
description: Topik ini memberikan informasi tentang cara mengatur default dimensi keuangan.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922942"
---
# <a name="financial-dimension-defaults"></a>Default dimensi keuangan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations menggunakan kerangka kerja [Dimensi keuangan](/dynamics365/finance/general-ledger/financial-dimensions) di Dynamics 365 Finance untuk memberikan wawasan tambahan tentang transaksi buku besar pembantu proyek dan buku besar umum.

Dimensi keuangan default dapat ditetapkan pada pelanggan, sumber pendanaan proyek, tonggak pencapaian, lini kontrak proyek, atau proyek.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Tentukan dimensi keuangan default untuk pelanggan

Default dimensi pelanggan ditentukan dalam Finance. Selesaikan langkah berikut ini untuk mengatur default dimensi.

1. Buka **piutang dagang** > **Pelanggan** > **Semua pelanggan**.
2. Pada halaman **Pelanggan**, pada tab **Dimensi keuangan**, tetapkan nilai dimensi keuangan untuk pelanggan tertentu.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Tentukan dimensi keuangan default untuk kontrak proyek

Kontrak proyek dibuat dan dipertahankan di Common Data Service (CDS). Atribut akuntansi untuk kontrak proyek diatur dalam modul **manajemen Proyek dan akuntansi** di Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Menetapkan dimensi keuangan untuk sumber pendanaan proyek

1. Buka **manajemen proyek dan akuntansi** > **Proyek** > **Kontrak proyek**.
2. Pilih rekaman yang ingin Anda perbarui, dan pada tab **Kontrak proyek**, pilih **Perlihatkan akuntansi default**.
3. Perluas **Informasi terkait** dan pilih tab **Sumber pendanaan**.
4. Atur Default dimensi keuangan. Perhatikan bahwa dimensi keuangan di-default dari akun pelanggan.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Menetapkan dimensi keuangan untuk baris kontrak proyek

1. Buka **manajemen proyek dan akuntansi** > **Proyek** > **Kontrak proyek**.
2. Pilih rekaman yang ingin Anda perbarui, dan pada tab **Kontrak proyek**, pilih **Perlihatkan akuntansi default**.
3. Perluas **Informasi terkait** dan pilih tab **baris kontrak**.
4. Atur Default dimensi keuangan. Default dimensi keuangan berlaku dan hanya dapat digunakan dengan baris kontrak Harga Tetap (tonggak pencapaian).

Default ini digunakan pada transaksi pada akun proyek terkait dan baris faktur.

## <a name="define-default-financial-dimensions-for-projects"></a>Tentukan dimensi keuangan default untuk proyek

Proyek dibuat dan dikelola di (CDS). Atribut akuntansi untuk proyek diatur dalam modul **manajemen Proyek dan akuntansi** di Finance.

1. Buka **manajemen proyek dan akuntansi** > **proyek** > **Semua proyek**.
2. Pilih rekaman yang ingin Anda perbarui, dan pada tab **proyek**, pilih **Perlihatkan akuntansi default**.
3. Perluas **Informasi terkait** dan pilih tab **Konfigurasi**.
4. Atur Default dimensi keuangan. Perhatikan bahwa dimensi keuangan di-default dari akun pelanggan. Jika proyek dikaitkan dengan baris kontrak dengan beberapa pelanggan kontrak proyek, pelanggan utama digunakan untuk dimensi keuangan default.

Dimensi keuangan default proyek digunakan untuk menetapkan default baris jurnal untuk transaksi waktu, pengeluaran, dan biaya di **Jurnal Integrasi Project Operations,** dan pada baris faktur proyek terkait.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Menerapkan dimensi keuangan untuk entri waktu proyek
Untuk menerapkan dimensi keuangan untuk entri waktu proyek, perhatikan bahwa nilai dimensi default didasarkan pada urutan berikut:

1. Sumber info
2. Project
3. Sumber pendanaan

Misalnya, jika dimensi default ditentukan pada sumber daya, itu akan diterapkan melalui default yang ditentukan pada proyek. Demikian pula, dimensi proyek default akan diterapkan melalui default yang ditentukan dalam sumber pendanaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
