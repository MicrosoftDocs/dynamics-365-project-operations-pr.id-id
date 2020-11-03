---
title: Aplikasi seluler Project Timesheet
description: Topik ini menyediakan informasi tentang aplikasi mobile Microsoft Dynamics 365 Project Timesheet. Aplikasi seluler Project Timesheet memungkinkan pengguna memasukkan dan menyetujui lembar waktu untuk proyek di perangkat selularnya.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b9cbd84ecb0d71a99982e158d7e0ea1e236fb369
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078657"
---
# <a name="project-timesheet-mobile-application"></a>Aplikasi seluler Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Gambaran Umum

Aplikasi seluler Microsoft Dynamics 365 Project Timesheet memungkinkan pengguna memasukkan dan menyetujui lembar waktu untuk proyek di perangkat selularnya (iPhone or Android). Aplikasi mobile ini mempermukaan fungsi lembar waktu yang berada di area manajemen proyek dan akuntansi Dynamics 365 Finance, meningkatkan produktivitas dan efisiensi pengguna, serta memungkinkan entri dan persetujuan lembar waktu proyek.

## <a name="download-and-install-the-mobile-app"></a>Men-download dan menginstal aplikasi seluler

Unduh dan instal aplikasi mobile Microsoft Dynamics 365 Project Timesheet untuk Android atau iPhone dari toko perangkat seluler untuk perangkat Anda.

## <a name="enable-the-app"></a>Aktifkan aplikasi 

Di Finance, aplikasi seluler Project Timesheet harus diaktifkan. Untuk mengaktifkan fungsi, buka **manajemen proyek dan parameter akuntansi \> Lembar waktu** lalu pilih parameter **Aktifkan Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Masuk ke aplikasi

1.  Buka aplikasi di perangkat seluler Anda.

2.  Masukkan URL Finance Anda.

3.  Saat pertama kali masuk, Anda akan diminta memasukkan nama pengguna dan sandi. Masukkan kredensial Anda.

4.  Anda akan masuk ke perusahaan default.

## <a name="submit-a-project-timesheet"></a>Kirim lembar waktu proyek

Anda dapat membuat dan mengirimkan lembar waktu proyek di aplikasi. Anda dapat mendasarkan lembar waktu baru pada informasi dari lembar waktu, baris tersimpan, atau tugas proyek sebelumnya. Jika Anda ditunjuk sebagai delegasi, Anda juga dapat memasukkan lembar waktu untuk pekerja lain. Untuk membuat lembar waktu sebagai delegasi, pilih tombol **menu** , lalu pilih nama sumber daya.

Halaman lembar waktu akan membuat lembar waktu baru untuk periode lembar waktu, berdasarkan tanggal saat ini. Pekan kerja akan ditampilkan. Jika periode lembar waktu mencakup beberapa minggu, Anda dapat memilih minggu kerja lain dari tab minggu kerja.
Jika lembar waktu ada untuk tanggal saat ini, maka akan ditampilkan. Jika Anda perlu membuat lembar waktu baru dalam periode lembar waktu yang berbeda, pilih tombol **menu** , lalu pilih **lembar waktu baru**.

Anda dapat memasukkan informasi proyek dengan mengklik tindakan tindakan **Tambah waktu** atau **Salin waktu dari**. Tindakan **Salin Waktu dari** akan menyalin informasi baris proyek, namun bukan jam. Menu **Salin waktu dari** mencakup pilihan berikut:

- **Salin dari lembar waktu yang ada** -Salin baris lembar waktu dari lembar waktu yang ada.

- **Salin dari favorit** -buat baris lembar waktu baru menggunakan pengaturan lembar waktu yang Anda pilih sebagai favorit.

- **Salin dari tugas** -buat baris lembar waktu baru dari proyek yang ditetapkan.

Informasi proyek yang ditampilkan tergantung pada parameter mobile yang Anda tetapkan pada halaman **manajemen proyek dan parameter akuntansi**.

Di bidang **entitas hukum** , pilih entitas hukum untuk pekerjaan proyek yang Anda lakukan. Bidang **entitas hukum** tersedia hanya jika dukungan lembar waktu antarperusahaan telah diaktifkan untuk entitas hukum Anda.

Pilih Pelanggan yang terkait dengan proyek untuk lembar waktu. Untuk rilis awal pada Android, entri oleh pelanggan tidak didukung, karena Anda harus memilih proyek terlebih dahulu. Jika Anda memilih proyek terlebih dahulu, bidang **pelanggan** akan terisi secara otomatis.

Di bidang **proyek** , pilih proyek yang Anda masukkan waktunya. Bidang **pelanggan** diisi secara otomatis.

Pencarian klien dan proyek memungkinkan pencarian di seluruh pelanggan dan proyek.

Pilih informasi di bidang **kategori** , **aktivitas** , **properti baris** , **pajak penjualan grup** , dan bidang **grup pajak penjualan item** sebagaimana diperlukan. Bidang ini dapat ditimpa.

Bidang **properti baris** akan diatur ke nilai default, berdasarkan parameter manajemen proyek dan akuntansi. Bila parameter proyek/kategori dan kategori/sumber daya diaktifkan, **nilai properti baris** akan diatur ke nilai default yang telah Anda tetapkan untuk validasi ini. Bila parameter proyek/kategori dan kategori/sumber daya tidak diaktifkan, **nilai properti baris** akan default sesuai dengan bidang **Aktifkan properti baris default** pada halaman **parameter manajemen proyek dan akuntansi**. Nilai **properti baris** dapat ditimpa.

Pilih hari untuk menambahkan waktu. Masukkan jumlah jam kerja setiap harinya.

Untuk menambahkan komentar tentang jam yang anda masukkan, klik **tambah komentar** , lalu masukkan komentar untuk audiens internal, audiens pelanggan, atau keduanya.
Komentar internal dapat dilihat oleh manajer proyek. Komentar Pelanggan disertakan dalam faktur.

Untuk menyimpan baris sebagai favorit, centang kotak, lalu klik **Simpan sebagai favorit**.

Dimensi keuangan dan dukungan lampiran tidak tersedia di aplikasi seluler.

Lanjutkan menambahkan baris proyek yang diperlukan untuk menyelesaikan lembar waktu Anda.

Klik **kirim** untuk mengirim lembar waktu ke alur kerja persetujuan.

## <a name="review-timesheets"></a>Tinjau Lembar waktu

Daftar lembar waktu yang perlu ditinjau akan tersedia dalam menu. Pilihan ini hanya tersedia jika Anda telah ditetapkan sebagai pemberi persetujuan alur kerja. Persetujuan header dan baris didukung. Persetujuan tingkat baris menawarkan kemampuan untuk menandai satu atau beberapa baris untuk disetujui. Setelah meninjau informasi lembar waktu, klik **setujui** , **Delegasikan** , atau **kembali** untuk melanjutkan alur kerja.
