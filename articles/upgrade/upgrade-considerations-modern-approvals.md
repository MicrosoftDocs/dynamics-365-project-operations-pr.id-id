---
title: Pertimbangan peningkatan untuk persetujuan Modern
description: Artikel ini mencakup poin yang harus dipertimbangkan administrator bila mereka mengaktifkan fungsi Persetujuan Modern.
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
# <a name="upgrade-considerations-for-modern-approvals"></a>Pertimbangan peningkatan untuk persetujuan Modern 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Sebagai bagian dari Rilis Gelombang 1 April 2022, fungsi Persetujuan Modern akan diaktifkan secara default. Fungsi ini akan meningkatkan keandalan logika persetujuan dan memastikan Anda dapat menentukan alasan kegagalan logika persetujuan.

Sebagai bagian dari perubahan ini, perubahan status untuk persetujuan proyek diperbarui. Status sekarang langsung berjalan dari **Diajukan** ke **Disetujui**. **Tertunda** tidak lagi menjadi status untuk persetujuan. Untuk menentukan apakah persetujuan tertunda, verifikasikan bahwa persetujuan adalah bagian dari suatu persetujuan yang ditetapkan, dan tinjau status penetapan persetujuan terlampir.

## <a name="before-you-upgrade"></a>Sebelum Anda meningkatkan

Sebelum meningkatkan ke Persetujuan Modern, pastikan Anda tidak memiliki persetujuan tertunda. Persetujuan Modern tidak menggunakan status **Tertunda**. Oleh karena itu, persetujuan apa pun yang tetap ditandai sebagai **Tertunda** setelah peningkatan tidak akan diproses.

## <a name="after-you-upgrade"></a>Setelah Anda melakukan peningkatan

Setelah meningkatkan ke Persetujuan Modern, administrator harus memvalidasi bahwa aliran cloud yang memproses persetujuan telah diaktifkan.

1. Masuk ke [flow.microsoft.com](https://flow.microsoft.com)
2. Di kanan atas halaman, ganti lingkungan menjadi lingkungan yang telah ditingkatkan.
3. Pilih **Solusi** untuk mencantumkan solusi yang diinstal di lingkungan.
4. Dalam daftar solusi, pilih **Project Operations** atau **Project Service**.
5. Ubah filter dari **Semua** ke **alur cloud**.
6. Verifikasikan bahwa opsi **Project Service - Jadwalkan Kembali Rangkaian Persetujuan Proyek** diatur ke **On**. Jika tidak, pilih alur, lalu pilih **Aktifkan**.
7. Verifikasikan bahwa pemrosesan terjadi setiap lima menit dengan meninjau daftar **Pekerjaan Sistem** di area **Pengaturan**.

## <a name="short-term-rollback"></a>putar kembali jangka pendek

Jika Anda tidak dapat mengikuti perubahan, atau jika Anda menemui masalah serius dengan fitur ini, Anda dapat sementara kembali ke alur persetujuan awal dengan melakukan langkah-langkah berikut:
1. Masuk ke lingkungan Anda dan pastikan tidak ada persetujuan yang tertunda.
2. Lihat **pengaturan** > **Parameter proyek**.
3. Pilih **Kontrol Fitur**, lalu pilih **Persetujuan Modern** untuk menonaktifkan fitur.

## <a name="removing-the-feature-flag"></a>Menghapus tanda fitur

Pada pembaruan Gelombang 2 Oktober 2022, kemampuan untuk menonaktifkan fitur ini akan dihilangkan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
