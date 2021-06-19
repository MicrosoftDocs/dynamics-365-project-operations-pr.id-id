---
title: Default dimensi keuangan
description: Topik ini memberikan informasi tentang cara mengatur default dimensi keuangan.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013310"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]