---
title: Menghapus estimasi proyek
description: Ini topik menyediakan informasi tentang menghapus estimasi proyek setelah selesai.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078537"
---
# <a name="eliminate-a-project-estimate"></a>Menghapus estimasi proyek

[!include [banner](../includes/banner.md)]

Perkiraan proyek memberikan tampilan keuangan untuk pekerjaan yang diperkirakan dan dijadwalkan untuk proyek. Untuk bekerja dengan estimasi untuk proyek, Anda harus melampirkan proyek ke proyek estimasi. Proyek estimasi selalu didasarkan pada proyek yang ada, namun beberapa proyek dapat merujuk ke satu proyek estimasi. Hanya proyek harga tetap dan investasi yang dapat dilampirkan untuk mengestimasi proyek, dan proyek-proyek tersebut harus termasuk dalam kelompok proyek yang sama dengan proyek estimasi.

Untuk menghapus estimasi proyek, itu harus diselesaikan. Langkah-langkah berikut menjelaskan cara menghapus estimasi.

1. Buka **manajemen proyek dan akuntansi** > **Semua proyek** dan buka proyek. 
2. Pada tab **Kelola** , pilih **Estimasi** , dan pada halaman **Estimasi** pilih **Hapus**.
3. Pada halaman **Hapus estimasi** pada tab **Umum** , atur opsi berikut ini:

   - **Kode periode** : Pilih kode periode untuk memilih estimasi proyek yang sesuai. 
   - **Tanggal estimasi** : Pilih tanggal estimasi yang sesuai untuk eliminasi.
   - **Hapus dengan peringatan WIP** : Aktifkan opsi ini untuk memberikan pemberitahuan ketika perkiraan yang terkait dengan pekerjaan yang sedang berlangsung (WIP) akan dihilangkan. Ketika opsi ini tidak diaktifkan, eliminasi tidak dapat dilanjutkan jika ada transaksi yang tidak diestimasi. 
   > [!NOTE]
   > Opsi ini hanya tersedia saat eliminasi diterapkan ke proyek estimasi. Ini tidak tersedia jika Anda menggunakan posting berkala. Pengaturan ini berfungsi dengan pengaturan pada tab **Estimasi** pada halaman **Parameter proyek** , di grup bidang **Perbolehkan penghapusan saat transaksi yang tidak diestimasi ada**.
   - **Atur tahap ke Selesai** : Aktifkan opsi ini untuk mengatur tahap estimasi proyek ke **Selesai** setelah Anda menjalankan eliminasi.
   - **Cetak Daftar estimasi** : Pilih informasi yang akan disertakan ketika daftar estimasi dicetak.
   - **Tampilkan Infolog** : Aktifkan opsi ini untuk menampilkan Infolog.
   - **Tanggal posting** : Pilih tanggal posting buku besar dari estimasi.

4.  Pilih **OK**.
5. Setelah proses eliminasi selesai, proyek estimasi yang dihapus ditampilkan dengan nilai negatif. 

Jika Anda tidak bermaksud menghapus estimasi, Anda dapat memilih estimasi yang dihapus dan memilih **Balikkan eliminasi**.   
