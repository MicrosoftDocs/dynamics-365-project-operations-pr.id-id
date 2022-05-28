---
title: Laporan pengeluaran yang ditata ulang (berisi video)
description: Laporan topik menjelaskan pengalaman yang didesain ulang dan ditata ulang untuk entri laporan pengeluaran.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 562ec3701a607ed95f663f3e0846d044b3bf504e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586946"
---
# <a name="expense-reports-reimagined"></a>Laporan pengeluaran model baru

Entri laporan pengeluaran telah dirancang ulang untuk menyederhanakan proses dan mengurangi waktu yang diperlukan untuk menyelesaikan laporan. Berikut adalah komponen utama dari pengalaman pengeluaran baru:

- Ruang kerja manajemen pengeluaran baru yang memungkinkan Anda mengakses pengeluaran delegasi.
- Pengalaman pencocokan tanda terima baru untuk lebih baik menampilkan tanda terima tingkat header dan menyederhanakan proses melampirkan tanda terima ke baris pengeluaran.
- Kisi hanya baca baru yang memungkinkan Anda melihat lebih banyak baris pengeluaran dan kolom data lainnya. Anda sekarang dapat melihat semua baris yang terperinci dan terpisah, bersama dengan pengeluaran induknya.
- Panel yang disederhanakan untuk mengedit pengeluaran.
- Pesan kesalahan, peringatan, dan kebijakan yang dirancang ulang untuk menyediakan konteks dan pemahaman yang benar mengenai masalah dan cara mengatasinya. Kami telah menghapus beberapa pesan yang muncul sebelum pengguna dapat menyelesaikan tugas mereka dan menangani masalah.
- Halaman baru untuk menentukan bidang yang diperlukan, bidang opsional, dan bidang yang tidak boleh disertakan. Halaman ini membantu mengurangi jumlah bidang yang harus ditetapkan.
- Tampilan dan nuansa baru untuk laporan pengeluaran, sehingga laporan tidak lagi tampak seakan-akan dirancang untuk persona akuntansi.

Untuk mengaktifkan pengalaman baru, gunakan ruang kerja **manajemen Fitur** untuk mengaktifkan fitur **ruang kerja yang nuansa baru laporan Pengeluaran**. Bila Anda mengaktifkan fitur ini, maka tindakan berikut terjadi:

- Ruang kerja pengeluaran yang ada digantikan dengan ruang kerja baru.
- Item menu baru untuk visibilitas bidang pengeluaran ditambahkan.
- Tidak ada item menu untuk laporan pengeluaran (halaman yang ada) atau bidang laporan pengeluaran dihapus.
- Alur kerja dan persetujuan apa pun tetap akan membawa Anda ke halaman laporan pengeluaran yang ada.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Fitur baru

| Fitur baru | KETERANGAN |
|---|----|
| Visibilitas bidang pengeluaran | Halaman konfigurasi baru memungkinkan Anda menentukan bidang yang harus dinonaktifkan untuk organisasi. Anda juga dapat menentukan bidang yang harus diisi dan bidang yang disarankan. |
| Bidang yang diperlukan | Konfigurasi sederhana baru memungkinkan Anda membuat beberapa bidang yang diperlukan tanpa harus menggunakan kerangka kebijakan. |
| Bidang Opsional | Halaman kedua untuk bidang opsional ditambahkan. Dengan cara ini, karyawan tidak akan merasa seolah-olah mereka harus mengatur bidang, namun bidang masih dapat diakses dengan mudah. |
| Menambahkan tanda terima yang tidak terlampir | Kemampuan untuk menambahkan tanda terima tidak terlampir ke laporan pengeluaran lebih terlihat dari ruang kerja dan laporan pengeluaran. |
| Pesan yang disempurnakan | Ada visibilitas yang lebih baik ke baris pengeluaran yang memiliki peringatan atau kesalahan. |
| Mengurangi pesan di bilah pesan| Jumlah pesan Infolog menurun, dan upaya dibuat untuk mencegah pesan duplikat ditampilkan di banyak kasus. |
| Dikelompokkan bersama tindakan umum | Antarmuka dibersihkan dengan penambahan tombol tindakan baru untuk sebagian besar tindakan tingkat baris Umum dan penambahan tombol elipsis (...) untuk header dan tindakan lainnya yang kurang sering. |
| Ruang kerja baru untuk meningkatkan visibilitas | Ruang kerja baru menyatukan fitur dan tautan yang memungkinkan pengguna beralih ke area yang berbeda. |
| Menambahkan biaya dan penerimaan yang ada selama pembuatan pengeluaran | Saat membuat laporan pengeluaran, Anda dapat menambahkan semua pengeluaran, atau memilih pengeluaran yang tidak dilampirkan. Pengeluaran yang tidak dilampirkan adalah pengeluaran yang diimpor dari umpan atau pengeluaran kartu kredit korporasi yang dibuat secara manual oleh pengguna, namun belum dilampirkan ke laporan pengeluaran.|
| Kalkulator kurs | Kalkulator kurs ditambahkan yang memungkinkan Anda menghitung nilai tukar untuk transaksi multi mata uang mandiri. |
| Simpan dan tambahkan baris pengeluaran baru | Tombol **Simpan** dan **baru** tersedia bila pengeluaran baru dimasukkan, untuk membantu Anda dengan cepat memasukkan baris pengeluaran. |
| Visibilitas yang lebih baik ke baris terpisah dan terperinci | Baris terperinci dan terpisah ditambahkan langsung ke daftar pengeluaran untuk meningkatkan visibilitas dan membantu Anda dengan mudah menentukan apakah ada kesalahan. |
| Melihat rincian subkategori di baris terperinci | Baris item dari pengeluaran induk memperlihatkan label subkategori pada laporan pengeluaran. Itemisasi memungkinkan Anda meninjau detail terperinci secara sekilas.|
|Merinci pengeluaran berulang dengan cepat | Ruang kerja pengeluaran yang ditata ulang menyediakan kemampuan untuk merinci pengeluaran berulang dengan cepat dengan menambahkan subkategori, tanggal mulai, dan kuantitas. Kuantitas mengacu pada berapa kali muatan diulang selama periode kontinu. |
| Tampilkan tanda terima selama itemisasi | Tanda terima dapat ditampilkan selama itemisasi. |
| Pilihan Uang muka | Pilih satu atau beberapa uang muka tunai untuk memenuhi satu transaksi pengeluaran. |
| saldo Uang muka | Tinjau saldo uang muka secara real time bila Anda membuat entri pengeluaran dengan uang muka yang disetujui dan dibayar. |

Rilis awal difokuskan pada skenario entri pengeluaran. Skenario pengeluaran laporan atau skenario persetujuan akan terus menggunakan halaman entri pengeluaran yang ada.


Fitur berikut tidak didukung pada ruang kerja nuansa baru laporan Pengeluaran, namun direncanakan untuk rilis mendatang: 

- Integrasi Permintaan perjalanan
- Entri pengeluaran uang saku
- Dukungan pemberi persetujuan sementara
- Kemampuan untuk melihat riwayat alur kerja


[!INCLUDE[footer-include](../includes/footer-banner.md)]
