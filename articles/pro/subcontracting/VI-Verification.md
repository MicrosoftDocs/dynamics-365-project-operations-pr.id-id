---
title: Verifikasi faktur vendor dengan aktual yang disetujui
description: Artikel ini menjelaskan bagaimana Microsoft Dynamics 365 Project Operations memungkinkan manajer proyek memverifikasi faktur vendor dengan aktual yang disetujui sebagai kontraktor melakukan pekerjaan dan mencatat waktu, serta pengeluaran dan materi yang digunakan oleh anggota tim proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522949"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifikasi faktur vendor dengan aktual yang disetujui

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Microsoft Dynamics 365 Project Operations memungkinkan manajer proyek memverifikasi baris faktur vendor dengan cara berikut:

- Gunakan bidang **Status verifikasi** di baris faktur vendor.
- Jika baris faktur vendor mereferensikan baris subkontrak, tautkan aktual biaya dari aktivitas subkontraktor ke baris faktur vendor tersebut. Tautan dibuat dengan mencocokkan aktual biaya ke baris faktur vendor.

    > [!NOTE]
    > Meskipun status verifikasi dapat dilacak untuk baris faktur vendor yang tidak mereferensikan subkontrak, aktual biaya tidak dapat ditautkan ke baris faktur vendor tersebut.

## <a name="verification-status"></a>Status verifikasi

Bidang **Status verifikasi** pada baris faktur vendor menunjukkan status verifikasi tersebut. Status berikut didukung:

1. Belum dimulai
2. Sedang berlangsung
3. Selesaikan

Baris faktur vendor yang memiliki status verifikasi **Belum Dimulai** bisa diedit.

Baris faktur vendor yang memiliki status verifikasi **Belum Dimulai** tidak bisa diedit lagi. Untuk baris faktur vendor yang mereferensikan subkontrak, status verifikasi secara otomatis diatur ke **Sedang berlangsung** segera setelah biaya pertama aktual cocok dengan baris faktur vendor.

Baris faktur vendor yang memiliki status verifikasi **Selesai** tidak bisa diedit lagi. Saat semua baris pada faktur vendor memiliki status verifikasi ini, faktur vendor dapat dikonfirmasi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Mencocokkan aktual biaya untuk baris faktur vendor

Pencocokan aktual biaya membantu proses verifikasi pada baris faktur vendor. Untuk mencocokkan aktual biaya dengan baris faktur vendor, ikuti langkah-langkah ini.

1. Buka baris faktur vendor, dan pilih tab **Aktual biaya yang tidak cocok**. Kisi menampilkan daftar aktual biaya yang mereferensikan baris subkontrak yang sama sebagai baris faktur vendor.
2. Pilih satu atau beberapa aktual biaya, lalu pilih toolbar **Cocok** di atas kisi. Sistem memvalidasi bahwa aktual biaya yang dipilih dapat dicocokkan. Setelah validasi berlalu, aktual biaya ditautkan ke baris faktur vendor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteria validasi yang digunakan untuk menautkan aktual biaya ke baris faktur vendor

Selama proses pencocokan, tautan antara biaya aktual dan baris faktur vendor dapat ditetapkan hanya jika kedua kondisi berikut terpenuhi:

- Bidang **Status penyesuaian** untuk setiap biaya yang dipilih sebenarnya harus kosong. Dengan kata lain, aktual biaya tidak boleh digantikan dengan aktual biaya lain selama pembatalan, pembatalan persetujuan, atau proses koreksi jurnal.
- Nilai dari bidang berikut ini cocok antara baris faktur vendor dan biaya aktual yang dipilih. Jika bidang apa pun tidak diatur pada baris faktur vendor, bidang tersebut tidak dipertimbangkan untuk pencocokan.

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

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Aktual biaya yang tidak cocok dari baris faktur vendor

Aktual biaya yang tidak cocok juga dapat membantu proses verifikasi pada faktur vendor dengan mengaktifkan tautan yang ditetapkan sebelumnya untuk dihilangkan. Aktual biaya bisa dibatalkan kecocokannya hanya dari baris faktur vendor yang memiliki status verifikasi **Sedang berlangsung**. Untuk membatalkan pencocokan dari baris faktur vendor, ikuti langkah-langkah ini.

1. Buka baris faktur vendor, dan pilih tab **Aktual biaya yang cocok**. Kisi menampilkan daftar aktual biaya yang mereferensikan baris subkontrak yang sama sebagai baris faktur vendor.
2. Pilih satu atau beberapa aktual biaya, lalu pilih toolbar **Batal mencocokkan** di atas kisi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
