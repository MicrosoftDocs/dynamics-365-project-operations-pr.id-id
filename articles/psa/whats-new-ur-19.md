---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 19, V3
description: Artikel ini mencantumkan fitur dan perbaikan yang tersedia di Project Service Automation Update Release 19, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: a17275220eec726107e8ce5f82bdf5cdd403033e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915510"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation Pembaruan Rilis 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini mencantumkan fitur dan perbaikan yang baru atau berubah untuk PSA V3, Rilis Pembaruan 19. Versi ini memiliki nomor pembuatan V3.10.30.41 dan umumnya tersedia melalui pembaruan mandiri pada Mei 2020.

## <a name="update-release-19"></a>Pembaruan rilis 19

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki: 

- Kesalahan yang berasal dari impor entri waktu tidak muncul dengan benar.
- Kisi waktu entri tidak mendukung perilaku bidang **hanya tanggal**.
- Sumber daya proyek tidak dapat membuat pengeluaran dengan proyek.

**Manajemen proyek**

Masalah berikut telah diperbaiki: 

-  Tugas cucu menyebabkan perkiraan upaya yang salah selama penghitungan penyelesaian (EAC).

**Sales**

Masalah berikut telah diperbaiki: 

- Tindakan **menghitung ulang** tidak bekerja dengan rincian baris kontrak pengeluaran atau rincian baris kuotasi.
- **Harga pembaruan** hilang untuk perkiraan pengeluaran.
-  Pelanggan tidak dapat memilih alasan status kustom kontrak dari halaman **kontrak proyek**.
- Pelanggan mengalami kinerja yang rusak saat membuat daftar harga kustom dari kuotasi.
- Pelanggan mengalami inkonsistensi dengan default **unit** pada **detail baris kuotasi** dan halaman **rincian baris kontrak**.
- Menambahkan item kategori transaksi yang tidak dikenakan biaya ke baris kontrak yang dikenakan biaya tidak akan menghormati jenis penagihan **Tidak dikenai biaya** dari kategori transaksi.
- Pelanggan tidak dapat menggunakan peran dan kategori yang baru ditambahkan pada kontrak yang dibuat sebelumnya.
- Pelanggan mengalami kinerja terdegradasi pengambilan tidak perlu di PreValidateProjectTeamMemberUpdate.cs
- Peran yang diatur sebagai tidak dikenakan biaya dalam Daftar **kategori sumber daya** harus ditambahkan ke **peran dikenai biaya** sebagai **Tidak dikenai biaya** pada baris kontrak untuk proyek.
- Pelanggan mungkin mengalami kinerja yang rusak saat membuat proyek karena **GetBookableResourceIdFromUser** mengambil semua kolom sumber daya yang dapat dipesan dan bukan hanya id utama.
- Entitas **TransactionType** kehilangan plug-in pembaruan pra-validasi untuk mencegah pengguna memasukkan **unit** dan **UnitGroups** yang tidak berlaku untuk jenis transaksi.
- Langkah **Hapus** tidak berfungsi untuk impor entri waktu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
