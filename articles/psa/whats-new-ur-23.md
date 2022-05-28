---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 23, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: cc918f1516d4751b3f8e70a93d8fc66058201f22
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581610"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation Pembaruan Rilis 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 23. Versi ini memiliki nomor pembuatan V 3.10.34.30 dan umumnya tersedia melalui pembaruan mandiri pada Agustus 2020.

## <a name="update-release-23"></a>Pembaruan rilis 23

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:
- Tangani kasus tepi dalam **Penghapusan anggota tim proyek** untuk memberikan pengecualian bermakna.
- Hasil impor tugas di layar Hapus kosong.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- **Kartu sumber daya pemanfaatan kisi sumber daya** menampilkan data yang salah saat skala waktu lebih dari lima hari.
- Bila pelanggan membuat sumber daya yang dapat dipesan, plug-in terkadang gagal menambahkan sumber daya secara otomatis ke grup Microsoft Office 365.
- Tampilan **rekonsiliasi** menampilkan kontur manual secara tidak benar dalam tampilan **Pekan** atau **bulan**.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Jumlah berlebihan entitas **retrievemultiple untuk usersettings** menyebabkan kinerja terdegradasi untuk persetujuan proyek dan operasi lainnya.
- Pencarian sumber daya kisi **perencanaan tugas** terbatas hanya menampilkan hingga lima anggota tim dari tim proyek. 
- Pencarian sumber daya kisi **perencanaan tugas** tidak memfilter sumber daya yang tidak aktif.
- Mode manual tidak berfungsi sebagaimana yang diharapkan dalam struktur rincian kerja Perencanaan proyek.
- Kisi **perencanaan tugas** menunjukkan **kategori transaksi tidak aktif**.
- Putaran kisi **Penetapan sumber daya** salah ketika tugas memiliki beberapa penetapan.
- Nilai pembulatan berbeda antara biaya yang direncanakan dan biaya aktual untuk satu tugas.

**Sales**

Masalah berikut telah diperbaiki:

- **Ambil Semua Kategori Transaksi** Klik dua kali membuat beberapa baris.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
