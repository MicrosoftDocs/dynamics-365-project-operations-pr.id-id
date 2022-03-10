---
title: Menautkan aktual ke rekaman asli
description: Laporan topik menjelaskan cara menautkan aktual ke rekaman asli seperti entri waktu, entri pengeluaran, atau log penggunaan bahan.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991760"
---
# <a name="link-actuals-to-original-records"></a>Menautkan aktual ke rekaman asli

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Di Dynamics 365 Project Operations, *transaksi bisnis* adalah konsep abstrak yang tidak diwakili oleh entitas. Namun, beberapa bidang dan proses umum pada entitas dirancang untuk menggunakan konsep transaksi bisnis. Entitas berikut ini menggunakan konsep ini:

- Rincian Baris Kuotasi
- Rincian Baris Kontrak
- Baris Perkiraan
- Lini Jurnal
- Aktual

Dari entitas ini, **rincian baris kuotasi**, **rincian baris kontrak**, dan **baris estimasi,** dipetakan ke fase estimasi dalam siklus hidup proyek. **Baris jurnal** dan **entitas aktual** dipetakan ke fase eksekusi dalam siklus hidup proyek.

Project Operations mengenali rekaman dalam lima entitas ini sebagai transaksi bisnis. Satu-satunya perbedaan adalah bahwa rekaman dalam entitas yang dipetakan ke fase estimasi dianggap sebagai perkiraan keuangan, sedangkan rekaman dalam entitas yang dipetakan ke fase eksekusi dianggap sebagai fakta keuangan yang telah terjadi.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi bisnis
Konsep berikut ini unik untuk konsep transaksi bisnis:

- Jenis Transaksi
- Kelas Transaksi
- Asal transaksi
- Koneksi Transaksi

### <a name="transaction-type"></a>Jenis Transaksi

Jenis transaksi menunjukkan waktu dan konteks dampak keuangan pada suatu proyek. Ini diwakili oleh rangkaian pilihan yang memiliki nilai yang didukung berikut di Project Operations:

  - Biaya
  - Kontrak proyek
  - Penjualan Belum Tertagih
  - Penjualan yang Ditagih
  - Penjualan Antar-organisasi
  - Biaya Unit Sumber Daya

### <a name="transaction-class"></a>Kelas Transaksi

Kelas transaksi mewakili jenis biaya yang berbeda yang dikeluarkan pada proyek. Ini diwakili oleh rangkaian pilihan yang memiliki nilai yang didukung berikut di Project Operations:

  - Waktu
  - Pengeluaran
  - Materi
  - Biaya
  - Tahap
  - Pajak

**Tonggak waktu** biasanya digunakan oleh logika bisnis untuk penagihan harga tetap di Project Operations.

### <a name="transaction-origin"></a>Asal transaksi

**Asal transaksi** adalah entitas yang menyimpan asal dari setiap transaksi bisnis. Saat proyek berjalan, setiap transaksi bisnis akan menghasilkan transaksi bisnis lain yang pada gilirannya akan membuat transaksi lain dan seterusnya. Entitas asal transaksi dirancang untuk menyimpan data tentang setiap asal transaksi untuk membantu pelaporan dan keterlacakan. 

### <a name="transaction-connection"></a>Koneksi Transaksi

**Koneksi transaksi** adalah entitas yang menyimpan relasi antara dua transaksi bisnis serupa, seperti aktual biaya dan penjualan yang terkait, atau pembalikan transaksi yang dipicu oleh aktivitas penagihan seperti konfirmasi faktur atau koreksi faktur.

Bersama-sama, **asal transaksi** dan **koneksi transaksi** membantu Anda terus melacak Relasi antara transaksi bisnis dan tindakan yang menyebabkan transaksi bisnis tertentu.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Contoh: cara kerja asal transaksi dengan koneksi transaksi

Contoh berikut menunjukkan pemrosesan tipikal waktu entri dalam siklus hidup proyek Project Operations.

> ![Waktu pemrosesan entri dalam siklus hidup Project Service.](media/basic-guide-17.png)
 
1. Pengajuan entri waktu membuat dua baris jurnal: satu baris untuk biaya dan satu baris untuk penjualan yang belum ditagih.
2. Persetujuan akhir entri waktu membuat dua aktual: satu aktual untuk biaya dan satu aktual untuk penjualan yang belum ditagih.
3. Saat faktur proyek baru dibuat, transaksi baris faktur dibuat menggunakan data dari nilai aktual penjualan yang belum ditagih. 
4. Setelah faktur dikonfirmasi, dua aktual baru dibuat: aktual pembalikan penjualan yang belum ditagih dan aktual penjualan tertagih.

Setiap aktivitas ini membuat rekaman di entitas **asal Transaksi** dan **koneksi Transaksi**. Rekaman baru ini membantu membuat riwayat Relasi antara rekaman yang dibuat di seluruh entri waktu, baris jurnal, aktual, dan rincian baris faktur.

Tabel berikut Menampilkan rekaman di entitas **asal transaksi** untuk alur kerja.

| Aktivitas                        | Asal                   | Jenis Asal                       | Transaksi                       | Jenis transaksi         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Pengajuan entri waktu        | GUID Rekaman Entri Waktu   | Entri Waktu                        | GUID Rekaman baris jurnal (biaya)   | Lini Jurnal             |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman baris jurnal (penjualan)  | Lini Jurnal                      |                          |
| Persetujuan Waktu                | GUID Rekaman baris jurnal | Lini Jurnal                      | GUID Rekaman Penjualan Belum Tertagih        | Aktual                   |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman Penjualan Belum Tertagih        | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Rekaman Aktual Biaya           | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman Aktual Biaya           | Aktual                            |                          |
| Pembuatan Faktur             | GUID Rekaman Entri Waktu   | Entri Waktu                        | GUID Transaksi Baris Faktur     | Transaksi Baris Faktur |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Transaksi Baris Faktur     | Transaksi Baris Faktur          |                          |
| Konfirmasi Faktur         | GUID Baris Faktur        | Baris Faktur                      | GUID Rekaman Penjualan Tertagih          | Aktual                   |
| GUID faktur                 | Faktur                  | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rincian Baris Faktur     | Rincian Baris Faktur      | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Pembalikan penjualan yang tidak ditagih      | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Pembalikan penjualan yang tidak ditagih      | Aktual                            |                          |
| Koreksi faktur draft     | GUID ILD lama             | Transaksi Baris Faktur          | GUID ILD Koreksi               | Transaksi Baris Faktur |
| GUID IL Lama                  | Baris Faktur             | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| GUID faktur lama             | Faktur                  | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| Koreksi faktur dikonfirmasi | GUID ILD lama             | Transaksi Baris Faktur          | GUID aktual penjualan ditagih terbalik | Aktual                   |
| GUID IL Lama                  | Baris Faktur             | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID faktur lama             | Faktur                  | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID ILD lama                 | Transaksi Baris Faktur | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID IL Lama                  | Baris Faktur             | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID faktur lama             | Faktur                  | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID ILD Koreksi          | Transaksi Baris Faktur | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID IL Koreksi           | Baris Faktur             | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID faktur Koreksi      | Faktur                  | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |

Tabel berikut Menampilkan rekaman di entitas **koneksi transaksi** untuk alur kerja.

| Aktivitas                          | Transaksi 1                 | Peran Transaksi 1 | Jenis Transaksi 1           | Transaksi 2                | Peran Transaksi 2 | Jenis Transaksi 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Pengajuan entri waktu          | GUID baris jurnal (penjualan)     | Penjualan Belum Tertagih     | msdyn_journalline            | GUID baris jurnal (biaya)     | Biaya               | msdyn_journalline  |
| Persetujuan Waktu                  | GUID Aktual Belum Tertagih (Penjualan)  | Penjualan Belum Tertagih     | msdyn_actual                 | GUID Aktual Biaya (biaya)       | Biaya               | msdyn_actual       |
| Pembuatan Faktur               | GUID Rincian Baris Faktur      | Penjualan yang Ditagih       | msdyn_invoicelinetransaction | GUID Aktual Penjualan Belum Tertagih   | Penjualan Belum Tertagih     | msdyn_actual       |
| Konfirmasi Faktur           | Membalikkan GUID aktual         | Balik          | msdyn_actual                 | GUID Penjualan Belum Tertagih Asli | Asli           | msdyn_actual       |
| GUID Penjualan Tertagih              | Penjualan yang Ditagih                  | msdyn_actual       | GUID Aktual Penjualan Belum Tertagih   | Penjualan Belum Tertagih               | msdyn_actual       |                    |
| Koreksi faktur draft       | GUID Transaksi Baris Faktur | Mengganti          | msdyn_invoicelinetransaction | GUID Penjualan Tertagih            | Asli           | msdyn_actual       |
| Konfirmasi Koreksi faktur     | GUID Pembalikan penjualan tertagih    | Balik          | msdyn_actual                 | GUID Penjualan Tertagih            | Asli           | msdyn_actual       |
| GUID Aktual penjualan Belum Tertagih Baru | Mengganti                     | msdyn_actual       | GUID Penjualan Tertagih            | Asli                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
