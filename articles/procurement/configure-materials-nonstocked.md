---
title: Mengkonfigurasi bahan non-stok dan faktur vendor tertunda
description: Laporan topik menjelaskan cara mengaktifkan bahan non-stok dan faktur vendor tertunda.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592972"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Mengkonfigurasi bahan non-stok dan faktur vendor tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

## <a name="minimum-version-requirement"></a>Persyaratan versi minimum

Menggunakan bahan non-stok dan faktur vendor tertunda untuk skenario berbasis non-stok/sumber daya Dynamics 365 Project Operations memerlukan versi berikut:

Solusi Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 atau lebih tinggi
- Solusi orkestrasi aplikasi penulisan ganda - 2.2.2.23 atau lebih tinggi

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) atau yang lebih tinggi. Pastikan lingkungan Finance Anda sudah terkini dan semua pembaruan kualitas diterapkan untuk memenuhi persyaratan versi minimum.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Jalankan peta penulisan ganda untuk materi non-stok dan integrasi faktur vendor

Bagian ini memberikan informasi tentang peta tertentu yang diperlukan untuk bahan non-stok dan faktur vendor. Pastikan peta prasyarat yang terdaftar di topik [Penyediaan lingkungan baru](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) berjalan pada lingkungan Anda.

1. Buka Lifecycle Services (LCS), navigasi ke proyek LCS, dan buka halaman **rincian Lingkungan**.
2. Di bagian **Informasi Lingkungan Common Data Service**, pilih **Tautkan ke CDS for Apps**. Setelah memilih tautan, Anda akan diarahkan ke daftar entitas di pemetaan.
3. Pastikan peta berikut berjalan. Jika tidak dijalankan, mulai dan pastikan untuk menyertakan semua peta tabel terkait.

    - CDS merilis produk (produk-produk) yang berbeda
    - Vendor v2 (msdyn_vendors)
    - Tabel Project Operations untuk estimasi bahan (msdyn_estimatelines)
    - Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices)
    - Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoicelines)
    - Aktual Integrasi Project Operations (msdyn_actuals). Pastikan Anda menjalankan versi peta 1.0.0.14 atau lebih tinggi. Anda dapat melihat versi aktif peta pada kolom **Versi** pada halaman **Penulisan Ganda**. Anda dapat mengaktifkan versi baru peta dengan memilih **versi Peta tabel** dan kemudian menyimpan versi yang dipilih.

Jika menggunakan data demo standar, Anda juga mungkin harus berhenti dan memulai ulang peta entitas berikut dengan sinkronisasi awal:
  - Hari pembayaran CDS V2 (msdyn_paymentdays)
  - Jadwal pembayaran (msdyn_paymentschedules)
  - Persyaratan pembayaran (msdyn_paymentterms)
  - Grup vendor (msdyn_vendorgroups)
  - Satuan (uom)

> [!NOTE]
> Sinkronisasi awal untuk grup dan unit vendor mungkin gagal untuk beberapa rekaman dalam demo himpunan data yang ada. Anda dapat mengabaikan kegagalan karena kegagalan tidak akan mencegah Anda menggunakan data demo dengan Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Mengonfigurasikan prasyarat di Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Mengaktifkan alur kerja untuk membuat akun berdasarkan entitas vendor

Solusi Orkestrasi Penulisan Ganda menyediakan [integrasi induk Vendor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Sebagai prasyarat untuk fitur ini, data vendor harus dibuat di entitas **Akun**. Aktifkan proses alur kerja template untuk membuat vendor dalam tabel **Akun** seperti dijelaskan dalam [Beralih di antara desain vendor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Atur produk untuk dibuat sebagai aktif

Materi yang tidak memiliki persediaan harus dikonfigurasi sebagai **produk yang dirilis** di Finance. Solusi Orkestrasi Penulisan Ganda menyediakan [integrasi produk yang dirilis ke katalog produk Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping) default. Secara default, produk dari Finance disinkronisasikan ke Dataverse dalam status draf. Untuk mensinkronisasi produk ke status aktif sehingga dapat langsung digunakan dalam dokumen penggunaan bahan atau faktur vendor tertunda, buka **Sistem** > **Administrasi** > **Administrasi Sistem** > **Pengaturan sistem**, dan pada tab **Penjualan**, atur **Buat produk dalam status aktif** ke **Ya**.

## <a name="configure-prerequisites-in-finance"></a>Mengonfigurasikan prasyarat di Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Aktifkan kunci fitur untuk faktur vendor tertunda

Selesaikan langkah-langkah berikut untuk mengaktifkan fungsi untuk menambahkan rincian proyek pada baris faktur vendor tertunda.

1. Di Finance, buka ruang kerja **Manajemen Fitur**.
2. Dalam daftar fitur, cari fitur **Aktifkan faktur vendor tertunda pada Project Operations untuk skenario berbasis sumber daya/non-persediaan** dan pilih **Aktifkan**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Mendefinisikan grup kategori dan kategori proyek untuk item

Konfigurasikan minimal satu grup kategori untuk jenis transaksi **Item**, dan minimal satu kategori proyek menggunakan grup ini. Untuk informasi selengkapnya, lihat [Mengonfigurasi kategori proyek](../project-accounting/configure-project-categories.md#category-groups).

Periksa profil biaya dan pendapatan proyek, dan konfigurasi pengaturan posting buku besar untuk transaksi item. Untuk informasi lebih lanjut, lihat [Mengkonfigurasi akuntansi untuk proyek yang dapat ditagih](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Atur Produk Pilihan

Dalam Project Operations, Anda dapat merekam estimasi bahan dan penggunaan untuk produk katalog yang dikonfigurasi dalam katalog produk yang dirilis dan untuk produk pilihan. Menggunakan produk pilihan memerlukan satu produk rilis yang dikonfigurasi di Finance untuk tujuan ini. Selesaikan langkah-langkah berikut untuk mengkonfigurasi produk pilihan. Ulangi langkah-langkah ini di setiap entitas hukum yang menggunakan Project Operations untuk skenario sumber daya/non-persediaan.

1. Di Keuangan, buka **Manajemen Informasi Produk** > **produk** > **Produk yang dirilis** dan pilih **Baru**.
2. Di bidang **Jenis produk**, pilih **Item** dan pada bidang **subtipe Produk**, pilih **Produk**.
3. Masukkan nomor produk (WRITEIN) dan nama produk (Produk Pilihan).
4. Pilih grup model item. Pastikan bahwa grup model item yang Anda pilih memiliki bidang **produk dalam persediaan kebijakan Inventaris** yang diatur ke **Salah**.
5. Pilih nilai di **grup Item**, **grup dimensi penyimpanan**, dan Bidang **grup dimensi pelacakan**. Gunakan **dimensi Penyimpanan** hanya untuk **Situs**, dan di bidang **Dimensi pelacakan**, pilih **Tidak Ada**.
6. Pilih nilai di bidang **unit Inventaris**, **Unit pembelian**, dan **unit Penjualan**, kemudian simpan perubahan Anda.
7. Pada tab **Rencana**, atur pengaturan urutan default, dan pada tab **Inventaris**, atur situs default dan pergudangan.
8. Buka **Manajemen proyek dan akuntansi** > **Konfigurasi** > **Parameter Manajemen Proyek dan akuntansi**, lalu buka **Project Operations di Dynamics 365 Dataverse**. 
9. Pada tab **Bahan**, di bidang **produk Pilihan**, pilih produk yang Anda buat.
10. Di lingkungan Dataverse Anda, di peta situs, buka entitas **Produk** dan cari rekaman produk pilihan. 
11. Buka rincian rekaman dan atur status produk ke **Pensiun**. Kondisi produk ini mencegah siapa pun tidak sengaja menggunakan rekaman ini secara langsung dalam estimasi materi dan dokumen penggunaan.

### <a name="set-up-a-procurement-integration-account"></a>Mengkonfigurasi akun integrasi pengadaan

Akun integrasi akuisi pengadaan digunakan sebagai akun klikring ketika memposting faktur vendor tertunda dengan baris yang dikaitkan ke proyek.

Ketika sistem memposting faktur vendor tertunda, akun ini digunakan untuk jumlah biaya proyek. Rincian faktur vendor diproses di Dataverse dan aktual proyek terkait dibuat. Informasi dari proyek yang sebenarnya ditambahkan ke jurnal Integrasi Project Operations. Saat Anda memposting jurnal integrasi, jumlah tersebut akan dihapus dari akun integrasi pembelian dan dicatat ke biaya proyek.

1. Untuk mengonfigurasikan akun integrasi pengadaan, buka **Manajemen proyek dan akuntansi** > **Konfigurasi** > **Parameter Manajemen Proyek dan akuntansi**, lalu buka **Project Operations di Dynamics 365 Dataverse**. 
2. Pilih tab **Bahan**, lalu pilih nilai dalam bidang **akun integrasi pengadaan**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Konfigurasikan default kategori proyek untuk item

1. Di Finance, buka **Manajemen proyek dan akuntansi** > **Konfigurasi** > **Parameter Manajemen Proyek dan akuntansi**, lalu buka **Project Operations di Dynamics 365 Dataverse**. 
2. Pada tab **default kategori Proyek**, di bidang **Item**, pilih nilai. Kategori proyek ini digunakan untuk transaksi bahan jika kategori proyek tidak diatur pada rekaman aktual proyek.
