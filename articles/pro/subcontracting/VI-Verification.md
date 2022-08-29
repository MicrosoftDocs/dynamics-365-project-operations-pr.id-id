---
title: Verifikasi faktur vendor dengan aktual yang disetujui
description: Artikel ini menjelaskan bagaimana Microsoft Dynamics 365 Project Operations mari manajer proyek memverifikasi faktur vendor dengan aktual yang disetujui sebagai kontraktor melakukan pekerjaan dan waktu yang tercatat, serta biaya dan materi yang digunakan oleh anggota tim proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ab9f69e36aa58bfe3a2f8e3455db66b6bceea968
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261750"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifikasi faktur vendor dengan aktual yang disetujui

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Microsoft Dynamics 365 Project Operations mari manajer proyek memverifikasi baris faktur vendor dengan cara berikut:

- Gunakan bidang **Status** verifikasi pada baris faktur vendor.
- Jika baris faktur vendor mereferensikan baris subkontrak, tautkan aktual biaya dari aktivitas subkontraktor ke baris faktur vendor tersebut. Tautan dibuat dengan mencocokkan aktual biaya dengan baris faktur vendor.

    > [!NOTE]
    > Meskipun status verifikasi dapat dilacak untuk baris faktur vendor yang tidak mereferensikan subkontrak, aktual biaya tidak dapat ditautkan ke baris faktur vendor tersebut.

## <a name="verification-status"></a>Status verifikasi

Kolom **Status** verifikasi pada baris faktur vendor menunjukkan status verifikasi tersebut. Status berikut didukung:

1. Belum dimulai
2. Sedang berlangsung
3. Selesaikan

Baris faktur vendor yang memiliki status **verifikasi Tidak dimulai** dapat diedit.

Baris faktur vendor yang memiliki status **verifikasi Sedang berlangsung** tidak dapat lagi diedit. Untuk baris faktur vendor yang mereferensikan subkontrak, status verifikasi secara otomatis diatur ke **Sedang berlangsung** segera setelah aktual biaya pertama dicocokkan dengan baris faktur vendor.

Baris faktur vendor yang memiliki status **verifikasi Selesai** tidak dapat lagi diedit. Ketika semua baris pada faktur vendor memiliki status verifikasi ini, faktur vendor dapat dikonfirmasi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Mencocokkan aktual biaya dengan baris faktur vendor

Pencocokan aktual biaya membantu proses verifikasi pada baris faktur vendor. Untuk mencocokkan aktual biaya dengan baris faktur vendor, ikuti langkah-langkah berikut.

1. Buka baris faktur vendor, dan pilih tab **Aktual biaya** yang tak tertandingi. Kisi memperlihatkan daftar aktual biaya yang mereferensikan baris subkontrak yang sama dengan baris faktur vendor.
2. Pilih satu atau beberapa aktual biaya, lalu pilih **Cocokkan** pada toolbar di atas kisi. Sistem memvalidasi bahwa aktual biaya yang dipilih dapat dicocokkan. Setelah validasi disahkan, aktual biaya ditautkan ke baris faktur vendor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteria validasi yang digunakan untuk menautkan aktual biaya ke baris faktur vendor

Selama proses pencocokan, tautan antara biaya aktual dan baris faktur vendor hanya dapat dibuat jika kedua kondisi berikut terpenuhi:

- Bidang **Status** penyesuaian untuk setiap aktual biaya yang dipilih harus kosong. Dengan kata lain, aktual biaya tidak boleh digantikan oleh aktual biaya lainnya selama penarikan kembali, pembatalan persetujuan, atau proses jurnal koreksi.
- Nilai bidang berikut dicocokkan antara baris faktur vendor dan aktual biaya yang dipilih. Jika ada bidang yang tidak diatur pada baris faktur vendor, bidang tersebut tidak dipertimbangkan untuk dicocokkan.

    - Kontrak proyek
    - Baris kontrak proyek
    - Kelas Transaksi
    - Project
    - Tugas
    - Kategori sumber daya
    - Kategori Transaksi
    - Produk
    - Baris subkontrak
    - Sumber daya yang dapat dipesan

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Biaya aktual yang tidak sesuai dari baris faktur vendor

Ketidakcocokan aktual biaya juga dapat membantu proses verifikasi pada faktur vendor dengan memungkinkan tautan yang dibuat sebelumnya untuk dihapus. Biaya aktual dapat tidak tertandingi hanya dari baris faktur vendor yang memiliki status **verifikasi Sedang berlangsung**. Untuk membatalkan biaya aktual yang sesuai dari baris faktur vendor, ikuti langkah-langkah berikut.

1. Buka baris faktur vendor, dan pilih tab **Aktual biaya yang** cocok. Kisi memperlihatkan daftar aktual biaya yang mereferensikan baris faktur vendor.
2. Pilih satu atau beberapa aktual biaya, lalu pilih **Batalkan Pertandingan** pada toolbar di atas kisi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
