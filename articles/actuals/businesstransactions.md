---
title: Transaksi bisnis di Project Operations
description: Artikel ini memberikan ikhtisar konsep transaksi bisnis di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923284"
---
# <a name="business-transactions-in-project-operations"></a>Transaksi bisnis di Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Di Microsoft Dynamics 365 Project Operations, *transaksi bisnis* adalah konsep abstrak yang tidak diwakili oleh entitas. Namun, beberapa bidang dan proses umum pada entitas dirancang untuk menggunakan konsep transaksi bisnis. Entitas berikut ini menggunakan abstraksi ini:

- Rincian Baris Kuotasi
- Rincian Baris Kontrak
- Baris Perkiraan
- Lini Jurnal
- Aktual

Dari entitas ini, rincian baris kuotasi, rincian baris kontrak, dan baris estimasi, dipetakan ke *fase estimasi* dalam siklus hidup proyek. Baris jurnal dan entitas aktual dipetakan ke *fase eksekusi* dalam siklus hidup proyek.

Project Operations memperlakukan rekaman dalam kelima entitas ini sebagai transaksi bisnis. Satu-satunya perbedaan adalah bahwa rekaman dalam entitas yang dipetakan ke fase estimasi (Detail Baris kuotasi, Detail baris kontrak, Dan Baris Estimasi) dianggap sebagai *perkiraan keuangan*, sedangkan rekaman dalam entitas yang dipetakan ke fase eksekusi (lini jurnal dan Aktual) dianggap sebagai *fakta keuangan* yang telah terjadi.

Untuk informasi lebih lanjut, Lihat [taksiran](../project-management/estimating-projects-overview.md) dan [aktual](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi bisnis

Konsep berikut ini unik untuk konsep transaksi bisnis:

- Jenis Transaksi
- Kelas Transaksi
- Asal transaksi
- Koneksi Transaksi

### <a name="transaction-type"></a>Jenis Transaksi

Jenis transaksi menunjukkan waktu dan konteks dampak keuangan pada suatu proyek. Ini didefinisikan oleh rangkaian pilihan yang memiliki nilai yang didukung berikut di Project Operations:

- Biaya
- Kontrak proyek
- Penjualan Belum Tertagih
- Penjualan yang Ditagih
- Penjualan Antar-organisasi
- Biaya Unit Sumber Daya

### <a name="transaction-class"></a>Kelas Transaksi

Kelas transaksi mewakili jenis biaya yang berbeda yang dikeluarkan pada proyek. Ini didefinisikan oleh rangkaian pilihan yang memiliki nilai yang didukung berikut di Project Operations:

- Waktu
- Pengeluaran
- Materi
- Biaya
- Tahap
- Pajak

> [!NOTE]
> Nilai **Tonggak waktu** biasanya digunakan oleh logika bisnis untuk penagihan harga tetap di Project Operations.

### <a name="transaction-origin"></a>Asal transaksi

Asal transaksi adalah entitas yang menyimpan asal setiap transaksi bisnis untuk membantu pelaporan dan keterlacakan. Saat eksekusi proyek dimulai, setiap transaksi bisnis membuat transaksi bisnis lain yang pada gilirannya akan membuat transaksi bisnis lainnya, dan seterusnya.

### <a name="transaction-connection"></a>Koneksi Transaksi

Koneksi transaksi adalah entitas yang menyimpan relasi antara dua transaksi bisnis serupa, seperti aktual biaya dan penjualan yang terkait, atau pembalikan transaksi yang dipicu oleh aktivitas penagihan seperti konfirmasi faktur atau koreksi faktur.

bersama-sama, asal transaksi dan entitas koneksi transaksi membantu anda melacak Relasi antara transaksi bisnis dan tindakan yang menyebabkan transaksi bisnis tertentu dibuat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
