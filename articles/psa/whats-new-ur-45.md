---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 45, V3
description: Artikel ini mencantumkan fitur dan perbaikan yang tersedia di Microsoft Dynamics 365 Project Service Automation Rilis Pembaruan 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169180"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini mencantumkan fitur dan perbaikan yang baru atau diubah untuk Project Service Automation Update Release 45, V3. Versi ini memiliki nomor build V3.10.76.168 dan secara umum tersedia melalui pembaruan mandiri pada Bulan Juli 2022.

## <a name="update-release-45"></a>Pembaruan rilis 45

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Penjualan**

- Pengguna tidak dapat berhasil membuat faktur setelah mereka mencoba membuat faktur tanpa penjualan yang belum ditagih, jika mereka juga melihat contoh halaman yang sama dan tidak me-refresh-nya.

**Waktu dan Pengeluaran**

- Ketika Persetujuan Modern diaktifkan dan persetujuan proyek yang ditarik kembali disetujui, tahap perekaman salah diperbarui ke **Permintaan Penarikan Kembali disetujui**.
- Saat Persetujuan Modern diaktifkan dan Cloud Flows tidak aktif, proses persetujuan tidak berhasil, dan pengguna yang mengirimkan atau menyetujui tidak diberi tahu.
