---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 37, V3
description: Topik ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727609"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 37, V3. Versi ini memiliki nomor pembuatan V3.10.58.120 dan umumnya tersedia melalui pembaruan mandiri pada November 2021.

## <a name="update-release-37"></a>Pembaruan rilis 37

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**
- Pengguna tidak dapat menghapus entri waktu dengan mengosongkan sel.
- Tampilan **persetujuan saya yang gagal** hanya berisi persetujuan proyek dengan status **Diajukan**.

**Manajemen proyek**
- Pengguna menerima kesalahan pengecualian referensi nihil saat membuka proyek di add-in desktop Microsoft jika nama posisi anggota tim Proyek kosong.
- Tidak ada tombol **Simpan** di halaman **Tugas Proyek** sehingga pengguna tidak dapat menyimpan perubahan ke rekaman tugas.
- Pengguna tidak dapat menghapus proyek yang memiliki tugas yang terkait dengan kuotasi dengan status **Menang**.

**Penjualan**
- Bidang **Mata Uang** di halaman **Proyek** diperbarui agar sesuai dengan mata uang template yang diterapkan.
- Biaya dihitung dengan keliru pada tugas yang memiliki beberapa mata uang.
