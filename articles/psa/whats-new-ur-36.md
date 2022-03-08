---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 36, V3
description: Topik ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606773"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 36, V3. Versi ini memiliki nomor pembuatan V3.10.57.152 dan umumnya tersedia melalui pembaruan mandiri pada Oktober 2021.

## <a name="update-release-36"></a>Pembaruan rilis 36

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Umum**
- Nama bidang **Template Jam Kerja Default** diterjemahkan dengan keliru di halaman **Parameter Proyek**.
- Plug-in asinkron tidak menangani pengecualian yang terkait dengan **SharedVariableService** dengan benar.

**Waktu dan Pengeluaran**
- Ketika baris jurnal tidak ada atau pengguna tidak memiliki hak istimewa yang benar untuk membaca baris jurnal, kesalahan yang tidak tepat terjadi saat persetujuan proyek dibatalkan.
- Pengguna tidak dapat membatalkan persetujuan bila pengeluaran atau entri waktu memiliki lebih dari satu persetujuan proyek terkait.
- **Ketidakhadiran** dan **Liburan** tidak diterjemahkan dengan benar untuk bahasa Tionghoa dalam pencarian pada halaman pembuatan cepat **Entri Waktu**.

**Manajemen sumber daya**
- Pengguna tidak dapat mencari sumber daya di **Asisten Jadwal** bila mode tampilan diatur ke **Hari**, **Pekan**, atau **Bulan**.
- Sumber daya generik tidak dibolehkan memiliki nama posisi kosong. 
- Menutup kontrak sebagai kalah tidak akan membatalkan pemesanan di masa mendatang.

**Penjualan**
- Bila lingkungan memiliki volume produk yang besar, performa akan menurun di kisi **Perkiraan Bahan**.
- Saat membuat proyek dari template, mata uang proyek tidak default ke unit kontrak Manajer Proyek masing-masing.
- Jumlah aktual tidak selalu sesuai dengan yang tercermin pada jatuh tempo proyek, atau jumlah menjadi negatif dalam skenario penarikan tertentu.
- Kesalahan terjadi saat Anda mengaitkan proyek yang dibuat dari template proyek ke baris kontrak.
- Pengguna dapat menghapus baris kontrak dengan tahapan, **Siap difaktur** dan **Faktur Dibuat**. Hal ini seharusnya tidak diizinkan.
- Bila estimasi diimpor dari proyek, ketertagihan detail baris kuotasi tidak diatur dengan benar saat penagihan berbasis tugas diaktifkan untuk baris kuotasi.
- Bila Anda menambahkan tahapan penagihan harga tetap, tahapan tidak tercermin dalam subkisi tahapan hingga halaman di-refresh.
- Pengecualian referensi nihil dibuat saat Anda membuat kontrak proyek dengan nama kuotasi nihil.
- Tugas mode manual dengan mata uang proyek berbeda dari mata uang sumber daya mengakibatkan estimasi harga salah.
- Pengguna tidak dapat menarik transaksi yang telah berhasil dikoreksi dengan faktur perbaikan.
- Kategori transaksi yang dinonaktifkan akan muncul dalam kisi **Estimasi Pengeluaran**.



