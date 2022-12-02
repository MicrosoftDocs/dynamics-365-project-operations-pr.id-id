---
title: Membuat kontrak lanjutan untuk penagihan berdasarkan progres
description: Artikel ini menjelaskan cara membuat kontrak proyek sehingga anda dapat membuat faktur untuk pelanggan, berdasarkan persentase pekerjaan yang diselesaikan.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26fe072b8241c7fdc96629f534e33a8fe53d3164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913670"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Membuat kontrak lanjutan untuk penagihan berdasarkan progres
[!include [banner](../includes/banner.md)]

Artikel ini menjelaskan cara membuat kontrak proyek sehingga anda dapat membuat faktur untuk pelanggan, berdasarkan persentase pekerjaan yang diselesaikan. Jumlah faktur akan secara otomatis dihitung untuk kategori anggaran pekerjaan yang Anda atur untuk proyek. Waktu faktur diatur saat Anda menegosiasikan kontrak proyek dengan pelanggan.

Gunakan prosedur dalam artikel ini untuk mengkonfigurasi kontrak, proyek terkait, dan aturan penagihan yang menghitung jumlah faktur untuk kategori anggaran pekerjaan yang anda atur untuk proyek.

Setelah membuat kontrak dan proyek, Anda dapat mengkonfigurasi rincian proyek. Misalnya, Anda dapat menentukan aktivitas dan menetapkan pekerja ke proyek.

## <a name="example"></a>Contoh

Organisasi Anda adalah perusahaan pengembang perangkat lunak. Anda setuju untuk mengembangkan paket akuntansi untuk pelanggan yang memiliki total biaya 20.000 dolar AS (USD). Organisasi Anda setuju untuk menagih pelanggan setelah Anda menyelesaikan persentase spesifik proyek. Anda mengkonfigurasi kategori proyek berikut untuk pekerjaan tersebut, sehingga Anda dapat menggunakannya dalam proses penagihan:

- Konsultasi
- Desain
- Penginstalan

Anda juga menyiapkan aturan penagihan yang menghitung jumlah faktur secara otomatis untuk persentase pekerjaan proyek yang diselesaikan di setiap kategori.

Manajer anggaran membuat anggaran untuk kategori proyek. Jumlah pekerjaan yang diselesaikan secara otomatis dihitung sebagai persentase kerja aktual dibandingkan dengan jumlah yang dianggarkan.

## <a name="prerequisites"></a>Prasyarat

Sebelum membuat proyek yang menggunakan aturan penagihan, Anda harus mengkonfigurasi urutan nomor untuk aturan penagihan dan jurnal biaya yang digunakan untuk memposting tagihan progres.

1. Buka **manajemen proyek dan akuntansi** \> **konfigurasi** \> **parameter manajemen proyek dan akuntansi**.
2. Pada halaman **parameter manajemen proyek dan akuntansi**, pada tab **urutan nomor**, atur urutan nomor yang akan digunakan saat aturan penagihan dibuat.
3. Buka **manajemen proyek dan akuntansi** \> **Jurnal** \> **Ongkos**.
4. Pada halaman **jurnal Ongkos**, pilih **baru**, lalu masukkan nama jurnal.

## <a name="create-a-contract-for-progress-billings"></a>Membuat kontrak untuk tagihan Progress

Gunakan prosedur ini untuk membuat kontrak proyek untuk proyek harga tetap. Anda membuat faktur proyek saat pekerjaan yang diselesaikan pada proyek mencapai persentase tertentu.

1. Buka **manajemen proyek dan akuntansi** \> **Proyek** \> **Kontrak proyek**.
2. Pada halaman **Kontrak Proyek**, pilih **Baru**.
3. Di kotak dialog **kontrak proyek baru**, atur bidang berikut:

    - **Nama**
    - **Jenis pendanaan**
    - **Sumber pendanaan**
    - **Mata uang penjualan** – secara default, mata uang ini digunakan untuk faktur Pelanggan yang terkait dengan kontrak proyek. Namun, Anda dapat mengubah mata uang penjualan pada faktur pelanggan tertentu.

4. Pilih **OK**. Informasi disalin ke header halaman **kontrak proyek**.
5. Di halaman **kontrak proyek**, isi sisa informasi yang diperlukan untuk proyek.

## <a name="create-a-project-for-progress-billings"></a>Membuat proyek untuk tagihan Progress

Ikuti langkah berikut untuk membuat proyek dan subproyek yang terkait dengan kontrak proyek.

1. Buka **manajemen proyek dan akuntansi** \> **proyek** \> **Semua proyek**.
2. Pada halaman **Semua Proyek**, pilih **Baru**.
3. Di kotak dialog **proyek baru**, di bidang **jenis proyek**, pilih **waktu dan material**.
4. Pilih grup proyek. Grup proyek menentukan informasi posting untuk proyek yang ditetapkan ke grup.
5. Pilih **Buat proyek baru**.
6. Setelah proyek dibuat, atur tahapan proyek **dalam proses**.

## <a name="create-a-budget-for-a-project"></a>Membuat anggaran untuk sebuah proyek

Kategori anggaran digunakan untuk secara otomatis menghitung jumlah faktur untuk persentase pekerjaan yang diselesaikan untuk setiap kategori. Ikuti langkah berikut untuk membuat kategori anggaran untuk estimasi biaya.

1. Buka **manajemen proyek dan akuntansi** \> **proyek** \> **Semua proyek**.
2. Pada halaman **semua proyek**, pilih dan buka proyek yang Anda inginkan.
3. Pada halaman **proyek**, di panel tindakan, pada tab **rencana**, di grup **anggaran**, pilih **anggaran proyek**.
4. Di halaman **anggaran proyek**, masukkan perkiraan biaya untuk setiap kategori dalam proyek.

## <a name="create-billing-rules-for-progress-billings"></a>Membuat aturan penagihan untuk Tagihan Progres

1. Buka **manajemen proyek dan akuntansi** \> **Proyek** \> **Kontrak proyek**.
2. Pada halaman **kontrak proyek**, pilih dan buka kontrak proyek.
3. Pada halaman kontrak proyek, pada fasttab **aturan penagihan**, pilih **Tambah**.
4. Pada halaman **aturan penagihan**, di bidang **jenis baris**, pilih **Progres**.
5. Pada fasttab **detail baris aturan penagihan**, di bidang **nilai kontrak**, masukkan nilai total kontrak.
6. Di bidang **kategori**, pilih kategori untuk memposting transaksi ongkos.
7. Di bidang **proyek**, pilih proyek yang menggunakan aturan penagihan ini.
8. Opsional: Tetapkan aturan penagihan ke proyek tambahan. Pada fasttab **proyek**, di Bagian **proyek yang tersedia**, pilih proyek, lalu pilih tombol panah kanan untuk menambahkan proyek ke Bagian **proyek yang dipilih**.
9. Opsional: menghitung jumlah persentase yang dipotong pelanggan dari pembayaran pada faktur. Pada fasttab **ketentuan retensi pembayaran**, pilih sumber pendanaan, lalu di bidang **persentase retensi**, masukkan persentase retensi.
10. Ulangi langkah ini untuk membuat aturan penagihan tambahan untuk kontrak proyek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]