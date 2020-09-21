---
title: Gunakan kategori transaksi sebagai dimensi harga
description: Topik ini menyediakan informasi tentang penggunaan kategori transaksi sebagai dimensi harga.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752506"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Gunakan kategori transaksi sebagai dimensi harga
Topik ini menampilkan cara menggunakan kategori transaksi sebagai dimensi harga. Sebelum memulai, jika Anda belum membuat solusi dimensi harga, Anda harus membuat yang baru. Jika Anda telah memiliki solusi dimensi harga, maka Anda dapat membuat perubahan dalam solusi tersebut. Jika anda belum membuat solusi dimensi harga baru untuk organisasi anda, selesaikan prosedur di topik [buat bidang dan entitas kustom](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Tambah kategori transaksi ke formulir dan tampilan
Untuk membuat kategori transaksi terlihat di UI dalam solusi dimensi harga, Anda harus meninjau semua formulir, dan tampilan entitas utama, dan menambahkan bidang ini ke formulir, dan tampilan entitas tersebut.
Tabel berikut ini adalah daftar lengkap dari tampilan dan formulir bawaan, dicantumkan setiap entitas, yang perlu diperbarui dengan bidang baru. Jika terdapat tampilan tambahan atau formulir dalam penyesuaian Anda pada entitas tersebut, tambahkan bidang baru ke bidang tersebut juga.

|  Entitas        | Formulir     |Tampilan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peran|• Informasi |• Harga Kategori Sumber Daya Aktif<br> • Tampilan Terkait Harga Kategori Sumber Daya|
|  Markup Harga Peran|• Informasi|• Markup Harga Peran Aktif<br>• Tampilan Terkait Markup Harga Peran|
|  Rincian baris kuotasi|• Informasi Proyek<br>• Pembuatan Cepat Proyek|• Rincian Baris Kuotasi Aktif<br>• Gabungan Rincian Baris Kuotasi<br>• Tampilan Terkait Rincian Baris Kuotasi|
|  Rincian Baris Kontrak Proyek|• Informasi Proyek<br>• Pembuatan Cepat Proyek|• Rincian Baris Kontrak Gabungan<br>• Rincian Baris Kontrak Aktif<br>• Tampilan Terkait Rincian Baris Kontrak|
|  Anggota Tim Proyek|• Informasi<br>• Formulir Baru|• Anggota Tim Proyek Aktif<br>• Anggota Tim Proyek<br>• Tampilan Terkait Anggota Tim Proyek|
|  Entri Waktu|• Informasi<br>• Buat Entri Waktu|• Entri Waktu Saya Menurut Tanggal<br>• Entri Waktu Saya untuk pekan Ini<br>• Entri waktu untuk persetujuan|
|  Lini Jurnal|• Informasi<br>• Buat Cepat|• Lini Jurnal Aktif<br>• Tampilan Terkait Lini Jurnal|
|  Rincian Baris Faktur|• Informasi<br>• Buat Cepat|• Rincian Baris Faktur Aktif<br>• Transaksi Faktur yang Dikenakan Biaya<br>• Transaksi Faktur Gratis<br>• Tampilan Terkait Rincian Baris Faktur<br>• Transaksi Faktur yang Tidak Dikenakan Biaya|
|  Aktual|• Informasi<br>• Aktual Aktif|• Tampilan Terkait Aktual|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Konfigurasi kategori transaksi sebagai dimensi harga

1. Di antarmuka web , buka **Project Service** > **Pengaturan** > **Parameters**. 
2. Pada halaman **parameter**, pada tab **Dimensi harga berbasis jumlah**, perhatikan bahwa kisi pada tab menampilkan rekaman di entitas **dimensi harga**.
3. Tambah **kategori transaksi** ke daftar ini dan atur bidang **berlaku untuk biaya** dan **berlaku untuk penjualan** diatur ke **ya**.
4. Di bidang **jenis dimensi**, pilih **berdasarkan jumlah**, lalu pilih prioritas untuk **kategori transaksi** yang terkait dengan biaya dan penjualan.
