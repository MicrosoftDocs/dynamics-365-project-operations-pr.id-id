---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 40, V3
description: Topik ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588648"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 40, V3. Versi ini memiliki nomor pembuatan V3.10.61.61 dan umumnya tersedia melalui pembaruan mandiri pada Februari 2022.

## <a name="update-release-40"></a>Pembaruan rilis 40

### <a name="features"></a>Fitur
Fase 1 dari peningkatan dari Project Service Automation ke Project Operations - Lite akan dirilis pada Februari 2022 untuk semua pelanggan. Untuk memeriksa kelayakan, lihat [Peningkatan dari Otomatisasi Layanan Proyek ke Operasi Proyek](upgrade-project-operations-non-stocked.md). Jika aplikasi tidak muncul di instans Anda di Power Platform Pusat Admin, hubungi dukungan dan minta agar penerbangan diaktifkan untuk lingkungan Anda. Permintaan Anda harus menyertakan daftar ID lingkungan tempat penerbangan harus diaktifkan.

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**
- Entri catatan tidak ada saat entri waktu ditolak atau dibatalkan. 

**Penjualan**

- Saat Anda memperbarui perkiraan biaya atau penjualan menggunakan plug-in out-of-the-box, Anda salah diizinkan untuk mengirim payload JSON yang tidak valid di luar antarmuka pengguna.
- Saat Anda memperbarui garis kutipan menggunakan tampilan cepat, Anda diizinkan untuk mengaktifkan tanda kutip.
