---
title: Membuat transaksi antarperusahaan
description: Topik ini memberikan informasi tentang cara membuat transaksi antarperusahaan.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 88e5658c9087fdb19adce1c23bc5cad0ad0fa434
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599977"
---
# <a name="create-intercompany-transactions"></a>Membuat transaksi antarperusahaan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Transaksi antarperusahaan adalah transaksi waktu dan pengeluaran dari kontrak proyek milik satu perusahaan atau unit organisasi, sedangkan sumber daya pada kontrak proyek adalah bagian dari perusahaan atau unit organisasi yang berbeda.

Apabila transaksi antarperusahaan disetujui, transaksi aktual berikut ini akan dibuat

| **Jenis transaksi** | **Daftar harga diterapkan** | **Mata uang transaksi** |
| --- | --- | --- |
| Biaya | Daftar harga unit kontrak | Mata uang pada baris harga |
| Penjualan belum tertagih. Dibuat hanya untuk nilai aktual yang terkait dengan baris kontrak dengan jenis, waktu, dan materi penagihan. | Daftar harga penjualan proyek kontrak | Mata uang kontrak |
| Biaya Unit Sumber Daya | Daftar harga unit sumber daya | Mata uang pada baris harga |
| Penjualan unit antarorganisasi | Daftar harga unit kontrak | Mata uang pada baris harga |

Biaya, biaya unit sumber daya, dan harga transaksi penjualan unit antarorganisasi, serta mata uang didorong oleh **unit organisasi**. Hal ini penting untuk diingat ketika memutuskan bagaimana membuat struktur perusahaan dan unit organisasi dalam penerapan Anda.

Saat Anda membuat peluang, kuotasi, kontrak proyek, dan record proyek, sistem akan memverifikasi bahwa mata uang unit kontrak sesuai dengan mata uang akuntansi perusahaan kontrak. Bila tidak sama, record ini tidak dapat dibuat. Mata uang unit organisasi ditentukan di Dynamics 365 Project Operations dengan membuka **Dataverse** > **Pengaturan** > **Unit Organisasi**. Mata uang akuntansi perusahaan didefinisikan dalam Dynamics 365 Finance dengan pergi ke **General Ledger** > **Ledger setup** > **Ledger**. Mata uang disinkronisasikan dengan lingkungan Dataverse Anda menggunakan peta Penulisan Ganda Buku Besar.

Sistem akan membuat biaya unit sumber daya dan nilai aktual penjualan unit antarorganisasi dalam situasi berikut:

  - Apabila unit sumber daya berbeda dengan unit kontrak
  - Apabila perusahaan sumber daya berbeda dengan perusahaan kontrak

Namun, hanya transaksi yang memiliki perusahaan sumber daya yang berbeda dari perusahaan kontraktor yang akan ditransfer ke lingkungan Dynamics 365 Finance untuk akuntansi tambahan.

Akuntansi untuk aktual proyek dicatat dalam jurnal integrasi Project Operations di Keuangan. Sistem membuat baris jurnal berikut ini.

| **Jenis transaksi** | **Badan hukum** | **Membuat transaksi proyek pada posting** | **Default dimensi keuangan dari** | **Grup pajak penjualan penagihan dan grup pajak penjualan item tagihan default** |
| --- | --- | --- | --- | --- |
| Biaya | Belum ditambahkan ke jurnal integrasi | N\A | N\A | N\A |
| Penjualan Belum Tertagih | Jurnal integrasi entitas hukum peminjam | Ya | Project | **Grup pajak penjualan penagihan**: Berdasarkan **pelanggan kontrak** <br/> **Grup pajak penjualan item penagihan**: Dari kategori proyek entitas hukum saat ini pada baris jurnal |
| Biaya Unit Sumber Daya | Jurnal integrasi entitas hukum pemberi pinjaman | No | Pelanggan antarperusahaan | **Grup pajak penjualan penagihan**: Berdasarkan **pelanggan antarperusahaan** <br/> **Grup pajak penjualan item penagihan**: Dari kategori proyek entitas hukum saat ini pada baris jurnal |
| Penjualan antarorganisasi | Jurnal integrasi entitas hukum pemberi pinjaman | No | Pelanggan antarperusahaan | **Grup pajak penjualan penagihan**: Berdasarkan **pelanggan antarperusahaan** <br/> **Grup pajak penjualan item penagihan**: Dari kategori proyek entitas hukum saat ini pada baris jurnal |

### <a name="example-intercompany-transactions"></a>Contoh: Transaksi antarperusahaan

Molly Clark, pengembang yang bekerja di GBPM mencatat 10 jam kerja untuk proyek USPM Adventure Works, yang disetujui oleh manajer proyek. Biaya pengembang di GBPM adalah 88 GBP per jam. GBPM akan menagih USPM 120 USD per jam kerja pengembang. USPM akan menagih Adventure Works pelanggan, 200 USD untuk pekerjaan yang dilakukan oleh sumber daya GBPM. Untuk informasi lebih lanjut, lihat [Mengonfigurasi faktur antarperusahaan](configure-intercompany-invoicing.md).

1. Di Project Operations, buka **Sumber Daya**, lalu pilih **Molly Clark** dari daftar. Di tab **Penjadwalan**, di bidang **Perusahaan**, pilih **GBPM**.
2. Buka **Penjualan** > **Pelanggan**, lalu pilih **Baru** untuk membuat record pelanggan baru untuk Adventure Works.
    1. Atur perusahaan ke **USPM**.
    2. Atur **Jenis hubungan** ke **Pelanggan**.
    3. Pilih **Grup pelanggan 10 – Domestik**.
    4. Atur mata uang ke **USD**.
    5. Simpan rekaman ini.
3. Buka **Penjualan** > **Kontrak Proyek** dan buat kontrak proyek baru untuk Adventure Works.
    1. Atur Perusahaan pemilik ke **USPM** dan unit kontrak ke **Contoso Robotics US**.
    2. Pilih Adventure Works sebagai pelanggan.
    3. Pilih daftar harga produk dan simpan record.
    4. Di tab **Baris Kontrak**, buat baris kontrak baru. Atur nama, lalu pilih **Waktu dan Materi** sebagai metode penagihan.
    5. Buat proyek baru dan kaitkan dengan baris kontrak ini.
4. Masuk sebagai sumber daya, **Molly Clark**. Buka **Proyek** > **Entri waktu**, dan buat entri waktu untuk proyek Adventure Works.
5. Masuk sebagai Manajer proyek. Buka **Proyek** > **Persetujuan**, dan setujui transaksi entri waktu yang dicatat oleh Molly Clark.
6. Navigasi ke proyek Adventure Works dan pilih **Terkait** > **Aktual**. Transaksi aktual berikut dibuat.

| **Jenis transaksi** | **Harga** | **mata uang transaksi** | **Jumlah** |
| --- | --- | --- | --- |
| Biaya | 120 | USD | 1200 |
| Penjualan Belum Tertagih | 200 | USD | 2000 |
| Biaya Unit Sumber Daya | 88 | GBP | 880 |
| Penjualan unit antarorganisasi | 120 | USD | 1200 |

7. Masuk sebagai akuntan USPM. Buka instans Keuangan di Project Operations, dan pilih **USPM** perusahaan. 
8. Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Project Operations di Customer Engagement** > **Impor dari penahapan** dan pilih untuk menjalankan proses berkala. Proses berkala ini akan mengisi jurnal Integrasi Project Operations.
9. Buka **Manajemen dan akuntansi proyek** > **Jurnal** > **jurnal integrasi Project Operations** dan tinjau baris jurnal. Sistem membuat baris berikut ini.

    | **Jenis transaksi** | **Harga** | **mata uang transaksi** | **Jumlah** |
    | --- | --- | --- | --- |
    | Penjualan Belum Tertagih | 200 | USD | 2000 |

    Jika sistem diatur untuk menambahkan pendapatan pada proyek ini, berikut ini item yang diposting:

    - Debit: Proyek – Nilai penjualan WIP 200 USD
    - Kredit: Proyek – Pendapatan yang Terkumpul 200 USD

    Penjualan yang belum tertagih ini sekarang siap untuk pembuatan faktur. Faktur untuk Adventure Works pelanggan dapat diposting secara finansial bila diperlukan.

10. Masuk sebagai akuntan **GBPM**. Buka instans Keuangan di Project Operations, dan buka **GBPM** perusahaan. 
11. Buka **Manajemen proyek dan akuntansi** > **Berkala** > **Integrasi Project Operations** > **Impor dari tabel penahapan** dan jalankan proses berkala untuk mengisi jurnal Integrasi Project Operations.
12. Buka **Manajemen dan akuntansi proyek** > **Jurnal** > **jurnal integrasi Project Operations** dan tinjau barisnya. Sistem membuat item berikut ini.

    | **Jenis transaksi** | **Harga** | **mata uang transaksi** | **Jumlah** |
    | --- | --- | --- | --- |
    | Biaya Unit Sumber Daya | 88 | GBP | 880 |
    | Penjualan unit antarorganisasi | 120 | USD | 1200 |

    Memposting record ini akan menghasilkan transaksi voucher berikut:

    - Debit: Biaya proyek 88 GBP
    - Kredit: Alokasi penggajian 88 GBP

    Jika sistem diatur untuk menambahkan pendapatan antarperusahaan, berikut ini item yang diposting:

    - Debit: Proyek – Nilai penjualan WIP 120 USD
    - Kredit: Proyek – Pendapatan yang Terkumpul 120 USD

    Sistem sekarang siap membuat faktur pelanggan antarperusahaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
