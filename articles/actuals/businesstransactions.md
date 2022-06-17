---
title: Transaksi bisnis di Project Operations
description: Artikel ini memberikan gambaran umum tentang konsep transaksi bisnis di Microsoft Dynamics 365 Project Operations.
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

Di Microsoft Dynamics 365 Project Operations, *transaksi* bisnis adalah konsep abstrak yang tidak diwakili oleh entitas mana pun. Namun, beberapa bidang dan proses umum pada entitas dirancang untuk menggunakan konsep transaksi bisnis. Entitas berikut ini menggunakan abstraksi ini:

- Rincian Baris Kuotasi
- Rincian Baris Kontrak
- Baris Perkiraan
- Lini Jurnal
- Aktual

Dari entitas ini, detail garis Kutipan, detail baris Kontrak, dan garis Perkiraan dipetakan *ke fase* estimasi dalam siklus hidup proyek. Baris Jurnal dan entitas Aktual dipetakan *ke fase* eksekusi dalam siklus hidup proyek.

Operasi Proyek memperlakukan catatan di kelima entitas ini sebagai transaksi bisnis. Satu-satunya perbedaan adalah bahwa catatan dalam entitas yang dipetakan ke fase estimasi (Detail garis kutipan, Detail garis kontrak, dan garis Perkiraan) dianggap sebagai *perkiraan* keuangan, sedangkan catatan dalam entitas yang dipetakan ke fase eksekusi (Garis jurnal dan Aktual) dianggap sebagai *fakta* keuangan yang telah terjadi.

Untuk informasi lebih lanjut, Lihat [taksiran](../project-management/estimating-projects-overview.md) dan [aktual](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi bisnis

Konsep berikut ini unik untuk konsep transaksi bisnis:

- Jenis Transaksi
- Kelas Transaksi
- Asal transaksi
- Koneksi Transaksi

### <a name="transaction-type"></a>Jenis Transaksi

Jenis transaksi menunjukkan waktu dan konteks dampak keuangan pada suatu proyek. Ini didefinisikan oleh rangkaian pilihan yang memiliki nilai yang didukung berikut dalam Operasi Proyek:

- Biaya
- Kontrak proyek
- Penjualan Belum Tertagih
- Penjualan yang Ditagih
- Penjualan Antar-organisasi
- Biaya Unit Sumber Daya

### <a name="transaction-class"></a>Kelas Transaksi

Kelas transaksi mewakili jenis biaya yang berbeda yang dikeluarkan pada proyek. Ini didefinisikan oleh rangkaian pilihan yang memiliki nilai yang didukung berikut dalam Operasi Proyek:

- Waktu
- Pengeluaran
- Materi
- Biaya
- Tahap
- Pajak

> [!NOTE]
> Nilai **Milestone** biasanya digunakan oleh logika bisnis untuk penagihan harga tetap di Project Operations.

### <a name="transaction-origin"></a>Asal transaksi

Asal transaksi adalah entitas yang menyimpan asal setiap transaksi bisnis untuk membantu pelaporan dan keterlacakan. Saat pelaksanaan proyek dimulai, setiap transaksi bisnis menciptakan transaksi bisnis lain yang pada gilirannya akan membuat transaksi bisnis lain, dan seterusnya.

### <a name="transaction-connection"></a>Koneksi Transaksi

Koneksi transaksi adalah entitas yang menyimpan hubungan antara dua transaksi bisnis serupa, seperti biaya dan aktual penjualan terkait atau pembalikan transaksi yang dipicu oleh aktivitas penagihan seperti konfirmasi faktur atau koreksi faktur.

Bersama-sama, entitas asal Transaksi dan koneksi Transaksi membantu Anda melacak Relasi antara transaksi bisnis dan tindakan yang menyebabkan transaksi bisnis tertentu dibuat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
