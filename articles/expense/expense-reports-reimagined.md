---
title: Laporan pengeluaran model baru
description: Topik ini menyediakan informasi tentang pengalaman yang didesain ulang dan yang dirancang ulang untuk entri laporan pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122798"
---
# <a name="expense-reports-reimagined"></a>Laporan pengeluaran model baru

Entri laporan pengeluaran telah dirancang ulang untuk menyederhanakan proses dan mengurangi waktu yang diperlukan untuk menyelesaikan laporan. Berikut adalah komponen utama dari pengalaman pengeluaran baru:

- Ruang kerja manajemen pengeluaran baru yang memungkinkan Anda mengakses pengeluaran delegasi.
- Pengalaman pencocokan tanda terima baru untuk lebih baik menampilkan tanda terima tingkat header dan menyederhanakan proses melampirkan tanda terima ke baris pengeluaran.
- Kisi baru baca-saja yang memungkinkan Anda melihat lebih banyak baris pengeluaran dan kolom data tambahan. Anda sekarang dapat melihat semua baris yang terperinci dan terpisah, bersama dengan pengeluaran induknya.
- Panel yang disederhanakan untuk mengedit pengeluaran.
- Pesan kesalahan, peringatan, dan kebijakan yang dirancang ulang untuk menyediakan konteks dan pemahaman yang benar mengenai masalah dan cara mengatasinya. Kami telah menghapus beberapa pesan yang muncul sebelum pengguna dapat menyelesaikan tugas mereka dan menangani masalah.
- Halaman baru untuk menentukan bidang yang diperlukan, bidang opsional, dan bidang yang tidak boleh disertakan. Halaman ini membantu mengurangi jumlah bidang yang harus ditetapkan.
- Tampilan dan nuansa baru untuk laporan pengeluaran, sehingga laporan tidak lagi tampak seakan-akan dirancang untuk persona akuntansi.

Untuk mengaktifkan pengalaman baru, gunakan ruang kerja **fitur manajemen** untuk mengaktifkan fitur **penulisan ulang laporan pengeluaran**. Bila Anda mengaktifkan fitur ini, maka tindakan berikut terjadi:

- Ruang kerja pengeluaran yang ada digantikan dengan ruang kerja baru.
- Item menu baru untuk visibilitas bidang pengeluaran ditambahkan.
- Tidak ada item menu untuk laporan pengeluaran (halaman yang ada) atau bidang laporan pengeluaran dihapus.
- Alur kerja dan persetujuan apa pun tetap akan membawa Anda ke halaman laporan pengeluaran yang ada.

## <a name="getting-started-video-for-new-users"></a>Persiapan video untuk pengguna baru

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Video [Pengalaman pengeluaran di Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (ditampilkan di atas) tercakup dalam [Daftar putar Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) yang tersedia di YouTube.

## <a name="new-features"></a>Fitur baru

| Fitur baru | KETERANGAN |
|---|----|
| Visibilitas bidang pengeluaran | Halaman penataan baru memungkinkan Anda menentukan bidang yang harus dinonaktifkan untuk organisasi, bidang yang harus diminta, dan bidang yang disarankan. |
| Bidang yang diperlukan | Konfigurasi sederhana baru memungkinkan Anda membuat beberapa bidang yang diperlukan tanpa harus menggunakan kerangka kebijakan. |
| Bidang Opsional | Halaman kedua untuk bidang opsional ditambahkan. Dengan cara ini, karyawan tidak akan merasa seolah-olah mereka harus mengatur bidang, namun bidang masih dapat diakses dengan mudah. |
| Menambahkan tanda terima yang tidak terlampir | Kemampuan untuk menambahkan tanda terima tidak terlampir ke laporan pengeluaran lebih terlihat dari ruang kerja dan laporan pengeluaran. |
| Pesan yang disempurnakan | Ada visibilitas yang lebih baik ke baris pengeluaran yang memiliki peringatan atau kesalahan. |
| Mengurangi pesan di bilah pesan| Jumlah pesan Infolog menurun, dan upaya dibuat untuk mencegah pesan duplikat ditampilkan di banyak kasus. |
| Dikelompokkan bersama tindakan umum | Antarmuka dibersihkan dengan penambahan tombol tindakan baru untuk sebagian besar tindakan tingkat baris Umum dan penambahan tombol elipsis (...) untuk header dan tindakan lainnya yang kurang sering. |
| Ruang kerja baru untuk meningkatkan visibilitas | Ruang kerja baru menyatukan fitur dan tautan yang memungkinkan pengguna beralih ke area yang berbeda. |
| Menambahkan biaya dan penerimaan yang ada selama pembuatan pengeluaran | Saat membuat laporan pengeluaran, Anda dapat menambahkan semua pengeluaran dan kuitansi yang dipilih. |
| Kalkulator kurs | Kalkulator kurs ditambahkan yang memungkinkan Anda menghitung nilai tukar untuk transaksi multi mata uang mandiri. |
| Simpan dan tambahkan baris pengeluaran baru | Tombol **Simpan** dan **baru** tersedia bila pengeluaran baru dimasukkan, untuk membantu Anda dengan cepat memasukkan baris pengeluaran. |
| Visibilitas yang lebih baik ke baris terpisah dan terperinci | Baris terperinci dan terpisah ditambahkan langsung ke daftar pengeluaran untuk meningkatkan visibilitas dan membantu Anda dengan mudah menentukan apakah ada kesalahan. |
| Tampilkan tanda terima selama itemisasi | Tanda terima dapat ditampilkan selama itemisasi. |

Rilis awal difokuskan pada skenario entri pengeluaran. Skenario pengeluaran laporan atau skenario persetujuan akan terus menggunakan halaman entri pengeluaran yang ada.

Fitur berikut ada di halaman lama namun belum ada di halaman baru. Fitur ini akan diperkenalkan ulang selama beberapa rilis berikutnya:

- Persetujuan
- Persetujuan utang dagang dan kemampuan untuk mengedit akuntansi
- Beberapa titik masuk
- Integrasi Permintaan perjalanan
- Entitas data untuk visibilitas bidang pengeluaran
- Entri untuk pengeluaran uang saku
- Alur kerja tingkat baris
- Dukungan pemberi persetujuan sementara
- Itemisasi lanjutan
