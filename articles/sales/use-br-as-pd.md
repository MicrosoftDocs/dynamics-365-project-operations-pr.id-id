---
title: Menggunakan sumber daya yang dapat dipesan sebagai dimensi harga
description: Artikel ini menyediakan informasi tentang cara menggunakan sumber daya yang dapat dipesan sebagai dimensi harga.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c467c45885bbd8931eccc75862f537c0f46433ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914820"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Menggunakan sumber daya yang dapat dipesan sebagai dimensi harga

 _**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_ 

Artikel ini menyediakan informasi tentang cara menggunakan sumber daya yang dapat dipesan sebagai dimensi harga. Jika strategi penetapan harga diatur sedemikian rupa sehingga setiap sumber daya yang dapat dipesan harus memiliki harga atau tarif biaya tertentu, gunakan sumber daya yang dapat dipesan sebagai dimensi harga.

## <a name="prerequisites"></a>Prasyarat
Sebelum menyelesaikan prosedur di artikel ini, Anda harus memiliki solusi dimensi harga baru untuk organisasi Anda. Jika Anda belum membuatnya, lihat [Membuat bidang dan entitas kustom](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Menambahkan bidang Sumber Daya yang Dapat Dipesan untuk formulir dan tampilan
Agar bidang **Sumber Daya yang Dapat Dipesan** terlihat di solusi dimensi harga, Anda harus menambahkan bidang ke semua formulir dan tampilan sebagai entitas.

Tabel berikut mencantumkan semua formulir dan tampilan siap pakai, berdasarkan entitas. Anda juga harus menambahkan bidang baru pada formulir atau tampilan tambahan di entitas yang disesuaikan.

|   Entity        | Formlir   |Tampilan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peran| Informasi | - Harga Kategori Sumber Daya Aktif<br> - Terkait Harga Kategori Sumber Daya |
|  Markup Harga Peran| Informasi| - Markup Harga Peran Aktif<br>- Terkait Markup Harga Peran |
|  Rincian baris kuotasi| - Informasi Proyek<br>- Pembuatan Cepat Proyek| - Rincian Baris Kuotasi Aktif<br>- Gabungan Rincian Baris Kuotasi<br>- Terkait Rincian Baris Kuotasi |
|  Rincian Baris Kontrak Proyek| - Informasi Proyek<br>- Pembuatan Cepat Proyek| - Rincian Baris Kontrak Gabungan<br>- Rincian Baris Kontrak Aktif<br>- Terkait Rincian Baris Kontrak |
|  Tugas Proyek| - Informasi<br>- Formulir Baru| &nbsp; |
|  Anggota Tim Proyek| - Informasi<br>- Formulir Baru| - Anggota Tim Proyek Aktif<br>- Anggota Tim Proyek<br>- Terkait Anggota Tim Proyek |
|  Entri Waktu| - Informasi<br>- Buat Entri Waktu| - Entri Waktu Saya Menurut Tanggal<br>- Entri Waktu Saya untuk Pekan Ini<br>- Entri Waktu untuk Persetujuan|
|  Lini Jurnal| - Informasi<br>- Buat Cepat| - Lini Jurnal Aktif<br>- Terkait Lini Jurnal |
|  Rincian Baris Faktur| - Informasi<br>- Buat Cepat| - Rincian Baris Faktur Aktif<br>- Transaksi Faktur Kena Biaya<br>- Transaksi Faktur Gratis<br>- Terkait Rincian Baris Faktur <br>- Transaksi Faktur Tidak Kena Biaya|
|  Aktual| - Informasi<br>- Aktual Aktif| Aktual Terkait |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Mengonfigurasikan sumber daya yang dapat dipesan sebagai dimensi harga
Untuk mengonfigurasikan sumber daya yang dapat dipesan sebagai dimensi harga, ikuti langkah-langkah berikut:

1. Buka **Pengaturan** > **Parameter**. 
2. Pada halaman **Parameter**, di tab **Dimensi Harga Berbasis Jumlah**, pastikan kisi menampilkan record di entitas **Dimensi Harga**. 
2. Tambahkan **sumber daya yang dapat dipesan** ke daftar dimensi harga sebagai **msdyn_bookableresource**. 
3. Di **Berlaku untuk biaya** dan **Berlaku untuk penjualan**, pilih nilai.
4. Di **Jenis Dimensi**, pilih **Berbasis jumlah**. 
5. Pilih prioritas biaya dan penjualan untuk sumber daya yang dapat dipesan. Biasanya, sumber daya yang dapat dipesan memiliki prioritas tertinggi saat disertakan sebagai dimensi harga. Tetapkan prioritas ke **1** (atau **0** tergantung pada cara Anda menghitung prioritas) untuk memastikan perilaku ini.

## <a name="set-up-pricing-dimension-field-names"></a>Konfigurasi Nama Bidang Dimensi Harga

Apabila nama bidang dimensi harga pada tabel **Harga Peran** berbeda dari nama bidang di entitas lain di mana harga default digunakan, record dimensi harga harus dibuat mengetahui perbedaan nama tersebut.  

Untuk sumber daya yang dapat dipesan, entitas **Anggota Tim Proyek** memiliki nama bidang yang sedikit berbeda dengan yang disebut di entitas **Harga Peran**: 

 - Entitas **Anggota Tim Proyek** = **msdyn_bookableresourceid**
 - Entitas **Harga Peran** = **msdyn_bookableresource**

Record dimensi harga untuk **msydn_bookableresource** harus dibuat mengetahui perbedaan ini.

1. Klik dua kali baris di kisi **Dimensi Harga** untuk membuka halaman dimensi **msdyn_bookableresource**.
2. Pada halaman dimensi, pada tab **terkait**, pilih **Nama Bidang Dimensi Harga**.

  ![Tab Nama Bidang Dimensi Harga.](media/PD-fieldname.png)

3. Pada tampilan terkait yang terbuka, pilih **Tambahkan Nama Bidang Dimensi Harga Baru**.

  ![Tambahkan Nama Bidang Dimensi Harga.](media/Add-NewPD-fieldname.png)

  Ini akan membuka halaman **nama bidang dimensi harga baru** untuk **msdyn_bookableresource**. 

4. Pada halaman **Nama Bidang Dimensi Harga Baru**, tambahkan **msdyn_projectteam** ke **Nama Logik Entitas**.
5. Tambahkan **msdyn_bookableresourceid** ke **Nama Bidang**.

 ![Formulir Nama Bidang Dimensi Harga Baru.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]