---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 14, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 14 V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8504ac5a0ce7254baee9139e4407e712c758540d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594307"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation Pembaruan Rilis 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA). Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 14. Versi ini memiliki nomor pembuatan V3.10.4.21 dan tersedia pada jadwal berikut ini:

- **Ketersediaan umum (pembaruan mandiri):** Januari 2020
- **Pembaruan otomatis:** Februari 2020

## <a name="update-release-14"></a>Pembaruan rilis 14

### <a name="enhancements"></a>Peningkatan

- Sales

     - Nilai bidang kustom dari **detail baris kuotasi** disalin ke **detail baris kontrak proyek** saat kuotasi diperbarui ke **ditutup sebagai menang**.
     - Proyek yang dikonfirmasi dapat **ditutup sebagai kalah**.

- Manajemen sumber daya

     - Saat memperpanjang Pemesanan, pengguna akan diminta dengan kotak dialog konfirmasi untuk merangkum hasil Pemesanan dan menyediakan tautan untuk mempertahankan Pemesanan.


### <a name="bug-fixes"></a>Perbaikan bug

- Waktu dan Pengeluaran

     - Tetap: meningkatkan pengalaman pengguna saat pengguna belum memilih entri yang akan dikoreksi.

- Manajemen sumber daya

     - Tetap: Pemesanan sumber daya beberapa kali meluapkan nama sumber daya dapat dipesan.

- Sales

     - Tetap: Total harga penjualan tidak dihitung hingga pengguna juga memasukkan harga biaya untuk perkiraan pengeluaran pada suatu proyek.
     - Tetap: menutup kuotasi sebagai **menang** gagal jika kontrak proyek terkait tidak dalam status **draf**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
