---
title: Transaksi bisnis dalam Operasi Proyek
description: Hal ini topik memberikan gambaran umum tentang konsep transaksi bisnis di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582208"
---
# <a name="business-transactions-in-project-operations"></a>Transaksi bisnis dalam Operasi Proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Di Microsoft Dynamics 365 Project Operations, *transaksi* bisnis adalah konsep abstrak yang tidak diwakili oleh entitas mana pun. Namun, beberapa bidang dan proses umum pada entitas dirancang untuk menggunakan konsep transaksi bisnis. Entitas berikut ini menggunakan abstraksi ini:

- Rincian Baris Kuotasi
- Rincian Baris Kontrak
- Baris Perkiraan
- Lini Jurnal
- Aktual

Dari entitas ini, detail garis Kutipan, detail garis kontrak, dan garis Perkiraan dipetakan ke *fase* estimasi dalam siklus hidup proyek. Baris Jurnal dan entitas Aktual dipetakan ke *fase* eksekusi dalam siklus hidup proyek.

Operasi Proyek memperlakukan catatan di kelima entitas ini sebagai transaksi bisnis. Satu-satunya perbedaan adalah bahwa catatan dalam entitas yang dipetakan ke fase estimasi (rincian garis kutipan, rincian garis kontrak, dan garis Perkiraan) dianggap sebagai *perkiraan* keuangan, sedangkan catatan dalam entitas yang dipetakan ke fase eksekusi (Garis jurnal dan Aktual) dianggap sebagai *fakta* keuangan yang telah terjadi.

Untuk informasi lebih lanjut, Lihat [taksiran](../project-management/estimating-projects-overview.md) dan [aktual](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi bisnis

Konsep berikut ini unik untuk konsep transaksi bisnis:

- Jenis Transaksi
- Kelas Transaksi
- Asal transaksi
- Koneksi Transaksi

### <a name="transaction-type"></a>Jenis Transaksi

Jenis transaksi menunjukkan waktu dan konteks dampak keuangan pada suatu proyek. Ini didefinisikan oleh rangkaian pilihan yang memiliki nilai-nilai yang didukung berikut dalam Operasi Proyek:

- Biaya
- Kontrak proyek
- Penjualan Belum Tertagih
- Penjualan yang Ditagih
- Penjualan Antar-organisasi
- Biaya Unit Sumber Daya

### <a name="transaction-class"></a>Kelas Transaksi

Kelas transaksi mewakili jenis biaya yang berbeda yang dikeluarkan pada proyek. Ini didefinisikan oleh rangkaian pilihan yang memiliki nilai-nilai yang didukung berikut dalam Operasi Proyek:

- Waktu
- Pengeluaran
- Materi
- Biaya
- Tahap
- Pajak

> [!NOTE]
> Nilai **Milestone** biasanya digunakan oleh logika bisnis untuk penagihan harga tetap dalam Operasi Proyek.

### <a name="transaction-origin"></a>Asal transaksi

Asal transaksi adalah entitas yang menyimpan asal setiap transaksi bisnis untuk membantu pelaporan dan penelusuran. Ketika eksekusi proyek dimulai, setiap transaksi bisnis menciptakan transaksi bisnis lain yang pada gilirannya akan menciptakan transaksi bisnis lain, dan sebagainya.

### <a name="transaction-connection"></a>Koneksi Transaksi

Koneksi transaksi adalah entitas yang menyimpan hubungan antara dua transaksi bisnis serupa, seperti biaya dan aktual penjualan terkait atau pembalikan transaksi yang dipicu oleh aktivitas penagihan seperti konfirmasi faktur atau koreksi faktur.

Bersama-sama, entitas asal Transaksi dan koneksi Transaksi membantu Anda melacak Relasi antara transaksi bisnis dan tindakan yang menyebabkan transaksi bisnis tertentu dibuat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
