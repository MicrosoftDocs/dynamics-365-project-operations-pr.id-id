---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 40, V3
description: Artikel ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 40, V3.
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912796"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 40, V3. Versi ini memiliki nomor pembuatan V3.10.61.61 dan umumnya tersedia melalui pembaruan mandiri pada Februari 2022.

## <a name="update-release-40"></a>Pembaruan rilis 40

### <a name="features"></a>Fitur
Fase 1 peningkatan dari Project Service Automation ke Project Operations - Lite akan dirilis pada bulan Februari 2022 kepada semua pelanggan. Untuk memeriksa kelayakan, lihat [Tingkatkan dari Project Service Automation ke Project Operations](upgrade-project-operations-non-stocked.md). Jika aplikasi tidak muncul dalam instans Anda di Pusat Admin Power Platform, hubungi dukungan dan minta agar perpindahan diaktifkan untuk lingkungan Anda. Permintaan Anda harus mencakup daftar ID lingkungan dengan kebutuhan perpindahan yang akan diaktifkan.

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**
- Entri catatan tidak ada saat entri waktu ditolak atau dibatalkan. 

**Penjualan**

- Bila Anda memperbarui perkiraan biaya atau penjualan menggunakan plug-in siap pakai, maka Anda tidak dibolehkan mengirim muatan JSON yang tidak valid di luar antarmuka pengguna.
- Bila Anda memperbarui baris kuotasi menggunakan tampilan cepat, Anda diizinkan untuk mengaktifkan kuotasi.
