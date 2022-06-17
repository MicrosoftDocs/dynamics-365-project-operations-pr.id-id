---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 38, V3
description: Artikel ini mencantumkan fitur dan perbaikan yang tersedia di Microsoft Dynamics 365 Project Service Automation Rilis Pembaruan 38, V3.
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915189"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Aplikasi ini kompatibel dengan Dynamics 365 9.x. Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini mencantumkan fitur dan perbaikan yang baru atau diubah untuk Project Service Automation Update Release 38, V3. Versi ini memiliki nomor pembuatan V3.10.59.117 dan umumnya tersedia melalui pembaruan mandiri pada Desember 2021.

## <a name="update-release-38"></a>Pembaruan rilis 38

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**

- Pengecualian terjadi ketika panjang log set persetujuan melebihi 100.000 rekaman.
- Pengguna tidak dapat mengakses **kisi Entri** Waktu dari halaman utama Entri **Waktu**.
- Kotak **dialog Impor** Entri Waktu tidak memperlihatkan teks apa pun saat tidak ada item yang memenuhi syarat untuk diimpor.
- Pengguna dapat membuat kumpulan persetujuan di **mana bidang Status** Target diatur ke **Tidak Diketahui**.

**Manajemen proyek**

- Kontur tidak ditampilkan dengan benar dalam penugasan sumber daya untuk UTC(+09:30) dan UTC(+10:00) saat waktu musim panas dimulai.
- Bidang **Kolom** Tambahan untuk struktur rincian kerja disembunyikan di beberapa lokasi.
- Pemilih tanggal untuk kontrol kalender dalam kisi Tugas **Proyek tidak dilokalkan** dengan benar untuk bahasa Mandarin.

**Penjualan**

- **Nilai Kinerja** Kontrak dan **Biaya** Aktual Proyek tidak cocok ketika sumber daya yang dapat dipesan yang memiliki unit kontrak dan mata uang yang berbeda mengirimkan entri waktu.
- Alur kerja kustom untuk mengonfirmasi faktur secara otomatis gagal saat faktur diimpor sebagai solusi terkelola. Pesan berikut ditampilkan: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Status faktur tidak valid."
- Ketika **Root** dipilih sebagai opsi ringkasan, dan proyek memiliki perkiraan dari campuran kelas transaksi (misalnya, kombinasi waktu, pengeluaran, dan perkiraan material), sistem merangkum di seluruh kelas transaksi sebagai satu baris biaya.
- Dalam skenario di mana garis pengeluaran ditambahkan sebelum garis kontrak dikaitkan dengan proyek, harga yang benar tidak dimasukkan sebagai nilai default di **bidang Harga** Pembaruan.
- Jumlah penjualan negatif tidak diperbolehkan pada **entitas Proyek** dan **Tugas**.
