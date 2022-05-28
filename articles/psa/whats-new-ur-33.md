---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 33, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601482"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 33. Versi ini memiliki nomor build V3.10.54.98 dan secara umum tersedia melalui pembaruan mandiri pada Bulan Juli 2021.

## <a name="update-release-33"></a>Pembaruan rilis 33

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Dua bidang yang terkunci, **msdyn_description** dan **msdyn_externaldescription** dapat diedit setelah pengiriman.
- Pesan kesalahan terjadi jika pengeluaran dibuat yang tidak terkait dengan proyek.
- Bila entri waktu dibuat, peran sumber daya akan default ke peran tidak aktif.
- Baris jurnal yang terkait dengan pengeluaran yang ditarik dan dihapus tidak akan dihapus.
- Pada **Formulir Buat Cepat entri Waktu**, perbarui tampilan **Daftar Tugas Proyek** untuk mengubah tanggal yang ditampilkan secara default ke tanggal mulai tugas.
- Ketika Anda membuat entri waktu dari tab **Terkait** sumber daya yang dapat dipesan, entri waktu salah dibuat untuk pengguna yang masuk, bukan sumber daya yang dapat dipesan induk.
- Bidang baru ditambahkan ke kotak dialog **MDD persetujuan massal**.

**Perencanaan proyek**

Masalah berikut telah diperbaiki:
- Kinerja pembuatan proyek yang lambat saat template jam kerja proyek diterapkan dengan kalender kompleks.
- Bila tanggal mulai lebih besar dari tanggal berakhir, kesalahan ditampilkan di template salin proyek karena perbedaan pada komponen waktu tiap bidang.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:
- Parameter yang salah digunakan dalam kueri pemanfaatan sumber daya dan XML mengakibatkan hasil filter yang salah pada kisi **Pemanfaatan Sumber Daya**.
- Konfirmasi **Perluas Pemesanan** menampilkan tanggal berakhir yang salah untuk pemesanan.

**Penjualan**

Masalah berikut telah diperbaiki:
- Pesan kesalahan terjadi jika harga kategori dibuat dengan nilai yang tidak ada.
- Pesan kesalahan terjadi jika tahapan baris kontrak dibuat tanpa baris pesanan.
