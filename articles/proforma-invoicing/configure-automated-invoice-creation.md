---
title: Mengonfigurasi pembuatan faktur otomatis
description: Topik ini menyediakan informasi tentang mengkonfigurasi sistem untuk menghasilkan faktur secara otomatis.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898130"
---
# <a name="configure-automated-invoice-creation"></a>Mengonfigurasi pembuatan faktur otomatis

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Selesaikan langkah-langkah berikut untuk mengkonfigurasi faktur otomatis berjalan dalam Project Operations.

1. Buka **Pengaturan** \> **Pekerjaan bets**.
2. Membuat batch pekerjaan, dan namai **Project operations buat faktur**. Nama pekerjaan batch harus mencakup istilah "Buat faktur".
3. Di bidang **jenis pekerjaan**, pilih **tidak ada**. Secara default, **frekuensi harian** dan opsi **aktif** diatur ke **ya**.
4. Pilih **Jalankan alur kerja**. Di kotak dialog **mencari rekaman**, Anda akan melihat tiga alur kerja:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pilih **ProcessRunCaller** dan kemudian pilih **Tambahkan**.
6. Pilih **OK** di kotak dialog berikutnya. Alur kerja **tidur** diikuti dengan alur kerja **proses**.

    Anda juga dapat memilih **ProcessRunner** di langkah 5. Kemudian, bila Anda memilih **OK**, alur kerja **proses** diikuti dengan alur kerja **tidur**.

Alur kerja **ProcessRunCaller** dan **ProcessRunner** membuat faktur. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** adalah alur kerja yang benar-benar membuat faktur. Ia melalui semua baris kontrak pembuatan faktur, dan membuat faktur untuk baris tersebut. Untuk menentukan baris kontrak yang harus dibuat faktur, pekerjaan akan melihat tanggal faktur berjalan untuk baris kontrak. Jika baris kontrak milik satu kontrak memiliki tanggal yang sama saat menjalankan faktur, transaksi digabungkan menjadi satu faktur yang memiliki dua baris faktur. Jika tidak ada transaksi untuk membuat faktur, pekerjaan akan melompati pembuatan faktur.

Setelah **ProcessRunner** selesai berjalan, maka ia memanggil **ProcessRunCaller**, menyediakan waktu berakhir, dan ditutup. **ProcessRunCaller** kemudian memulai timer yang berjalan selama 24 jam dari waktu berakhir yang ditentukan. Di akhir timer, **ProcessRunCaller** ditutup.

Pekerjaan proses batch untuk membuat faktur adalah pekerjaan berulang. Jika proses batch ini dijalankan berkali-kali, beberapa instans pekerjaan dibuat dan menyebabkan kesalahan. Oleh karena itu, Anda harus memulai proses batch hanya satu kali, dan Anda harus me-restart hanya jika berhenti berjalan.

> [!NOTE]
> Faktur bets hanya berjalan untuk baris kontrak proyek yang dikonfigurasi dengan jadwal faktur. Baris kontrak dengan metode penagihan harga tetap harus mengonfigurasikan tonggak waktu. Baris kontrak proyek dengan metode waktu dan materi penagihan akan memerlukan pengaturan jadwal faktur berdasarkan tanggal. Hal yang sama berlaku untuk baris kontrak berbasis proyek.     
