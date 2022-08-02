---
title: Terbaru Juni 2022 - Penyebaran Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Juni 2022 penyebaran Microsoft Dynamics 365 Project Operations lite.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031197"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Terbaru Juni 2022 - Penyebaran Project Operations lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam Dataverse versi lingkungan 4.43.0.77 atau 4.43.0.119

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Subkontrak | 2708885 | Memperbaiki pesan kesalahan yang muncul saat pengguna membuat catatan header pemesanan sumber daya yang dapat dipesan di mana tidak ada sumber daya yang dapat dipesan yang diisi. |
| Perencanaan dan pelacakan proyek | 2629441 | Mengoreksi logika pemicu alur kerja untuk membantu mencegah loop tak terbatas saat tugas proyek diperbarui. |
| Waktu dan pengeluaran | 2641209 | Impor entri waktu dari penugasan/pemesanan harus menyimpan referensi sumber daya yang dapat dipesan. |
| Perencanaan dan pelacakan proyek | 2651148 | Header dokumen proyek harus dijaga.|
| Perencanaan dan pelacakan proyek | 2653145 | Menambahkan validasi untuk memastikan bahwa rekaman proyek tidak dapat dibuat yang memiliki karakter yang tidak valid dalam namanya. |
| Waktu dan pengeluaran | 2654710 | Mengoreksi pemfilteran pada **halaman Persetujuan**. |
| Penagihan dan harga | 2667805 | Menambahkan validasi untuk membantu mencegah aktual penjualan yang ditagih dibuat jika mendukung aktual penjualan yang tidak ditagih tidak ada. |
| Penagihan dan harga | 2668378 | Menambahkan validasi untuk membantu mencegah dimensi harga kustom ditambahkan kecuali nama logis dan nama bidang diisi. |
| Waktu dan pengeluaran | 2700428 | Meningkatkan logika persetujuan untuk memastikan bahwa set persetujuan lain untuk proyek dapat diproses bahkan jika salah satu set persetujuan terjebak dalam pekerjaan sistem. |
