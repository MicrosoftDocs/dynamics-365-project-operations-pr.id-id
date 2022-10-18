---
title: Project Service Automation ke Project Operations proses konversi penjadwalan proyek
description: Artikel ini memberikan gambaran umum tentang perubahan fitur untuk Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation ke Project Operations proses konversi penjadwalan proyek

Setelah proyek berhasil ditingkatkan dari Microsoft Dynamics 365 Project Service Automation 3.X ke Dynamics 365 Project Operations Lite, mengedit tugas proyek dalam struktur rincian kerja kisi tugas (WBS) tidak dimungkinkan. Pelanggan akan dapat meninjau WBS di jaringan pelacakan tempat bidang baru telah ditambahkan untuk memberikan semua detail yang terkait dengan tugas tersebut. Untuk proyek di mana pengeditan ke WBS diperlukan, Anda dapat secara selektif mengonversi proyek yang memenuhi syarat ke Proyek baru untuk pengalaman penjadwalan web.

## <a name="project-conversion-process"></a>Proses konversi proyek

Untuk mengonversi proyek, ikuti langkah-langkah berikut.

1. Buka halaman utama proyek, dan pilih **Konversi** pada Panel Tindakan.
1. Dalam kotak pesan konfirmasi, pilih **OK** untuk memulai konversi proyek. Tindakan berikut terjadi:

    1. Bilah pesan yang muncul di halaman utama proyek menyatakan, "Jadwal proyek sedang dikonversi. Anda tidak dapat membuat perubahan pada proyek sampai konversi selesai."
    1. Anda akan diarahkan ke daftar proyek.

    Setelah konversi proyek selesai, tindakan berikut terjadi:

    1. Manajer proyek yang ditugaskan menerima pemberitahuan di sisi kanan aplikasi.
    1. Bilah pesan yang menyatakan bahwa konversi sedang berlangsung akan dihapus.
    1. Tab **Jadwal** memperlihatkan pengalaman penjadwalan baru dengan Project untuk web. Setiap pengguna yang memiliki lisensi dan peran keamanan yang sesuai dapat mengedit WBS.
    1. **Bidang Mesin** penjadwalan diperbarui ke **Project untuk web**.
    1. Tombol **Konversi** dihapus dari Panel Tindakan.

> [!IMPORTANT]
> Konversi massal proyek tidak diizinkan. Setiap upaya untuk memperbarui sejumlah besar proyek pada saat yang sama akan dibatasi. Keterbatasan ini membantu memastikan kinerja tinggi untuk semua pelanggan.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tugas manual vs. tugas otomatis

Ketika lingkungan ditingkatkan dari Project Service Automation ke Operasi Proyek, semua tugas di WBS dianggap dijadwalkan secara otomatis. Konsep tugas yang dijadwalkan secara manual tidak tersedia di Project untuk web. Namun, Anda dapat menentukan perilaku penjadwalan yang disukai untuk proyek Anda dengan menggunakan [pengaturan mode](/project-management/scheduling-modes.md) penjadwalan saat Anda membuat proyek baru.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operasi yang dibatasi untuk project prakonversi

Bagian ini menguraikan perbedaan fungsional yang dapat Anda harapkan ketika proyek belum dikonversi.

### <a name="copy-project"></a>Salin proyek

Operasi **Salin** hanya didukung pada proyek yang dikonversi. Proyek yang ditingkatkan tidak dapat disalin sebelum konversi.

### <a name="move-project"></a>Pindahkan proyek

Perubahan pada tanggal mulai proyek tidak akan secara proporsional memindahkan awal tugas kecuali proyek telah dikonversi.

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Apa perbedaan antara proyek yang dikonversi dan proyek baru yang dibuat setelah peningkatan selesai?

Untuk proyek yang dikonversi setelah lingkungan ditingkatkan, bendera akan ditetapkan yang menginstruksikan jadwal untuk hanya menghormati kalender proyek. Perilaku ini cocok dengan perilaku dalam Project Service Automation. Namun, bendera tidak akan ditetapkan untuk proyek baru yang dibuat setelah peningkatan. Oleh karena itu, jadwal akan menghormati jam kerja sumber daya ketika mereka ditugaskan untuk suatu tugas.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Apa yang harus saya lakukan jika proyek saya gagal dikonversi?

Jika proyek Anda gagal dikonversi, langkah pertama adalah meninjau log kesalahan untuk mengidentifikasi masalah umum yang terkait dengan WBS Anda. Jika log tidak menunjukkan kesalahan tertentu yang dapat Anda ambil tindakan, hubungi Dukungan Pelanggan sehingga kasus Anda dapat ditinjau lebih lanjut.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Bagaimana penutupan bisnis ditangani di Project untuk web?

Project for the web tidak menghormati penutupan bisnis yang ditentukan perusahaan di tingkat organisasi. Namun, itu akan menghormati jenis hari libur lain yang didefinisikan dalam template jam kerja tertentu.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Apa batasan Project untuk web?

Lihat [Membuat struktur rincian kerja: Batasan Proyek](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Dapatkah saya mengharapkan perubahan pada perkiraan biaya dan penjualan saya?

Dalam kasus yang jarang terjadi di mana kontur penetapan sumber daya dihitung ulang, atau di mana mereka jatuh pada batas tanggal yang berbeda dari proyek sumber, Anda mungkin melihat perbedaan dalam perkiraan penjualan dan biaya. Sebagai bagian dari proses peningkatan, pelanggan diharapkan untuk menguji serangkaian sampel proyek yang representatif, sehingga mereka dapat memahami potensi perubahan jadwal.
