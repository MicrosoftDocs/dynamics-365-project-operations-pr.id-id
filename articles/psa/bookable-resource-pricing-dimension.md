---
title: Gunakan sumber daya yang dapat dipesan sebagai dimensi harga
description: Topik ini menyediakan informasi tentang penggunaan sumber daya yang dapat dipesan sebagai dimensi harga.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d9b25a768f892d83c09d37ce76291d6c8e75b1be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145002"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Gunakan sumber daya yang dapat dipesan sebagai dimensi harga

[!include [banner](../includes/psa-now-project-operations.md)]

Topik ini menyediakan informasi tentang penggunaan sumber daya yang dapat dipesan sebagai dimensi harga. Sebelum memulai, jika Anda belum membuat solusi dimensi harga, Anda harus membuat yang baru. Jika Anda telah memiliki solusi dimensi harga, maka Anda dapat membuat perubahan dalam solusi tersebut. Jika anda belum membuat solusi dimensi harga baru untuk organisasi anda, selesaikan prosedur di topik [buat bidang dan entitas kustom](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Tambah sumber daya yang dapat dipesan untuk formulir dan tampilan
Untuk membuat bidang terlihat di UI dalam solusi dimensi harga, Anda harus meninjau semua formulir, dan tampilan entitas Project Service utama, dan menambahkan bidang ini ke formulir, dan tampilan entitas tersebut.
Tabel berikut ini adalah daftar lengkap dari tampilan dan formulir bawaan, yang didaftarkan oleh entitas, yang perlu diperbarui. Jika terdapat tampilan tambahan atau formulir dalam penyesuaian Anda pada entitas tersebut, tambahkan bidang baru ke bidang tersebut juga.
Buka penelusur solusi untuk solusi dimensi harga, lalu klik **publikasikan semua penyesuaian**.


|   Entitas        | Formulir   |Tampilan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peran|• Informasi |• Harga Kategori Sumber Daya Aktif<br> • Tampilan Terkait Harga Kategori Sumber Daya|
|  Markup Harga Peran|• Informasi|• Markup Harga Peran Aktif<br>• Tampilan Terkait Markup Harga Peran|
|  Rincian baris kuotasi|• Informasi Proyek<br>• Pembuatan Cepat Proyek|• Rincian Baris Kuotasi Aktif<br>• Gabungan Rincian Baris Kuotasi<br>• Tampilan Terkait Rincian Baris Kuotasi|
|  Rincian Baris Kontrak Proyek|• Informasi Proyek<br>• Pembuatan Cepat Proyek|• Rincian Baris Kontrak Gabungan<br>• Rincian Baris Kontrak Aktif<br>• Tampilan Terkait Rincian Baris Kontrak|
|  Tugas Proyek|• Informasi<br>• Formulir Baru||
|  Anggota Tim Proyek|• Informasi<br>• Formulir Baru|• Anggota Tim Proyek Aktif<br>• Anggota Tim Proyek<br>• Tampilan Terkait Anggota Tim Proyek|
|  Entri Waktu|• Informasi<br>• Buat Entri Waktu|• Entri Waktu Saya Menurut Tanggal<br>• Entri Waktu Saya untuk pekan Ini<br>• Entri waktu untuk persetujuan|
|  Lini Jurnal|• Informasi<br>• Buat Cepat|• Lini Jurnal Aktif<br>• Tampilan Terkait Lini Jurnal|
|  Rincian Baris Faktur|• Informasi<br>• Buat Cepat|• Rincian Baris Faktur Aktif<br>• Transaksi Faktur Kena Biaya<br>• Transaksi Faktur Gratis<br>• Tampilan Terkait Rincian Baris Faktur<br>• Transaksi Faktur Tidak Kena Biaya|
|  Aktual|• Informasi<br>• Aktual Aktif|• Tampilan Terkait Aktual|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Konfigurasi sumber daya yang dapat dipesan sebagai dimensi harga

1. Di antarmuka web , buka **Project Service** > **Pengaturan** > **Parameters**. Pada halaman **parameter**, pada tab **Dimensi harga berbasis jumlah**, perhatikan bahwa kisi pada tab menampilkan rekaman di entitas dimensi harga. 
2. Tambahkan **sumber daya yang dapat dipesan** ke daftar dimensi harga sebagai **msdyn_bookableresource**. 
3. Tentukan konteks sumber daya yang dapat dipesan berfungsi sebagai dimensi harga dan atur nilai **berlaku untuk biaya** dan **berlaku untuk penjualan**.
4. Di bidang **jenis dimensi**, pilih **berdasarkan jumlah**. 
5. Pilih prioritas biaya dan penjualan untuk sumber daya yang dapat dipesan. Biasanya, bila tercakup sebagai dimensi harga, sumber daya yang dapat dipesan memiliki prioritas tertinggi sehingga pengaturan ini menjadi **1** (atau **0** tergantung pada cara Anda menghitung prioritas) akan memastikan perilaku tersebut.

## <a name="set-up-pricing-dimension-field-names"></a>Konfigurasi Nama Bidang Dimensi Harga

Bila nama bidang dari dimensi harga pada tabel **peran harga** berbeda dari nama bidang di entitas lain di mana default harga harus berfungsi, rekaman dimensi harga harus dibuat sadar akan nama yang berbeda.    
Untuk sumber daya yang dapat dipesan, entitas **anggota tim proyek** memiliki nama bidang yang sedikitberbeda(**msdyn_bookableresourceid**) dari apa yang disebut pada entitas **harga peran** (**msdyn_ bookableresource**). Rekaman dimensi harga untuk **msydn_bookableresource** harus dibuat mengetahui hal ini. 
1. Untuk melakukannya, klik dua kali baris di kisi **dimensi harga** untuk membuka halaman dimensi **msdyn_bookableresource**.
2. Pada halaman dimensi, pada tab **terkait**, klik **nama bidang dimensi harga**.

 ![Tab Nama Bidang Dimensi Harga](media/PD-fieldname.png)

4. Pada tampilan terkait yang terbuka, klik **Tambah nama bidang dimensi harga baru**.

 ![Tambahkan Nama Bidang Dimensi Harga](media/Add-NewPD-fieldname.png)


Ini akan membuka halaman **nama bidang dimensi harga baru** untuk **msdyn_bookableresource**. 

5. Tambahkan **msdyn_projectteam** ke bidang **nama logis entitas** dan **msdyn_bookableresourceid** ke bidang **nama bidang**. Simpan rekaman ini.

 ![Formulir Nama Bidang Dimensi Harga Baru](media/PD-fieldname-Added.png)
