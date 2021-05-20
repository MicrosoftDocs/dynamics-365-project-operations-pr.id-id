---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 29, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948644"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 29. Versi ini memiliki nomor pembuatan V3.10.47.7 dan umumnya tersedia melalui pembaruan mandiri pada Februari 2021.

## <a name="update-release-29"></a>Pembaruan rilis 29

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Pengguna tidak dapat melihat jam kerja yang dicatat pada hari non-kerja dalam kisi entri waktu.
- Entri pengeluaran yang disetujui dapat diedit pada kisi.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Logika validasi tidak ditemukan untuk memastikan jam kerja penetapan sumber daya tidak dapat negatif.
- Tindakan kustom, **AssignResourcesForTask** akan memperbarui semua bidang dan bukan hanya bidang yang diubah.
- Saat menyalin proyek di lingkungan dengan plug-in atau alur kerja yang terdaftar di aktivitas **CreateProject**, atribut **msdyn_bulkgenerationstatus** tidak diperbarui jika **CopyWBSToAddress** gagal.
- Saat Anda memperluas kalender proyek, hari kerja tidak disusun dalam urutan menaik yang menyebabkan beberapa pembaruan tugas proyek gagal.
- Mengubah Manajer Proyek pada proyek yang ada akan memicu logika default unit organisasional.

**Penjualan**

Masalah berikut telah diperbaiki:

- Tab **Performa Kontrak** di halaman **Kontrak** gagal secara hening selama inisialisasi saat tidak ada baris kontrak.