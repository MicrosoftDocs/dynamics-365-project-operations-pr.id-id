---
title: Merekam tanda terima dengan OCR
description: Topik ini menyediakan informasi tentang pemrosesan pengenalan karakter optik (OCR) untuk tanda terima.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cfd88acec9df8468668bedbb55b399d100650e765a6ed647ed528ecca9f1554
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007735"
---
# <a name="capture-a-receipt-using-ocr"></a>Merekam tanda terima dengan OCR

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Entri pengeluaran telah disempurnakan melalui pengenalan pemrosesan pengenalan karakter optik (OCR) untuk tanda terima. Fungsi ini dirancang untuk meningkatkan pengalaman pengguna saat membuat laporan pengeluaran.

## <a name="key-features"></a>Fitur utama

- Sistem mengekstrak nama pedagang, tanggal, dan jumlah total dari kuitansi.
- Sistem akan mencoba mencocokkan tanda terima yang tidak dilampirkan dengan transaksi pengeluaran yang tidak dilampirkan.
- Anda dapat membuat transaksi pengeluaran yang dimasukkan secara manual dari tanda terima.

## <a name="attach-receipts-to-an-expense-report"></a>Melampirkan tanda terima ke laporan pengeluaran

Untuk secara otomatis melampirkan tanda terima yang mencakup transaksi kartu kredit saat laporan pengeluaran dibuat, selesaikan langkah-langkah berikut.

  1. Buka ruang kerja **manajemen pengeluaran**.
  2. Pada tab **tanda terima**, Verifikasikan bahwa ada tanda terima tanpa lampiran. Anda juga dapat mengunggah tanda terima pada tab **tanda terima**.
  3. Pada tab **Pengeluaran**, Verifikasikan bahwa ada Pengeluaran tanpa lampiran. Biasanya, administrator pengeluaran mengimpor pengeluaran ini dari penyedia kartu kredit.
  4. Pilih **laporan pengeluaran baru**. Perhatikan bahwa Anda dapat menyertakan pengeluaran, dan tanda terima, sekarang juga, saat membuat laporan pengeluaran. Jika Anda menambahkan pengeluaran dan tanda terima, pencocokan otomatis tanda terima terhadap pengeluaran akan dipicu.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Membuat atau mencocokkan tanda terima ke laporan pengeluaran
Untuk membuat pengeluaran, atau mencocokkan pengeluaran dari tanda terima, selesaikan langkah-langkah berikut.

  1. Pada laporan pengeluaran, di tab **tanda terima**, lampirkan tanda terima dengan memilih **Tambah tanda terima**.
  2. Di dalam gambar tanda terima yang telah diunggah, perhatikan pilihan **buat** dan **Cocokkan**.

      - Pilih **buat** untuk membuat transaksi pengeluaran yang dimasukkan secara manual dan masukkan nilai yang diekstrak dari tanda terima.
      - Jika Anda memilih **Cocokkan**, sistem akan mencoba mencocokkan pengeluaran yang ada dengan tanda terima.

## <a name="installation"></a>Penginstalan

Untuk menggunakan kemampuan pengeluaran tingkat lanjut ini, instal Add-in Layanan Manajemen pengeluaran untuk Microsoft Dynamics 365 Finance, dan Aktifkan fitur tersebut dalam instans Anda. Anda dapat mengakses Add-in dari proyek di Microsoft Dynamics Lifecycle Services (LCS).

1. Masuk ke LCS, dan buka lingkungan yang diinginkan.
2. Buka **rincian lengkap**.
3. Pilih **Kelola**, atau gulir ke bawah ke fasttab **Add-in lingkungan**.
4. Pilih **Instal Add-in baru**.
5. Pilih **Layanan Manajemen pengeluaran**.
6. Ikuti panduan penginstalan, dan Setujui persyaratan dan ketentuan.
7. Pilih **Instal**.

Di ruang kerja **manajemen fitur**, Aktifkan fitur berikut:

- Laporan pengeluaran model baru
- Pencocokan otomatis dan membuat pengeluaran dari tanda terima

Bila Anda mengaktifkan fitur ini, maka tindakan berikut terjadi:

- **Ruang kerja manajemen pengeluaran** yang ada digantikan dengan ruang kerja baru.
- Item menu baru untuk visibilitas bidang pengeluaran ditambahkan.
- Anda tetap dapat membuka halaman **laporan pengeluaran** sebelumnya dengan membuka **manajemen pengeluaran > pengeluaran saya > laporan pengeluaran**.
- Alur kerja dan persetujuan apa pun tetap akan membawa Anda ke halaman laporan pengeluaran yang ada.
- Kuitansi akan diproses melalui Microsoft Azure Cognitive Services, dan metadata akan diekstrak dan ditambahkan.
- Pilihan ditambahkan yang memungkinkan Anda membuat laporan pengeluaran yang mencakup tanda terima tanpa lampiran yang dicocokkan.
- Pilihan yang ditambahkan ke laporan pengeluaran memungkinkan Anda membuat baris pengeluaran dari tanda terima, atau mencoba mencocokkan tanda terima yang ada ke baris pengeluaran yang ada.

## <a name="frequently-asked-questions"></a>Tanya jawab

**Apakah Microsoft menggunakan data saya untuk modelnya?**

Tidak, Microsoft telah membangun model Pembelajaran Mesin umum untuk layanan pemrosesan tanda terima. Model ini tidak didasarkan pada tanda terima yang Anda Unggah.

**Di manakah fitur ini tersedia dan diproses?**

Saat ini, Amerika Serikat didukung.

**Ke mana tanda terima saya pergi?**

Finance akan menghubungi Cognitive Services untuk mengekstrak data bidang. Cognitive Services akan menyimpan salinan tAnda terima Anda hingga 24 jam saat pemrosesan terjadi. Setelah pemrosesan selesai, Cognitive Services akan menghapus tanda terima. Kuitansi tetap tersimpan di Finance.

Untuk informasi lebih lanjut, lihat [mengaktifkan pemahaman tanda terima dengan kemampuan baru Pengenal formulir](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
