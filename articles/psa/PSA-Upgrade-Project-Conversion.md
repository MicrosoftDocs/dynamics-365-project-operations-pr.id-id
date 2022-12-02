---
title: Proses konversi penjadwalan proyek Project Service Automation ke Project Operations
description: Artikel ini memberikan ringkasan perubahan fitur untuk Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642572"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proses konversi penjadwalan proyek Project Service Automation ke Project Operations

Setelah proyek berhasil ditingkatkan dari Microsoft Dynamics 365 Project Service Automation 3.X ke Dynamics 365 Project Operations Lite, pengeditan tugas proyek di struktur rincian kerja (WBS) kisi tugas tidak mungkin dilakukan. Pelanggan akan dapat meninjau WBS di kisi pelacakan dengan bidang baru telah ditambahkan untuk memberikan semua rincian yang terkait dengan tugas. Untuk proyek yang memerlukan pengeditan WBS, Anda dapat secara selektif mengkonversi proyek yang memenuhi syarat ke pengalaman penjadwalan baru Project for the Web.

## <a name="project-conversion-process"></a>Proses konversi proyek

Untuk mengonversikan proyek, Ikuti langkah berikut.

1. Buka halaman utama proyek, lalu pilih **Konversi** pada Panel Tindakan.
1. Di kotak konfirmasi, pilih **OK** untuk memulai konversi proyek. Tindakan berikut terjadi:

    1. Bilah pesan yang muncul di halaman utama proyek menyatakan, "Jadwal proyek sedang dikonversi. Anda tidak dapat membuat perubahan pada proyek hingga konversi selesai."
    1. Anda akan dialihkan ke daftar proyek.

    Setelah konversi proyek selesai, tindakan berikut terjadi:

    1. Manajer proyek yang ditugaskan menerima pemberitahuan di sisi kanan aplikasi.
    1. Bilah pesan yang menyatakan bahwa konversi sedang berlangsung akan dihilangkan.
    1. Tab **Jadwal** menampilkan pengalaman penjadwalan baru dengan Project for the Web. Pengguna mana pun yang memiliki lisensi dan peran keamanan yang sesuai dapat mengedit WBS.
    1. Bidang **mesin penjadwalan** diperbarui ke **Project for the Web**.
    1. Tombol **Konversi** akan dihilangkan dari Panel Tindakan.

> [!IMPORTANT]
> Konversi massal proyek tidak diizinkan. Setiap upaya untuk memperbarui volume besar proyek pada waktu yang sama akan dihambat. Pembatasan ini akan membantu memastikan kinerja tinggi untuk semua pelanggan.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tugas manual vs. tugas otomatis

Bila lingkungan ditingkatkan dari Project Service Automation ke Project Operations, semua tugas di WBS dianggap secara otomatis dijadwalkan. Konsep tugas terjadwal manual tidak tersedia di Project for the Web. Namun, Anda dapat menentukan perilaku penjadwalan yang diinginkan untuk proyek Dengan menggunakan pengaturan [mode penjadwalan](/project-management/scheduling-modes.md) saat Anda membuat proyek baru.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operasi yang dibatasi untuk proyek pra-konversi

Bagian ini menjelaskan perbedaan fungsi yang dapat Anda harapkan bila proyek belum dikonversi.

### <a name="copy-project"></a>Salin Proyek

Operasi **Salin** hanya didukung pada proyek yang dikonversi. Proyek yang ditingkatkan tidak dapat disalin sebelum konversi.

### <a name="move-project"></a>Pindahkan Proyek

Perubahan pada tanggal mulai proyek tidak akan secara proporsional memindahkan awal tugas kecuali jika proyek telah dikonversi.

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Apa perbedaan antara proyek yang dikonversi dan proyek baru yang dibuat setelah peningkatan selesai?

Untuk proyek yang dikonversi setelah lingkungan ditingkatkan, tanda akan ditetapkan yang akan menginstruksikan jadwal agar hanya memperhatikan kalender proyek. Perilaku ini sesuai dengan perilaku dalam Project Service Automation. Namun, tanda tidak akan ditetapkan untuk proyek baru yang dibuat setelah peningkatan. Oleh karena itu, jadwal akan memperhatikan jam kerja sumber daya saat ditetapkan ke tugas.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Apa yang harus dilakukan jika proyek gagal dikonversi?

Jika proyek Anda gagal dikonversi, langkah pertama adalah memeriksa log kesalahan untuk mengidentifikasi masalah umum yang terkait dengan WBS Anda. Jika log tidak menunjukkan kesalahan tertentu yang dapat Anda lakukan, hubungi Dukungan Pelanggan agar kasus Anda dapat ditinjau lebih lanjut.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Bagaimana penutupan bisnis yang ditangani di Project for the Web?

Project for the Web tidak memperhatikan penutupan bisnis yang ditentukan perusahaan pada tingkat organisasi. Namun, layanan ini akan memperhatikan jenis hari libur lainnya yang ditentukan dalam template jam kerja yang ditentukan.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Apa saja batasan Project for the Web?

Lihat [struktur rincian kerja untuk proyek: Keterbatasan Proyek](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Dapatkah saya mengharapkan perubahan pada estimasi biaya dan penjualan saya?

Dalam kasus yang jarang terjadi saat kontur penugasan sumber daya akan dihitung ulang atau jatuh pada batas tanggal yang berbeda dibandingkan proyek sumber, Anda mungkin melihat perbedaan dalam estimasi penjualan dan biaya. Sebagai bagian dari proses peningkatan, pelanggan diharapkan menguji rangkaian proyek sampel perwakilan, sehingga mereka dapat memahami kemungkinan perubahan jadwal.
