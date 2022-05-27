---
title: Meningkatkan pertimbangan untuk Persetujuan Modern
description: Topik mencakup poin-poin yang harus dipertimbangkan administrator ketika mereka mengaktifkan fungsionalitas Persetujuan Modern.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578390"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Meningkatkan pertimbangan untuk Persetujuan Modern 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Sebagai bagian dari Rilis Gelombang 1 April 2022, fungsionalitas Persetujuan Modern akan diaktifkan secara default. Fungsi ini meningkatkan keandalan logika persetujuan dan memastikan bahwa Anda dapat menentukan alasan jika logika persetujuan gagal.

Sebagai bagian dari perubahan ini, perubahan status untuk persetujuan proyek diperbarui. Status sekarang langsung dari **Diserahkan** ke **Disetujui**. **Tertunda** tidak lagi menjadi status untuk persetujuan. Untuk menentukan apakah persetujuan tertunda, verifikasi bahwa persetujuan tersebut adalah bagian dari set persetujuan, dan tinjau keadaan set persetujuan terlampir.

## <a name="before-you-upgrade"></a>Sebelum Anda upgrade

Sebelum Anda meningkatkan ke Persetujuan Modern, pastikan Anda tidak memiliki persetujuan yang tertunda. Persetujuan Modern tidak menggunakan **status Tertunda**. Oleh karena itu, setiap persetujuan yang masih ditandai sebagai **Tertunda** setelah peningkatan tidak akan diproses.

## <a name="after-you-upgrade"></a>Setelah Anda upgrade

Setelah Anda meningkatkan ke Persetujuan Modern, administrator harus memvalidasi bahwa aliran cloud yang memproses persetujuan telah diaktifkan.

1. Masuk ke [flow.microsoft.com](https://flow.microsoft.com)
2. Di kanan atas halaman, alihkan lingkungan Anda ke lingkungan yang telah Anda tingkatkan.
3. Pilih **Solusi** untuk mencantumkan solusi yang diinstal di lingkungan.
4. Dalam daftar solusi, pilih **Operasi** Proyek atau **Layanan** Proyek.
5. Ubah filter dari **Semua** ke **Cloud Flows**.
6. Verifikasi bahwa **opsi Project Service – Repetitively Schedule Project Approval Sets** diatur ke **Aktif**. Jika tidak, pilih alur, lalu pilih **Nyalakan**.
7. Verifikasi bahwa pemrosesan terjadi setiap lima menit dengan **meninjau daftar Pekerjaan** Sistem di **area Pengaturan**.

## <a name="short-term-rollback"></a>Kemunduran jangka pendek

Jika Anda tidak dapat mengambil perubahan, atau jika Anda mengalami masalah parah dengan fitur ini, Anda dapat sementara kembali ke alur persetujuan asli dengan melakukan langkah-langkah berikut:
1. Masuk ke lingkungan Anda dan verifikasi bahwa tidak ada persetujuan yang tertunda.
2. Buka **Pengaturan** > **Parameter** Proyek.
3. Pilih **Kontrol** Fitur lalu pilih **Persetujuan** Modern untuk menonaktifkan fitur.

## <a name="removing-the-feature-flag"></a>Menghapus bendera fitur

Dalam pembaruan Wave 2 Oktober 2022, kemampuan untuk mematikan fitur ini akan dihapus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
