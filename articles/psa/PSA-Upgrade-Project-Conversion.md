---
title: Perubahan fitur untuk Otomatisasi Layanan Proyek ke Operasi Proyek
description: Artikel ini memberikan gambaran umum tentang perubahan fitur untuk Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621341"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Perubahan fitur untuk Otomatisasi Layanan Proyek ke Operasi Proyek

Setelah proyek berhasil ditingkatkan dari Microsoft Dynamics 365 Project Service Automation 3.X ke Dynamics 365 Project Operations Lite, mengedit tugas proyek dalam struktur rincian kerja jaringan tugas (WBS) tidak dimungkinkan. Pelanggan akan dapat meninjau WBS di grid pelacakan di mana bidang baru telah ditambahkan untuk memberikan semua detail yang terkait dengan tugas. Untuk proyek di mana pengeditan pada WBS diperlukan, Anda dapat secara selektif mengonversi proyek yang memenuhi syarat ke Proyek baru untuk pengalaman penjadwalan web.

## <a name="project-conversion-process"></a>Proses konversi proyek

Untuk mengonversi proyek, ikuti langkah-langkah berikut.

1. Buka halaman utama proyek, dan pilih **Konversi** di Panel Tindakan.
1. Dalam kotak pesan konfirmasi, pilih **OK** untuk memulai konversi proyek. Tindakan berikut terjadi:

    1. Bilah pesan yang muncul di halaman utama proyek menyatakan, "Jadwal proyek sedang dikonversi. Anda tidak dapat membuat perubahan pada proyek sampai konversi selesai."
    1. Anda diarahkan ke daftar proyek.

    Setelah konversi proyek selesai, tindakan berikut terjadi:

    1. Manajer proyek yang ditugaskan menerima pemberitahuan di sisi kanan aplikasi.
    1. Bilah pesan yang menyatakan bahwa konversi sedang berlangsung akan dihapus.
    1. Tab **Jadwal** memperlihatkan pengalaman penjadwalan baru dengan Project untuk web. Setiap pengguna yang memiliki lisensi dan peran keamanan yang sesuai dapat mengedit WBS.
    1. Bidang **Mesin** penjadwalan diperbarui ke **Project untuk web**.
    1. Tombol **Konversi** dihapus dari Panel Tindakan.

> [!IMPORTANT]
> Konversi massal proyek tidak diizinkan. Setiap upaya untuk memperbarui volume besar proyek pada saat yang sama akan dibatasi. Keterbatasan ini membantu memastikan kinerja tinggi untuk semua pelanggan.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tugas manual vs. tugas otomatis

Ketika lingkungan ditingkatkan dari Otomatisasi Layanan Proyek ke Operasi Proyek, semua tugas di WBS dianggap dijadwalkan secara otomatis. Konsep tugas terjadwal secara manual tidak tersedia di Project untuk web. Namun, Anda dapat menentukan perilaku penjadwalan yang disukai untuk proyek Anda dengan menggunakan pengaturan mode [penjadwalan saat](/project-management/scheduling-modes.md) Anda membuat proyek baru.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operasi yang dibatasi untuk proyek pra-konversi

Bagian ini menguraikan perbedaan fungsional yang dapat Anda harapkan ketika proyek belum dikonversi.

### <a name="copy-project"></a>Salin proyek

Operasi **Salin** hanya didukung pada proyek yang dikonversi. Proyek yang ditingkatkan tidak dapat disalin sebelum konversi.

### <a name="move-project"></a>Memindahkan proyek

Perubahan pada tanggal mulai proyek tidak akan secara proporsional memindahkan awal tugas kecuali proyek telah dikonversi.

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Apa perbedaan antara proyek yang dikonversi dan proyek baru yang dibuat setelah peningkatan selesai?

Untuk proyek yang dikonversi setelah lingkungan ditingkatkan, bendera akan ditetapkan yang menginstruksikan jadwal untuk menghormati hanya kalender proyek. Perilaku ini cocok dengan perilaku dalam Project Service Automation. Namun, bendera tidak akan ditetapkan untuk proyek baru yang dibuat setelah peningkatan. Oleh karena itu, jadwal akan menghormati jam kerja sumber daya ketika mereka ditugaskan untuk suatu tugas.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Apa yang harus saya lakukan jika proyek saya gagal dikonversi?

Jika proyek Anda gagal dikonversi, langkah pertama adalah meninjau log kesalahan untuk mengidentifikasi masalah umum yang terkait dengan WBS Anda. Jika log tidak menunjukkan kesalahan tertentu yang dapat Anda lakukan tindakannya, hubungi Dukungan Pelanggan sehingga kasus Anda dapat ditinjau lebih lanjut.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Bagaimana penutupan bisnis ditangani di Project untuk web?

Project untuk web tidak menghormati penutupan bisnis yang ditentukan perusahaan di tingkat organisasi. Namun, ini akan menghormati jenis hari libur lain yang didefinisikan dalam template jam kerja tertentu.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Apa saja batasan Project untuk web?

Lihat [Membuat struktur rincian kerja: Batasan](/project-management/create-wbs#project-limitations.md) Proyek.

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Dapatkah saya mengharapkan perubahan pada perkiraan biaya dan penjualan saya?

Dalam kasus yang jarang terjadi di mana kontur penugasan sumber daya dihitung ulang, atau di mana mereka jatuh pada batas tanggal yang berbeda dari proyek sumber, Anda mungkin melihat perbedaan dalam perkiraan penjualan dan biaya. Sebagai bagian dari proses peningkatan, pelanggan diharapkan untuk menguji serangkaian sampel proyek yang representatif, sehingga mereka dapat memahami potensi perubahan jadwal.
