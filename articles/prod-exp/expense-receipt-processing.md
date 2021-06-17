---
title: Pemrosesan tanda terima pengeluaran
description: Topik ini menyediakan informasi tentang pemrosesan pengenalan karakter optik (OCR) untuk tanda terima. Fitur ini dirancang untuk meningkatkan pengalaman pengguna saat membuat laporan pengeluaran di Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993510"
---
# <a name="expense-receipt-processing"></a>Pemrosesan tanda terima pengeluaran

Entri pengeluaran telah disempurnakan melalui pengenalan pemrosesan pengenalan karakter optik (OCR) untuk tanda terima. Fitur ini dirancang untuk meningkatkan pengalaman pengguna saat membuat laporan pengeluaran.

## <a name="key-features"></a>Fitur utama

- Nama pedagang, tanggal, dan jumlah total diekstrak dari kuitansi.
- Fitur ini mencoba mencocokkan tanda terima yang tidak dilampirkan dengan transaksi pengeluaran yang tidak dilampirkan.
- Pengguna dapat membuat transaksi pengeluaran yang dimasukkan secara manual dari tanda terima.

## <a name="usage-examples"></a>Contoh penggunaan

Untuk secara otomatis melampirkan tanda terima yang mencakup transaksi kartu kredit saat laporan pengeluaran dibuat, lakukan yang berikut:

  1. Buka ruang kerja **manajemen pengeluaran**.
  2. Pada tab **tanda terima**, Verifikasikan bahwa ada tanda terima tanpa lampiran. Anda juga dapat mengunggah tanda terima pada tab **tanda terima**.
  3. Pada tab **Pengeluaran**, Verifikasikan bahwa ada Pengeluaran tanpa lampiran. Biasanya, administrator pengeluaran mengimpor pengeluaran ini dari penyedia kartu kredit.
  4. Pilih **laporan pengeluaran baru**. Perhatikan bahwa Anda dapat menyertakan pengeluaran, dan tanda terima, sekarang juga, saat membuat laporan pengeluaran. Jika Anda menambahkan pengeluaran dan tanda terima, pencocokan otomatis tanda terima terhadap pengeluaran akan dipicu.

Untuk membuat pengeluaran, atau mencocokkan pengeluaran dari tanda terima, lakukan langkah berikut:

  1. Pada laporan pengeluaran, di tab **tanda terima**, lampirkan tanda terima dengan memilih **Tambah tanda terima**.
  2. Di dalam gambar tanda terima yang telah diunggah, perhatikan pilihan **buat** dan **Cocokkan**.

      - Pilih **buat** untuk membuat transaksi pengeluaran yang dimasukkan secara manual dan masukkan nilai yang diekstrak dari tanda terima.
      - Jika Anda memilih **Cocokkan**, sistem akan mencoba mencocokkan pengeluaran yang ada dengan tanda terima.

## <a name="installation"></a>Penginstalan

Fitur ini bekerja sama dengan fitur **Konsep baru laporan pengeluaran** untuk membantu menyederhanakan pengalaman pengeluaran. Fitur ini hanya tersedia untuk lingkungan tingkat 2 +, yakni Sandbox dan produksi.

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

Untuk informasi lebih lanjut tentang fitur dengan konsep baru laporan pengeluaran, lihat [Konsep baru laporan pengeluaran](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Tanya jawab

**Apakah Microsoft menggunakan data saya untuk modelnya?**

Tidak, Microsoft telah membangun model Pembelajaran Mesin umum untuk layanan pemrosesan tanda terima. Model ini tidak didasarkan pada tanda terima yang Anda Unggah.

**Di manakah fitur ini tersedia dan diproses?**

Saat ini, Amerika Serikat didukung.

**Ke mana tanda terima saya pergi?**

Finance akan menghubungi Cognitive Services untuk mengekstrak data bidang. Cognitive Services akan menyimpan salinan tAnda terima Anda hingga 24 jam saat pemrosesan terjadi. Setelah pemrosesan selesai, Cognitive Services akan menghapus tanda terima. Kuitansi tetap tersimpan di Finance.

Untuk informasi lebih lanjut, lihat [mengaktifkan pemahaman tanda terima dengan kemampuan baru Pengenal formulir](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]