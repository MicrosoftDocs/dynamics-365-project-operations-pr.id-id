---
title: Ruang kerja seluler entri waktu proyek
description: Topik ini menyediakan informasi tentang ruang kerja seluler entri waktu proyek. Ruang kerja ini memungkinkan pengguna memasukkan dan menghemat waktu terhadap proyek menggunakan perangkat seluler mereka.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 64a80d931332a4d6edfcd175d7168a7815ddca38
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683956"
---
# <a name="project-time-entry-mobile-workspace"></a>Ruang kerja seluler entri waktu proyek

[!include [banner](../includes/banner.md)]

Topik ini menyediakan informasi tentang ruang kerja seluler **entri waktu proyek**. Ruang kerja ini memungkinkan pengguna memasukkan dan menghemat waktu terhadap proyek menggunakan perangkat seluler mereka.

Ruang kerja Mobile ini ditujukan untuk digunakan dengan aplikasi mobile Dynamics 365 Unified Ops. 

## <a name="overview"></a>Gambaran Umum
Sebagai bagian dari pekerjaan sehari-hari, sumber daya proyek sering berada di lokasi atau bepergian. Ruang kerja seluler **entri waktu proyek** memungkinkan pengguna memasukkan waktu yang dapat ditagih atau tidak dapat ditagih terhadap proyek pada perangkat selular pilihan mereka. Oleh karena itu, sumber daya proyek dapat merekam entri waktu Kapan saja dan dimana pun. Mereka juga dapat melihat entri waktu yang telah direkam. 

Khususnya, di ruang kerja seluler **entri waktu proyek**, pengguna dapat melakukan tugas ini:

-   Untuk tanggal yang dipilih, masukkan jumlah jam yang Anda habiskan pada tugas tertentu.
-   Cari berdasarkan nama proyek atau pelanggan untuk menemukan proyek untuk memasukkan waktunya.
-   Tentukan kategori dan aktivitas untuk waktu yang Anda habiskan.
-   Tagih waktu sebagai dapat ditagih atau tidak dapat ditagih untuk proyek.
-   Atau, masukkan Komentar eksternal atau internal.

## <a name="prerequisites"></a>Prasyarat
Prasyarat berbeda, berdasarkan versi Microsoft Dynamics 365 yang telah disebarkan untuk organisasi Anda.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Prasyarat jika Anda menggunakan Dynamics 365 Finance
Jika Finance telah disebarkan untuk organisasi Anda, administrator sistem harus mempublikasikan ruang kerja seluler **entri waktu proyek**. Untuk petunjuk, lihat [publikasikan ruang kerja seluler](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Prasyarat jika Anda menggunakan versi 1611 dengan pembaruan platform 3 atau yang lebih baru
Jika versi 1611 dengan pembaruan platform 3 atau yang lebih baru telah disebarkan untuk organisasi Anda, administrator sistem harus menyelesaikan prasyarat berikut. 

<table>
<thead>
<tr class="header">
<th>Prasyarat</th>
<th>Peran</th>
<th>Deskripsi</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Menerapkan KB 4018050.</td>
<td>Administrator Sistem</td>
<td>KB 4018050 adalah pembaruan X + + atau hotfix metadata yang berisi ruang kerja seluler <strong>entri waktu proyek</strong>. Untuk menerapkan KB 4018050, administrator sistem harus mengikuti langkah-langkah berikut.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Unduh hotfix metadata dari Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Menginstal hotfix metadata</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Membuat paket yang dapat disebarkan</a> yang berisi model <strong>applicationsuite</strong> dan <strong>projectmobile</strong>, dan kemudian meng-upload paket yang dapat disebarkan untuk LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Terapkan paket yang dapat disebarkan</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publikasikan Ruang kerja seluler <strong>entri waktu proyek</strong>.</td>
<td>Administrator Sistem</td>
<td>Lihat <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">publikasikan ruang kerja seluler</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Men-download dan menginstal aplikasi seluler

Unduh dan instal aplikasi seluler Keuangan dan Operasi:

-   [Untuk Android ponsel](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Untuk iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Masuk ke aplikasi seluler
1.  Buka aplikasi di perangkat seluler Anda.
2.  Masukkan URL Dynamics 365.
3.  Saat pertama kali masuk, Anda akan diminta memasukkan nama pengguna dan sandi. Masukkan kredensial Anda.
4.  Setelah Anda masuk, ruang kerja yang tersedia untuk perusahaan Anda akan ditampilkan. Perhatikan bahwa jika administrator sistem Anda mempublikasikan ruang kerja baru nanti, Anda harus me-refresh Daftar ruang kerja seluler.

[![Tarik untuk me-refresh.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Masukkan waktu dengan menggunakan ruang kerja seluler entri waktu proyek
1.  Di perangkat seluler, pilih ruang kerja **entri waktu proyek**.
2.  Pilih **Entri waktu proyek**. Tanggal kalender untuk minggu ini ditampilkan.
3.  Untuk tanggal yang dipilih, pilih **tindakan** &gt; **entri baru**.
4.  Masukkan jumlah jam untuk dicatat.
5.  Pilih proyek untuk entri waktu. Daftar menampilkan proyek yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, lihat [platform seluler](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Jika proyek Anda tidak ada dalam daftar, pilih **Cari**. Cari berdasarkan nama, atau beralih ke pencarian berdasarkan nama atau pelanggan proyek.
7.  Pilih kategori. Daftar menampilkan kategori yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, lihat [platform seluler](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Jika kategori Anda tidak ada dalam daftar, pilih **Cari**. Cari berdasarkan Kategori, atau beralih ke pencarian berdasarkan nama kategori.
9.  Pilih aktivitas. Daftar menampilkan aktivitas yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, lihat [platform seluler](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Jika aktivitas Anda tidak ada dalam daftar, pilih **Cari**. Cari berdasarkan nomor aktivitas, atau beralih ke pencarian berdasarkan tujuan.

11. Pilih properti baris.
12. Opsional: Masukkan Komentar eksternal dan internal.
13. Pilih **Selesai**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]