---
title: Yang baru di Project Service Automation Rilis Pembaruan 15, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 15, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752433"
---
# <a name="project-service-automation-v3-update-release-15"></a>Project Service Automation V3, Pembaruan Rilis 15

Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA). Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 15. Versi ini memiliki nomor pembuatan V3.10.5.28 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2020.

## <a name="update-release-15"></a>Pembaruan rilis 15 

### <a name="enhancements"></a>Peningkatan

- Manajemen proyek

### <a name="bug-fixes"></a>Perbaikan bug

- Waktu dan Pengeluaran

  - Tetap: menambahkan penanganan kesalahan dalam beban di tampilan rekonsiliasi.
  - Tetap: Pusat sumber daya proyek: Ubah nama **jumlah** untuk mengurangi ambiguitas.
  - Tetap: Sesuaikan tampilan **kolom Salin entri waktu** untuk mencakup jenis.
  - Tetap: mengedit durasi entri waktu dalam tampilan kisi menggunakan hasil angka desimal dalam kesalahan yang tidak diketahui untuk sejumlah nomor.

- Manajemen proyek

  - Tetap: menu drop-down untuk **gunakan dalam tampilan pelacakan** sekarang diperluas berdasarkan lebar pilihan.
  - Tetap: saat mengelola proyek di zona waktu + 13, penghitungan tugas dapat menampilkan hasil yang tidak akurat.
  - Tetap: **waktu berakhir anggota tim** telah dikoreksi saat menggunakan kalender 24 jam.
  - Tetap: Mengaktifkan kembali **BPF** di formulir utama **msdyn_project**.
  - Tetap: penghitungan tugas tidak lagi mengabaikan satu hari.
  - Tetap: banner pemberitahuan baru telah ditambahkan ke formulir proyek saat zona waktu berbeda antara pengguna dan proyek.

- Sales

  - Tetap: pencarian kategori perkiraan biaya dapat digunakan untuk memfilter duplikat.
  - Tetap: kode di **PluginDomain.ExecuteInTryCatchBlock(..)** tidak lagi menyembunyikan asal pengecualian.
  - Tetap: tidak lagi mendapatkan pesan kesalahan dalam **pencarian proyek** dalam formulir **baris kuotasi** saat terdapat lebih dari 1000 proyek.
  - Tetap: kisi **perkiraan** untuk perkiraan tenaga kerja dan perkiraan biaya sekarang menampilkan simbol mata uang yang benar.
  - Tetap: setelah organisasi pembaruan PSA dari rilis pembaruan 14 ke rilis pembaruan 15, tab **jadwal** tidak lagi ditampilkan sebagai kosong pada formulir **proyek**.
