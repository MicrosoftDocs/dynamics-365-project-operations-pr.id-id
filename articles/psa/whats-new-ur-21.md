---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 21, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002331"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation Pembaruan Rilis 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 21. Versi ini memiliki nomor pembuatan V 3.10.32.50 dan umumnya tersedia melalui pembaruan mandiri pada Juni 2020.

## <a name="update-release-21"></a>Pembaruan rilis 21

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Ketika menghosting **kontrol kisi entri waktu** di dasbor, kisi tidak menggunakan lebar penuh kontainer kisi dasbor.
- Untuk zona waktu tertentu, kontrol kisi **entri waktu** tidak menampilkan rekaman.
- Entri waktu setelah 9:00 PM muncul pada hari yang salah.
- Pengguna tidak dapat mengajukan pengeluaran jika kategori pengeluaran, **tanda terima pengeluaran yang diperlukan** tidak memiliki nilai.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- Pemesanan tidak aktif ditampilkan dalam tampilan **rekonsiliasi**.
- Pemenuhan sumber daya umum kehilangan validasi untuk memastikan bahwa status pemesanan yang valid itu ada.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Kisi formulir **proyek** (**penetapan sumber daya**, **tugas**, tampilan **rekonsiliasi**, **perkiraan pengeluaran**) tetap dapat diedit bahkan saat proyek tidak aktif.
- Pelanggan duplikat tidak dapat digabungkan dengan pelanggan yang ditautkan ke kontrak proyek yang telah dikonfirmasi.
- Bila sumber daya yang belum memiliki kalender yang valid ditambahkan, sistem tidak memberikan pesan kesalahan yang mudah digunakan pengguna.
- Tombol **Tambah tugas** pada kisi tugas diaktifkan saat proyek ditautkan ke **Add-In Microsoft Project**.
- Upaya bertumbuh tak terkendali bila tugas dengan kategori ditetapkan ke sumber daya dengan peran yang telah ditentukan harga biayanya.

**Sales**

Penyempurnaan berikut telah dilakukan:

- **Frekuensi faktur** dan **awal penagihan** telah dipindahkan ke tab **jadwal faktur**.

Masalah berikut telah diperbaiki:

- **Total harga penjualan** adalah nol (0) untuk **kategori** meskipun **peran** memiliki total harga penjualan yang bukan nol.
- Pelanggan tidak dapat mengubah nilai bidang **status faktur** menjadi **siap untuk faktur** saat proses kustom lain memperbarui bidang tambahan.
- Tombol **Segarkan baris faktur** dapat membuat beberapa baris duplikat jika berulang kali dipilih.
- Tombol **Perbarui Harga** tidak berfungsi pada subgrid **Harga Peran** dalam formulir **Tampilan Cepat**.
- Logika **resolusi daftar harga penjualan** menangani zona waktu dengan tidak baik, sehingga pilihan daftar harganya salah.
- Biaya **total aktual proyek** dapat dinonaktifkan dengan jumlah pecahan setelah entri satu kali disetujui.
- Logika **resolusi harga** tidak menyediakan pesan kesalahan yang mudah digunakan jika **Harga Peran yang Diperoleh** tidak memiliki nilai pada bidang **'unit utama'** dan **'harga di unit utama'**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]