---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 20, V3
description: Artikel ini mencantumkan fitur dan perbaikan yang tersedia di Project Service Automation Update Release 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913066"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation Pembaruan Rilis 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini mencantumkan fitur dan perbaikan yang baru atau berubah untuk Project Service Automation V3, Update Release 20. Versi ini memiliki nomor pembuatan V 3.10.31.37 dan umumnya tersedia melalui pembaruan mandiri pada Juni 2020.

## <a name="update-release-20"></a>Pembaruan rilis 20

### <a name="bug-fixes"></a>Perbaikan bug

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Mengimpor anggota tim proyek dengan metode alokasi yang memerlukan jam menghasilkan pesan kesalahan yang tidak jelas saat jam yang ditentukan adalah nol.
- Pengguna menerima kesalahan yang salah ketika jumlah maksimum karakter telah dimasukkan ke dalam bidang **Deskripsi** untuk tugas proyek.
- Halaman **unduh add-in Microsoft Dynamics 365 Project Service Automation** akan mengalihkan ke halaman unduh bahasa Inggris bila pengaturan bahasa pengguna diatur ke bahasa Jepang.
- Bila terjadi kesalahan server, label sinkronisasi pada tab **jadwal** formulir **proyek** terkadang tetap ada.
- Pembaruan tugas berlebihan dikirim ke server saat tugas dimodifikasi.

**Sales**

Masalah berikut telah diperbaiki:

- Pada formulir **kontrak**, klik dua kali **buat faktur** akan membuat dua faktur untuk rekaman aktual tunggal.
- Di Internet Explorer 11, pengguna tidak dapat membuat entri pengeluaran.
- Pembalikan biaya dan pembalikan aktual penjualan yang tidak ditagihkan tidak terkait.
- Tombol **refresh aktual** pada formulir **proyek** tidak me- refresh **jam aktual tugas**.
- Plugin **PreValidateProjectTeamMemberCreate** dapat membuat sumber daya duplikat generik yang dapat dipesan saat atribut **msdyn_isgenericresourceprojectscoped** diatur ke **Salah**.
- **Hitung ulang** menghapus biaya yang dibebankan pada detail baris kuotasi berdasarkan produk dan rincian baris kontrak.
- Dalam skenario tertentu, plug-in **PostEstimateLineUpdate** menampilkan kesalahan pengecualian referensi kosong.
- Durasi fase waktu pada **diagram analisis profitabilitas** tidak sesuai dengan durasi biaya dalam detail baris kuotasi harga tetap dari kuotasi.
- Nilai grup unit dan unit tidak ter-default dengan benar untuk kategori pengeluaran pada **rincian baris kontrak** dan formulir **rincian baris kuotasi**.
- Izin daftar **harga unit organisasi** tumpang tindih di efektivitas tanggal.
- Pengguna tidak diizinkan untuk mengubah **orgunit** saat jenis pesanan tidak berbasis pekerjaan karena akan menyebabkan kesalahan pengecualian referensi kosong.
- Saat mencoba menavigasi dari formulir **rincian baris kuotasi**, kembali ke tab **kuotasi**, formulir akan menyegarkan dan menampilkan tab **ringkasan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
