---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 22, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006560"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation Pembaruan Rilis 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 22. Versi ini memiliki nomor pembuatan V 3.10.33.48 dan umumnya tersedia melalui pembaruan mandiri pada Juni 2020.

## <a name="update-release-22"></a>Pembaruan rilis 22

### <a name="bug-fixes"></a>Perbaikan bug



**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- **Entri waktu** tidak secara otomatis ditambahkan dalam jadwal entri waktu setelah impor.
- pemilih tanggal kisi **Entri waktu** tidak mengenali pengaturan wilayah pengguna.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- Dalam mode manual, perubahan kontur **tugas sumber daya** tidak dikenali saat menghasilkan **kebutuhan sumber daya**.
- **Permintaan sumber daya** tidak mendukung status permintaan kustom.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Menggunakan klik dua kali pada EstimateGridControl tidak akan dengan benar mengurai nomor format Belanda.
- Jam yang ditetapkan tidak diperbarui dengan benar saat penetapan diubah menggunakan Add-in klien desktop Microsoft Project.
- Pelacakan proyek dan perkiraan kisi menampilkan kode mata uang penjualan yang salah ketika mata uang kontrak berbeda dari mata uang pelanggan dan organisasi dikonfigurasi untuk menampilkan kode mata uang dan bukan simbol mata uang.
- Tanggal selesai anggota tim akan ditambahkan satu hari jika jadwal jam kerja adalah 24 jam per hari.
- Pada jadwal proyek, menambahkan kategori transaksi ke tugas tidak memicu Simpan otomatis.
- Kesalahan berikut ditampilkan saat menambahkan anggota tim ke template proyek: "Persyaratan sumber daya tidak dapat dikaitkan dengan template proyek". 
- Skrip aturan pita "msdyn.Approval.CanApproveOrReject"menampilkan kesalahan batas waktu.

**Sales**

Masalah berikut telah diperbaiki:

- Pesan kesalahan validasi tidak ditampilkan bila daftar harga biaya dipilih dalam pencarian daftar harga pada formulir/entitas 'daftar harga proyek kuotasi baru'.
- Penutupan kuotasi sebagai menang tidak menavigasi ke kontrak yang dibuat jika BPF yang melekat pada kuotasi berada dalam tahapan akhir.
- Membalikkan **penjualan yang belum ditagih** ditautkan ke biaya awal bila entri waktu dipanggil.
- Setelah memilih tombol **konfirmasikan**, status faktur tidak akan diubah ke **dikonfirmasi** kecuali faktur diperbarui.


[!INCLUDE[footer-include](../includes/footer-banner.md)]