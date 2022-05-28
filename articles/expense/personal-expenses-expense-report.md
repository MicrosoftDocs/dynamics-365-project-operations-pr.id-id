---
title: Menangani Pengeluaran pribadi pada laporan pengeluaran
description: Informasi topik ini berisi informasi tentang cara menangani pengeluaran pribadi yang ditanggung oleh karyawan saat bepergian untuk keperluan bisnis.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: d35bf6960bb60e2ad4184e1b5f188695a3525be0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586532"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Menangani Pengeluaran pribadi pada laporan pengeluaran

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Selama perjalanan bisnis, karyawan dapat membebankan biaya pribadi ke kartu kredit perusahaan mereka. Jika proses belum ditentukan untuk menangani pengeluaran pribadi, proses persetujuan laporan pengeluaran mungkin terganggu saat karyawan mengirimkan laporan pengeluaran terperinci mereka.

Ada dua metode yang dapat Anda gunakan untuk menangani pengeluaran pribadi karyawan:

  - **Dibayar oleh karyawan**: organisasi Anda tidak membayar pengeluaran pribadi yang muncul pada tagihan untuk kartu kredit perusahaan. Sebaliknya, karyawan membayar vendor kartu kredit secara langsung untuk pengeluaran. 
  - **Dibayar oleh perusahaan**: Organisasi Anda membayar tagihan penuh untuk kartu kredit korporasi, kemudian mendebit akun pekerja untuk pengeluaran pribadi.

Anda dapat memilih metode yang digunakan organisasi pada halaman **parameter manajemen pengeluaran**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Mengaktifkan fungsi pengeluaran terpisah bila bidang jumlah pribadi telah ditentukan nilainya

Fitur, **Aktifkan fungsi pengeluaran terpisah bila bidang jumlah pribadi telah ditentukan nilainya** hanya berlaku untuk laporan pengeluaran yang disetujui menggunakan alur kerja tingkat baris. Laporan disetujui dengan membuka **Proses Laporan pengeluaran** > **Laporan pengeluaran yang ditetapkan kepada saya** > **Buka laporan pengeluaran**. 

Untuk mengaktifkan fitur ini, buka **Ruang Kerja** > **Manajemen Fitur**, pilih **Aktifkan fungsi pengeluaran terpisah bila bidang jumlah pribadi memiliki nilai yang ditentukan**, lalu pilih **Aktifkan sekarang**. 

Bila fitur diaktifkan, baris pengeluaran yang menggunakan fungsi ini akan menghasilkan dua baris saat laporan dikirim. Dua baris dibuat sehingga pemberi izin dapat menyetujui setiap baris secara terpisah.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
