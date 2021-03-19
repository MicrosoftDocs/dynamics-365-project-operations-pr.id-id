---
title: Kelola sumber daya
description: Topik ini menyediakan informasi tentang cara Anda mengelola sumber daya.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d47be6c11ced70b94b7497dfbc0c67d1a3f631b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275002"
---
# <a name="manage-resources"></a>Kelola sumber daya

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation mencakup dasbor manajer sumber daya yang memberikan ikhtisar visual mengenai permintaan dan pemanfaatan sumber daya di seluruh organisasi. Anda dapat menggunakan diagram di dasbor ini untuk memvisualisasikan informasi berikut:

- **Permintaan sumber daya**- diagram **permintaan sumber daya aktif** menampilkan sumber daya yang telah diajukan. Sumber daya dikumpulkan baik oleh peran maupun proyek.
- **Permintaan sumber daya yang belum diajukan** – diagram **permintaan sumber daya yang belum ditetapkan** menampilkan semua persyaratan sumber daya yang belum diajukan. Hal ini membantu manajer sumber daya melihat permintaan yang tidak tegas dan dapat diajukan melalui permintaan sumber daya.
- **Pemanfaatan yang dapat ditagih selama seminggu terakhir** – diagram **pemanfaatan berdasarkan peran** menunjukkan persentase pemanfaatan aktual yang dilakukan organisasi berdasarkan target yang dapat ditagih berdasarkan peran.

    > [!NOTE]
    > Untuk membuat diagram **pemanfaatan berdasarkan peran** tersedia, buat pekerjaan yang menjalankan alur kerja UpdateRoleUtilization. Pekerjaan rutin ini berjalan setiap tujuh hari untuk menghitung pemanfaatan yang dapat ditagih selama tujuh hari sebelumnya. Hasil akan digabungkan berdasarkan peran.

## <a name="manage-project-team-members"></a>Kelola Anggota Tim Proyek

Manajer proyek dapat menggunakan dasbor manajer sumber daya untuk mengelola sumber daya pada proyek. Misalnya, mereka dapat menambahkan anggota tim secara langsung ke proyek dan memesan anggota tim untuk memenuhi persyaratan sumber daya yang ditangkap oleh sumber daya generik.

### <a name="add-a-team-member-directly-to-a-project"></a>Tambahkan anggota tim langsung ke proyek

Untuk menambahkan anggota tim secara langsung ke proyek, pada halaman **proyek**, pada tab **tim**, pilih **baru**. Kotak dialog **buat cepat: anggota tim proyek** akan ditampilkan. Di kotak dialog ini, Anda dapat melakukan tugas berikut:

- **Memesan sumber daya bernama**-di bidang **sumber daya dapat dipesan**, pilih nama sumber daya. Kemudian pilih peran, atur periode, dan pilih metode alokasi. Sumber daya bernama yang Anda pilih ditambahkan ke proyek menggunakan metode alokasi yang dipilih dan kalender sumber daya.
- **Menambahkan sumber daya generik** – biarkan bidang **sumber daya dapat dipesan** kosong, lalu pilih peran, atur periode, dan pilih metode alokasi yang diinginkan. Sumber daya generik ditambahkan ke tim sebagai placeholder untuk menyimpan pola permintaan yang digunakan untuk memesan sumber daya pada tim. Persyaratan dibuat sesuai dengan kalender proyek.
- **Tambahkan sumber daya bernama ke tim tanpa menggunakan kapasitas sumber daya**-di bidang **sumber daya dapat dipesan**, pilih sumber daya. Kemudian pilih periode, dan pilih metode alokasi **Tidak ada**. Sumber daya ditambahkan ke tim, namun kapasitas sumber daya tidak dihabiskan melalui pemesanan.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Pesan anggota tim untuk memenuhi persyaratan sumber daya untuk sumber daya generik

Dalam PSA, Anda dapat memesan sumber daya generik pada tim proyek, dan dapat menentukan peran, kapasitas yang diperlukan, dan bagaimana kapasitas tersebut didistribusikan. Pada persyaratan sumber daya, Anda dapat menentukan atribut yang terkait dengan sumber daya generik . Atribut ini mencakup keterampilan yang diperlukan, unit organisasi yang disukai, dan sumber daya pilihan.

Ikuti langkah berikut untuk menentukan keterampilan yang diperlukan pada sumber daya generik untuk pengembang.

1. Pada halaman **proyek**, pada tab **tim**, pilih **baru** untuk memesan sumber daya generik.

    ![Sumber daya generik yang dipesan pada tim](media/Resource-Management-image9.png)

2. Di tampilan **semua anggota tim**, di kolom **persyaratan sumber daya**, pilih tautan untuk menambahkan keterampilan yang diperlukan untuk sumber daya generik.

    ![Tautan persyaratan](media/Resource-Management-image10.png)

3. Pada halaman **persyaratan sumber daya** yang muncul, di kisi **keahlian**, pilih elipsis (**...**) kemudian pilih **Tambah karakteristik kebutuhan baru** untuk menambahkan keterampilan yang diperlukan untuk pengembang Anda.

    ![Perintah Tambahkan Karakteristik Persyaratan Baru](media/Resource-Management-image11.png)

4. Di kotak dialog **buat cepat: karakteristik persyaratan** yang muncul, di bidang **karakteristik**, pilih keahlian yang diperlukan. Selanjutnya, di bidang **nilai peringkat**, pilih tingkat kemahiran untuk keahlian tersebut. Terakhir, di bidang **persyaratan sumber daya**, atur persyaratan sumber daya sumber dari unit organisasi atau bahkan sumber daya bernama. Setelah selesai, pilih **Simpan**.

    ![Kotak dialog buat cepat: karakteristik persyaratan](media/Resource-Management-image12.png)

5. Pada halaman **persyaratan sumber daya**, pilih **Pesan** untuk memenuhi persyaratan sumber daya.

    ![Tombol pesan di halaman persyaratan sumber daya](media/Resource-Management-image13.png)

    Anda juga dapat memilih sumber daya generik di kisi **semua anggota tim**, lalu pilih **Pesan**.

    ![Tombol pesan di atas kisi semua anggota tim](media/Resource-Management-image14.png)

    > [!NOTE]
    > Dalam contoh ini, ada 40 jam yang diperlukan namun tidak ada jam Pemesanan aktual, karena sumber daya generik tidak memiliki Pemesanan. Selain itu, tidak ada jam yang ditetapkan, karena sumber daya generik ditambahkan langsung ke tim. Tidak ditambahkan menggunakan penetapan tugas.

    Pada halaman **asisten penjadwalan**, Anda dapat memfilter sumber daya yang tersedia berdasarkan persyaratan yang ditentukan pada persyaratan sumber daya. Sumber daya diurutkan berdasarkan parameter pengurutan yang ditentukan di papan jadwal.

    ![Halaman Asisten Penjadwalan](media/Resource-Management-image15.png)

    Berikut adalah beberapa filter yang sering digunakan:

    - **Karakteristik bersama dengan peringkat** -filter berdasarkan keterampilan, sertifikasi, dan kualitas sumber daya lainnya, selain peringkat kemahiran.
    - **Peran** – filter berdasarkan peran default yang ditetapkan ke sumber daya yang dapat dipesan.
    - **Unit organisasi** – memfilter sumber daya yang dapat dipesan berdasarkan unit organisasi yang ditetapkan untuknya.

6. Jika Anda tidak puas dengan hasil pencarian persyaratan awal, Anda dapat mengubah kriteria filter. Perluas panel **tampilan filter** di sebelah kiri, lalu pilih **pencarian** untuk menemukan sumber daya tambahan.

    ![Panel Tampilan Filter](media/Resource-Management-image16.png)

7. Untuk mengubah cara pengurutan, **Urutkan**.

    ![Perintah Urutkan](media/Resource-Management-image17.png)

8. Pilih sumber daya sesuai permintaan yang ditentukan pada persyaratan, seperti ditunjukkan di bagian atas kisi. Anda dapat menghapus pilihan sel di kisi dan membiarkan kapasitas sumber daya terbuka. Hanya satu sumber daya setiap kalinya yang dapat dipilih sebagai dipesan.

9. Pilih **Pesan** untuk memesan sumber daya yang dipilih dan biarkan papan jadwal terbuka, sehingga Anda dapat memilih sumber daya tambahan. Atau, pilih **Pesan & keluar** untuk memesan sumber daya yang dipilih dan tutup papan jadwal.

    ![Sumber Daya untuk dipesan](media/Resource-Management-image19.png)

    Anda akan menerima pemberitahuan tentang jam dipesan. Indikator permintaan menunjukkan seberapa besar persyaratan Pemesanan terpenuhi dan berapa banyak yang tersisa. Anda juga dapat mengetahui jumlah kapasitas sumber daya yang dihabiskan. Pilih **Perluas** untuk melihat rincian lebih lanjut tentang Pemesanan sumber daya.

9. Kembali ke tampilan **semua anggota tim**. Di kisi, perhatikan bahwa sumber daya umum telah digantikan oleh sumber daya bernama, dan 40 jam terdaftar sebagai dipesan untuk sumber daya tersebut.

    ![Diperbarui kisi semua anggota tim](media/Resource-Management-image20.png)

    > [!NOTE]
    > Tidak ada jam yang ditetapkan ditampilkan, karena mereka dipesan langsung pada tim. Mereka tidak dipesan menggunakan penetapan tugas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tetapkan sumber daya generik ke tugas dan buat persyaratan sumber daya

Dalam PSA, Anda dapat membuat tugas, lalu menetapkan sumber daya generik. Dengan cara ini, permintaan sumber daya dapat diwakili oleh placeholder saat Anda memperkirakan jadwal dan angka keuangan. Selanjutnya Anda dapat membuat persyaratan sumber daya untuk sumber daya generik dan memenuhinya.

1. Pada halaman **proyek**, pada tab **jadwal**, pilih **Tambah** untuk membuat tugas.

    ![Tugas Baru dibuat](media/Resource-Management-image21.png)

2. Di bidang **sumber daya**, pilih simbol **pemilih sumber daya**. Pemilih sumber daya muncul dan menampilkan anggota tim yang ada untuk proyek.

    ![Pemilih sumber daya](media/Resource-Management-image22.png)

3. Masukkan nama sumber daya generik baru, lalu pilih **buat**.

    ![Nama sumber daya generik baru yang dimasukkan](media/Resource-Management-image23.png)

4. Di kotak dialog **buat cepat: anggota tim proyek** yang muncul, di bidang **Peran**, pilih peran untuk sumber daya generik. Di bidang **unit sumber daya**, pilih unit organisasi untuk sumber daya generik. Kemudian pilih **Simpan**.

    ![Kotak dialog buat cepat: anggota tim proyek](media/Resource-Management-image24.png)

    Anggota tim generik kini ditetapkan ke tugas.

    ![Anggota tim generik ditetapkan ke tugas](media/Resource-Management-image25.png)

    Pada tab **tim**, Anda akan melihat anggota tim generik baru. Perhatikan bahwa hanya jam yang ditetapkan. Jam tersebut adalah jumlah semua tugas yang ditetapkan ke anggota tim generik. Anggota tim generik belum memerlukan persyaratan jam atau sumber daya.

    ![Anggota tim persyaratan pada tab tim](media/Resource-Management-image26.png)

5. Anda sekarang dapat menetapkan anggota tim umum untuk tugas lain menggunakan pemilih sumber daya.

    ![Anggota tim persyaratan dalam pemilih sumber daya](media/Resource-Management-image27.png)

    Setelah selesai menetapkan sumber daya generik untuk tugas, Anda dapat membuat persyaratan sumber daya untuk sumber daya generik.

5. Pada tab **tim**, pilih sumber daya generik, lalu pilih **buat persyaratan**.

    ![Perintah Buat Persyaratan](media/Resource-Management-image28.png)

    Bila persyaratan dibuat, anggota tim generik akan memiliki jam wajib dan tautan untuk persyaratan sumber daya.

    ![Tautan Persyaratan Sumber Daya](media/Resource-Management-image29.png)

    Setelah Anda memesan sumber daya bernama, sumber daya generik dihapus dari tim dan digantikan dengan sumber daya bernama.

    ![Sumber daya generik digantikan oleh sumber daya bernama](media/Resource-Management-image30.png)

    Pada tab **jadwal**, tugas sumber daya generik akan dihapus dan digantikan oleh sumber daya bernama.

    ![Pada tab jadwal, tugas sumber daya generik digantikan oleh sumber daya bernama](media/Resource-Management-image31.png)

    > [!NOTE]
    > Perilaku ini hanya terjadi bila sumber daya bernama sepenuhnya dipesan untuk persyaratan sumber daya generik. Bila sumber daya bernama sebagian menggantikan persyaratan sumber daya generik atau beberapa sumber daya bernama menggantikan persyaratan sumber daya generik, sumber daya generik tetap ditetapkan ke tugas.

    Dalam ilustrasi berikut, tugas 80 jam telah direncanakan selama lima hari (16 jam per hari selama lima hari) dan ditetapkan ke sumber daya generik yang dinamai **fungsional**.

    ![80-jam, tugas lima hari yang ditetapkan ke sumber daya generik fungsional](media/Resource-Management-image32.png)

    Bila Anda membuat persyaratan, maka untuk 80 jam selama lima hari.

    ![Persyaratan dihasilkan untuk 80 jam selama lima hari](media/Resource-Management-image33.png)

    Karena sumber daya yang tersedia hanya berfungsi selama delapan jam per hari, dua sumber daya diperlukan untuk memenuhi persyaratan.

    ![Sumber daya kedua](media/Resource-Management-image35.png)

    Pada tab **tim**, Anda sekarang dapat melihat bahwa sumber daya generik tidak memiliki jam yang diperlukan, namun jam yang ditetapkan tetap ditampilkan bersama dengan dua sumber daya bernama yang membentuk pemenuhan.

    ![Dua sumber daya bernama di tab tim](media/Resource-Management-image36.png)

    Pada tab **jadwal**, sumber daya generik tetap ditetapkan ke tugas.

    ![Sumber daya generik pada tab jadwal](media/Resource-Management-image37.png)

PSA tidak menetapkan sumber daya ke tugas, karena perilaku tersebut akan menghasilkan jadwal yang kurang dapat diprediksi. Dalam contoh sederhana ini, mudah untuk membagi jam secara merata antara dua sumber daya. Namun, dalam skenario yang lebih kompleks yang melibatkan beberapa tugas dan beberapa sumber daya, PSA harus membuat asumsi tentang cara mengalokasikan Pemesanan yang diterima untuk beberapa sumber daya di beberapa tugas.

Oleh karena itu, dalam skenario ini, manajer proyek bertanggung jawab untuk menguraikan beberapa Pemesanan dan menetapkannya sesuai kebutuhan. Untuk mengalokasikan Pemesanan, manajer proyek menetapkan tugas dari sumber daya generik ke sumber daya bernama dan kemudian menggunakan tampilan **rekonsiliasi** untuk memastikan bahwa alokasi berfungsi dengan pemesanan.

### <a name="edit-a-resource-requirement"></a>Edit Persyaratan Sumber Daya

Setelah persyaratan sumber daya dibuat, manajer proyek atau manajer sumber daya mungkin ingin mengedit rincian untuk menyempurnakan kriteria pencarian bila papan jadwal digunakan. Untuk mengedit persyaratan sumber daya, ikuti langkah-langkah berikut.

1. Pada halaman **proyek**, pada tab **tim**, pilih tautan ke persyaratan apa pun di sumber daya generik.
2. Di halaman **persyaratan sumber daya** yang muncul, Anda dapat memperbarui beberapa atribut. Berikut adalah beberapa contoh:

    - Nama
    - Tanggal Mulai
    - Tanggal Selesai
    - Durasi
    - Jenis Sumber Daya

Pada halaman **persyaratan sumber daya**, manajer proyek atau manajer sumber daya juga dapat menentukan informasi berikut:

- Keterampilan
- Peran
- Preferensi Sumber Daya
- Unit Organisasi Pilihan

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Perbarui Pemesanan sumber daya setelah mereka dipesan pada proyek

Setelah menambahkan sumber daya generik atau bernama ke tim proyek, Anda dapat mengubah Pemesanan sumber daya.

1. Pada halaman **proyek**, pada tab **tim**, pilih anggota tim, lalu pilih **Kelola Pemesanan**.

    ![Papan jadwal dibuka untuk anggota tim yang dipilih](media/Resource-Management-image40.png)

    Papan jadwal akan ditampilkan dan menampilkan Pemesanan anggota tim proyek. Perluas rekaman anggota tim untuk melihat jam yang telah dipesan terhadap proyek ini dan proyek lainnya yang memakan kapasitas anggota tim.

2. Pilih dan tarik Pemesanan untuk memperluas atau mempersingkat. Kotak dialog **buat Pemesanan sumber daya** muncul yang memungkinkan Anda menyesuaikan Pemesanan.

    ![Kotak dialog Buat Pemesanan Sumber Daya](media/Resource-Management-image41.png)

3. Klik kanan Pemesanan. Anda kemudian dapat menggunakan menu pintasan untuk menyelesaikan tindakan berikut:

    - Ubah Status Pemesanan.
    - Edit Pemesanan.
    - Gantikan sumber daya pada tim proyek.

### <a name="change-the-booking-status"></a>Ubah Status Pemesanan

Anda dapat mengubah status pemesanan default atau kustom.

![Perintah Ubah Status](media/Resource-Management-image42.png)

Status berikut termasuk dalam PSA:

- **Dibatalkan** -status ini membatalkan pemesanan sumber daya dan membebaskan kapasitas sumber daya.
- **Pemesanan definitif** -status ini mengkonsumsi kapasitas sumber daya. Pemesanan biasanya memiliki status ini saat Anda membuka **Kelola Pemesanan** dari kisi **semua anggota tim** di halaman **proyek**.
- **Pemesanan tentatif** – status ini menambahkan sumber daya ke tim namun tidak mengkonsumsi kapasitas sumber daya. Ini menunjukkan bahwa sumber daya telah dicadangkan untuk pekerjaan potensial namun masih memiliki kapasitas jika diperlukan pada pekerjaan lain. Di tampilan ketersediaan sumber daya secara keseluruhan, Pemesanan tentatif memiliki status yang berbeda dengan Pemesanan definitif.
- **Diusulkan** -status ini mewakili usulan manajer sumber daya atau manajer proyek untuk sumber daya. Proposal tidak mengkonsumsi kapasitas sumber daya, dan sumber daya tidak ditambahkan ke tim proyek. Untuk pemesanan definitif sumber daya pada tim, manajer proyek harus menerima proposal.

### <a name="submit-resource-requests"></a>Kirim permintaan sumber daya

Permintaan sumber daya digunakan untuk melakukan permintaan (persyaratan sumber daya) yang harus dipenuhi oleh Manajer sumber daya. Untuk sumber daya generik yang sudah ada di tim, Anda dapat mengajukan permintaan sumber daya secara langsung. Permintaan sumber daya dapat dipenuhi dengan dua cara:

- Manajer sumber daya langsung memenuhi permintaan. Dalam kasus ini, sumber daya umum digantikan dengan pemesanan definitif yang memiliki sumber daya bernama.
- Manajer sumber daya mengusulkan sumber daya untuk manajer proyek, dan manajer proyek menyetujui atau menolak sumber daya yang diusulkan.

#### <a name="direct-fulfillment-of-resource-requests"></a>Pemenuhan langsung permintaan sumber daya

Bila persyaratan sumber daya dihasilkan, manajer proyek dapat mengajukan permintaan sumber daya umum dengan memilih sumber daya, lalu memilih **Ajukan permintaan**.

![Tombol Ajukan permintaan](media/Resource-Management-image45.png)

Komentar tentang sumber daya dapat diberikan kepada manajer sumber daya yang memenuhi permintaan. Setelah permintaan diajukan, bidang **status** untuk anggota tim akan diubah ke **Diajukan**.

![Memasukkan Komentar opsional](media/Resource-Management-image46.png)

Ketika manajer sumber daya memenuhi permintaan, anggota tim generik digantikan dengan sumber daya bernama di kisi **semua anggota tim**.

![Anggota tim generik digantikan oleh sumber daya bernama di kisi semua anggota tim](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Menggunakan proposal sumber daya untuk permintaan sumber daya

Alih-alih langsung memesan sumber daya pada permintaan sumber daya, manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek. Manajer sumber daya dapat menggunakan pilihan ini bila pencocokan yang tepat dengan persyaratan tidak tersedia. Bila manajer sumber daya mengusulkan suatu sumber daya, manajer proyek melihat bahwa bidang **status** untuk anggota tim generik diubah ke **perlu ditinjau**.

![Status anggota tim generik diubah ke perlu ditinjau](media/Resource-Management-image48.png)

Untuk melihat sumber daya yang diusulkan bersama dengan visualisasi dari efek dari Pemesanan proposal, klik dua kali anggota tim yang memiliki status **Perlu ditinjau**. Kemudian pilih tab **sumber daya yang diusulkan**.

![Tab Sumber Daya yang Diusulkan](media/Resource-Management-image49.png)

Pilih **terima semua proposal** untuk menerima semua sumber daya yang diusulkan atau **Tolak semua proposal** untuk menolaknya. Jika Anda menerima sumber daya yang diusulkan, mereka dipesan secara definitif pada proyek sebagai anggota tim dan mengganti sumber daya generik.

> [!NOTE]
> Anda harus menerima atau menolak semua sumber daya yang diusulkan. Anda tidak dapat menerima atau menolaknya secara parsial.

### <a name="substitute-a-resource-on-the-project-team"></a>Gantikan sumber daya pada tim proyek

Terkadang, manajer proyek harus mengganti anggota tim yang dipesan pada suatu proyek.

1. Pada halaman **proyek**, pada tab **tim**, pilih sumber daya yang memerlukan pengganti, lalu pilih **Kelola Pemesanan**.
2. Perluas sumber daya untuk melihat proyek yang ditetapkan untuknya.

    ![Sumber daya diperluas untuk menampilkan proyek yang ditugaskan](media/Resource-Management-image50.png)

3. Klik kanan proyek, lalu pilih **ganti sumber daya**.
4. Jika Anda mengetahui sumber daya yang ingin Anda ganti untuk sumber daya saat ini, pilih atau ketik nama, lalu pilih **tetapkan ulang**.

    ![Menentukan sumber daya pengganti](media/Resource-Management-image51.png)

    Atau, ikuti langkah berikut untuk mencari sumber daya:

    1. Pilih **Cari Pengganti**.

        ![Mencari sumber daya pengganti](media/Resource-Management-image52.png)

        Asisten jadwal akan menampilkan daftar pengganti yang tersedia. Di asisten jadwal, Anda dapat memfilter lebih lanjut sumber daya yang tersedia untuk menemukan pengganti yang sesuai.

        ![Daftar pengganti yang tersedia](media/Resource-Management-image53.png)

    2. Untuk mengganti sumber daya, pilih sumber daya yang diinginkan, lalu pilih **Ganti**.

        ![Sumber Daya Pengganti dipilih](media/Resource-Management-image54.png)

    Pemesanan dan penugasan digantikan dengan sumber daya baru.

    ![Pemesanan dan penugasan digantikan dengan sumber daya baru](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Rekonsiliasi pemesanan dan penugasan Anggota tim

Untuk anggota tim, Pemesanan dan tugas secara longgar digabungkan. Dengan kata lain, sumber daya dapat memiliki tugas namun tidak ada pemesanan, atau mereka dapat memiliki Pemesanan namun tidak ada tugas. Idealnya, Pemesanan dan penetapan harus selaras, sehingga sumber daya memiliki kapasitas untuk melakukan tugas tugas. Namun, Pemesanan mungkin didasarkan pada ketersediaan, dan waktu tugas dapat berubah saat proyek berlanjut. Oleh karena itu, pasangan longgar Pemesanan dan penugasan memberikan fleksibilitas.

PSA memiliki tab **rekonsiliasi** yang memungkinkan manajer proyek merekonsiliasi Pemesanan anggota tim dan tugas mereka untuk tim proyek.

![Tab Rekonsiliasi](media/Resource-Management-image56.png)

Tab **rekonsiliasi** menampilkan Pemesanan dan tugas hingga tingkat penetapan tugas individual untuk setiap anggota tim. Ini menunjukkan jam di sel yang menunjukkan periode waktu dari bulan ke hari.

Tab juga menampilkan Total keseluruhan bersih untuk proyek, bersama dengan kolom total.

Untuk setiap sumber daya, tab akan menghitung perbedaan antara Pemesanan anggota tim dan Rollup tugas anggota tim. Idealnya, perbedaan ini harus 0 (nol). Dengan kata lain, tidak ada perbedaan antara Pemesanan dan tugas. Perbedaan berwarna dan berarsir untuk menarik perhatian ke dua kondisi:

- **Kekurangan Pemesanan** – kekurangan Pemesanan terjadi bila sumber daya memiliki lebih banyak tugas daripada Pemesanan. Karena kapasitas ini belum dicadangkan, manajer proyek mungkin ingin memperbaiki kondisi ini dengan memperluas Pemesanan sumber daya untuk mengatasi defisit.
- **Pemesanan berlebih** – kelebihan Pemesanan terjadi saat sumber daya telah dipesan ke proyek namun belum ditetapkan ke tugas. Kondisi ini mungkin dapat diterima dalam kasus saat sumber daya dipesan ke proyek sebelum penetapan tugas terjadi. Namun, dalam kasus lain, sumber daya tidak direncanakan untuk ditetapkan ke tugas. Dalam kasus ini, manajer proyek harus mempertimbangkan membatalkan pemesanan sumber daya, sehingga kapasitas dapat digunakan untuk proyek lain.

Dalam kasus tertentu, bila Anda melihat waktu pada tingkat yang lebih tinggi daripada tingkat hari (misalnya, tingkat bulan), Anda mungkin melihat perbedaan bersih nol untuk sumber daya (dengan kata lain, Pemesanan = penetapan). Namun, jika Anda melihat waktu di tingkat minggu, Anda mungkin melihat bahwa ada tugas yang dilakukan nol jam dan Pemesanan 40 jam di minggu pertama, namun penetapan 40 jam dan Pemesanan dalam nol jam di minggu kedua. Secara keseluruhan, Pemesanan dan penugasan akan didamaikan, namun berbeda dari satu minggu ke hari berikutnya.

Bila Anda melihat waktu di tingkat yang lebih tinggi, sel dalam tab **rekonsiliasi** memiliki indikator untuk menginformasikan bahwa ada perbedaan pada tingkat yang lebih rendah. Dengan mengklik dua kali di sel, Anda dapat memperbesar untuk melihat perbedaannya. Anda kemudian dapat klik kanan untuk memperkecil. Dengan memilih sumber daya, lalu menggunakan kontrol **perbedaan berikutnya** pada Toolbar kisi, Anda dapat membuka perbedaan berikutnya antara Pemesanan dan tugas untuk sumber daya tersebut. Selanjutnya Anda dapat menggunakan kontrol **perbedaan sebelumnya** untuk kembali. Anda juga dapat menonaktifkan indikator perbedaan dan perilaku navigasi dalam **pengaturan**.

![Indikator perbedaan](media/Resource-Management-image57.png)

Jika Anda memiliki penetapan tugas untuk sumber daya, namun tidak ada pemesanan, pada halaman **proyek**, pada tab **rekonsiliasi**, pilih kekurangan Pemesanan, lalu pilih **Perluas Pemesanan**. Kotak dialog **Perluas Pemesanan** muncul dan menunjukkan Pemesanan yang diperlukan untuk mengatasi kekurangan sumber daya. Juga menampilkan Pemesanan sumber daya yang ada di seluruh proyek atau entitas yang dapat dijadwalkan lainnya. Jika Anda memilih **OK** untuk membuat pemesanan untuk sumber daya, terlepas dari ketersediaan sumber daya tersebut, Anda dapat menyebabkan pemesanan berlebihan.

![Kotak dialog Perluas Pemesanan](media/Resource-Management-image58.png)

Manajer proyek atau manajer sumber daya kemudian dapat menggunakan papan jadwal untuk mengelola setiap situasi dengan sumber daya yang dipesan berlebihan di luar kapasitasnya.


[!INCLUDE[footer-include](../includes/footer-banner.md)]