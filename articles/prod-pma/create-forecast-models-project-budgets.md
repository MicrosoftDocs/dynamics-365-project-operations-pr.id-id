---
title: Membuat model perkiraan untuk anggaran proyek
description: Topik ini menjelaskan cara membuat model perkiraan untuk anggaran yang tersisa.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078620"
---
# <a name="create-forecast-models-for-project-budgets"></a>Membuat model perkiraan untuk anggaran proyek 

[!include [banner](../includes/banner.md)]

Topik ini menjelaskan cara membuat model perkiraan untuk anggaran yang tersisa. Proyek yang terkait dengan kontrol anggaran menggunakan dua jenis anggaran: asli dan tersisa. Saat membuat anggaran proyek, Anda harus menentukan model perkiraan anggaran asli dan yang tersisa yang dibuat di halaman **model perkiraan**. Anggaran proyek berdasarkan model tertentu dibuat saat Anda menerapkan anggaran proyek.

> [!NOTE]
> Model perkiraan yang digunakan untuk kontrol anggaran tidak dapat memiliki submodel atau digunakan sebagai submodel.

1. Pilih **manajemen proyek dan akuntansi** > **pengaturan** > **perkiraan**  > **model perkiraan**.
2. Pilih **baru** untuk membuat model perkiraan baru, lalu masukkan nomor id model dan nama untuk model baru. 
3. Atur pilihan **berhenti** ke **ya** untuk mencegah perubahan pada baris perkiraan untuk model perkiraan. 
4. Jika baris perkiraan yang terkait dengan model harus menghasilkan perkiraan arus kas di buku besar, atur **sertakan dalam perkiraan arus kas** ke **ya**. 
5. Untuk menggunakan tanggal proyek sebagai tanggal faktur, atur **tanggal faktur perkiraan** menjadi **ya**. 
6. Di bidang **Jenis anggaran** , pilih salah satu jenis model berikut:

   - **Anggaran asli** : menggunakan jumlah anggaran asli yang diterapkan saat anggaran awal dibuat dan disetujui.
   - **Anggaran tersisa** : Gunakan jumlah anggaran yang tersisa selama masa pakai proyek. Saldo dalam model perkiraan ini dikurangi dengan transaksi aktual dan ditingkatkan atau dikurangi dengan revisi anggaran.
   - **Penerusan** : Gunakan jumlah anggaran penerusan untuk proyek. Penerusan adalah proses opsional yang dapat dijalankan untuk mentransfer jumlah anggaran yang tidak terpakai dari satu tahun fiskal ke yang lain.

7. Atur pilihan berikut bila diperlukan:

   - Aktifkan **Tanggal faktur perkiraan** untuk menggunakan tanggal proyek sebagai tanggal faktur.
   - Aktifkan **perkiraan dengan WIP** untuk perkiraan berdasarkan pekerjaan yang sedang berlangsung (WIP), lalu pilih jenis WIP. 
   - Anda dapat menyimpan **jenis anggaran** default sebagai **tidak ada** atau memasukkan jenis baru. Jenis anggaran tidak dapat diubah setelah Anda mengubah rekaman.     
    > [!NOTE]
    > Jika Anda mengubah jenis anggaran default, Semua pilihan lain tidak akan tersedia untuk pembaruan, dan Anda tidak dapat menggunakan kembali model perkiraan ini. 
   


 

