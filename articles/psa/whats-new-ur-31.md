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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999135"
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







