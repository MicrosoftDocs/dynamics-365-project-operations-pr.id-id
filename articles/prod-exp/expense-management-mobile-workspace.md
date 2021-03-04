---
title: Ruang kerja seluler manajemen pengeluaran
description: Topik ini menyediakan informasi tentang ruang kerja seluler manajemen pengeluaran. Ruang kerja ini memungkinkan pengguna mengambil dan mengunggah tanda terima, sehingga dapat dilampirkan ke laporan pengeluaran nanti. Pengguna juga dapat dengan cepat membuat baris pengeluaran menggunakan tanda terima terlampir, dan membuat serta mengelola laporan pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b6d577861a6ebfae55b64a8a06143256e0f1ff40
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960476"
---
# <a name="expense-management-mobile-workspace"></a>Ruang kerja seluler manajemen pengeluaran

Topik ini menyediakan informasi tentang ruang kerja seluler **manajemen pengeluaran**. Ruang kerja ini memungkinkan pengguna mengambil dan mengunggah tanda terima, sehingga dapat dilampirkan ke laporan pengeluaran nanti. Pengguna juga dapat dengan cepat membuat baris pengeluaran menggunakan tanda terima terlampir, dan membuat serta mengelola laporan pengeluaran. Selain itu, pemberi izin dapat menggunakan ruang kerja seluler **manajemen pengeluaran** untuk melihat laporan pengeluaran yang ditetapkan kepadanya, dan menyetujui atau menolak laporan pengeluaran tersebut.


Ruang kerja Mobile ini ditujukan untuk digunakan dengan aplikasi mobile Dynamics 365 Unified Ops.


## <a name="overview"></a>Gambaran Umum

Banyak organisasi memerlukan salinan tanda terima yang dilampirkan pada laporan terkait perjalanan atau pengeluaran yang terkait dengan bisnis yang diajukan karyawan untuk penggantian. Ruang kerja seluler **Manajemen pengeluaran** memungkinkan pengguna dengan cepat membuat baris pengeluaran baru pada perangkat mobile pilihan mereka menggunakan foto terlampir dari tanda terima. Atau, pengguna dapat mengambil foto tanda terima dan kemudian melampirkannya ke laporan pengeluaran nanti. Karyawan juga dapat membuat dan mengelola laporan pengeluaran mereka, lalu mengirimkannya untuk persetujuan dan penggantian dengan menggunakan perangkat seluler mereka.


Khususnya, ruang kerja seluler **manajemen pengeluaran** memungkinkan pengguna melakukan tugas ini:

- Ambil foto tanda terima, dan Unggah ke Dynamics 365 Finance. Selanjutnya, Anda dapat melampirkan foto tersebut ke laporan pengeluaran nanti.
- Unggah file sebagai tanda terima yang diambil. Selanjutnya, Anda dapat melampirkan file tersebut ke laporan pengeluaran nanti.
- Buat baris pengeluaran baru menggunakan tanda terima terlampir. Selanjutnya Anda dapat menambahkan item baris ke laporan pengeluaran nanti, dan mengirimkannya untuk persetujuan dan penggantian.

Anda juga dapat menggunakan fitur ini:

- Buat laporan pengeluaran baru.
- Melampirkan transaksi kartu kredit dan biaya lainnya yang dibuat sebelumnya ke laporan pengeluaran.
- Buat pengeluaran baru untuk laporan pengeluaran.
- Lampirkan tanda terima untuk pengeluaran apa pun untuk laporan pengeluaran, baik dengan mengambil foto tanda terima maupun dengan mengunggah file sebagai tanda terima.
- Tergantung pada kebijakan pengeluaran perusahaan, tambahkan daftar tamu ke pengeluaran.
- Tergantung pada kebijakan pengeluaran perusahaan, merinci pengeluaran.
- Ajukan Laporan pengeluaran untuk mendapatkan persetujuan dan penggantian.
- Setujui atau Tolak laporan pengeluaran yang mana Anda persetujuan yang ditetapkan.

## <a name="prerequisites"></a>Prasyarat
Prasyarat bervariasi, berdasarkan versi yang telah disebarkan untuk organisasi Anda.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Prasyarat jika Anda menggunakan Dynamics 365 Finance 
Jika Finance telah disebarkan untuk organisasi Anda, administrator sistem harus mempublikasikan ruang kerja seluler **Manajemen pengeluaran**. Untuk petunjuk, lihat [publikasikan ruang kerja seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Prasyarat jika Anda menggunakan versi 1611 dengan pembaruan platform 3 atau yang lebih baru
Jika versi 1611 dengan pembaruan platform 3 atau yang lebih baru telah disebarkan untuk organisasi Anda, administrator sistem harus menyelesaikan prasyarat berikut. 

<table>
<thead>
<tr class="header">
<th>Prasyarat</th>
<th>Peran</th>
<th>KETERANGAN</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Menerapkan KB 4019015.</td>
<td>Administrator Sistem</td>
<td>KB 4019015 adalah pembaruan X + + atau hotfix metadata yang berisi ruang kerja seluler <strong>Manajemen pengeluaran</strong>. Untuk menerapkan KB 4019015, administrator sistem harus mengikuti langkah-langkah berikut.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Unduh hotfix metadata dari Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Menginstal hotfix metadata</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Membuat paket yang dapat disebarkan</a> yang berisi model <strong>applicationsuite</strong> dan <strong>ExpenseMobile</strong>, dan kemudian meng-upload paket yang dapat disebarkan untuk LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Terapkan paket yang dapat disebarkan</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publikasikan ruang kerja seluler <strong>manajemen pengeluaran</strong>.</td>
<td>Administrator Sistem</td>
<td>Lihat <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">publikasikan ruang kerja seluler</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Men-download dan menginstal aplikasi seluler Dynamics 365 for Operations
Unduh dan instal aplikasi seluler Dynamics 365 Unified Ops:

- [Untuk Android ponsel](https://go.microsoft.com/fwlink/?linkid=850662)
- [Untuk iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Masuk ke aplikasi seluler
1. Buka aplikasi di perangkat seluler Anda.
2. Masukkan URL Dynamics 365.
4. Saat pertama kali masuk, Anda akan diminta memasukkan nama pengguna dan sandi. Masukkan kredensial Anda.
5. Setelah Anda masuk, ruang kerja yang tersedia untuk perusahaan Anda akan ditampilkan. Perhatikan bahwa jika administrator sistem Anda mempublikasikan ruang kerja baru nanti, Anda harus me-refresh Daftar ruang kerja seluler.


[![Tarik untuk me-refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Mengambil tanda terima menggunakan ruang kerja seluler manajemen pengeluaran

1. Di perangkat seluler, buka ruang kerja **manajemen pengeluaran**.
2. Pilih **Ambil tanda terima**.
3. Pilih **Ambil foto** atau **pilih gambar**.
4. Ikuti salah satu langkah berikut:

    - Jika Anda memilih **Ambil foto**, ikuti langkah berikut:

        1. Anda akan diarahkan ke kamera di perangkat seluler, sehingga Anda dapat mengambil foto tanda terima. Setelah selesai mengambil foto, pilih **OK** untuk menerima foto.
        2. Opsional: masukkan nama untuk foto, lalu masukkan catatan.

    - Jika Anda memilih **pilih gambar**, ikuti langkah berikut:

        1. Pilih gambar dalam daftar.
        2. Opsional: masukkan nama untuk gambar, lalu masukkan catatan.

5. Pilih **Selesai**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Dengan cepat masukkan pengeluaran dengan menggunakan ruang kerja seluler manajemen pengeluaran
1. Di perangkat seluler, buka ruang kerja **manajemen pengeluaran**.
2. Pilih **entri pengeluaran cepat**.
3. Pilih kategori pengeluaran. Anda melihat daftar kategori pengeluaran yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, pengembang harus melihat [platform seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika kategori Anda tidak ada dalam daftar, pilih **Cari** untuk melakukan pencarian online. Cari berdasarkan Kategori pengeluaran, atau beralih ke pencarian berdasarkan jenis pengeluaran.
4. Masukkan tanggal transaksi pengeluaran.
5. Opsional: masukkan Penjual untuk pengeluaran.
6. Masukkan jumlah pengeluaran.
7. Pilih mata uang pengeluaran. Anda melihat daftar kode mata uang yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 400 mata uang dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, pengembang harus melihat [platform seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika mata uang Anda tidak ada dalam daftar, pilih **Cari** untuk melakukan pencarian online. Cari berdasarkan mata uang, atau beralih ke pencarian berdasarkan nama.
8. Pilih **Ambil foto** atau **pilih gambar**.
9. Ikuti salah satu langkah berikut:

    - Jika Anda memilih **Ambil foto**, Anda akan diarahkan ke kamera di perangkat seluler, sehingga Anda dapat mengambil foto tanda terima. Setelah selesai mengambil foto, pilih **OK** untuk menerima foto.
    - Jika Anda memilih **pilih gambar**, pilih gambar dalam daftar.

10. Pilih **Selesai**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Setujui laporan pengeluaran dengan menggunakan ruang kerja seluler manajemen pengeluaran (jika Anda menggunakan Pembaruan 2017 Juli)
1. Di perangkat seluler, buka ruang kerja **manajemen pengeluaran**.
2. **Persetujuan pengeluaran** menunjukkan jumlah laporan pengeluaran yang ditetapkan kepada Anda untuk disetujui. Nomor akan diperbarui kira-kira setiap 30 menit. Pilih **persetujuan pengeluaran**.

    Korporat daftar pengeluaran yang ditetapkan kepada Anda untuk disetujui ditampilkan.
    
3. Pilih laporan pengeluaran untuk melihat rincian pengeluaran untuk itu.
4. Pilih pengeluaran untuk melihat rincian untuk itu. Informasi yang ditampilkan untuk pengeluaran mencakup tanda terima, tamu, dan detail perincian.
5. Kembali pada halaman **laporan pengeluaran**, pilih untuk menyetujui atau menolak laporan pengeluaran.
6. Masukkan Komentar untuk tindakan persetujuan.
7. Pilih **Selesai**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Buat laporan pengeluaran baru dan ajukan untuk persetujuan dengan menggunakan ruang kerja seluler manajemen pengeluaran (jika Anda menggunakan Pembaruan 2017 Juli)
1. Di perangkat seluler, buka ruang kerja **manajemen pengeluaran**.
2. Pilih **entri pengeluaran**.
3. Pilih **laporan baru**, atau pilih laporan pengeluaran yang ada dalam daftar.
4. Untuk laporan pengeluaran baru, masukkan tujuan dan informasi tambahan yang tersedia. Informasi ini berbeda-beda, tergantung pada cara manajemen pengeluaran dikonfigurasi untuk perusahaan Anda.
5. Pilih **Selesai**.
6. Untuk menambahkan pengeluaran yang ada, seperti transaksi kartu kredit, ke laporan pengeluaran, pilih **lampirkan**.
7. Pilih satu atau beberapa pengeluaran dalam daftar.
8. Pilih **Selesai**.
9. Untuk menambahkan pengeluaran baru ke laporan biaya, pilih **pengeluaran baru**.
10. Pilih kategori pengeluaran. Anda melihat daftar kategori pengeluaran yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, pengembang harus melihat [platform seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika kategori Anda tidak ada dalam daftar, pilih **Cari** untuk melakukan pencarian online. Cari berdasarkan Kategori pengeluaran, atau beralih ke pencarian berdasarkan jenis pengeluaran.
11. Opsional: masukkan Penjual untuk pengeluaran.
12. Masukkan tanggal transaksi pengeluaran.
13. Masukkan jumlah pengeluaran.
14. Pilih mata uang pengeluaran. Anda melihat daftar kode mata uang yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 400 mata uang dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, pengembang harus melihat [platform seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika mata uang Anda tidak ada dalam daftar, pilih **Cari** untuk melakukan pencarian online. Cari berdasarkan mata uang, atau beralih ke pencarian berdasarkan nama.
15. Pilih **Selesai**.
16. Untuk menambahkan rincian lainnya ke pengeluaran, pilih **Tambah rincian lainnya**. Bidang yang tersedia tergantung pada konfigurasi manajemen pengeluaran untuk perusahaan Anda.
17. Jika kebijakan perusahaan memerlukan tanda terima untuk pengeluaran, pilih **tanda terima**, lalu ikuti langkah-langkah berikut:

    1. Pilih **Ambil tanda terima** atau **lampirkan tanda terima**.
    2. Ikuti salah satu langkah berikut:

        - Jika Anda memilih **Ambil tanda terima**, ikuti langkah berikut:

            1. Pilih **Ambil foto** atau **pilih gambar**.
            2. Ikuti salah satu langkah berikut:

                - Jika Anda memilih **Ambil foto**, ikuti langkah berikut:

                    1. Anda akan diarahkan ke kamera di perangkat seluler, sehingga Anda dapat mengambil foto tanda terima. Setelah selesai mengambil foto, pilih **OK** untuk menerima foto.
                    2. Opsional: masukkan nama untuk foto, lalu masukkan catatan.

                - Jika Anda memilih **pilih gambar**, ikuti langkah berikut:

                    1. Pilih gambar dalam daftar.
                    2. Opsional: masukkan nama untuk gambar, lalu masukkan catatan.

            3.  Pilih **Selesai**.

        - Jika Anda memilih **Lampirkan tanda terima**, ikuti langkah berikut:

            1.  Pilih satu atau beberapa gambar dalam daftar.
            2.  Pilih **Selesai**.

    3. Pilih tombol **kembali** untuk kembali ke rincian pengeluaran.

18. Jika kebijakan perusahaan memerlukan tamu untuk pengeluaran, pilih **Tamu**, lalu ikuti langkah-langkah berikut:

    1. Pilih **tamu**, **tamu sebelumnya**, atau **rekan kerja**.
    2. Ikuti salah satu langkah berikut:

        - Jika Anda memilih **Tamu**, ikuti langkah berikut:

            1. Masukkan nama tamu.
            2. Opsional: masukkan organisasi dan/atau negara tamu.
            3. Opsional: Masukkan jabatan tamu.
            4. Pilih **Selesai**.

        - Jika Anda memilih **Tamu sebelumnya**, ikuti langkah berikut:

            1. Pilih satu atau beberapa tamu sebelumnya dalam daftar. Anda akan melihat daftar tamu sebelumnya yang telah ditambahkan ke laporan pengeluaran sebelumnya yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, pengembang harus melihat [platform seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika tamu sebelumnya tidak ada dalam daftar, pilih **Cari** untuk melakukan pencarian online. Cari berdasarkan nama, atau beralih ke pencarian berdasarkan organisasi, negara, atau jabatan.
            2. Pilih **Selesai**.

        - Jika Anda memilih **Rekan kerja**, ikuti langkah berikut:

            1. Pilih satu atau beberapa rekan kerja dalam daftar. Anda melihat daftar rekan kerja yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, pengembang harus melihat [platform seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika rekan kerja Anda tidak ada dalam daftar, pilih **Cari** untuk melakukan pencarian online. Cari berdasarkan nama, atau beralih ke pencarian berdasarkan perusahaan atau jabatan.
            2. Pilih **Selesai**.

    3. Pilih tombol **kembali** untuk kembali ke rincian pengeluaran.

19. Jika kebijakan perusahaan mengharuskan agar pengeluaran dirinci, pilih **Rinci**, lalu ikuti langkah-langkah berikut:

    1. Pilih tanggal pertama yang akan diperinci.
    2. Pilih **Tambah Perincian**.
    3. Pilih subkategori perincian pengeluaran. Anda melihat daftar subkategori pengeluaran yang dimuat ke aplikasi Anda untuk penggunaan offline. Secara default, 50 item dimuat, namun pengembang dapat mengubah nomor ini. Untuk informasi selengkapnya, pengembang harus melihat [platform seluler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika subkategori Anda tidak ada dalam daftar, pilih **Cari** untuk melakukan pencarian online. Cari berdasarkan nama subkategori pengeluaran.
    4. Masukkan jumlah transaksi untuk perincian.
    5. Edit tanggal transaksi jika diperlukan.
    6. Pilih **Selesai**.
    7. Ulangi langkah sebelumnya hingga Anda selesai menambahkan semua itemisasi untuk tanggal yang dipilih.
    8. Untuk hari tambahan, Anda dapat memilih **salin ke hari berikutnya** untuk menyalin itemisasi ke hari berikutnya. Atau, Anda dapat memilih tanggal untuk merinci dan kemudian menambahkan itemisasi seperti yang Anda lakukan untuk tanggal pertama.
    9. Setelah selesai merinci pengeluaran, pilih tombol **kembali** untuk kembali ke rincian pengeluaran.

20. Pilih tombol **kembali** untuk kembali ke halaman **laporan pengeluaran**.
21. Ulangi langkah sebelumnya hingga Anda selesai menambahkan semua pengeluaran.
22. Pilih **kirim**.
23. Masukkan Komentar untuk penyetuju.
24. Pilih **Selesai**.
