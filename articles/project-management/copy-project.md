---
title: Menyalin proyek
description: Artikel ini menyediakan informasi tentang menyalin proyek di Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925768"
---
# <a name="copy-a-project"></a>Menyalin proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dengan Dynamics 365 Project Operations, Anda dapat dengan cepat membangun proyek baru dengan memilih **Salin Proyek** pada formulir **Proyek**. Untuk menyalin proyek, buka proyek yang akan disalin, lalu pilih **Salin proyek**. Tindakan akan menyalin yang berikut:

- Properti proyek 
- Struktur rincian kerja
- Anggota tim proyek
- Perkiraan proyek
- Estimasi pengeluaran proyek
- Estimasi bahan proyek
- Daftar Periksa Proyek
- Kelompok Proyek

## <a name="project-properties"></a>Properti proyek

Saat proyek disalin, nilai pada bidang berikut akan disalin.

| Bidang | Project Operations Bahan Non-Stok | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nama | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| yang terhormat | :heavy_check_mark: | :heavy_check_mark: | |
| Template kalender | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Mata uang | :heavy_check_mark: | :heavy_check_mark: | |
| Unit Kontrak | :heavy_check_mark: | :heavy_check_mark: | |
| Perusahaan Pemilik | :heavy_check_mark: | | |
| Manajer Proyek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Keseluruhan Status Proyek | :heavy_check_mark: | :heavy_check_mark: | |
| Komentar | :heavy_check_mark: | :heavy_check_mark: | |
| Estimasi | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Perkiraan Tanggal Mulai</p><p><strong>Catatan:</strong> Bidang ini menyebutkan tanggal ketika proyek dibuat dari salinan. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Perkiraan Tanggal Selesai</p><p><strong>Catatan:</strong> Tanggal dalam bidang ini disesuaikan berdasarkan tanggal mulai proyek baru yang dibuat dari salinan.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Upaya (Jam) | :heavy_check_mark: | :heavy_check_mark: | |
| Perkiraan Biaya Tenaga Kerja | :heavy_check_mark: | :heavy_check_mark: | |
| Perkiraan Biaya Pengeluaran | :heavy_check_mark: | :heavy_check_mark: | |
| Perkiraan Biaya Materi | | :heavy_check_mark: | |

> [!NOTE]
> Salin proyek adalah operasi yang berjalan lama. Rekaman proyek, atribut yang relevan, dan banyak entitas terkait juga disalin. Karena sifat operasi yang berjalan lama, setelah salinan dimulai, halaman proyek target dikunci untuk pengeditan hingga operasi penyalinan selesai.

## <a name="work-breakdown-structure"></a>Struktur rincian kerja

Saat proyek disalin, seluruh struktur rincian kerja berisi sumber daya disalin. Sumber daya bernama digantikan dengan sumber daya generik. Jika sumber daya bernama tidak memiliki jam kerja yang sama seperti sumber daya generik, jadwal akan dihitung ulang dan durasi tugas dapat berubah.

## <a name="project-team-members"></a>Anggota tim proyek

Bila tim proyek disalin dari proyek sumber, sumber daya generik akan disalin. Tugas sumber generik juga dikelola seperti proyek sumber. Sumber daya bernama akan dikonversi ke anggota tim generik.

> [!NOTE]
> Anggota tim dan penugasan tidak disalin di Project for the Web.

## <a name="estimates"></a>Estimasi

Bila proyek disalin, baris estimasi bahan, pengeluaran, dan sumber daya disalin dari proyek sumber. 

Untuk informasi tentang cara mengakses salinan proyek secara programatik, lihat [mengembangkan template proyek dengan salinan proyek](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Kuotasi dan kontrak

Kuotasi dan kontrak tidak ditautkan ke proyek tujuan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
