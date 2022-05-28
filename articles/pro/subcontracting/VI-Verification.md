---
title: Verifikasi faktur vendor dengan aktual yang disetujui
description: Ini topik menjelaskan bagaimana Microsoft Dynamics 365 Project Operations mari manajer proyek memverifikasi faktur vendor dengan aktual yang disetujui sebagai kontraktor melakukan pekerjaan dan mencatat waktu, dan biaya dan bahan yang digunakan oleh anggota tim proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585474"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifikasi faktur vendor dengan aktual yang disetujui

[!include [banner](../../includes/dataverse-preview.md)]

_ **Berlaku Untuk:** Penyebaran lite - deal to proforma invoicing

Microsoft Dynamics 365 Project Operations mari manajer proyek memverifikasi baris faktur vendor dengan cara berikut:

- Gunakan bidang **Status** verifikasi pada baris faktur vendor.
- Jika jalur faktur vendor merujuk pada jalur subkontrak, biaya tautan aktual dari aktivitas subkontraktor ke jalur faktur vendor tersebut. Tautan dibuat dengan mencocokkan aktual biaya dengan baris faktur vendor.

    > [!NOTE]
    > Meskipun status verifikasi dapat dilacak untuk jalur faktur vendor yang tidak mereferensikan subkontrak, aktual biaya tidak dapat ditautkan ke baris faktur vendor tersebut.

## <a name="verification-status"></a>Status verifikasi

Bidang **Status** verifikasi pada baris faktur vendor menunjukkan status verifikasi tersebut. Status berikut didukung:

1. Belum dimulai
2. Sedang berlangsung
3. Selesaikan

Baris faktur vendor yang memiliki status **verifikasi Tidak dimulai** dapat diedit.

Baris faktur vendor yang memiliki status **verifikasi Sedang berlangsung** tidak dapat lagi diedit. Untuk baris faktur vendor yang merujuk subkontrak, status verifikasi secara otomatis diatur ke **Sedang berlangsung** segera setelah biaya aktual pertama dicocokkan dengan baris faktur vendor.

Baris faktur vendor yang memiliki status **verifikasi Selesai** tidak dapat lagi diedit. Ketika semua baris pada faktur vendor memiliki status verifikasi ini, faktur vendor dapat dikonfirmasi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Mencocokkan aktual biaya dengan baris faktur vendor

Pencocokan aktual biaya membantu proses verifikasi pada jalur faktur vendor. Untuk mencocokkan aktual biaya dengan baris faktur vendor, ikuti langkah-langkah berikut.

1. Buka baris faktur vendor, dan pilih **tab Aktual** biaya yang tak tertandingi. Kisi menunjukkan daftar aktual biaya yang merujuk pada garis subkontrak yang sama dengan baris faktur vendor.
2. Pilih satu atau beberapa aktual biaya, lalu pilih **Cocokkan** pada toolbar di atas kisi. Sistem memvalidasi bahwa aktual biaya yang dipilih dapat dicocokkan. Setelah validasi berlalu, aktual biaya ditautkan ke baris faktur vendor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriteria validasi yang digunakan untuk menautkan aktual biaya ke jalur faktur vendor

Selama proses pencocokan, tautan antara biaya aktual dan baris faktur vendor hanya dapat dibuat jika kedua kondisi berikut terpenuhi:

- Bidang **status** Penyesuaian untuk setiap aktual biaya yang dipilih harus kosong. Dengan kata lain, aktual biaya tidak boleh diganti dengan aktual biaya lainnya selama penarikan, pembatalan persetujuan, atau proses jurnal koreksi.
- Nilai bidang berikut dicocokkan antara baris faktur vendor dan biaya aktual yang dipilih. Jika ada bidang yang tidak diatur pada baris faktur vendor, itu tidak dipertimbangkan untuk dicocokkan.

    - Kontrak proyek
    - Baris kontrak proyek
    - Kelas Transaksi
    - Project
    - Tugas
    - Kategori sumber daya
    - Kategori Transaksi
    - Produk
    - Jalur subkontrak
    - Sumber daya yang dapat dipesan

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Aktual biaya yang tak tertandingi dari baris faktur vendor

Tak tertandingi dari aktual biaya juga dapat membantu proses verifikasi pada faktur vendor dengan memungkinkan link yang telah ditetapkan sebelumnya untuk dihapus. Aktual biaya hanya dapat ditandingi dari jalur faktur vendor yang memiliki status **verifikasi Sedang berlangsung**. Untuk biaya aktual yang tak tertandingi dari baris faktur vendor, ikuti langkah-langkah ini.

1. Buka baris faktur vendor, dan pilih **tab Aktual biaya yang** cocok. Kisi menunjukkan daftar aktual biaya yang mereferensikan baris faktur vendor.
2. Pilih satu atau beberapa aktual biaya, lalu pilih **Tak Tertandingi** pada toolbar di atas kisi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]