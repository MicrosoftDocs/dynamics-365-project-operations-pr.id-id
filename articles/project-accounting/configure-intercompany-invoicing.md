---
title: Mengonfigurasikan faktur antarperusahaan
description: Topik ini berisi informasi dan contoh tentang cara mengonfigurasi faktur antarperusahaan untuk berbagai proyek.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ad6022670048e5aa3635998852b78c49af461d4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591592"
---
# <a name="configure-intercompany-invoicing"></a>Mengonfigurasikan faktur antarperusahaan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Lakukan langkah-langkah berikut untuk menyiapkan faktur antarperusahaan untuk proyek di Dynamics 365 Project Operations. Transaksi antarperusahaan adalah transaksi waktu dan pengeluaran dari kontrak proyek milik satu perusahaan atau unit organisasi, sedangkan sumber daya pada kontrak proyek adalah bagian dari perusahaan atau unit organisasi yang berbeda.

## <a name="example-configure-intercompany-invoicing"></a>Contoh: Mengonfigurasikan faktur antarperusahaan

Pada contoh berikut, Contoso Robotics USA (USPM) adalah entitas hukum yang meminjam dan Contoso Robotics UK (GBPM) adalah entitas hukum pemberi pinjaman. 

1. **Konfigurasikan akuntansi antarperusahaan di antara beberapa entitas hukum**. Setiap pasangan entitas hukum peminjam dan pemberi pinjaman harus dikonfigurasi pada halaman [Akuntansi antarperusahaan](/dynamics365/finance/general-ledger/intercompany-accounting-setup) buku besar.
    
    1. Di Dynamics 365 Finance, buka **Pengaturan** > **Posting Buku Besar** > **Umum Akuntansi antar perusahaan**. Buat record dengan informasi berikut:

        - **Perusahaan asal** = **GBPM**
        - **Perusahaan tujuan** = **USPM**

2. **Konfigurasikan hubungan dagang di antara entitas hukum**. Record pelanggan yang mewakili entitas hukum peminjam harus dibuat di entitas hukum pemberi pinjaman. Record vendor yang mewakili entitas hukum peminjam harus dibuat di entitas hukum pemberi pinjaman.

     1. Di Keuangan, pilih entitas hukum **GBPM**.
     2. Buka **Piutang dagang** > **Pelanggan** > **Semua pelanggan**. Buat catatan baru untuk entitas hukum, **USPM**.
     3. Perluas **Nama**, filter record berdasarkan **Jenis**, lalu pilih **Entitas hukum**. 
     4. Cari dan pilih record pelanggan untuk **Contoso Robotics USA (USPM)**.
     5. Pilih **Gunakan pencocokan**. 
     6. Pilih grup pelanggan **50 - Pelanggan antarperusahaan**, lalu simpan rekaman.
     7. Pilih entitas hukum **USPM**.
     8. Buka **Utang dagang** > **Vendor** > **Semua vendor**. Buat record baru untuk entitas hukum, **GBPM**.
     9. Perluas **Nama**, filter record berdasarkan **Jenis**, lalu pilih **Entitas hukum**. 
     10. Cari dan pilih record pelanggan untuk **Contoso Robotics UK (GBPM)**.
     11. Pilih **Gunakan pencocokan**, pilih grup vendor, lalu simpan record.
     12. Di record vendor, pilih **Umum** > **Konfigurasi** > **Antarperusahaan**.
     13. Di tab **Hubungan dagang**, atur **Aktif** ke **Ya**.
     14. Atur bidang **perusahaan pelanggan** ke **GBPM** dan di **rekaman akun Saya**, pilih rekaman pelanggan yang Anda buat sebelumnya dalam prosedur.

3. **Konfigurasikan pengaturan antarperusahaan dalam parameter manajemen proyek dan akuntansi Proyek**. 

    1. Pilih entitas hukum **USPM** dan buka **Manajemen dan akuntansi proyek** > **Pengaturan** > **Parameter manajemen dan akuntansi proyek**.
    2. Di tab **Antarperusahaan**, pilih kategori pengadaan untuk mencocokkan faktur vendor yang dibuat secara otomatis.
    3. Di **Kategori default**, pilih **Sumber daya antarperusahaan**.
    4. Pilih entitas hukum **GBPM** dan buka **Manajemen dan akuntansi proyek** > **Pengaturan** > **Parameter manajemen dan akuntansi proyek**.
    5. Di tab **Antarperusahaan**, pilih kategori proyek default untuk setiap jenis transaksi. Kategori proyek digunakan untuk konfigurasi pajak bila kategori yang ditagih dalam transaksi antarperusahaan hanya ada di entitas hukum yang meminjam. Anda dapat memilih untuk mengakumulasikan pendapatan untuk transaksi antarperusahaan. Penambahan terjadi saat transaksi diposting melalui jurnal Integrasi Project Operations di entitas hukum pemberi pinjaman. Jurnal dikembalikan saat faktur antarperusahaan diposting.
    6. Di grup **Saat sumber daya pemberi pinjaman**, pilih **...** > **Baru**. 
    7. Di kisi, pilih informasi berikut:

          - **Entitas hukum peminjam** = **USPM**
          - **Pendapatan akrual** = **Ya**
          - **Kategori lembar waktu default** = **Default – Jam**
          - **Kategori pengeluaran default** = **Default – pengeluaran**

4. **Atur akun pendapatan dan biaya antarperusahaan di pengaturan posting buku besar**. Akun pendapatan antarperusahaan dikreditkan apabila faktur pelanggan antarperusahaan diposting di entitas hukum pemberi pinjaman. Akun biaya antarperusahaan didebit apabila faktur vendor tertunda yang sesuai diposting di entitas hukum peminjam. Akun ini diatur di entitas hukum yang sesuai. 
      
     1. Di Keuangan, pilih entitas bisnis peminjam **USPM**. 
     2. Buka **Manajemen dan akuntansi proyek** > **Pengaturan** > **Posting** > **Pengaturan posting buku besar**. 
     3. Di tab **Akun biaya**, di **Jenis akun buku besar**, pilih **Biaya antarperusahaan**. Buat record baru dengan informasi berikut:
      
        - **Entitas hukum pemberi peminjam** = **GBPM**
        - **Akun utama** = Pilih akun utama untuk biaya antarperusahaan. Konfigurasi ini wajib diisi. Konfigurasi digunakan untuk alur interperusahaan di Finance, tetapi tidak pada alur interperusahaan terkait proyek. Pilihan ini tidak memiliki dampak hilir. 
        
     4. Pilih entitas hukum pemberi pinjaman, **GBPM**. 
     5. Buka **Manajemen dan akuntansi proyek** > **Pengaturan** > **Posting** > **Pengaturan posting buku besar**. 
     6. Di tab **Akun pendapatan**, di **Jenis akun buku besar**, pilih **Pendapatan antarperusahaan**. Buat record baru dengan informasi berikut:

        - **Entitas hukum peminjam** = **USPM**
        - **Akun utama** = Pilih akun utama untuk pendapatan antarperusahaan. Konfigurasi ini wajib diisi. Konfigurasi digunakan untuk alur interperusahaan di Finance, tetapi tidak pada alur interperusahaan terkait proyek. Pilihan ini tidak memiliki dampak hilir. 

5. **Konfigurasikan harga transfer untuk tenaga kerja**. Harga transfer antarperusahaan dikonfigurasi di Project Operations pada Dataverse. Konfigurasikan [tingkat biaya tenaga kerja](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) dan [tingkat tagihan tenaga kerja](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) untuk faktur antarperusahaan. Harga transfer tidak didukung untuk transaksi pengeluaran antarperusahaan. Harga jual unit antarorganisasi akan selalu diatur ke nilai yang sama dengan harga biaya unit sumber daya.

      Biaya sumber daya pengembang di Contoso Robotics UK adalah 88 GBP per jam. Contoso Robotics UK akan menagih Contoso Robotics USA sebesar 120 USD untuk setiap jam bekerja sumber daya ini di proyek AS. Contoso Robotics USA akan menagih Adventure Works pelanggan sebesar 200 USD untuk pekerjaan yang dilakukan oleh sumber daya pengembang Contoso Robotics UK.

      1. Di Project Operations pada Dataverse, buka **Penjualan** > **Daftar harga**. Buat daftar harga biaya baru yang disebut **Tarif biaya Contoso Robotics UK.** 
      2. Di daftar harga biaya, buat record dengan informasi berikut:
         - **Peran** = **Pengembang**
         - **Biaya** = **88 GBP**
      3. Buka **Pengaturan** > **Unit organisasi** dan lampirkan daftar harga biaya ke unit organisasi **Contoso Robotics UK**.
      4. Buka **Penjualan** > **Daftar harga**. Buat daftar harga biaya yang disebut **Tarif biaya Contoso Robotics USA**. 
      5. Di daftar harga biaya, buat record dengan informasi berikut:
          - **Peran** = **Pengembang**
          - **Perusahaan sumber daya** = **Contoso Robotics UK**
          - **Biaya** = **120 USD**
      6. Buka **Pengaturan** > **Unit organisasi** dan lampirkan daftar harga biaya **tarif biaya Contoso Robotics UK** ke unit organisasi **Contoso Robotics USA**.
      7. Buka **Penjualan** > **Daftar harga**. Buat daftar harga penjualan yang disebut **Tarif tagihan Adventure Works**. 
      8. Di daftar harga penjualan, buat record dengan informasi berikut:
          - **Peran** = **Pengembang**
          - **Perusahaan sumber daya** = **Contoso Robotics UK**
          - **Tarif tagihan** = **200 USD**
      9. Buka **Penjualan** > **Kontrak proyek** dan lampirkan **Tarif tagihan Adventure Works** ke daftar harga proyek Adventure Works dari kontrak proyek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
