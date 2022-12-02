---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 36, V3
description: Artikel ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 36, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924986"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 36, V3. Versi ini memiliki nomor pembuatan V3.10.57.152 dan umumnya tersedia melalui pembaruan mandiri pada Oktober 2021.

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



