---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 38, V3
description: Topik ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598722"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 38, V3. Versi ini memiliki nomor pembuatan V3.10.59.117 dan umumnya tersedia melalui pembaruan mandiri pada Desember 2021.

## <a name="update-release-38"></a>Pembaruan rilis 38

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**

- Pengecualian terjadi ketika panjang log set persetujuan melebihi 100.000 catatan.
- Pengguna tidak dapat mengakses **kisi Entri** Waktu dari halaman utama Entri **Waktu**.
- Kotak **dialog Impor** Entri Waktu tidak menampilkan teks apa pun saat tidak ada item yang memenuhi syarat untuk diimpor.
- Pengguna dapat membuat set persetujuan di mana **bidang Status** Target diatur ke **Tidak Diketahui**.

**Manajemen proyek**

- Kontur tidak ditampilkan dengan benar dalam penetapan sumber daya untuk UTC(+09:30) dan UTC(+10:00) saat waktu musim panas dimulai.
- Bidang **Kolom** Tambahan untuk struktur perincian kerja disembunyikan di beberapa lokasi.
- Pemilih tanggal untuk kontrol kalender di kisi Tugas **Proyek tidak dilokalkan** dengan benar untuk bahasa Mandarin.

**Penjualan**

- **Nilai Kinerja** Kontrak dan **Biaya** Aktual Proyek tidak cocok saat sumber daya yang dapat dipesan yang memiliki unit kontrak dan mata uang yang berbeda mengirimkan entri waktu.
- Alur kerja kustom untuk mengonfirmasi faktur secara otomatis gagal saat faktur diimpor sebagai solusi terkelola. Pesan berikut ditampilkan: "Microsoft.Xrm.Sdk.InvalidPluginExecutionExceptionException Message: Status faktur tidak valid."
- Ketika **Root** dipilih sebagai opsi ringkasan, dan proyek memiliki perkiraan dari campuran kelas transaksi (misalnya, kombinasi waktu, biaya, dan perkiraan material), sistem merangkum seluruh kelas transaksi sebagai satu jalur biaya.
- Dalam skenario di mana garis pengeluaran ditambahkan sebelum garis kontrak dikaitkan dengan proyek, harga yang benar tidak dimasukkan sebagai nilai default di **bidang Perbarui Harga**.
- Jumlah penjualan negatif tidak diperbolehkan pada **entitas Proyek** dan **Tugas**.
