---
title: Mode penjadwalan
description: Topik ini menyediakan informasi tentang mode penjadwalan.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588418"
---
# <a name="scheduling-modes"></a>Mode penjadwalan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Dynamics 365 Project Operations memberikan kemampuan bagi organisasi untuk menentukan cara mengelola perubahan pada variabel utama dalam tugas dalam struktur perincian kerja. Berdasarkan kebutuhan organisasi yang spesifik, Manajer Proyek dapat membuat perubahan pada mode penjadwalan saat proyek dibuat.

Ada tiga mode penjadwalan yang tersedia di Project Operations:

  - Durasi tetap (ini adalah mode default)
  - Upaya tetap (*Pekerjaan*)
  - Unit tetap

Nilai yang dipengaruhi oleh definisi mode penjadwalan tertentu ditentukan oleh rumus berikut:

  Upaya = Durasi x Unit

Saat menentukan mode penjadwalan proyek, Anda menetapkan salah satu nilai ini, yang kemudian tidak dapat diubah. Mempertahankan nilai ini sebagai konstanta menempatkan prioritas pada nilai tersebut, yang akan memberitahukan sistem untuk tidak mengubahnya ketika kedua nilai lainnya berubah. Tabel berikut memberikan informasi tentang dampak memilih mode tertentu.

| **Dalam tugas ini**             | **Jika Anda merevisi unit**   | **Jika Anda merevisi durasi** | **Jika Anda merevisi upaya**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tugas Unit tetap     | Durasi akan dihitung ulang. | Upaya akan dihitung ulang.    | Durasi akan dihitung ulang. |
| Tugas Upaya tetap    | Durasi akan dihitung ulang. | Unit akan dihitung ulang.    | Durasi akan dihitung ulang. |
| Tugas Durasi tetap  | Upaya akan dihitung ulang.   | Upaya akan dihitung ulang.    | Unit akan dihitung ulang.   |

Untuk informasi lebih lanjut tentang dampak mode tertentu, lihat [Mengubah jenis tugas untuk penjadwalan yang lebih akurat](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Dalam topik, istilah **Pekerjaan** digunakan, bukan **Upaya**.

## <a name="change-the-organizations-scheduling-mode"></a>Mengubah mode penjadwalan organisasi

Selesaikan langkah-langkah berikut untuk menentukan mode penjadwalan organisasi.

1. Buka **Parameter** \> **Umum** \> **Pengaturan**, lalu pilih parameter proyek. 
2. Pada halaman **Parameter Proyek**, pilih mode penjadwalan default untuk organisasi, lalu tentukan kemampuan manajer Proyek untuk menimpa pengaturan saat membuat proyek baru.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Mengubah pengaturan mode penjadwalan pada proyek

Jika organisasi mengizinkan Manajer proyek menimpa mode penjadwalan default, manajer proyek dapat membuat perubahan tersebut saat mereka membuat proyek baru. Namun, setelah proyek disimpan, mode penjadwalan tidak dapat diubah.

## <a name="copied-projects"></a>Proyek yang disalin

Karena proyek dibuat saat tindakan salin proyek dilakukan, manajer proyek tidak dapat mengatur mode penjadwalan. Proyek tujuan akan selalu diatur default ke mode yang ditentukan pada tingkat organisasional.

## <a name="copied-tasks"></a>Tugas yang disalin

Ketika tugas disalin dari satu proyek ke proyek lain, tugas mewarisi mode penjadwalan proyek tujuan.
