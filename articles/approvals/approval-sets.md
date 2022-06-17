---
title: Rangkaian persetujuan
description: Artikel ini menjelaskan cara bekerja dengan set persetujuan, permintaan, dan subset dari operasi tersebut.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918086"
---
# <a name="approval-sets"></a>Rangkaian persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Rangkaian persetujuan mengelompokkan permintaan persetujuan grup ke dalam subset operasi yang lebih kecil. Pengelompokan ini memungkinkan persetujuan untuk diproses menurut proyek, dalam urutan tertentu, dan memungkinkan untuk mencoba ulang dan mengurutkan. Mengelompokkan permintaan persetujuan akan meningkatkan keandalan dan keterlacakan pemrosesan persetujuan untuk volume persetujuan yang besar.

Rangkaian persetujuan menunjukkan status pemrosesan keseluruhan rekaman terkait. Bila rekaman persetujuan diproses menggunakan kumpulan persetujuan, rekaman akan berpindah dari **Diajukan** ke **Disetujui**, dan tidak lagi ditautkan ke rangkaian persetujuan. Jika rekaman gagal saat diajukan untuk persetujuan, rekaman tetap dalam status **Diajukan** dan rangkaian persetujuan ditandai sebagai gagal. Rangkaian persetujuan akan mencatat pesan kesalahan kegagalan.

## <a name="processing-approvals-and-approval-sets"></a>Memproses persetujuan dan rangkaian persetujuan
Persetujuan yang diantrekan untuk pemrosesan dapat dilihat di tampilan **Pemrosesan Persetujuan**. Sistem memproses semua entri beberapa kali secara asinkron, termasuk mencoba ulang persetujuan jika upaya sebelumnya gagal.

Bidang **Usia Rangkaian Persetujuan** mencatat jumlah upaya yang tersisa untuk memproses rangkaian sebelum ditandai sebagai gagal.

Set persetujuan diproses melalui aktivasi berkala berdasarkan **Cloud Flow** bernama **Project Service - Recurrently Schedule Project Approval Sets**. Ini ditemukan dalam **Solusi** bernama **Operasi Proyek**. 

Pastikan alur diaktifkan dengan menyelesaikan langkah-langkah berikut.

1. Sebagai administrator, masuk ke [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Di sudut kanan atas, beralihlah ke lingkungan yang Anda gunakan untuk Dynamics 365 Project Operations.
3. Pilih **Solusi** untuk membuat daftar solusi yang diinstal di lingkungan.
4. Dalam daftar solusi, pilih **Operasi** Proyek.
5. Ubah filter dari **Semua** ke **Cloud Flows**.
6. Verifikasi bahwa **alur Project Service – Recurrently Schedule Project Approval Sets** diatur ke **Aktif**. Jika tidak, pilih alur, lalu pilih **Aktifkan**.
7. Verifikasi bahwa pemrosesan terjadi setiap lima menit dengan **meninjau daftar Pekerjaan** Sistem di **area Pengaturan** dalam lingkungan Operasi Dataverse Proyek Anda.

## <a name="failed-approvals-and-approval-sets"></a>Persetujuan dan rangkaian persetujuan yang gagal
Tampilan **Persetujuan Gagal** mencantumkan semua persetujuan yang memerlukan intervensi pengguna. Buka log rangkaian persetujuan yang terkait untuk mengidentifikasi penyebab kegagalan.
Memilih **Coba lagi** menambahkan ke jumlah usia rangkaian persetujuan, memindahkan rangkaian persetujuan kembali ke status **Pemrosesan**, dan mencoba memproses rekaman yang tersisa.

## <a name="configure-approval-sets"></a>Konfigurasikan Rangkaian Persetujuan

### <a name="enable-the-approval-sets-feature"></a>Aktifkan fitur Rangkaian Persetujuan
Sebelum Anda mengaktifkan fitur rangkaian Persetujuan, pastikan tidak ada persetujuan yang saat ini diproses.

- Buka halaman **parameter Proyek**, lalu pilih **Kontrol Fitur** > **Aktifkan Persetujuan Modern**.

### <a name="turn-off-the-approval-sets-feature"></a>Nonaktifkan fitur Rangkaian Persetujuan
Sebelum Anda menonaktifkan fitur rangkaian Persetujuan, pastikan tidak ada persetujuan yang saat ini diproses.

- Buka halaman **parameter Proyek**, lalu pilih **Kontrol Fitur** > **Nonaktifkan Persetujuan Modern**.

### <a name="configuring-the-asynchronous-threshold"></a>Mengkonfigurasi ambang batas asinkron 
Bila rangkaian persetujuan dibuat, pemrosesan akan berpindah ke latar belakang bila jumlah rekaman yang dipilih untuk disetujui melebihi ambang batas yang ditunjukkan. Gunakan bidang **Ambang Batas Asinkron** untuk mengkonfigurasi ketika pemrosesan persetujuan harus dijalankan secara sinkron atau asinkron. Pilih salah satu dari nilai berikut ini:

  - Nol: Semua permintaan harus diproses secara asinkron. 
  - Angka yang lebih besar dari nol: Persetujuan diproses secara asinkron hanya bila jumlah persetujuan yang diajukan melebihi nilai ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
