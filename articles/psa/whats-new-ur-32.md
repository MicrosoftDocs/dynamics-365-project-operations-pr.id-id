---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 32, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994865"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 32. Versi ini memiliki nomor build V3.10.53.108 dan secara umum tersedia melalui pembaruan mandiri pada Bulan Juni 2021.

## <a name="update-release-32"></a>Pembaruan rilis 32

### <a name="bug-fixes"></a>Perbaikan bug

#### <a name="general"></a>Umum

- Bila peningkatan utama gagal, hanya titik masuk aplikasi utama yang harus diblokir, untuk memastikan entitas bersama tetap dapat diakses.

#### <a name="time-and-expense"></a>Waktu dan Pengeluaran

Masalah berikut telah diperbaiki:

- **TimeEntriesImportSourceResourceAssignment** tidak mempertahankan waktu mulai dan berakhir potongan kontur penetapan sumber daya.
- Bila Anda memilih **Buka Entri** pada kisi **Entri Waktu**, Anda mungkin dicegah memilih formulir lain.
- Saat Anda mengimpor penetapan ke entri waktu, kueri kode klien dapat menghasilkan URL panjang yang menggagalkan kueri.
- Di kisi **Entri Waktu**, setelah nilai dihapus dari sel, fokus tidak tetap berada di kisi.
- Tombol **Tolak** telah dihilangkan dari tampilan **Pemrosesan persetujuan** untuk persetujuan modern.
- Stabilitas dan performa persetujuan massal entri waktu terpengaruh kebuntuan dan kegagalan untuk menangani dengan benar penyesuaian yang terkait dengan entitas **Entri Waktu**.

#### <a name="project-planning"></a>Perencanaan proyek

- Pengecualian referensi nihil dibuat saat Anda memperbarui proyek yang memiliki nilai nihil di bidang **Unit Kontrak**.
- **Segarkan Total Proyek** dengan keliru menghitung biaya tersisa dan penjualan yang tersisa di proyek.
- Penghitungan harga berulang mempengaruhi performa yang terkait dengan pembaruan pada kontur penugasan sumber daya.

#### <a name="resource-management"></a>Manajemen sumber daya

Masalah berikut telah diperbaiki:

- Ketika kapasitas kalender sumber daya yang dapat dipesan lebih dari 1, Project Service Automation dengan keliru mengenali kapasitas sebagai 0 (nol). Oleh karena itu, lingkaran tak terbatas terjadi di tampilan jadwal.

#### <a name="sales"></a>Penjualan

Masalah berikut telah diperbaiki:

- Ketika baris jurnal dibuat yang memiliki jenis transaksi kustom, pengecualian referensi nihil berikut terjadi: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Peran dan kategori yang dinonaktifkan sebelum kuotasi disalin seharusnya tidak ditambahkan ke peran dan kategori yang dikenakan biaya dari kuotasi yang baru disalin.
- Tanggal dokumen dan tanggal akuntansi tidak selaras dengan tanggal mulai yang diberikan pada detail baris faktur yang dibuat secara langsung pada draf faktur.
- Pengecualian referensi nihil dibuat dalam skenario yang terkait dengan penonaktifan peran dan kategori sebelum kuotasi disalin.
- Tindakan **Harga Pembaruan** di halaman **Proyek** tidak memperbarui estimasi pengeluaran dan estimasi bahan.
