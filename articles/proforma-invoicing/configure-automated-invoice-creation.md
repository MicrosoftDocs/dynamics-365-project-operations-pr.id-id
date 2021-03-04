---
title: Mengonfigurasi pembuatan faktur otomatis
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi sistem untuk menghasilkan faktur secara otomatis.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122437"
---
# <a name="configure-automatic-invoice-creation"></a>Mengonfigurasi pembuatan faktur otomatis

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Selesaikan langkah-langkah berikut untuk mengkonfigurasi faktur otomatis berjalan dalam Dynamics 365 Project Operations.

1. Buka **Pengaturan** > **Pekerjaan bets**.
2. Membuat batch pekerjaan, dan namai **Project operations buat faktur**. Nama pekerjaan batch harus mencakup kata "Buat faktur".
3. Di bidang **jenis pekerjaan**, pilih **tidak ada**. Secara default, **frekuensi harian** dan opsi **aktif** diatur ke **ya**.
4. Pilih **Jalankan alur kerja**. Di kotak dialog **mencari rekaman**, Anda akan melihat tiga alur kerja:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pilih **ProcessRunCaller** dan kemudian pilih **Tambahkan**.
6. Pilih **OK** di kotak dialog berikutnya. Alur kerja **tidur** diikuti dengan alur kerja **proses**.

  > [!NOTE]
  > Anda juga dapat memilih **ProcessRunner** di langkah 5. Kemudian, bila Anda memilih **OK**, alur kerja **proses** diikuti dengan alur kerja **tidur**.

Alur kerja **ProcessRunCaller** dan **ProcessRunner** membuat faktur. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** adalah alur kerja yang benar-benar membuat faktur. Ia melalui semua baris kontrak pembuatan faktur, dan membuat faktur untuk baris tersebut. Untuk menentukan baris kontrak yang harus dibuat faktur, pekerjaan akan melihat tanggal faktur berjalan untuk baris kontrak. Jika baris kontrak milik satu kontrak memiliki tanggal yang sama saat menjalankan faktur, transaksi digabungkan menjadi satu faktur yang memiliki dua baris faktur. Jika tidak ada transaksi untuk membuat faktur, pekerjaan akan melompati pembuatan faktur.

Setelah **ProcessRunner** selesai berjalan, maka ia memanggil **ProcessRunCaller**, menyediakan waktu berakhir, dan ditutup. **ProcessRunCaller** kemudian memulai timer yang berjalan selama 24 jam dari waktu berakhir yang ditentukan. Di akhir timer, **ProcessRunCaller** ditutup.

Pekerjaan proses batch untuk membuat faktur adalah pekerjaan berulang. Jika proses batch ini dijalankan berkali-kali, beberapa instans pekerjaan dibuat dan menyebabkan kesalahan. Oleh karena itu, Anda harus memulai proses batch hanya satu kali, dan Anda harus me-restart hanya jika berhenti berjalan.

> [!NOTE]
> Faktur bets hanya berjalan untuk baris kontrak proyek yang dikonfigurasi dengan jadwal faktur. Baris kontrak dengan metode penagihan harga tetap harus mengonfigurasikan tonggak waktu. Baris kontrak proyek dengan metode waktu dan materi penagihan akan memerlukan pengaturan jadwal faktur berdasarkan tanggal. Hal yang sama berlaku untuk baris kontrak berbasis proyek.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]