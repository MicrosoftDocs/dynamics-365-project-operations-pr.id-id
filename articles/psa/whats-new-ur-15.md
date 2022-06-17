---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 15, V3
description: Artikel ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Update Release 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915648"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation Pembaruan Rilis 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA). Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini mencantumkan fitur dan perbaikan yang baru atau berubah untuk PSA V3, Rilis Pembaruan 15. Versi ini memiliki nomor pembuatan V3.10.5.28 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2020.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
