---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 28, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948691"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, rilis pembaruan 28 Versi ini memiliki nomor pembuatan V3.10.46.32 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2021.

## <a name="update-release-28"></a>Pembaruan rilis 28

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Pengguna dapat menggunakan **Pengeditan Massal** untuk memperbarui entri waktu yang telah disetujui dan dikirimkan.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Dalam kasus di mana tugas GUID diinterpretasikan sebagai angka, tugas tidak bisa dibuka untuk diedit menggunakan **Edit Tugas** di pita pada halaman **struktur rincian kerja**.

**Sales**

Masalah berikut telah diperbaiki:

- Pengecualian referensi null dihasilkan ketika plug-in **GetEstimatesForProject** dipanggil.
- **Tandai siap untuk faktur** pada kisi tonggak pencapaian hanya sebagian memperbarui atribut, kecuali untuk atribut **InvoiceStatus**, yang diperbarui.



[!INCLUDE[footer-include](../includes/footer-banner.md)]