---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 30, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852863"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 30. Versi ini memiliki nomor pembuatan V3.10.51.61 dan umumnya tersedia melalui pembaruan mandiri pada April 2021.

## <a name="update-release-30"></a>Pembaruan rilis 30

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Kesalahan terjadi saat Anda membuat dan menyimpan entri waktu pada halaman **Buat Cepat** jika bidang **Peran** dihilangkan.
- Filter Entri Waktu menerapkan operator filter yang salah.
- Lembar waktu yang disalin tidak akan secara otomatis ditampilkan bila Anda memilih **Salin Pekan** pada kontrol entri waktu.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- Saat Anda memperpanjang masa pemesanan, status pemesanan yang ditetapkan ke pemesanan definitif salah. Memperluas pemesanan sesuai status pemesanan yang didefinisikan sebagai **Berkomitmen** dalam metadata konfigurasi pemesanan.
- Bila status pemesanan yang valid tidak ditentukan, pesan kesalahan tidak dilokalkan dengan benar.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Proyek tidak dapat dibuat dalam satu mata uang dan mencakup tugas terkait dalam mata uang lain.

**Penjualan**

Masalah berikut telah diperbaiki:

- Bila daftar harga disalin, harga tidak diperbarui.
- Menutup kuotasi sebagai menang gagal bila detail biaya memiliki nilai untuk asal.
- Pada entitas **Tugas Proyek**, **Perkiraan Biaya** telah diubah namanya menjadi **Biaya Terencana (Dasar)**.
- Pengecualian referensi nihil dibuat saat faktur dibuat atau dihapus.
