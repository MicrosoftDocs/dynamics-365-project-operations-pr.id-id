---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 34, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588694"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 34. Versi ini memiliki nomor build V3.10.55.38 dan secara umum tersedia melalui pembaruan mandiri pada Bulan Juli 2021.

## <a name="update-release-34"></a>Pembaruan rilis 34

### <a name="bug-fixes"></a>Perbaikan bug
Masalah berikut telah diperbaiki.

**Umum**

- Pembaruan yang digerakkan penerbit tidak mengaktifkan alur kerja persetujuan modern baru.
- Atribut **Status Target** dan **Tipe Tindakan** hilang di halaman utama **Kumpulan Persetujuan**.

**Waktu dan Pengeluaran**

- Tidak dapat menyetujui permintaan penarikan kembali menggunakan alur persetujuan modern.
- Menyalin entri waktu dalam sepekan tidak berfungsi saat menyalin entri yang tidak terkait dengan pengguna yang masuk.

**Perencanaan proyek**

- Kontur penetapan sumber daya rusak saat mengimpor dari add-in desktop Microsoft Project.

**Manajemen sumber daya**

- Saat Anda menerbitkan proyek dari add-in klien desktop Microsoft Project, tanggal akhir persyaratan yang ada diubah.
- Presisi desimal melebihi dua tempat desimal dalam dialog konfirmasi pemesanan diperpanjang.

**Penjualan**

- Saat Anda menambahkan baris berbasis produk dengan produk yang ada ke kontrak proyek, pengecualian **kunci tidak ditemukan dalam kamus** ditampilkan.
- Prospek tidak dapat memenuhi syarat saat jenis pesanan dipetakan dari prospek ke peluang.
