---
title: Tingkatkan pertimbangan untuk Persetujuan Modern
description: Artikel ini mencakup poin-poin yang harus dipertimbangkan administrator ketika mereka mengaktifkan fungsionalitas Persetujuan Modern.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931748"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Tingkatkan pertimbangan untuk Persetujuan Modern 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Sebagai bagian dari Rilis Gelombang 1 April 2022, fungsionalitas Persetujuan Modern akan diaktifkan secara default. Fungsionalitas ini meningkatkan keandalan logika persetujuan dan memastikan bahwa Anda dapat menentukan alasannya jika logika persetujuan gagal.

Sebagai bagian dari perubahan ini, perubahan status untuk persetujuan proyek diperbarui. Status sekarang langsung dari **Diserahkan** ke **Disetujui**. **Tertunda** tidak lagi menjadi status untuk persetujuan. Untuk menentukan apakah persetujuan tertunda, verifikasi bahwa persetujuan adalah bagian dari set persetujuan, dan tinjau status dari set persetujuan terlampir.

## <a name="before-you-upgrade"></a>Sebelum Anda meningkatkan

Sebelum Anda meningkatkan ke Persetujuan Modern, pastikan Anda tidak memiliki persetujuan yang tertunda. Persetujuan Modern tidak menggunakan **status Tertunda**. Oleh karena itu, setiap persetujuan yang masih ditandai sebagai **Tertunda** setelah peningkatan tidak akan diproses.

## <a name="after-you-upgrade"></a>Setelah Anda meningkatkan

Setelah Anda meningkatkan ke Persetujuan Modern, administrator harus memvalidasi bahwa alur cloud yang memproses persetujuan telah diaktifkan.

1. Masuk ke [flow.microsoft.com](https://flow.microsoft.com)
2. Di kanan atas halaman, alihkan lingkungan Anda ke lingkungan yang telah Anda tingkatkan.
3. Pilih **Solusi** untuk membuat daftar solusi yang diinstal di lingkungan.
4. Dalam daftar solusi, pilih **Operasi** Proyek atau **Layanan** Proyek.
5. Ubah filter dari **Semua** ke **Cloud Flows**.
6. Verifikasi bahwa **opsi Project Service – Recurrently Schedule Project Approval Sets** diatur ke **Aktif**. Jika tidak, pilih alur, lalu pilih **Aktifkan**.
7. Verifikasi bahwa pemrosesan terjadi setiap lima menit dengan **meninjau daftar Pekerjaan** Sistem di **area Pengaturan**.

## <a name="short-term-rollback"></a>Kemunduran jangka pendek

Jika Anda tidak dapat mengambil perubahan, atau jika Anda mengalami masalah parah dengan fitur ini, Anda dapat kembali sementara ke alur persetujuan awal dengan melakukan langkah-langkah berikut:
1. Masuk ke lingkungan Anda dan verifikasi bahwa tidak ada persetujuan yang tertunda.
2. Buka **Parameter** > **Proyek Pengaturan**.
3. Pilih **Kontrol** Fitur lalu pilih **Persetujuan** Modern untuk menonaktifkan fitur.

## <a name="removing-the-feature-flag"></a>Menghapus bendera fitur

Pada update Gelombang 2 Oktober 2022, kemampuan untuk mematikan fitur ini akan dihapus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
