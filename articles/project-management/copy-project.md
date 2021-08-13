---
title: Menyalin proyek
description: Topik ini menyediakan informasi tentang menyalin proyek di Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007195"
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

## <a name="project-properties"></a>Properti proyek

Saat proyek disalin, nilai pada bidang berikut akan disalin:

- Nama
- KETERANGAN
- Pelanggan
- Template kalender
- Mata uang
- Unit Kontrak
- Manajer Proyek
- Status
- Keseluruhan Status Proyek
- Komentar
- Estimasi
- Estimasi Tanggal Mulai: Tanggal proyek dibuat dari salinan.
- Estimasi Tanggal Selesai: Tanggal ini disesuaikan berdasarkan tanggal mulai proyek baru yang dibuat dari salinan.
- Upaya (Jam)
- Perkiraan Biaya Tenaga Kerja
- Perkiraan Biaya Pengeluaran
- Perkiraan Biaya Materi

> [!NOTE]
> Salin proyek adalah operasi yang berjalan lama. Rekaman proyek, atribut yang relevan, dan banyak entitas terkait juga disalin. Karena sifat operasi yang berjalan lama, setelah salinan dimulai, halaman proyek target dikunci untuk pengeditan hingga operasi penyalinan selesai.

## <a name="work-breakdown-structure"></a>Struktur rincian kerja

Saat proyek disalin, seluruh struktur rincian kerja berisi sumber daya disalin. Sumber daya bernama digantikan dengan sumber daya generik. Jika sumber daya bernama tidak memiliki jam kerja yang sama seperti sumber daya generik, jadwal akan dihitung ulang dan durasi tugas dapat berubah.

## <a name="project-team-members"></a>Anggota tim proyek

Bila tim proyek disalin dari proyek sumber, sumber daya generik akan disalin. Tugas sumber generik juga dikelola seperti proyek sumber. Sumber daya bernama akan dikonversi ke anggota tim generik.

## <a name="estimates"></a>Estimasi

Bila proyek disalin, baris estimasi bahan, pengeluaran, dan sumber daya disalin dari proyek sumber. 

Untuk informasi tentang cara mengakses salinan proyek secara programatik, lihat [mengembangkan template proyek dengan salinan proyek](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
