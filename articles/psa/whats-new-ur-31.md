---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 31, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002155"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 31. Versi ini memiliki nomor pembuatan V3.10.52.77 dan umumnya tersedia melalui pembaruan mandiri pada Mei 2021.

## <a name="update-release-31"></a>Pembaruan rilis 31

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Tombol perintah kontrol entri waktu di halaman **Sumber Daya yang Dapat Dipesan** membingungkan.
- Pengecualian referensi nihil dibuat di **Project.SetTrackingFields** saat menyetujui entri waktu.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- **Membuat Anggota Tim** tidak menampilkan pengaturan metadata konfigurasi pemesanan dengan benar untuk **Status komitmen Pemesanan Default**.
- Ketika beralih dari PSA 1.X ke 3.X, proses peningkatan gagal di **UpgradeResourceRequirements**.


**Penjualan**

Masalah berikut telah diperbaiki:

- Pendapatan aktual mengkonversi jumlah ke mata uang proyek di kisi pelacakan.
- Default mata uang tidak jelas saat membuat baris jurnal, baris kuotasi, dan baris kontrak dalam skenario dengan mata uang dasar organisasi berbeda dari mata uang proyek.
- **Kueri validasi koreksi yang tertunda** tidak difilter berdasarkan proyek.
- Penjualan tersisa dihitung dengan salah di proyek.
- Kuotasi berdasarkan kontak gagal bila dibuat tanpa daftar harga.
- Spinner pemrosesan tidak ditampilkan saat Anda memilih **Konfirmasikan Faktur**.
- Spinner pemrosesan tidak ditampilkan saat Anda memilih **Buat Faktur**.
- Menutup kuotasi sebagai kalah tidak akan membatalkan pemesanan.







