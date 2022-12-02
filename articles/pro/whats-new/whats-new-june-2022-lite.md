---
title: Terbaru Juni 2022 - Penyebaran Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam penyebaran Microsoft Dynamics 365 Project Operations lite yang rilis pada Juni 2022.
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

- Project Operations di lingkungan Dataverse versi 4.43.0.77 or 4.43.0.119

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Membuat subkontrak | 2708885 | Memperbaiki pesan kesalahan yang muncul saat pengguna membuat rekaman header pemesanan sumber daya yang dapat dipesan dengan sumber daya yang tidak dapat dipesan. |
| Perencanaan dan pelacakan proyek | 2629441 | Mengoreksi logika pemicu alur kerja untuk membantu mencegah perulangan tak terbatas saat tugas proyek diperbarui. |
| Waktu dan pengeluaran | 2641209 | Impor entri waktu dari penetapan/pemesanan harus mempertahankan referensi sumber daya yang dapat dipesan. |
| Perencanaan dan pelacakan proyek | 2651148 | Header dokumen proyek harus dilindungi.|
| Perencanaan dan pelacakan proyek | 2653145 | Validasi yang ditambahkan untuk memastikan bahwa rekaman proyek tidak dapat dibuat yang memiliki karakter yang tidak valid atas namanya. |
| Waktu dan pengeluaran | 2654710 | Mengoreksi pemfilteran pada halaman **Persetujuan**. |
| Penagihan dan harga | 2667805 | Menambahkan Validasi untuk membantu mencegah aktual penjualan yang ditagih dibuat jika aktual penjualan belum ditagih pendukung tidak ada. |
| Penagihan dan harga | 2668378 | Menambahkan Validasi untuk membantu mencegah dimensi harga kustom tidak ditambahkan, kecuali jika nama logis dan nama bidang diisi. |
| Waktu dan pengeluaran | 2700428 | Meningkatkan logika persetujuan untuk memastikan bahwa set persetujuan lain untuk proyek dapat diproses meskipun salah satu dari set persetujuan terjebak dalam pekerjaan sistem. |
