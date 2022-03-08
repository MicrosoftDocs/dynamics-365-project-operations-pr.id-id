---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 35, V3
description: Topik ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473269"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 35, V3. Versi ini memiliki nomor build V3.10.56.110 dan secara umum tersedia melalui pembaruan mandiri pada Bulan September 2021.

## <a name="update-release-35"></a>Pembaruan rilis 35

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**

- Pemberi izin proyek menerima kesalahan hak istimewa baca saat mereka menyetujui entri pengeluaran dengan peran **Pemberi Izin Proyek**.
- Pemberi izin proyek menerima kesalahan hak istimewa menulis **msdyn_projectapproval** ketika mereka membatalkan entri waktu yang disetujui dengan peran **Pemberi Izin Proyek**.
- Bila Anda memilih **Salin pekan** dalam entri waktu di dynamics 365 untuk ponsel - modul aplikasi Pusat Project Resource, kesalahan berikut terjadi: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Kebijakan **Coba lagi** secara otomatis menyetujui entri yang sebelumnya ditolak.
- Subkisi **Kumpulan Persetujuan** menunjukkan tindakan pita yang tidak berlaku.
- Ikon tidak ada untuk **Tugas Proyek** dan **Peran Sumber Daya** pada entitas **Entri Waktu**.
- Saat Anda mengimpor penetapan sumber daya, entri waktu impor tidak memiliki durasi yang benar untuk penetapan yang dibuat melalui tugas mode manual.
- **Hapus** hilang dari halaman **rekaman Pencarian Tingkat Lanjut untuk Entri Waktu**.
- **Simpan** hilang dari halaman **informasi entri Waktu**. Masalah ini akan mencegah perubahan disimpan saat halaman ditutup.

**Perencanaan proyek**

- Kisi **Penetapan Sumber Daya** dan **Rekonsiliasi Sumber Daya** tidak mengurutkan atribut yang dikelompokkan secara abjad.
- Tugas tidak dapat dibuat jika perilaku tanggal disesuaikan ke **Hanya Tanggal**.

**Manajemen sumber daya**

- Jika Dynamics 365 Field Service maupun Project Service Automation diinstal, masalah tumpang tindih terjadi saat **Tampilan Terkait Persyaratan Sumber Daya** dikaitkan dengan halaman utama.
- Mengeklik dua kali **Simpan** di kotak dialog **Buat Cepat Anggota Tim** mencegah persyaratan sumber daya dibuat.

**Penjualan**

- Pengecualian akan terjadi jika Anda menghapus tugas yang terkait dengan kuotasi yang memiliki status **Menang**.
