---
title: Transaksi bisnis
description: Topik ini menyediakan informasi tentang transaksi bisnis.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 28555f29e65c11255c8966f3d4b900512aa01c30fef0a9cef3a3794edaf92a0b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987530"
---
# <a name="business-transactions"></a>Transaksi bisnis

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Di Dynamics 365 Project Service Automation, *transaksi bisnis* adalah konsep abstrak yang tidak diwakili oleh entitas. Namun, beberapa bidang dan proses umum pada entitas dirancang untuk menggunakan konsep transaksi bisnis. Entitas berikut ini menggunakan abstraksi ini:

- Rincian Baris Kuotasi
- Rincian Baris Kontrak
- Baris Perkiraan
- Lini Jurnal
- Aktual

Dari entitas-entitas ini, rincian baris kuotasi, rincian baris kontrak, dan baris perkiraan dipetakan ke fase perkiraan dalam siklus hidup proyek. Baris jurnal dan entitas aktual dipetakan ke fase eksekusi dalam siklus hidup proyek.

PSA memperlakukan rekaman dalam lima entitas ini sebagai transaksi bisnis. Satu-satunya perbedaan adalah bahwa rekaman dalam entitas yang dipetakan ke fase estimasi dianggap sebagai perkiraan keuangan, sedangkan rekaman dalam entitas yang dipetakan ke fase eksekusi dianggap sebagai fakta keuangan yang telah terjadi.

Untuk informasi lebih lanjut, Lihat [taksiran](estimates.md) dan [aktual](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi bisnis
Konsep berikut ini unik untuk konsep transaksi bisnis:

- Jenis Transaksi
- Kelas Transaksi
- Asal transaksi
- Koneksi Transaksi

### <a name="transaction-type"></a>Jenis Transaksi

Jenis transaksi menunjukkan waktu dan konteks dampak keuangan pada suatu proyek. Ini diwakili oleh rangkaian pilihan yang memiliki nilai yang didukung berikut di PSA:
- Biaya
- Kontrak proyek
- Penjualan Belum Tertagih
- Penjualan yang Ditagih
- Penjualan Antar-organisasi
- Biaya Unit Sumber Daya

### <a name="transaction-class"></a>Kelas Transaksi

Kelas transaksi mewakili jenis biaya yang berbeda yang dikeluarkan pada proyek. Ini diwakili oleh rangkaian pilihan yang memiliki nilai yang didukung berikut di PSA:

- Time
- Pengeluaran
- Materi
- Biaya
- Tahap
- Pajak

Nilai **tonggak waktu** biasanya digunakan oleh logika bisnis untuk penagihan harga tetap di PSA.

### <a name="transaction-origin"></a>Asal transaksi

Asal transaksi adalah entitas yang menyimpan asal dari setiap transaksi bisnis. Saat eksekusi proyek berlangsung, setiap transaksi bisnis akan menimbulkan transaksi bisnis lain yang pada gilirannya akan membuat yang lain dan seterusnya. Entitas asal transaksi dirancang untuk menyimpan data tentang asal setiap transaksi untuk membantu pelaporan dan ketertelusuran. 

### <a name="transaction-connection"></a>Koneksi Transaksi

Koneksi transaksi adalah entitas yang menyimpan relasi antara dua transaksi bisnis serupa, seperti aktual biaya dan penjualan yang terkait, atau pembalikan transaksi yang dipicu oleh aktivitas penagihan seperti konfirmasi faktur atau koreksi faktur.

bersama-sama, asal transaksi dan entitas koneksi transaksi membantu Anda terus melacak Relasi antara transaksi bisnis dan tindakan yang menyebabkan pembuatan transaksi bisnis tertentu.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Contoh: cara kerja asal transaksi dengan koneksi transaksi

Contoh berikut menunjukkan pemrosesan tipikal waktu entri dalam siklus hidup proyek PSA.

> ![Waktu pemrosesan entri dalam siklus hidup Project Service.](media/basic-guide-17.png)
 
1. Pengajuan entri waktu menyebabkan pembuatan dua baris jurnal: satu untuk biaya dan satu untuk penjualan yang belum ditagih.
2. Persetujuan akhir entri waktu menyebabkan pembuatan dua nilai aktual: satu untuk biaya dan satu untuk penjualan yang belum ditagih.
3. Saat pengguna membuat faktur proyek, transaksi baris faktur dibuat menggunakan data dari nilai aktual penjualan yang belum ditagih. 
4. Setelah faktur dikonfirmasi, dua aktual baru dibuat: pembalikan aktual penjualan yang belum ditagih dan penjualan tertagih.

Setiap peristiwa ini memicu pembuatan rekaman di asal transaksi dan entitas koneksi transaksi untuk membantu membuat jejak Relasi antara rekaman yang dibuat sepanjang waktu masuk, baris jurnal, aktual, dan rincian baris faktur.

Tabel berikut Menampilkan rekaman di entitas asal transaksi untuk alur kerja sebelumnya.

| Aktivitas                        | Asal                   | Jenis Asal                       | Transaksi                       | Jenis Transaksi         |
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

Tabel berikut Menampilkan rekaman di entitas koneksi transaksi untuk alur kerja sebelumnya.

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