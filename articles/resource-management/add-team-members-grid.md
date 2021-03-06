---
title: Menambahkan anggota tim dari kisi anggota Tim
description: Topik ini menyediakan informasi tentang cara Anda mengelola sumber daya anggota tim.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 0f975d295b4c0ccef9827767beabd32ffd761faa
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897725"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Menambahkan anggota tim dari kisi anggota Tim

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mencakup dasbor manajer sumber daya yang memberikan ikhtisar visual mengenai permintaan dan pemanfaatan sumber daya di seluruh organisasi. Anda dapat menggunakan diagram di dasbor ini untuk memvisualisasikan informasi berikut:

- **Permintaan sumber daya**: diagram **permintaan sumber daya aktif** menampilkan sumber daya yang telah diajukan. Sumber daya dikumpulkan baik oleh peran maupun proyek.
- **Permintaan sumber daya yang belum diajukan**: diagram **permintaan sumber daya yang belum ditetapkan** menampilkan semua persyaratan sumber daya yang belum diajukan. Diagram ini membantu manajer sumber daya melihat permintaan yang tidak tegas dan dapat diajukan melalui permintaan sumber daya.
- **Pemanfaatan yang dapat ditagih selama seminggu terakhir**: diagram **pemanfaatan berdasarkan peran** menunjukkan persentase pemanfaatan aktual yang dilakukan organisasi berdasarkan target yang dapat ditagih berdasarkan peran.

    > [!NOTE]
    > Untuk membuat diagram **pemanfaatan berdasarkan peran** tersedia, buat pekerjaan yang menjalankan alur kerja **UpdateRoleUtilization**. Pekerjaan rutin ini berjalan setiap tujuh hari untuk menghitung pemanfaatan yang dapat ditagih selama tujuh hari sebelumnya. Hasil akan digabungkan berdasarkan peran.

## <a name="manage-project-team-members"></a>Kelola Anggota Tim Proyek

Manajer proyek dapat menggunakan dasbor manajer sumber daya untuk mengelola sumber daya pada proyek. Misalnya, mereka dapat menambahkan anggota tim secara langsung ke proyek dan memesan anggota tim untuk memenuhi persyaratan sumber daya yang ditangkap oleh sumber daya generik.

### <a name="add-a-team-member-directly-to-a-project"></a>Tambahkan anggota tim langsung ke proyek

Untuk menambahkan anggota tim secara langsung ke proyek, pada formulir **proyek**, pada tab **tim**, pilih **baru**. Kotak dialog **buat cepat: anggota tim proyek** akan ditampilkan. Di kotak dialog ini, Anda dapat melakukan tugas berikut:

- **Memesan sumber daya bernama**: di bidang **sumber daya dapat dipesan**, pilih nama sumber daya. Kemudian pilih peran, atur periode, dan pilih metode alokasi. Sumber daya bernama yang Anda pilih ditambahkan ke proyek menggunakan metode alokasi yang dipilih dan kalender sumber daya.
- **Menambahkan sumber daya generik**: biarkan bidang **sumber daya dapat dipesan** kosong, lalu pilih peran, atur periode, dan pilih metode alokasi yang diinginkan. Sumber daya umum ditambahkan ke tim sebagai placeholder. Placeholder memiliki pola permintaan yang digunakan untuk memesan sumber daya bernama pada tim. Persyaratan dibuat sesuai dengan kalender proyek.
- **Tambahkan sumber daya bernama ke tim tanpa menggunakan kapasitas sumber daya**: di bidang **sumber daya dapat dipesan**, pilih sumber daya. Pilih periode, kemudian pilih metode alokasi **Tidak ada**. Sumber daya ditambahkan ke tim, namun kapasitas sumber daya tidak dihabiskan melalui pemesanan.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Pesan anggota tim untuk memenuhi persyaratan sumber daya untuk sumber daya generik

Dalam Project Operations, Anda dapat memesan sumber daya generik pada tim proyek. Anda juga dapat menentukan peran, kapasitas yang diperlukan, dan bagaimana kapasitas tersebut didistribusikan. Untuk persyaratan sumber daya, Anda dapat menentukan atribut yang terkait dengan sumber daya generik . Atribut ini mencakup keterampilan yang diperlukan, unit organisasi yang disukai, dan sumber daya pilihan.

Selesaikan langkah berikut untuk menentukan keterampilan yang diperlukan pada sumber daya generik untuk pengembang.

1. Pada formulir **proyek**, pada tab **tim**, pilih **baru** untuk memesan sumber daya generik.
2. Di tampilan **semua anggota tim**, di kolom **persyaratan sumber daya**, pilih tautan untuk menambahkan keterampilan yang diperlukan untuk sumber daya generik.
3. Pada formulir **persyaratan sumber daya**, di kisi **keahlian**, pilih elipsis (**...**) kemudian pilih **Tambah karakteristik kebutuhan baru** untuk menambahkan keterampilan yang diperlukan untuk pengembang Anda.
4. Di formulir dialog **buat cepat: karakteristik persyaratan**, di bidang **karakteristik**, pilih keahlian yang diperlukan.
5. Di bidang **nilai peringkat**, pilih tingkat kemahiran untuk keahlian tersebut. 
6. Di bidang **persyaratan sumber daya**, atur persyaratan sumber daya sumber dari unit organisasi atau bahkan sumber daya bernama. Setelah selesai, pilih **Simpan**.
7. Pada formulir **persyaratan sumber daya**, pilih **Pesan** untuk memenuhi persyaratan sumber daya. Anda juga dapat memilih sumber daya generik di kisi **semua anggota tim**, lalu pilih **Pesan**.

    > [!NOTE]
    > Dalam contoh ini, ada 40 jam yang diperlukan namun tidak ada jam Pemesanan aktual, karena sumber daya generik tidak memiliki Pemesanan. Selain itu, tidak ada jam yang ditetapkan, karena sumber daya generik ditambahkan langsung ke tim, daripada ditambahkan dengan menggunakan penetapan tugas.

    Pada formulir **asisten penjadwalan**, Anda dapat memfilter sumber daya yang tersedia berdasarkan persyaratan yang ditentukan pada persyaratan sumber daya. Sumber daya diurutkan berdasarkan parameter pengurutan yang ditentukan di papan jadwal.

   Beberapa filter yang paling umum digunakan adalah:

    - **Karakteristik bersama dengan peringkat**: filter berdasarkan keterampilan, sertifikasi, dan kualitas sumber daya lainnya, selain peringkat kemahiran.
    - **Peran**: filter berdasarkan peran default yang ditetapkan ke sumber daya yang dapat dipesan.
    - **Unit organisasi**: memfilter sumber daya yang dapat dipesan berdasarkan unit organisasi yang ditetapkan untuknya.

8. Jika Anda tidak puas dengan hasil pencarian persyaratan awal, Anda dapat mengubah kriteria filter. Perluas panel **tampilan filter** di sebelah kiri, lalu pilih **pencarian** untuk menemukan sumber daya tambahan. Untuk mengubah cara pengurutan, **Urutkan**.
9. Pilih sumber daya sesuai permintaan yang ditentukan pada persyaratan, seperti ditunjukkan di bagian atas kisi. Anda dapat menghapus pilihan sel di kisi dan membiarkan kapasitas sumber daya terbuka. Hanya satu sumber daya setiap kalinya yang dapat dipilih sebagai dipesan.
10. Pilih **Pesan** untuk memesan sumber daya yang dipilih dan biarkan papan jadwal terbuka, sehingga Anda dapat memilih sumber daya tambahan. Atau, pilih **Pesan & keluar** untuk memesan sumber daya yang dipilih dan tutup papan jadwal.
11. Kembali ke tampilan **semua anggota tim**. Di kisi, perhatikan bahwa sumber daya umum telah digantikan oleh sumber daya bernama, dan 40 jam terdaftar sebagai dipesan untuk sumber daya tersebut.

    > [!NOTE]
    > Tidak ada jam yang ditetapkan ditampilkan, karena mereka dipesan langsung pada tim. Mereka tidak dipesan menggunakan penetapan tugas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Tetapkan sumber daya generik ke tugas dan buat persyaratan sumber daya

Dalam Project Operations, Anda dapat membuat tugas, lalu menetapkan sumber daya generik. Permintaan sumber daya kemudian dapat diwakili oleh placeholder saat Anda memperkirakan jadwal dan angka keuangan. Selanjutnya Anda dapat membuat persyaratan sumber daya untuk sumber daya generik dan memenuhinya.

1. Pada formulir **proyek**, pada tab **jadwal**, pilih **Tambah** untuk membuat tugas.
2. Di bidang **sumber daya**, pilih simbol **pemilih sumber daya**. Pemilih sumber daya muncul dan menampilkan anggota tim yang ada untuk proyek.
3. Masukkan nama sumber daya generik baru, lalu pilih **buat**.
4. Di kotak dialog **buat cepat: anggota tim proyek** yang muncul, di bidang **Peran**, pilih peran untuk sumber daya generik. 
5. Di bidang **unit sumber daya**, pilih unit organisasi untuk sumber daya generik. Kemudian pilih **Simpan**. Anggota tim generik kini ditetapkan ke tugas.

   Pada tab **tim**, Anda akan melihat anggota tim generik baru. Perhatikan bahwa hanya jam yang ditetapkan. Jam tersebut adalah jumlah semua tugas yang ditetapkan ke anggota tim generik. Anggota tim generik tidak memiliki jam yang diharuskan atau persyaratan sumber daya.

6. Anda sekarang dapat menetapkan anggota tim umum untuk tugas lain menggunakan pemilih sumber daya.

   Setelah selesai menetapkan sumber daya generik untuk tugas, Anda dapat membuat persyaratan sumber daya untuk sumber daya generik.

7. Pada tab **tim**, pilih sumber daya generik, lalu pilih **buat persyaratan**. Bila persyaratan dibuat, anggota tim generik akan memiliki jam wajib dan tautan untuk persyaratan sumber daya.

  Setelah Anda memesan sumber daya bernama, sumber daya generik dihapus dari tim dan digantikan dengan sumber daya bernama. Pada tab **jadwal**, tugas sumber daya generik akan dihapus dan digantikan oleh sumber daya bernama.

  > [!NOTE]
  > Perilaku ini hanya terjadi bila sumber daya bernama sepenuhnya dipesan untuk persyaratan sumber daya generik. Bila sumber daya bernama sebagian menggantikan persyaratan sumber daya generik atau beberapa sumber daya bernama menggantikan persyaratan sumber daya generik, sumber daya generik tetap ditetapkan ke tugas.

Project Operations tidak menetapkan sumber daya ke tugas, karena perilaku tersebut akan menghasilkan jadwal yang kurang dapat diprediksi. Dalam contoh sederhana ini, mudah untuk membagi jam secara merata antara dua sumber daya. Namun, dalam skenario yang lebih kompleks yang melibatkan beberapa tugas dan beberapa sumber daya, PSA harus membuat asumsi tentang cara mengalokasikan Pemesanan yang diterima untuk beberapa sumber daya di beberapa tugas.

Oleh karena itu, dalam skenario ini, manajer proyek bertanggung jawab untuk menguraikan beberapa Pemesanan dan menetapkannya sesuai kebutuhan. Untuk mengalokasikan Pemesanan, manajer proyek menetapkan tugas dari sumber daya generik ke sumber daya bernama dan kemudian menggunakan tampilan **rekonsiliasi** untuk memastikan bahwa alokasi berfungsi dengan pemesanan.

### <a name="edit-a-resource-requirement"></a>Edit Persyaratan Sumber Daya

Setelah persyaratan sumber daya dibuat, manajer proyek atau manajer sumber daya mungkin ingin mengedit rincian untuk menyempurnakan kriteria pencarian bila papan jadwal digunakan. Untuk mengedit persyaratan sumber daya, ikuti langkah-langkah berikut.

1. Pada formulir **proyek**, pada tab **tim**, pilih tautan ke persyaratan apa pun di sumber daya generik.
2. Pada formulir **persyaratan sumber daya** yang muncul, masukkan informasi bidang yang diperlukan

   Pada formulir **persyaratan sumber daya**, manajer proyek atau manajer sumber daya juga dapat menentukan keahlian, peran, preferensi sumber daya, dan unit organisasi yang diinginkan.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Perbarui Pemesanan sumber daya setelah mereka dipesan pada proyek

Setelah menambahkan sumber daya generik atau bernama ke tim proyek, Anda dapat mengubah Pemesanan sumber daya.

1. Pada formulir **proyek**, pada tab **tim**, pilih anggota tim, lalu pilih **Kelola Pemesanan**.
 
   Papan jadwal akan ditampilkan dan menampilkan Pemesanan anggota tim proyek. Perluas rekaman anggota tim untuk melihat jam yang telah dipesan terhadap proyek ini dan proyek lainnya yang memakan kapasitas anggota tim.

2. Pilih dan tarik Pemesanan untuk memperluas atau mempersingkat. Kotak dialog **buat Pemesanan sumber daya** muncul yang memungkinkan Anda menyesuaikan Pemesanan.
3. Klik kanan Pemesanan. Anda kemudian dapat menggunakan menu pintasan untuk menyelesaikan tindakan berikut:

    - Ubah Status Pemesanan
    - Edit Pemesanan
    - Gantikan sumber daya pada tim proyek

### <a name="change-the-booking-status"></a>Ubah Status Pemesanan

Anda dapat mengubah status pemesanan default atau kustom.

Status berikut termasuk dalam Project Operations:

- **Dibatalkan**: Membatalkan pemesanan sumber daya dan membebaskan kapasitas sumber daya.
- **Pemesanan Definitif**: mengkonsumsi kapasitas sumber daya. Pemesanan biasanya memiliki status ini saat Anda membuka **Kelola Pemesanan** dari kisi **semua anggota tim** di formulir **proyek**.
- **Pemesanan tentatif**: Menambahkan sumber daya ke tim namun tidak mengkonsumsi kapasitas sumber daya. Status ini menunjukkan bahwa sumber daya telah dicadangkan untuk pekerjaan potensial namun masih memiliki kapasitas jika diperlukan pada pekerjaan lain. Di tampilan ketersediaan sumber daya secara keseluruhan, Pemesanan tentatif memiliki status yang berbeda dengan Pemesanan definitif.
- **Diusulkan**: Mewakili usulan manajer sumber daya atau manajer proyek untuk sumber daya. Proposal tidak mengkonsumsi kapasitas sumber daya, dan sumber daya tidak ditambahkan ke tim proyek. Untuk pemesanan definitif sumber daya pada tim, manajer proyek harus menerima proposal.

### <a name="submit-resource-requests"></a>Mengajukan permintaan sumber daya

Permintaan sumber daya digunakan untuk melakukan permintaan (persyaratan sumber daya) yang harus dipenuhi oleh Manajer sumber daya. Untuk sumber daya generik yang sudah ada di tim, Anda dapat mengajukan permintaan sumber daya secara langsung. Permintaan sumber daya dapat dipenuhi dengan dua cara:

- Manajer sumber daya langsung memenuhi permintaan. Dalam kasus ini, sumber daya umum digantikan dengan pemesanan definitif yang memiliki sumber daya bernama.
- Manajer sumber daya mengusulkan sumber daya untuk manajer proyek, dan manajer proyek menyetujui atau menolak sumber daya yang diusulkan.

#### <a name="direct-fulfillment-of-resource-requests"></a>Pemenuhan langsung permintaan sumber daya

Bila persyaratan sumber daya dihasilkan, manajer proyek dapat mengajukan permintaan sumber daya umum dengan memilih sumber daya, lalu memilih **Ajukan permintaan**. Komentar tentang sumber daya dapat diberikan kepada manajer sumber daya yang memenuhi permintaan. Setelah permintaan diajukan, bidang **status** untuk anggota tim akan diubah ke **Diajukan**. Ketika manajer sumber daya memenuhi permintaan, anggota tim generik digantikan dengan sumber daya bernama di kisi **semua anggota tim**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Menggunakan proposal sumber daya untuk permintaan sumber daya

Alih-alih langsung memesan sumber daya pada permintaan sumber daya, manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek. Manajer sumber daya dapat menggunakan pilihan ini bila pencocokan yang tepat dengan persyaratan tidak tersedia. Bila manajer sumber daya mengusulkan suatu sumber daya, manajer proyek melihat bahwa bidang **status** untuk anggota tim generik diubah ke **perlu ditinjau**.

Anda dapat melihat sumber daya yang diusulkan bersama dengan visualisasi untuk efek dari Pemesanan proposal. 

1. Klik dua kali anggota tim yang memiliki status **peninjauan kebutuhan**. 
2. Pilih tab **sumber daya yang diusulkan**.
3. Pilih **terima semua proposal** untuk menerima semua sumber daya yang diusulkan atau **Tolak semua proposal** untuk menolaknya. Jika Anda menerima sumber daya yang diusulkan, mereka dipesan secara definitif pada proyek sebagai anggota tim dan mengganti sumber daya generik.

> [!NOTE]
> Anda harus menerima atau menolak semua sumber daya yang diusulkan. Anda tidak dapat menerima atau menolaknya secara parsial.

### <a name="substitute-a-resource-on-the-project-team"></a>Gantikan sumber daya pada tim proyek

Terkadang, manajer proyek harus mengganti anggota tim yang dipesan pada suatu proyek.

1. Pada formulir **proyek**, pada tab **tim**, pilih sumber daya yang memerlukan pengganti, lalu pilih **Kelola Pemesanan**.
2. Perluas sumber daya untuk melihat proyek yang ditetapkan untuknya.
3. Klik kanan proyek, lalu pilih **ganti sumber daya**.
4. Jika Anda mengetahui sumber daya yang ingin Anda ganti untuk sumber daya saat ini, pilih atau ketik nama, lalu pilih **tetapkan ulang**.

Atau. Jika Anda perlu mencari sumber daya, selesaikan langkah berikut.

1. Pilih **Cari Pengganti**.

   Asisten jadwal akan menampilkan daftar pengganti yang tersedia. Di asisten jadwal, Anda dapat memfilter lebih lanjut sumber daya yang tersedia untuk menemukan pengganti yang sesuai.

2. Untuk mengganti sumber daya, pilih sumber daya yang diinginkan, lalu pilih **Ganti**.   

   Pemesanan dan penugasan digantikan dengan sumber daya baru.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Rekonsiliasi pemesanan dan penugasan Anggota tim

Untuk anggota tim, Pemesanan dan tugas secara longgar digabungkan. Dengan kata lain, sumber daya dapat memiliki tugas namun tidak ada pemesanan, atau mereka dapat memiliki Pemesanan namun tidak ada tugas. Idealnya, Pemesanan dan penetapan harus selaras, sehingga sumber daya memiliki kapasitas untuk melakukan tugas tugas. Namun, Pemesanan mungkin didasarkan pada ketersediaan, dan waktu tugas dapat berubah saat proyek berlanjut. Oleh karena itu, pasangan longgar Pemesanan dan penugasan memberikan fleksibilitas.

Project Operations memiliki tab **rekonsiliasi** yang memungkinkan manajer proyek merekonsiliasi Pemesanan anggota tim dan tugas mereka untuk tim proyek.

Tab **rekonsiliasi** menampilkan Pemesanan dan tugas hingga tingkat penetapan tugas individual untuk setiap anggota tim. Ini menunjukkan jam di sel yang menunjukkan periode waktu dari bulan ke hari.

Tab juga menampilkan Total keseluruhan bersih untuk proyek, bersama dengan kolom total.

Untuk setiap sumber daya, tab akan menghitung perbedaan antara Pemesanan anggota tim dan Rollup tugas anggota tim. Idealnya, perbedaan ini harus 0 (nol). Dengan kata lain, tidak ada perbedaan antara Pemesanan dan tugas. Perbedaan berwarna dan berarsir untuk menarik perhatian ke dua kondisi:

- **Kekurangan Pemesanan**: Terjadi bila sumber daya memiliki lebih banyak tugas daripada Pemesanan. Karena kapasitas ini belum dicadangkan, manajer proyek mungkin ingin memperbaiki kondisi ini dengan memperluas Pemesanan sumber daya untuk mengatasi defisit.
- **Pemesanan berlebih**: Terjadi saat sumber daya telah dipesan ke proyek namun belum ditetapkan ke tugas. Kondisi ini mungkin dapat diterima dalam kasus saat sumber daya dipesan ke proyek sebelum penetapan tugas terjadi. Namun, dalam kasus lain, sumber daya tidak direncanakan untuk ditetapkan ke tugas. Dalam kasus ini, manajer proyek harus mempertimbangkan membatalkan pemesanan sumber daya, sehingga kapasitas dapat digunakan untuk proyek lain.

Dalam kasus tertentu, bila Anda melihat waktu pada tingkat yang lebih tinggi daripada tingkat hari (misalnya, tingkat bulan), Anda mungkin melihat perbedaan bersih nol untuk sumber daya. Dengan kata lain, Pemesanan = penetapan. Namun, jika Anda melihat waktu di tingkat minggu, Anda mungkin melihat bahwa ada tugas yang dilakukan nol jam dan Pemesanan 40 jam di minggu pertama, namun penetapan 40 jam dan Pemesanan dalam nol jam di minggu kedua. Secara keseluruhan, Pemesanan dan penugasan akan didamaikan, namun berbeda dari satu minggu ke hari berikutnya.

Bila Anda melihat waktu di tingkat yang lebih tinggi, sel dalam tab **rekonsiliasi** memiliki indikator untuk menginformasikan bahwa ada perbedaan pada tingkat yang lebih rendah. Klik dua kali sel untuk memperbesar untuk melihat perbedaannya. Anda kemudian dapat klik kanan untuk memperkecil. Dengan memilih sumber daya, lalu memilih **perbedaan berikutnya** pada Toolbar kisi, Anda dapat membuka perbedaan berikutnya antara Pemesanan dan tugas untuk sumber daya tersebut. Pilih **Perbedaan sebelumnya** untuk kembali. Anda juga dapat menonaktifkan indikator perbedaan dan perilaku navigasi dalam **pengaturan**.

Jika Anda memiliki penetapan tugas untuk sumber daya, namun tidak ada pemesanan, pada formulir **proyek**, pada tab **rekonsiliasi**, pilih kekurangan Pemesanan, lalu pilih **Perluas Pemesanan**. Kotak dialog **Perluas Pemesanan** muncul dan menunjukkan Pemesanan yang diperlukan untuk mengatasi kekurangan sumber daya. Kotak dialog juga menampilkan Pemesanan sumber daya yang ada di seluruh proyek atau entitas yang dapat dijadwalkan lainnya. Jika Anda memilih **OK** untuk membuat pemesanan untuk sumber daya, terlepas dari ketersediaan sumber daya tersebut, Anda dapat menyebabkan pemesanan berlebihan.

Manajer proyek atau manajer sumber daya kemudian dapat menggunakan papan jadwal untuk mengelola setiap situasi dengan sumber daya yang dipesan berlebihan di luar kapasitasnya.
