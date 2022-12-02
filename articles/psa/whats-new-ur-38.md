---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 38, V3
description: Artikel ini berisi fitur dan perbaikan yang tersedia dalam Rilis Pembaruan Microsoft Dynamics 365 Project Service Automation 38, V3.
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

Artikel ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 38, V3. Versi ini memiliki nomor pembuatan V3.10.59.117 dan umumnya tersedia melalui pembaruan mandiri pada Desember 2021.

## <a name="update-release-38"></a>Pembaruan rilis 38

### <a name="bug-fixes"></a>Perbaikan bug

Masalah berikut telah diperbaiki.

**Waktu dan Pengeluaran**

- Pengecualian terjadi bila panjang log kumpulan persetujuan melebihi 100.000 rekaman.
- Pengguna tidak dapat mengakses kisi **Entri Waktu** dari halaman utama **Entri Waktu**.
- Kotak dialog **Impor Entri Waktu** tidak menampilkan teks bila tidak ada item yang memenuhi syarat untuk impor.
- Pengguna dapat membuat penetapan persetujuan dengan bidang **Status Target** diatur ke **Tidak Dikenal**.

**Manajemen proyek**

- Kontur tidak ditampilkan dengan benar pada penugasan sumber daya untuk UTC(+09:30) dan UTC(+10:00) saat daylight saving time dimulai.
- Bidang **Kolom Tambahan** untuk struktur rincian kerj atersembunyi di beberapa lokal.
- Pemilih tanggal untuk kontrol kalender di kisi **Tugas Proyek** tidak dilokalkan dengan benar untuk bahasa Tionghoa.

**Penjualan**

- **Nilai performa Kontrak** dan **Biaya Aktual Proyek** tidak sesuai dengan sumber daya yang dapat dipesan dengan unit kontrak dan mata uang yang berbeda mengajukan entri waktu.
- Alur kerja kustom untuk secara otomatis mengkonfirmasikan faktur gagal saat faktur diimpor sebagai solusi terkelola. Pesan berikut ditampilkan: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Invalid invoice status"
- Bila **Root** dipilih sebagai pilihan ringkasan, dan proyek memiliki estimasi dari campuran kelas transaksi (misalnya, kombinasi waktu, pengeluaran, dan estimasi bahan), sistem merangkum seluruh kelas transaksi sebagai satu baris biaya.
- Dalam skenario penambahan baris pengeluaran sebelum baris kontrak dikaitkan dengan proyek, harga yang benar tidak dimasukkan sebagai nilai default dalam bidang **Perbarui Harga**.
- Jumlah penjualan negatif tidak diizinkan pada entitas **Proyek** dan **Tugas**.
