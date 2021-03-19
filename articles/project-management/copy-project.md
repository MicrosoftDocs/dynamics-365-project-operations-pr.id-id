---
title: Menyalin proyek
description: Topik ini menyediakan informasi tentang menyalin proyek di Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479523"
---
# <a name="copy-a-project"></a>Menyalin proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dengan Dynamics 365 Project Operations, Anda dapat dengan cepat membangun proyek baru dengan memilih **Salin Proyek** pada formulir **Proyek**. Untuk menyalin proyek, buka proyek yang akan disalin, lalu pilih **Salin proyek**. Tindakan akan menyalin:

- Properti proyek (Perkiraan tanggal mulai disalin dari proyek sumber)
- Struktur rincian kerja
- Anggota tim proyek
- Perkiraan proyek
- Estimasi pengeluaran proyek

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
- Perkiraan
- Perkiraan Tanggal Mulai
- Tanggal Berakhir
- Upaya (Jam)
- Perkiraan Biaya Tenaga Kerja
- Perkiraan Biaya Pengeluaran

## <a name="work-breakdown-structure"></a>Struktur rincian kerja

Saat proyek disalin, seluruh struktur rincian kerja berisi sumber daya disalin. Sumber daya bernama digantikan dengan sumber daya generik. Jika sumber daya bernama tidak memiliki jam kerja yang sama seperti sumber daya generik, jadwal akan dihitung ulang dan durasi tugas dapat berubah.

## <a name="project-team-members"></a>Anggota tim proyek

Bila tim proyek disalin dari proyek sumber, sumber daya generik akan disalin. Tugas sumber generik juga dikelola seperti proyek sumber. Sumber daya bernama akan dikonversi ke anggota tim generik.

## <a name="estimates"></a>Perkiraan

Saat proyek disalin, baris sumber daya maupun perkiraan pengeluaran disalin dari proyek sumber. 

Untuk informasi tentang cara mengakses salinan proyek secara programatik, lihat [mengembangkan template proyek dengan salinan proyek](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
