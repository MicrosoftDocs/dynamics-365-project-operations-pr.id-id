---
title: Konfigurasi sumber daya proyek
description: Artikel ini menyediakan informasi tentang menyiapkan atau meminta sumber daya proyek.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933772"
---
# <a name="set-up-project-resources"></a>Konfigurasi sumber daya proyek

[!include [banner](../includes/banner.md)]

Anda harus mengkonfigurasi kalender dan mengaitkannya dengan karyawan atau pekerja. Kalender digunakan untuk menjadwalkan proyek dan waktu kerja sumber daya yang dicadangkan untuk proyek. Selama pengaturan kalender, manajer proyek dapat melakukan perataan sumber daya sebagai bagian dari pengoptimalan sumber daya. Berdasarkan jadwal kalender, pembatasan dapat diletakkan pada sumber daya. Anda dapat mengkonfigurasi kalender di halaman **kalender**.

Bila Anda mengkonfigurasi pekerja sebagai sumber daya proyek, Anda dapat memilih dari pekerja yang bekerja di perusahaan yang akan Anda siapkan sumber dayanya. Atau, Anda dapat memilih pekerja dari perusahaan lain di organisasi Anda. Pekerja ini disebut sebagai sumber daya antarperusahaan.

Prosedur berikut menjelaskan cara mengkonfigurasi pekerja sebagai sumber daya proyek di perusahaan Anda dan cara mengkonfigurasi sumber daya proyek antarperusahaan.

## <a name="set-up-a-worker-as-a-project-resource"></a>Mengkonfigurasi pekerja sebagai sumber daya proyek

1. Pada halaman **pekerja**, dalam **Daftar pekerja**, pilih pekerja yang Anda tambahkan sebagai sumber daya proyek, dan buka rekaman pekerja.
2. Pada panel tindakan, pilih **proyek** &gt; **konfigurasi** &gt; **Konfigurasi proyek**.
3. Pilih kalender, lalu tutup halaman.

Anda juga dapat menentukan proyek default untuk sumber daya sebagai jenis pra-penugasan. Pra-penugasan dapat digunakan saat manajer sumber daya atau manajer proyek mengetahui proyek yang akan dikerjakan oleh sumber daya sebelumnya. Pra-penugasan juga dapat didasarkan pada permintaan sponsor proyek atau pelanggan. Untuk melakukan pra-penugasan proyek, pada halaman **Tugaskan proyek**, pada tab **proyek**, dalam **Daftar proyek yang tersisa**, pilih proyek yang sesuai.

## <a name="set-up-an-intercompany-resource"></a>Mengkonfigurasi sumber daya Antarperusahaan

Bila Anda mengkonfigurasi pekerja sebagai sumber daya antar, Anda harus menyelesaikan konfigurasi di perusahaan pemberi yang eminjamkan dan perusahaan yang meminjam.

### <a name="in-the-lending-company"></a>Di perusahaan yang meminjamkan

1. Dalam Finance, verifikasikan bahwa perusahaan yang meminjamkan dipilih, lalu selesaikan prosedur di bagian sebelumnya, "Atur pekerja sebagai sumber daya proyek."
2. Pada halaman **Akuntansi antarperusahaan**, pilih **baru**.
3. Di bidang **id entitas hukum**, pilih perusahaan yang meminjamkan. Isi bidang tersisa sebagaimana dibutuhkan, lalu pilih **Simpan**.
4. Pada halaman **Transfer harga**, pilih **baru**.
5. Di bidang **Entitas hukum yang meminjam**, pilih perusahaan yang sesuai.
6. Untuk meminjamkan pada perusahaan yang meminjam, hanya sumber daya yang Anda buat di awal bagian ini, di bidang **sumber daya**, pilih nama sumber daya yang Anda buat. Untuk membuat semua sumber daya di perusahaan pinjaman yang tersedia untuk perusahaan pinjaman, biarkan bidang **sumber daya** kosong.
7. Pada halaman **manajemen proyek dan parameter akuntansi**, pada tab **Antarperusahaan**, atur pilihan **Aktifkan penjadwalan sumber daya dan lembar waktu** ke **ya**.

### <a name="in-the-borrowing-company"></a>Di perusahaan yang meminjam

- Pada halaman **daftar sumber daya**, di filter pencarian, masukkan nama sumber daya yang Anda buat untuk perusahaan yang eminjamkan, untuk memverifikasi bahwa nama tersebut tercakup dalam daftar sumber daya untuk perusahaan yang meminjam.

## <a name="request-project-resources"></a>Meminta sumber daya proyek
Fungsi untuk penjadwalan sumber daya proyek hanya memungkinkan manajer sumber daya mendistribusikan sumber daya pada keterlibatan atau proyek. Untuk mengaktifkan fungsi ini, selesaikan tugas berikut, atau Verifikasikan bahwa mereka telah selesai:

- Atur urutan nomor.
- Konfigurasikan manajemen proyek dan alur kerja akuntansi.
- Aktifkan alur kerja permintaan sumber daya.

Setelah tugas sebelumnya selesai, Anda dapat menyelesaikan tugas berikut saat memerlukan:

- Buat permintaan sumber daya dari sumber daya staf yang dipesan dengan tentatif.
- Memantau permintaan sumber daya.
- Memenuhi permintaan sumber daya.
- Meminta staf sumber daya dari WBS.
- Memesan sumber daya ke proyek tanpa meminta sumber daya staf.


[!INCLUDE[footer-include](../includes/footer-banner.md)]