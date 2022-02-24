---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 27, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 27, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 7f05b082e7c67937c78c82dcd9e094ee3b989e94
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948513"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 27. Versi ini memiliki nomor pembuatan V3.10.45.98 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2021.

## <a name="update-release-27"></a>Pembaruan rilis 27

### <a name="bug-fixes"></a>Perbaikan bug

**Umum**

Masalah berikut telah diperbaiki:

- Log yang dihasilkan oleh plug-in di Project Service Automation belum disetel ke penghapusan otomatis.
- Peningkatan otomatis gagal karena solusi Project Service Automation berisi NavBarArea null lama dan elemen judul.

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Kisi **Entri Waktu** menampilkan data yang salah untuk perilaku tanggal **TimeZone Independen**.
- Kisi **Entri Waktu** membuat waktu yang salah untuk perilaku tanggal **TimeZone Independen**.
- Pencarian tugas tidak terbatas pada proyek yang dipilih pada halaman **Edit Entri Waktu**.
- Persetujuan waktu untuk entri waktu nonproyek diblokir karena sistem sedang mencari pemberi izin proyek.
- Entri yang benar pada Aktual menampilkan pesan kesalahan yang salah.
- Ketika tugas berisi nilai kosong untuk biaya aktual dan total proyek disegarkan, kesalahan berikut terjadi, "Kunci yang diberikan tidak ada dalam kamus".
- Dalam kasus tertentu, Filter **Kelompokkan Menurut** pada tab **Perkiraan Proyek** tidak menampilkan estimasi pengeluaran.
- Interval **waktu musim panas** tidak benar untuk entri waktu.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Penyempurnaan cache, yang meningkatkan kinerja yang terkait dengan pemuatan halaman **Proyek**.
- Aturan bisnis usang mencegah tugas proyek diselesaikan.
- Kontur Add-in Proyek Microsoft tidak menghormati kalender add-in yang mengakibatkan persyaratan sumber daya yang salah.
- Membuat proyek dari templat telah salah menetapkan tanggal penugasan dan mencegah kemampuan untuk menghasilkan persyaratan sumber daya.
- Pengguna tidak dapat mengakses Opsi **Kategori**, **Deskripsi**, **status** dengan menggunakan keyboard.
- Nilai penjualan aktual proyek tidak termasuk nilai penjualan biaya dan material.
- Agregasi penjualan aktual dan biaya aktual terjadi dengan salah dengan nilai tukar yang berbeda.
- Deskripsi dalam **Templat Jam Kerja Default** menyesatkan.
- Indentasi tugas tidak menghapus **Kategori** di antarmuka pengguna hingga disegarkan.
- Validasi yang hilang untuk memastikan memindahkan proyek di luar tanggal akhir tidak diizinkan.

**Sales**

Masalah berikut telah diperbaiki:

- Pengecualian referensi null dihasilkan pada baris kuotasi proyek karena **Impor dari Estimasi Proyek** terlihat saat proyek belum dipilih.
- Kesalahan berikut, "Referensi objek tidak diatur ke instans objek" terjadi saat menutup kuotasi sebagai **Menang**.
- Status penyesuaian tidak diatur selama pembalikan aktual saat melepas tautan proyek dari baris kontrak.
- Ketika Dynamics 365 Field Service dan Project Service Automation diinstal, opsi **Kunci harga**, dan **Gunakan Harga Saat** Ini tidak ditampilkan pada saat yang sama di halaman **Faktur**.
- Untuk bahasa Jepang, ada terjemahan yang tidak konsisten dengan halaman berbasis kalender lainnya.
- **Aktifkan** dan **Nonaktifkan** telah dihapus dari entitas **Asosiasi Daftar Harga** di Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]