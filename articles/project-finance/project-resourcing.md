---
title: Penentuan sumber daya proyek
description: Topik ini menyediakan informasi tentang penentuan sumber daya proyek.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752372"
---
# <a name="project-resourcing"></a>Penentuan sumber daya proyek

[!include [banner](../includes/banner.md)]

Topik ini menyediakan informasi tentang penentuan sumber daya proyek.

Satu tantangan untuk manajer proyek dan manajer sumber daya selama tahap perencanaan proyek adalah alokasi sumber daya, di mana mereka harus menentukan dan mencadangkan sumber daya yang benar untuk mengerjakan proyek. Di Dynamics 365 Finance, kemampuan sumber daya untuk proyek memungkinkan Anda menentukan peran yang dianggap sebagai sumber daya sementara yang dapat dicadangkan untuk keterlibatan atau bagian keterlibatan tertentu. Jenis penentuan sumber daya ini memungkinkan manajer dan manajer proyek menyelesaikan tugas berikut:

- Menentukan peran yang memiliki kompetensi yang diperlukan, sehingga mudah untuk mencocokkan sumber daya.
- menggunakan peran untuk menentukan jadwal keterlibatan awal yang didasarkan pada sumber daya cadangan.
- Mengestimasi biaya dan menentukan anggaran awal, berdasarkan peran dan sumber daya yang ditetapkan untuk proyek.
- menggunakan peran untuk memperkirakan jumlah pemesanan sumber daya yang diperlukan untuk setiap keterlibatan.
- Memperkirakan jumlah sumber daya yang diperlukan untuk seluruh siklus hidup suatu proyek.
- Merencanakan struktur rincian kerja (WBS) dengan menggunakan penetapan awal sumber daya.

[![Siklus hidup proyek](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Seiring berjalannya Perencanaan proyek, sumber daya yang direncanakan dapat digantikan dengan sumber daya staf. Manajer Proyek juga dapat kembali dan memperbarui reservasi sumber daya selama setiap tahapan proyek.

## <a name="set-up-project-resources"></a>Konfigurasi sumber daya proyek
Anda harus mengkonfigurasi kalender dan mengaitkannya dengan karyawan atau pekerja. Kalender digunakan untuk menjadwalkan proyek dan waktu kerja sumber daya yang dicadangkan untuk proyek. Selama pengaturan kalender, manajer proyek dapat melakukan perataan sumber daya sebagai bagian dari pengoptimalan sumber daya. Berdasarkan jadwal kalender, pembatasan dapat diletakkan pada sumber daya. Anda dapat mengkonfigurasi kalender di halaman **kalender**.

Bila Anda mengkonfigurasi pekerja sebagai sumber daya proyek, Anda dapat memilih dari pekerja yang bekerja di perusahaan yang akan Anda siapkan sumber dayanya. Atau, Anda dapat memilih pekerja dari perusahaan lain di organisasi Anda. Pekerja ini disebut sebagai sumber daya antarperusahaan.

Prosedur berikut menjelaskan cara mengkonfigurasi pekerja sebagai sumber daya proyek di perusahaan Anda dan cara mengkonfigurasi sumber daya proyek antarperusahaan.

### <a name="set-up-a-worker-as-a-project-resource"></a>Mengkonfigurasi pekerja sebagai sumber daya proyek

1. Pada halaman **pekerja**, dalam **Daftar pekerja**, pilih pekerja yang Anda tambahkan sebagai sumber daya proyek, dan buka rekaman pekerja.
2. Pada panel tindakan, pilih **proyek** &gt; **konfigurasi** &gt; **Konfigurasi proyek**.
3. Pilih kalender, lalu tutup halaman.

Anda juga dapat menentukan proyek default untuk sumber daya sebagai jenis pra-penugasan. Pra-penugasan dapat digunakan saat manajer sumber daya atau manajer proyek mengetahui proyek yang akan dikerjakan oleh sumber daya sebelumnya. Pra-penugasan juga dapat didasarkan pada permintaan sponsor proyek atau pelanggan. Untuk melakukan pra-penugasan proyek, pada halaman **Tugaskan proyek**, pada tab **proyek**, dalam **Daftar proyek yang tersisa**, pilih proyek yang sesuai.

### <a name="set-up-an-intercompany-resource"></a>Mengkonfigurasi sumber daya Antarperusahaan

Bila Anda mengkonfigurasi pekerja sebagai sumber daya antar, Anda harus menyelesaikan konfigurasi di perusahaan pemberi yang eminjamkan dan perusahaan yang meminjam.

**Di perusahaan yang meminjamkan**

1. Dalam Finance, verifikasikan bahwa perusahaan yang meminjamkan dipilih, lalu selesaikan prosedur di bagian sebelumnya, "Atur pekerja sebagai sumber daya proyek."
2. Pada halaman **Akuntansi antarperusahaan**, pilih **baru**.
3. Di bidang **id entitas hukum**, pilih perusahaan yang meminjamkan. Isi bidang tersisa sebagaimana dibutuhkan, lalu pilih **Simpan**.
4. Pada halaman **Transfer harga**, pilih **baru**.
5. Di bidang **Entitas hukum yang meminjam**, pilih perusahaan yang sesuai.
6. Untuk meminjamkan pada perusahaan yang meminjam, hanya sumber daya yang Anda buat di awal bagian ini, di bidang **sumber daya**, pilih nama sumber daya yang Anda buat. Untuk membuat semua sumber daya di perusahaan pinjaman yang tersedia untuk perusahaan pinjaman, biarkan bidang **sumber daya** kosong.
7. Pada halaman **manajemen proyek dan parameter akuntansi**, pada tab **Antarperusahaan**, atur pilihan **Aktifkan penjadwalan sumber daya dan lembar waktu** ke **ya**.

**Di perusahaan yang meminjam**

- Pada halaman **daftar sumber daya**, di filter pencarian, masukkan nama sumber daya yang Anda buat untuk perusahaan yang eminjamkan, untuk memverifikasi bahwa nama tersebut tercakup dalam daftar sumber daya untuk perusahaan yang meminjam.

## <a name="manage-resource-competencies"></a>Mengelola kompetensi sumber daya
Kompetensi sumber daya adalah bagian penting dari manajemen sumber daya. Kompetensi dapat digunakan sebagai dasar untuk menentukan sumber daya yang memiliki keseimbangan yang benar antara keahlian, pendidikan, sertifikasi, dan pengalaman proyek. Anda harus mengkonfigurasi informasi ini untuk setiap sumber daya dan memperbaruinya secara teratur. Dengan cara ini, Anda dapat memaksimalkan kemampuan bila kompetensi sumber daya tertentu cocok selama penugasan sumber daya proyek.

[![Contoh keterampilan, sertifikasi, pendidikan, dan pengalaman proyek](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Prosedur berikut menjelaskan cara mengkonfigurasi beberapa kompetensi untuk sumber daya.

Untuk mengkonfigurasi kompetensi pekerja, Anda dapat menggunakan halaman daftar **pekerja** dalam sumber daya manusia atau halaman daftar **sumber daya** dalam manajemen proyek dan akuntansi. Untuk prosedur berikut, halaman daftar **pekerja** dalam sumber daya manusia digunakan.

### <a name="set-up-competencies-certificates"></a>Konfigurasikan kompetensi: sertifikat

1. Pada halaman daftar **pekerja**, pilih baris untuk pekerja untuk menambahkan informasi sertifikat.
2. Pada panel tindakan, pada tab **Pekerja**, di grup **Kompetensi**, pilih **sertifikat**.
3. Pilih **Baru** , lalu di **Jenis sertifikat**, pilih **PMP**.
4. Di bidang **tanggal mulai**, pilih **1/10/2015**, lalu pilih **Simpan**.

### <a name="set-up-competencies-skills"></a>Konfigurasikan kompetensi: Keterampilan

1. Pada halaman daftar **pekerja**, pastikan pekerja yang Anda gunakan dalam prosedur sebelumnya masih dipilih. Kemudian, pada panel tindakan, pada tab **Pekerja**, di grup **Kompetensi**, pilih **Keterampilan**.
2. Pilih **baru**.
3. Di bidang **keterampilan**, pilih **manajemen proyek**.
4. Di bidang **Level**, pilih **5 pakar**.
5. Di bidang **Tanggal Level**, pilih **14/1/2014**.
6. Di bidang **Tahun pengalaman**, masukkan **10**.
7. Pilih **Simpan**, lalu tutup halaman.

## <a name="create-a-new-project"></a>Buat proyek baru
1. Di **Manajemen proyek**, pilih **Proyek baru** dan masukkan nilai berikut:

    - **Jenis proyek:** waktu dan material
    - **Nama proyek:** Peningkatan XYZ fase 2
    - **Grup proyek:** TM\_WIP
    - **ID Kontrak Proyek:** 00000002

2. Pilih **Buat proyek baru**.

### <a name="assign-a-resource-to-a-project"></a>Menetapkan sumber daya untuk proyek

1. Pada halaman **pekerja**, dalam **Daftar pekerja**, pilih rekaman untuk pekerja yang sebelumnya Anda konfigurasikan kompetensinya, dan buka rekaman pekerja.
2. Pada panel tindakan, pada tab **Proyek**, di grup **Konfigurasi**, pilih **tetapkan proyek**.
3. Pada halaman **penugasan proyek validasi sumber daya**, pada tab **proyek**, di bidang **Tambah proyek ke proyek yang dipilih**, filter proyek **Peningkatan XYZ fase 2**.
4. Di panel **proyek lainnya**, pilih proyek, lalu pilih tombol panah untuk menambahkannya ke panel **proyek yang dipilih**.

Anda juga dapat menetapkan kategori untuk sumber daya sesuai kebutuhan. Jenis kategori adalah **biaya** atau **pendapatan**. Jenis kategori ditentukan oleh organisasi Anda. Jika tidak ada kategori yang ditetapkan untuk sumber daya, Finance akan mencari kategori default pada harga jam untuk biaya dan pendapatan.

### <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurasi sumber daya proyek dan karakteristik peran

Manajer proyek dapat menggunakan fungsi sumber daya proyek untuk membuat peran yang diperlukan untuk proyek. Peran dapat digunakan jika sumber daya terkonfirmasi masih belum diketahui saat sumber daya dicadangkan. Peran dapat sementara dicadangkan sebagai sumber daya yang direncanakan, sehingga Anda dapat melanjutkan tahapan Perencanaan proyek.

[![Contoh peran](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Skenario:** Aswono dipekerjakan untuk menyelesaikan proyek waktu dan material yang memiliki Piagam proyek disetujui. Manajer Proyek Junior masih menyelesaikan cakupan proyek. Manajer sumber daya saat ini mengidentifikasi sumber daya tertentu yang akan dicadangkan untuk mengerjakan proyek baru. Karena sifat penting proyek, sponsor proyek meminta manajer proyek senior sebagai salah satu peran. Manajer sumber daya harus mendapatkan sumber daya baru dan menentukan peran dalam sistem seandainya manajer proyek Junior memerlukan informasi sumber daya selama perencanaan proyek.

Langkah-langkah berikut ini menunjukkan cara manajer sumber daya dapat mengkonfigurasi peran manajer proyek senior dan mengaitkan karakteristik sumber daya dengannya. Selanjutnya, peran dapat digunakan untuk mencari sumber daya yang tersedia yang sesuai dengan kompetensi sumber daya yang diperlukan.

1. Di **Konfigurasi Peran**, pilih **baru** dan masukkan nilai berikut:

    - **ID peran:** manajer proyek senior
    - **Deskripsi:** manajer proyek senior

2. Pilih **Buat**.
3. Pilih peran **manajer proyek senior**, lalu pilih **Konfigurasikan karakteristik**.
4. Di bidang **Jenis karakteristik**, pilih **Keterampilan**.
5. Di bidang **Karakteristik yang tersedia**, masukkan keterampilan yang akan dicari.
6. Di bidang **Jenis karakteristik**, pilih **sertifikat**.
7. Di bidang **Karakteristik yang tersedia**, masukkan jenis sertifikat yang akan dicari.

### <a name="assign-a-project-resource-to-a-project"></a>Menetapkan sumber daya proyek untuk proyek

1. Pada halaman **semua proyek**, pilih proyek **peningkatan XYZ fase 2**.
2. Pada tab **tim proyek dan penjadwalan**, pilih **Tambah**.
3. Di bidang **peran**, pilih **anggota tim**.
4. Pilih **Pesan dari kalender**.
5. Pada halaman **ketersediaan sumber daya**, pilih **lihat pengaturan**.
6. Pada halaman **Atur pengaturan tampilan**, masukkan nilai berikut:

    - **Format untuk tampilan rentang tanggal:** Hari
    - **Tampilkan deskripsi ketersediaan:** ya
    - **Menampilkan kapasitas tersisa:** ya

7. Di daftar sumber daya, pilih sumber daya.
8. Pilih **Definitif** dan **kapasitas penuh**.


### <a name="assign-a-resource-to-a-default-role"></a>Menetapkan sumber daya ke peran keamanan

Untuk membantu manajer proyek atau sumber daya dapat menelusuri dengan detail lebih lanjut tentang sumber daya yang dapat dicadangkan untuk proyek. Anda dapat mengaitkan peran default dengan sumber daya yang ada atau sumber daya yang baru diperoleh. Misalnya, ketika Daniel dipekerjakan, dia memiliki pengalaman dan keterampilan untuk mengisi peran analis bisnis. Manajer sumber daya menetapkan peran ini sebagai peran default Daniel. Oleh karena itu, manajer sumber daya menambahkan Daniel ke kumpulan analis bisnis yang tersedia untuk bekerja pada proyek.

Selama reservasi sumber daya, manajer proyek dapat memfilter sumber daya peran yang tersedia untuk proyek. Mereka dapat menggunakan informasi ini sebagai salah satu kriteria saat mereka melakukan analisis keputusan multi-kriteria selama pemenuhan sumber daya. Mereka juga dapat menambahkan karakteristik sumber daya lain ke filter untuk mencari sumber daya yang memiliki keterampilan khusus, pendidikan, dan pengalaman untuk proyek tertentu.

**Skenario:** proyek yang disetujui telah dimulai, dan peran manajer proyek senior dicadangkan sebagai sumber daya yang direncanakan selama tahap perencanaan proyek. Manajer sumber daya sekarang memperoleh sumber daya untuk memenuhi peran manajer proyek senior.

1. Pada halaman **daftar sumber daya**, pilih **Daniel goldschmidt**.
2. Di **Peran sumber daya**, pilih **baru** dan masukkan nilai berikut:

    - **Efektif:** masukkan tanggal saat ini.
    - **Kedaluwarsa:** Masukkan **tidak pernah**.
    - **Peran:** Masukkan **manajer proyek senior**.

3. Pilih **Simpan**, lalu tutup halaman.
4. Pada tab **kompetensi**, tambahkan Keterampilan **projectmgmt** dan sertifikat **PMP**.

## <a name="set-up-role-based-pricing"></a>Mengkonfigurasi harga berdasarkan peran
Semua harga biaya, penjualan, dan transfer dapat diatur untuk peran.

1. Pada halaman **harga penjualan (jam)**, pilih **baru**, lalu masukkan tanggal berlaku.
2. Di kolom **peran**, pilih peran.
3. Di kolom **harga**, masukkan harga untuk peran sumber daya yang dipilih.

## <a name="form-a-project-team"></a>bentuk tim proyek
Untuk menggunakan peran yang sebelumnya diatur dalam proyek, manajer proyek harus mengaitkan peran dengan proyek. Peran ganda dapat ditetapkan untuk proyek. Untuk mencegah kebingungan, peran ini akan secara otomatis dilabeli saat reservasi. Misalnya, jika manajer proyek memerlukan tiga insinyur perangkat lunak, tiga peran insinyur perangkat lunak yang memiliki label **insinyur perangkat lunak 1**, **insinyur perangkat lunak 2**, dan **insinyur perangkat lunak 3** yang akan dibuat secara otomatis. Jika karakteristik peran sebelumnya diatur untuk peran, peran akan diterapkan sebagai filter selama pencarian untuk sumber daya. Karakteristik tambahan dapat ditambahkan sebagaimana diperlukan untuk lebih menyempurnakan pencarian.

Pengaturan tampilan juga dapat disesuaikan untuk memberikan tampilan yang lebih baik ketersediaan sumber daya. Tersedia pilihan untuk menampilkan ketersediaan per jam, harian, mingguan, bulanan, kuartalan, dan tahunan. Ada juga pilihan untuk menunjukkan kapasitas yang tersedia dan tersisa pada sumber daya. Pilihan ini berguna untuk manajemen waktu, saat Anda memperkirakan waktu yang tersedia untuk aktivitas atau ketersediaan sumber daya.

Manajer proyek dapat memilih peran pada halaman dan kemudian, jika ada sumber daya yang tersedia yang sesuai dengan persyaratan, pilih untuk mencadangkan sumber daya untuk mengisi peran. Perhatikan bahwa sumber daya tidak harus dicadangkan pada saat ini dalam tahap perencanaan. Bila Anda membuat WBS, Anda dapat mengganti peran dengan sumber daya staf untuk proyek. Jika peran diganti dengan sumber daya staf di WBS, pengaturan sumber daya secara otomatis memperbarui daftar tim proyek dan penjadwalan.

[![Daftar tim proyek yang mencakup peran dan sumber daya aktual](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Manajer Proyek memiliki berbagai pilihan untuk memesan sumber daya untuk proyek, seperti **kapasitas yang tersisa**, **kapasitas penuh**, **persentase kapasitas**, dan **Tentukan jam**. Pilihan Pemesanan ini dapat dibatalkan sewaktu-waktu jika tugas sumber daya berubah. Dua jenis Pemesanan yang didukung:

- **Definitif** -sumber daya reservasi disetujui dan dikonfirmasi untuk bekerja pada keterlibatan untuk durasi yang ditentukan.
- **Tentatif** - Reservasi sumber daya diatur secara tentatif untuk bekerja pada keterlibatan untuk durasi yang ditentukan.

Prosedur berikut menjelaskan cara membuat tim proyek.

### <a name="create-a-project-team"></a>Membuat tim proyek

1. Pada halaman daftar **semua proyek**, pilih proyek, lalu pilih **Edit**.
2. Pada tab **tim proyek dan penjadwalan**, di bidang **tanggal akhir jadwal**, masukkan tanggal mulai jadwal ditambah satu bulan. Misalnya, jika tanggal mulai jadwal adalah 24 Juni 2017 (24/06/2017), masukkan **24/07/2017**.
3. Pilih **Tambahkan**.
4. Di panel **Tambah peran ke proyek**, di bidang **peran**, pilih **manajer proyek senior**.
5. Pilih **kompetensi yang diperlukan**.
6. Pada halaman **Pilih karakteristik**, karakteristik yang telah Anda atur untuk peran senior manajer proyek dipilih secara default. Pilih **OK**.
7. Pada halaman **Tambah peran ke proyek**, di bidang **jumlah sumber daya**, masukkan **1**.
8. Di bidang **sumber daya**, pencarian menampilkan semua sumber daya yang memiliki kompetensi yang diperlukan. Pilih **Daniel Goldschmidt**, lalu pilih **buat**.
9. Pada halaman **Proyek**, pilih **Tambah**.
10. Di panel **Tambah peran ke proyek**, di bidang **peran**, pilih **Anggota tim**. Di bidang **Jumlah sumber daya**, masukkan **5**.
11. Pilih **Buat**.
12. Pada halaman **proyek**, pilih **penuhi sumber daya**.

## <a name="resource-capacity-synchronization"></a>Sinkronisasi kapasitas sumber daya
Proses untuk sinkronisasi sumber daya membantu menjamin bahwa informasi untuk kalender dan kalender dasar menetes ke dalam penjadwalan sumber daya proyek. Jika kalender diubah, proses akan melakukan pembaruan yang diperlukan terhadap penjadwalan sumber daya proyek. Proses juga membantu meningkatkan kinerja, karena informasi sumber daya kalender disinkronisasikan terlebih dahulu. Oleh karena itu, pembaruan untuk informasi penjadwalan sumber daya terjadi lebih cepat. Sebaiknya jadwalkan proses sebagai kumpulan, bukan satu per satu. Jika tidak, ada risiko bahwa seseorang akan melupakan tanggal inklusif saat informasi terakhir disinkronisasi. Jika tanggal inklusif tidak digunakan, kesenjangan dapat terjadi selama sinkronisasi tanggal.

![Sinkronisasi kalender](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sinkronisasikan akumulasi kapasitas sumber daya

Proses sinkronisasi dirancang untuk mensinkronisasi semua informasi kalender sumber daya. Informasi ini mencakup informasi kalender dasar tentang perubahan pada tabel kapasitas kalender sumber daya proyek. Jika sumber daya baru ditambahkan dalam proyek, sinkronisasi akan membantu menjamin bahwa informasi kalender yang diperbarui tersedia. Sinkronisasi ini dapat dilakukan kapan pun.

Sebaiknya Anda menggunakan kumpulan. Pilihan tersedia selama sinkronisasi Pemesanan kapasitas.

1. Pilih **manajemen proyek dan akuntansi** &gt; **Periodik** &gt; **Sinkronisasi kapasitas** &gt; **Sinkronisasi akumulasi kapasitas sumber daya**.
2. Atur pilihan dalam tabel berikut.

    | Opsi      | Deskripsi |
    |-------------|-------------|
    | Kode periode | Atau pilih kode interval tanggal buku besar untuk mengatur tanggal mulai dan berakhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya. |
    | Tanggal mulai  | Masukkan tanggal mulai untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya. |
    | Tanggal berakhir    | Masukkan tanggal akhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya. |

[![Proses Sinkronisasi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Mengkonfigurasi peran pada template WBS
Manajer proyek dapat mengkonfigurasi template WBS yang dapat diterapkan saat membuat WBS untuk proyek baru. Manajer proyek dapat menambahkan peran saat membuat template. Gunakan prosedur berikut untuk menetapkan peran ke template WBS.

1. Pilih **Proyek manajemen dan akuntansi** &gt; **konfigurasi** &gt; **Proyek** &gt; **template struktur rincian kerja**.
2. Pilih **rincian** untuk template WBS yang dipilih.
3. Pilih tugas dalam daftar, lalu di bidang **peran**, pilih peran yang akan ditetapkan ke tugas.

### <a name="work-with-a-wbs"></a>Menggunakan WBS

Anda dapat membuat WBS baru, atau Anda dapat menyalin WBS dari template WBS yang ada. Manajer proyek dapat dengan mudah mengelola sumber daya dengan menetapkan peran untuk tugas baru di WBS. Peran dapat digantikan setelah sumber daya diperoleh atau setelah sumber daya yang dikonfirmasi untuk bekerja pada tugas teridentifikasi. Fleksibilitas ini memungkinkan manajer proyek melakukan tugas berikut:

- Mengidentifikasi jumlah sumber daya yang diperlukan untuk paket kerja WBS.
- Estimasi biaya proyek.
- Tentukan anggaran awal.
- Perkirakan durasi aktivitas, berdasarkan peran dan sumber daya.
- Kembangkan beberapa rencana manajemen proyek, berdasarkan informasi proyek yang tersedia.

Pilihan tambahan telah ditambahkan dalam WBS untuk lebih baik menggunakan fungsi sumber daya.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opsi</th>
<th>Deskripsi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Penetapan sumber daya</td>
<td>Lihat sumber daya yang ditetapkan, tanggal, jumlah jam, dan jenis Pemesanan untuk tugas di WBS.</td>
</tr>
<tr class="even">
<td>Buat otomatis tim</td>
<td>Secara otomatis menambahkan sumber daya terencana dengan menggunakan peran yang terkait dengan tugas. Finance secara otomatis menyarankan sumber daya terencana dengan menggunakan analisis keputusan multi-kriteria yang didasarkan pada peran. Setelah peran dan upaya (jam) telah ditetapkan untuk tugas di WBS, dan setelah struktur telah dirilis, pilih <strong>otomatis membuat tim</strong>. Jumlah sumber daya terencana yang diperlukan ditambahkan ke WBS dan tab <strong>penjadwalan proyek dan tim</strong>.</td>
</tr>
<tr class="odd">
<td>Sumber daya (Daftar tarik-turun)</td>
<td>Pada halaman <strong>peluncuran penugasan sumber daya</strong>, Anda dapat memilih sumber daya untuk definitif atau tentatif, berdasarkan durasi yang ditentukan. Anda dapat menyesuaikan pengaturan tampilan untuk melihat dan mengatur durasi aktivitas sumber daya. Anda dapat memilih dan menetapkan sumber daya pada tingkat paket kerja dengan menggunakan pilihan berikut:
<ul>
<li><strong>Terima</strong> – konfirmasikan perubahan pada sumber daya yang ditetapkan ke tugas.</li>
<li><strong>Batalkan</strong> – Batalkan perubahan pada sumber daya yang ditetapkan ke tugas.</li>
<li><strong>Tetapkan secara otomatis</strong> -sumber daya tersedia yang memiliki peran pencocokan dipilih secara otomatis dan ditetapkan ke tugas yang dipilih.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Pada halaman **semua proyek**, pilih proyek **peningkatan XYZ fase 2**.
2. Pilih **skema** &gt; **aktivitas** &gt; **struktur rincian kerja**.
3. Pilih **baru** untuk menambahkan aktivitas satu tingkat berikut ke WBS:

    - Memulai
    - Perencanaan
    - Menjalankan
    - Pemantauan dan Kontrol
    - Tutup

4. Atur tanggal dan upaya (jam), seperti ditunjukkan dalam ilustrasi berikut.

    [![Mengatur tanggal dan upaya](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pilih baris tugas **memulai**, lalu di bidang **peran**, pilih **manajer proyek senior**.
6. Pilih **Terbitkan**.
7. Pada baris yang sama, di bidang **sumber daya**, pilih **Daniel goldschmidt**, lalu pilih **terima**.
8. Pilih baris tugas **perencanaan**, lalu di bidang **peran**, pilih **analis bisnis**.
9. Pilih **publikasikan**, lalu pilih **Buat otomatis tim**.
10. Dalam kotak pesan yang ditampilkan, pilih **Ya**.
11. Di bidang **sumber daya**, Verifikasikan bahwa nilai adalah **analis bisnis 1**.
12. Untuk sumber daya **Analisis bisnis 1**, buka pencarian, dan pilih **peluncuran tugas sumber daya**. Kemudian pilih pekerja untuk tugas.
13. Pilih **Penugasan tentatif** &gt; **kapasitas penuh**.

    > [!NOTE] 
    > Anda tidak menerima peringatan bahwa sumber daya yang ditentukan sekarang 2, karena jumlah sumber daya tetap 1.

14. Pada halaman **struktur rincian kerja**, validasi tugas sumber daya pada WBS, dan kemudian pilih **Simpan**.

## <a name="resource-fulfillment-for-planned-resources"></a>Pemenuhan sumber daya untuk sumber daya terencana
Manajer proyek dapat merencanakan peran sumber daya yang diperlukan untuk proyek. Manajer sumber daya akan melihat sumber daya terencana ini sebagai permintaan pada **halaman pemenuhan sumber daya** dan dapat menetapkan sumber daya aktual.

1. Pada halaman **semua proyek**, pilih proyek **peningkatan XYZ fase 2**.
2. Pilih **Proyek**, lalu pilih **Edit**.
3. Pada tab **tim proyek dan penjadwalan**, pilih **Tambah**.
4. Di kotak dialog **Tambah peran**, pilih peran **pengembang perangkat lunak**.
5. Pilih **Buat**, lalu tutup halaman proyek.
6. Pada halaman **pemenuhan sumber daya**, pilih **pengembang perangkat lunak 1** untuk proyek **proyek peningkatan XYZ tahap 2**.
7. Pilih pekerja, kemudian pilih **tetapkan**.
8. Verifikasikan bahwa baris untuk **Pengembang perangkat lunak 1** telah dihapus untuk proyek **proyek peningkatan XYZ tahap 2**.
9. Pada tab **tim proyek dan penjadwalan**, untuk proyek **peningkatan XYZ fase 2**, Verifikasikan bahwa pekerja yang Anda pilih pada langkah sebelumnya telah ditambahkan sebagai **pengembang perangkat lunak**.

## <a name="requests-for-project-resources"></a>Permintaan sumber daya proyek
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

## <a name="monitor-project-teams"></a>Memantau tim proyek
1. Pada halaman **semua proyek**, pilih tautan **ID proyek** untuk proyek **peningkatan XYZ fase 2**.
2. Pada FastTab **tim proyek dan penjadwalan**, Verifikasikan bahwa sumber daya proyek yang tercantum sudah benar.
