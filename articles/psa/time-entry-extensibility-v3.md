---
title: Menyesuaikan entri waktu mingguan
description: Topik ini menyediakan informasi tentang cara menerapkan aturan bisnis kustom yang mendukung praktik organisasi.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a34244884bc81da74ae3bf550bde6f982d04abd3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149637"
---
# <a name="customize-weekly-time-entry"></a>Menyesuaikan entri waktu mingguan 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Di Microsoft Dynamics 365 Project Service Automation versi 3.3, Microsoft memperkenalkan kisi modern yang memungkinkan sumber daya proyek dengan cepat memasukkan waktu hingga satu minggu pada satu waktu. Kisi entri waktu mingguan baru dapat menampilkan total untuk entri berdasarkan tanggal, berdasarkan baris, atau minggu. Sumber daya dapat membuat salinan entri waktu dalam seminggu dan juga salinan massal dari minggu sebelumnya. Penyesuai sistem dapat menyesuaikan tampilan dengan menambahkan bidang, menambahkan pencarian ke entitas lain, dan menerapkan aturan bisnis kustom untuk mendukung praktik organisasi mereka.

Entri waktu dan kisi waktu mingguan baru dapat diakses melalui peta situs. Pengalaman entri waktu kustom yang tidak bisa diperluas yang merupakan bagian dari versi PSA sebelumnya telah digantikan oleh kisi entri waktu mingguan yang bisa diperluas, dan juga dengan pengalaman alternatif di kisi hanya baca dan kalender. Karena perubahan ini, pengguna dapat memasukkan waktu dalam jumlah mingguan.

## <a name="page-layout"></a>Tata letak halaman
Kisi entri waktu mingguan baru adalah kontrol kustom yang memiliki Toolbar dan dua bagian utama, **dimensi**, dan **durasi**. Toolbar mencakup tombol yang hanya berlaku untuk kontrol kustom ini untuk kisi entri waktu. Sebaliknya, tombol pada panel tindakan di bagian atas halaman berlaku untuk tiga jenis kontrol yang didukung untuk entri waktu: kontrol entri waktu mingguan, kontrol baca-saja, dan kontrol kalender.

### <a name="dimensions"></a>Dimensi
Bagian **dimensi** menunjukkan, sebagai heading kolom, Semua dimensi yang dapat dimasukkan. Dimensi berikut didukung secara default:

- Proyek
- Tugas Proyek
- Peran
- Jenis
- Status Entri

Bagian **dimensi** tidak memungkinkan pengeditan sebaris. Bagian ini didukung oleh tampilan yang memungkinkan bidang kustom ditambahkan ke kisi entri waktu mingguan. Untuk informasi tentang cara menambahkan bidang kustom, lihat bagian "ekstensibilitas" nanti di topik ini.

### <a name="duration"></a>Durasi
Bagian durasi menampilkan hari dalam seminggu sebagai header kolom. Bagian ini memungkinkan pengeditan sebaris. Setelah baris entri waktu dibuat yang memiliki dimensi yang sesuai, pengguna dapat dengan cepat memasukkan, secara sebaris, jumlah waktu yang dihabiskan pada dimensi tersebut.

## <a name="create-a-new-time-entry"></a>Buat entri waktu baru
Untuk membuat entri waktu baru dalam kisi entri waktu, pilih **baru**. Kotak dialog **buat cepat entri waktu** ditampilkan. Di kotak dialog ini, pengguna dapat memilih tanggal entri waktu, lalu memasukkan data untuk **proyek**, **tugas proyek**, **peran**, dan dimensi **durasi** dalam menit, jam, atau hari dengan mengetik **h**, **m**, atau **d**, bersama dengan nomor. Pengguna juga dapat memasukkan Deskripsi dan komentar yang dapat dibagikan secara eksternal untuk entri waktu. Bila pengguna menyimpan perubahannya, nilai yang mereka masukkan terhadap dimensi akan muncul di bagian **dimensi**. Informasi durasi yang mereka masukkan di bidang **durasi** akan muncul pada tanggal saat entri waktu dibuat.

Bidang pencarian didukung oleh tampilan sistem. Misalnya, setelah pengguna memasukkan proyek , bidang **tugas proyek** diatur ke tampilan **salinan** secara default. Untuk membuat entri waktu untuk tugas yang tidak ditetapkan ke pengguna, pilih **Ubah tampilan** di kotak dialog pencarian, lalu pilih tampilan **semua tugas proyek aktif**.

## <a name="edit-a-time-entry"></a>Editan Entri Waktu
Rincian dari beberapa bidang pada halaman entri waktu, seperti **Deskripsi** dan **komentar eksternal**, tidak ditampilkan di kisi entri waktu mingguan. Sebaliknya, indikator segitiga kecil muncul di sel durasi yang memiliki rincian tambahan ini. Pilih sel , lalu pilih **Edit rincian** untuk melihat data di panel **edit cepat**. Untuk mengedit atau memperbarui rincian untuk entri waktu tertentu yang bukan bagian dari kisi waktu mingguan, pengguna harus membuka panel **edit cepat**.

## <a name="copy-a-time-entry-row"></a>Salin baris Entri Waktu
Setelah baris entri pertama kali dibuat, pengguna dapat memilih **Salin baris** untuk menyalin seluruh baris ke baris baru. Bila baris disalin dengan cara ini, dimensi dan durasi juga disalin. Pengguna juga dapat memilih **Edit baris** untuk memperbarui nilai dimensi dan durasi sebaris di bagian **durasi**.

## <a name="open-a-time-entry"></a>Buka Entri Waktu
Untuk mendukung entri yang optimal dan cepat di bidang yang paling menonjol, kisi waktu mingguan menampilkan subkumpulan dimensi dan durasi waktu tertentu. Untuk melihat semua rincian entri satu kali, dalam **Edit entri**, pilih **buka**.

## <a name="submit-a-time-entry"></a>Ajukan entri waktu
Pengguna dapat mengirimkan entri satu kali atau grup entri waktu dengan memilih blok sel atau baris entri seluruh waktu, lalu memilih **Ajukan**. Entri waktu yang dikirim akan muncul sebagai entri yang menunggu persetujuan pada halaman **persetujuan** pemberi persetujuan. Setelah entri waktu berhasil diajukan, mereka tidak dapat diedit.

## <a name="recall-a-time-entry"></a>Tarik kembali entri waktu
Anda dapat menarik kembali entri waktu yang telah Anda ajukan. Anda dapat menanyakan entri satu kali, blok entri waktu, atau seluruh baris entri waktu. Entri waktu yang ditarik dapat diedit oleh sumber daya.

## <a name="time-entry-status"></a>Status Entri Waktu
Entri waktu baru secara otomatis ditetapkan status **draf**. Bila entri waktu diajukan, status akan diperbarui ke **Diajukan**. Bila entri waktu yang diajukan disetujui, status diperbarui ke **Disetujui**. Jika entri waktu ditolak, status akan diperbarui ke **dikembalikan**, dan entri dapat dikoreksi dan diajukan kembali. Hanya entri waktu yang memiliki status **draf** yang dapat dihapus.

## <a name="view-rejection-comments"></a>Lihat Komentar Penolakan
Bila entri waktu ditolak oleh pemberi izin, pemberi izin dapat menambahkan komentar penolakan untuk membantu sumber daya memahami alasan penolakan. Untuk melihat komentar penolakan untuk entri waktu, pilih **entri terbuka**. Komentar penolakan akan ditampilkan di Timeline. Di Timeline, sumber daya dapat merespons komentar penolakan sebelum dia mengajukan ulang entri.

## <a name="copy-week"></a>Salin minggu
Setelah beberapa entri waktu dibuat, pengguna dapat memilih **Salin Pekan** untuk membuat entri waktu secara massal. Kotak dialog **Salin** akan ditampilkan. Di bagian **dari periode**, gunakan bidang **tanggal mulai** dan **tanggal berakhir** untuk menentukan rentang tanggal untuk menyalin entri waktu. Di bagian **hingga periode**, di bidang **tanggal mulai**, tentukan tanggal untuk membuat entri waktu. Kemudian pilih **Salin**. Untuk tanggal yang ditentukan di periode "hingga", salinan entri waktu untuk hari yang sesuai dalam pekan itu dalam periode "dari" dibuat. Misalnya, entri waktu Senin dari pekan lalu disalin ke hari Senin dalam pekan yang ditentukan sebagai periode "hingga".

## <a name="import"></a>Impor
Proses dasar yang sama digunakan untuk mengimpor dari Pemesanan, tugas, dan pertukaran. Pengguna dapat menentukan rentang tanggal yang diimpor dari Pemesanan. Kemudian, mereka harus secara eksplisit memilih Pemesanan yang akan disalin ke dalam entri waktu draf. Pada rilis sebelumnya, entri waktu yang disarankan muncul di kisi dan kalender, dan hilang saat sesi diperbarui.

## <a name="extensibility"></a>Ekstensibilitas
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Tambahkan bidang kustom yang memiliki pencarian ke entitas lain
Ada tiga langkah utama untuk menambahkan bidang kustom ke kisi entri mingguan waktu.

1.  Tambahkan bidang kustom ke kotak dialog buat cepat
2.  Konfigurasikan kisi untuk menampilkan bidang kustom.
3.  Tambahkan bidang kustom ke alur tugas Edit baris atau aliran tugas Edit sel, yang sesuai.

Anda juga harus memastikan bahwa bidang baru memiliki validasi yang diperlukan di alur tugas Edit sel atau baris. Sebagai bagian dari langkah ini, Anda harus mengunci bidang, berdasarkan status entri waktu.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Tambahkan bidang kustom ke kotak dialog buat cepat
Anda harus menambahkan bidang kustom ke kotak dialog buat cepat waktu pembuatan entri waktu. Sehingga pengguna dapat memasukkan nilai saat menambahkan entri waktu menggunakan tombol **baru**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurasikan kisi untuk menampilkan bidang kustom
Ada dua cara untuk menambahkan bidang kustom ke kisi entri mingguan waktu. Pilihan pertama adalah menyesuaikan tampilan **entri waktu mingguan saya** dan menambahkan bidang kustom ke dalamnya. Anda dapat memilih posisi dan ukuran bidang kustom di kisi dengan mengedit properti tersebut dalam tampilan.

Pilihan kedua adalah membuat tampilan entri waktu kustom baru dan mengaturnya sebagai tampilan default. Tampilan ini harus berisi bidang **Deskripsi** dan **komentar eksternal**, selain kolom yang ingin Anda miliki di kisi. Anda dapat memilih posisi, ukuran, dan urutan default kisi dengan mengedit properti tersebut dalam tampilan. Selanjutnya, konfigurasikan kontrol kustom untuk tampilan ini sehingga merupakan kontrol **kisi entri waktu**. Tambahkan kontrol ini ke tampilan, dan pilih untuk web, ponsel, dan tablet. Selanjutnya, konfigurasikan parameter untuk kisi entri mingguan waktu. Atur bidang **tanggal mulai** ke **msdyn_date**, atur bidang **durasi** menjadi **msdyn_duration**, dan atur bidang **status** menjadi **msdyn_entrystatus**. Untuk tampilan default, bidang **daftar status baca-saja** diatur ke **192350002,192350003,192350004**, bidang **aliran tugas Edit baris** diatur ke **msdyn_timeentryrowedit,** dan Bidang **Alur tugas Edit sel** diatur ke **msdyn_timeentryedit**. Anda dapat menyesuaikan bidang ini untuk menambahkan atau menghapus status baca-saja, atau menggunakan pengalaman berbasis tugas (TBX) yang berbeda untuk pengeditan baris atau sel. Bidang ini harus terikat ke nilai statis.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Menambahkan bidang kustom ke alur tugas Edit yang sesuai
Halaman TBX yang digunakan untuk mengedit dapat ditemukan dalam **proses**. Halaman default adalah **Project Service-Edit baris entri waktu** dan **Project Service- Edit entri waktu**. Anda dapat mengedit halaman default ini atau membuat halaman TBX kustom baru.

> [!NOTE] 
> Kedua pilihan akan menghilangkan beberapa filter bawaan pada entitas **proyek** dan **tugas proyek**, sehingga semua tampilan pencarian untuk entitas akan terlihat. Per default, hanya tampilan pencarian yang relevan yang dapat dilihat.

Anda harus menentukan alur tugas yang sesuai untuk bidang kustom. Kemungkinan besar, jika Anda menambahkan bidang ke kisi, harus masuk di alur Edit tugas baris yang digunakan untuk bidang yang berlaku untuk seluruh baris entri waktu. Jika bidang kustom memiliki nilai unik setiap hari, seperti bidang kustom untuk **waktu berakhir**, bidang tersebut harus masuk dalam alur tugas Edit sel.

Untuk menambahkan bidang kustom ke alur tugas, tarik elemen **bidang** ke posisi yang sesuai pada halaman, lalu Atur properti. Atur properti **sumber** ke **entri waktu**, dan atur properti **bidang data** ke bidang kustom. Properti **bidang** menentukan nama tampilan pada halaman tbx. Pilih **terapkan** untuk menyimpan perubahan ke bidang. Pilih **Perbarui** untuk menyimpan perubahan ke halaman.

Untuk menggunakan halaman TBX kustom baru, buat proses baru. Atur kategori ke **alur proses bisnis**, atur entri entitas ke **waktu**, dan atur jenis proses bisnis untuk **menjalankan proses sebagai alur tugas**. Dalam **properti**, properti **nama halaman** harus diatur ke nama tampilan halaman. Tambahkan semua bidang yang relevan ke halaman TBX. Simpan dan Aktifkan proses, lalu Perbarui properti kontrol kustom untuk alur tugas yang relevan dengan nilai **nama** pada proses.

### <a name="add-new-option-set-values"></a>Tambahkan Nilai Rangkaian Pilihan baru
Untuk menambahkan nilai rangkaian pilihan ke bidang siap pakai, buka halaman pengeditan untuk bidang, lalu di dalam **jenis**, pilih **Edit** di sebelah rangkaian pilihan. Selanjutnya, tambahkan pilihan baru yang memiliki label dan warna kustom. Jika Anda ingin menambahkan status entri waktu baru, bidang siap pakai diberi nama **status entri**, bukan **status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Menentukan status entri waktu baru sebagai hanya baca
Untuk menetapkan status entri waktu baru sebagai hanya baca, tambahkan nilai entri waktu baru (nomor, bukan label) ke properti **daftar status hanya baca**. Bagian diedit dari kisi entri waktu akan dikunci untuk baris yang memiliki status baru.
Selanjutnya, tambahkan aturan bisnis untuk mengunci semua bidang pada waktu halaman tbx **Edit baris entri waktu** dan **Edit entri waktu**. Anda dapat mengakses aturan bisnis untuk halaman ini dengan membuka editor alur proses bisnis untuk halaman, lalu memilih **aturan bisnis**. Anda dapat menambahkan status baru ke kondisi di aturan bisnis yang ada, atau Anda dapat menambahkan aturan bisnis baru untuk status baru.

### <a name="add-custom-validation-rules"></a>Tambahkan aturan validasi kustom
Ada dua jenis aturan validasi yang dapat Anda tambahkan untuk pengalaman entri kisi waktu mingguan: • aturan bisnis sisi klien yang berfungsi di kotak dialog buat cepat dan pada halaman TBX • plug-in sisi server validasi yang berlaku untuk semua pembaruan entri waktu

#### <a name="business-rules"></a>Aturan bisnis
Gunakan aturan bisnis untuk mengunci dan membuka kunci bidang, masukkan nilai default di bidang, dan tentukan validasi yang memerlukan informasi hanya dari rekaman entri waktu saat ini. Anda dapat mengakses aturan bisnis untuk halaman TBX dengan membuka editor alur proses bisnis untuk halaman, lalu memilih **aturan bisnis**. Selanjutnya, Anda dapat mengedit aturan bisnis yang ada atau menambahkan aturan bisnis baru. Untuk validasi yang lebih disesuaikan, Anda dapat menggunakan aturan bisnis untuk menjalankan JavaScript.

#### <a name="plug-in-validations"></a>Validasi plug-in
Anda harus menggunakan validasi plug-in untuk validasi yang memerlukan konteks lebih daripada tersedia di rekaman entri satu kali, atau untuk validasi yang ingin Anda jalankan pada pembaruan inline di kisi. Untuk menyelesaikan validasi, buat plug-in kustom pada entitas **entri waktu**.

> [!IMPORTANT] 
> Saat ini, masalah yang diketahui pada halaman TBX mencegah pengguna mengoreksi informasi dan memilih ulang Selesai saat pembaruan gagal dalam validasi plug-in. Untuk mengatasinya, konfigurasikan validasi aturan bisnis untuk mencegah situasi ini sebisa mungkin.
