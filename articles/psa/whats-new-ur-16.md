---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 16, V3
description: Artikel ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926504"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation Pembaruan Rilis 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.  Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui solusi pilihan](/dynamics365/project-service/upgrade-psa-home-page).
Artikel ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 16. Versi ini memiliki nomor pembuatan V3.10.6.34 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2020.


## <a name="update-release-16"></a>Pembaruan rilis 16

### <a name="bug-fixes"></a>Perbaikan bug

-   Waktu dan Pengeluaran

    -   Diperbaiki pengguna yang mencoba mengirimkan entri waktu dan pengeluaran yang dihapus untuk persetujuan sekarang akan menerima pesan kesalahan yang relevan.

-   Manajemen proyek

    -   Diperbaiki: unit sumber daya yang ditentukan untuk anggota tim di template dihormati dengan template yang diterapkan ke proyek baru.

    -   Diperbaiki: peningkatan penanganan penugasan ulang kepemilikan rekaman.

    -   Diperbaiki: proyek yang ada dalam proses yang sedang disalin tidak akan diizinkan untuk disalin hingga semua operasi penyalinan selesai.

-   Manajemen sumber daya

    -   Diperbaiki" memperpanjang Pemesanan sekarang menangani durasi singkat dengan benar dan tidak lagi membuat nol jam untuk pemesanan diperpanjang.

    -   Diperbaiki: tampilan rekonsiliasi sekarang dirender saat zona waktu proyek adalah + 5:30 GMT dan zona waktu pengguna berbeda.

-   Sales

    -   Diperbaiki: saat proyek yang dipetakan ke baris kontrak dihapus dan proyek baru dipetakan, rekaman aktual pada proyek baru tidak dievaluasi ulang berdasarkan aturan penagihan dan harga yang ditentukan pada baris kontrak. Ini telah diperbaiki dalam rilis ini. Harga dan rekaman aktual pada proyek yang baru dipetakan akan dibalik dan dibuat ulang dengan benar berdasarkan aturan harga dan penagihan baris kontrak. Rekaman aktual proyek yang tidak dipetakan juga akan dievaluasi ulang dan dibuat ulang sebagai konsekuensinya.

    -   Diperbaiki: validasi tambahan telah ditambahkan ke bidang **jumlah** baris perkiraan untuk memastikan bahwa nilai null tidak dipertahankan.

    -   Diperbaiki: saat aktual telah diperbarui pada proyek, tombol refresh telah ditambahkan ke formulir utama proyek untuk memungkinkan pengguna mensinkronisasi ulang aktual.

    -   Diperbaiki: saat pengguna beralih dari 2. X ke 3. X, proyek dengan nilai NULL untuk nama proyek akan diizinkan.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
