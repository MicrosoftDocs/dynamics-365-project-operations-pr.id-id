---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 42, V3
description: Topik ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589200"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 42, V3. Versi ini memiliki nomor pembuatan V3.10.73.61 dan umumnya tersedia melalui pembaruan mandiri pada April 2022.

## <a name="update-release-42"></a>Pembaruan rilis 42

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**

- Ketika lembar waktu ditolak, pengguna yang menolaknya salah diidentifikasi sebagai **Sistem**.
- Saat entri waktu diimpor, **nilai Kategori** Sumber Daya hilang.
- Pemberi persetujuan proyek dapat menyetujui proyek yang dikirimkan saat izin mereka tidak diatur secara khusus ke **Dapat Menyetujui**.

**Penjualan**

- Ketika aktual dicatat pada tugas tingkat non-root, biaya aktual salah dikumpulkan.
