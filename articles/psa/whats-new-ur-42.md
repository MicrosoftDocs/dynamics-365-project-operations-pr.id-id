---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 42, V3
description: Artikel ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 42, V3.
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912719"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 42, V3. Versi ini memiliki nomor pembuatan V3.10.73.61 dan umumnya tersedia melalui pembaruan mandiri pada April 2022.

## <a name="update-release-42"></a>Pembaruan rilis 42

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**

- Bila lembar waktu ditolak, pengguna yang menolaknya tidak diidentifikasi dengan benar sebagai **Sistem**.
- Bila entri waktu diimpor, nilai **Kategori Sumber Daya** tidak ada.
- Pemberi izin proyek dapat menyetujui proyek yang diajukan bila izin mereka tidak diatur secara khusus ke **Dapat Menyetujui**.

**Penjualan**

- Ketika aktual dicatat pada tugas tingkat non-root, biaya aktual salah agregat.
