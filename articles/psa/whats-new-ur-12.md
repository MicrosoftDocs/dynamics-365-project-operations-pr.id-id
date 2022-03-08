---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 12, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 12, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 5f05488a652f7a699aaa5d8e644eae38d7083f404d3c461cdaabd1915b1a710a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004495"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation Pembaruan Rilis 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA). Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 12. Versi ini memiliki nomor pembuatan V 3.10.2.34 dan umumnya tersedia melalui pembaruan mandiri pada Oktober 2019.

## <a name="update-release-12"></a>Pembaruan rilis 12

### <a name="bug-fixes"></a>Perbaikan bug

- Waktu dan Pengeluaran

    - Tetap: pesan kesalahan entri waktu telah diperbarui dengan konteks yang lebih relevan.
    - Tetap: waktu entri kisi dan jadwal dengan benar menampilkan bilah penggulir vertikal bila diperlukan.
    - Tetap: Entri waktu yang biaya yang diajukan dapat disetujui.
    - Tetap: pesan dialog konfirmasi pembatalan persetujuan telah diperbaiki untuk mencerminkan status persetujuan bila diubah **dari disetujui** untuk **dikirim**.
    - Tetap: Bidang **harga**, **unit**, dan **kuantitas** sekarang terkunci pada rekaman pengeluaran setelah disetujui.

- Manajemen proyek

    - Tetap: tindakan **baru** pada formulir utama **anggota tim** telah dihapus.
    - Tetap: tugas sumber daya telah diperbarui ke akun untuk kesalahan pembulatan yang tidak akurat, yang menyebabkan pergeseran pada tanggal berakhir tugas.
    - Tetap: di kisi tugas, kesalahan sisi server yang relevan akan muncul ke pengguna.
    - Tetap: nama anggota tim sekarang dirender dalam pemilih tugas, bukan nama posisi.

- Manajemen sumber daya

    - Tetap: rincian kebutuhan sumber daya untuk proyek yang dibuat dari template sekarang menggunakan kalender proyek.
    - Tetap: keterampilan dan kompetensi sekarang default dari data Master peran ke persyaratan sumber daya yang dibuat untuk peran tersebut.

- Sales

    - Tetap: id objek duplikat yang ditemukan pada formulir **utama kontrak**.
    - Tetap: logika telah diperbarui untuk membuat tab **analisis kuotasi** terlihat sehingga menampilkan konfigurasi metadata tab.
    - Tetap: tanggal akuntansi pada rekaman aktual sekarang berasal dari tanggal waktu/tanggal entri pengeluaran dan bukan tanggal persetujuan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]