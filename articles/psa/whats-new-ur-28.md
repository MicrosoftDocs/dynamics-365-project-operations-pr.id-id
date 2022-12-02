---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 28, V3
description: Artikel ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 28, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930598"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, rilis pembaruan 28 Versi ini memiliki nomor pembuatan V3.10.46.32 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2021.

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
