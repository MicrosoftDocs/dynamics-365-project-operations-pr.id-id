---
title: Menyalin proyek
description: Topik ini menyediakan informasi tentang menyalin proyek di Dynamics 365 Project operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908253"
---
# <a name="copy-a-project"></a>Menyalin proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dengan Dynamics 365 Project Operations, Anda dapat dengan cepat membangun proyek baru dengan menggunakan tindakan **Salin proyek** pada **proyek**. Untuk menyalin proyek, pilih proyek, lalu pilih **Salin**. Tindakan akan menyalin:

- Properti proyek
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