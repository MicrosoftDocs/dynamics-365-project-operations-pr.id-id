---
title: Penginstalan data sampel
description: Aplikasi topik menyediakan informasi tentang menginstal data sampel di Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 377e50fc5772c4dc146ccee098bf2806bbc8c6b7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275092"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalasi data sampel untuk aplikasi Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Untuk membantu Anda membangun lingkungan demo sendiri, Microsoft memberikan paket data sampel dapat diunduh yang menampilkan kemampuan aplikasi Anda. Ada dua jenis paket data sampel:
- Data konfigurasi/referensi
- Data demo (data referensi/konfigurasi dan transaksi seperti perintah kerja dan proyek)

Paket data **referensi** sampel dapat diunduh dalam tiga paket berbeda, sehingga Anda dapat menginstal data hanya untuk project service, atau hanya untuk Field Service, atau Anda dapat menginstal data sampel untuk kedua aplikasi sekaligus.

Paket Data konfigurasi/referensi sampel adalah:

- [**V902PSMasterData** - Project Service versi 3.x saja](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Field Service versi 8.x saja](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x dan Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Paket data **demo** terbaru adalah:

 - [**FPSDemoData** - Field Service 8.x dan Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Petunjuk penginstalan sedikit berbeda dalam hal pengguna harus membuat dan mengkonfigurasikan bagian namun lainnya adalah sama seperti [**posting blog**](https://aka.ms/fpsdemodatablog)sebelumnya. Paket ini memiliki rangkaian data demo yang dikurangi dan memerlukan sekitar 3 jam untuk menginstal.

Paket data sampel ini tersedia dalam bahasa Inggris saja.

> [!IMPORTANT]
> **Tidak ada cara untuk menghapus instalasi data sampel.** Anda seharusnya hanya menginstal paket ini pada demonstrasi, evaluasi, pelatihan, dan menguji sistem. Juga perhatikan bahwa menginstal paket individual, dan kemudian menginstal paket individual lainnya, tidak didukung. (Dengan kata lain, Anda tidak dapat menginstal **FSMasterData** diikuti **PSMasterData**, atau sebaliknya.) Jika Anda merasa perlu data sampel untuk kedua aplikasi di setiap titik di masa mendatang, Anda harus menginstal paket **v902FPSMasterData**.

Saat Anda menginstal salah satu paket data sampel, proses instalasi melakukan tindakan berikut:

- Membuat atau menetapkan parameter default untuk menggunakan project service, Field Service, atau kedua aplikasi (jika ada).

- Impor sampel data untuk aplikasi, seperti sumber daya yang dapat dipesan, peran khusus aplikasi, penjualan dan daftar harga biaya, unit organisasi, rekaman proses penjualan, dan entitas lain untuk menunjukkan kemampuan utama.  

Dengan paket **data demo**, Anda mendapatkan data transaksi di atas dan tambahan seperti perintah kerja dan proyek.

Ingin mengetahui kemampuan yang dapat Anda demonstrasikan dengan data sampel? Lihat skenario fiktif Fabrikam Robotics dalam [catatan teknis](#technical-notes).

Jika Anda memiliki pertanyaan tentang cara menginstal paket data sampel ini, [kirim email di fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Persyaratan

Protokol penginstalan mengasumsikan berikut tentang target instans (organisasi):

- Bahasa dasar adalah bahasa Inggris dan mata uang dasar dolar AS (USD,$).

- Organisasi belum memiliki data project service atau Field Service, atau hanya memiliki data default barebone yang disertakan dengan setiap organisasi baru.

- Versi benar aplikasi bisnis sudah diinstal:
       
    - **Untuk FPSDemoData atau v902FPSMasterData:** organisasi memiliki Field Service versi 8.x dan project service versi 3.x diinstal.

    - **Untuk v902PSMasterData:** organisasi memiliki Project Service versi 3.x diinstal.

    - **Untuk v902FSMasterData:** organisasi memiliki Field Service versi 8.x diinstal.

> [!NOTE]
> Jika Anda harus menginstal data sampel di atas project service dan Field Service uji coba atau lingkungan demo yang ada yang sudah memiliki data (tidak disarankan), Anda harus menunda pra-pemeriksaan keamanan yang dilakukan oleh Penginstal. Untuk informasi lebih lanjut, lihat catatan teknis di bawah ini.

## <a name="prepare-for-installation"></a>Siapkan penginstalan

Anda harus Jalankan Penginstal di komputer dengan versi terbaru dari Windows (Windows 10 lebih disukai).

Anda harus merencanakan untuk komputer untuk tetap tersambung ke jaringan, dan untuk penginstalan untuk menjalankan hingga **satu jam** untuk **data konfigurasi/referensi**. (Biasanya penginstalan waktu sekitar 30 menit untuk **FPSMasterData**, yang mencakup data sampel untuk kedua aplikasi.) Untuk **FPSDemoData**, penginstalan akan memerlukan sekitar **3 jam**.

Fungsi screensaver komputer harus dinonaktifkan. Jika tidak, sesi kredensial untuk penginstalan mungkin akan hilang saat screensaver aktif (kecuali Anda menjaga sesi selalu aktif).

> [!div class="mx-imgBorder"]
> ![Tangkapan layar pengaturan screensaver, dengan screensaver dinonaktifkan](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Unduh dan ekstrak

Penginstal data sampel Project Service dan Field Service didistribusikan sebagai eksekusi yang terekstrak. Nama file mungkin berbeda tergantung pada paket data sampel, namun jika tidak langkah-langkah tetap sama tidak peduli paket yang Anda instal.

Setelah mengunduh paket, jalankan file .exe, dan kemudian terima persyaratan dan ketentuan untuk mengekstrak file terkompresi zip. Kemudian Anda perlu mengekstrak isi file itu ke folder di komputer.

Tergantung pada sistem operasi dan pengaturan keamanan, Anda mungkin harus melakukan langkah-langkah berikut setelah membuka Kemasan zip file:

1. Cari dan klik kanan **FPSDemoData.dll** file dalam folder **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Pilih **buka blokir**.

3. Pilih **Terapkan**.

4. Pilih **OK**.


## <a name="create-or-configure-users"></a>Membuat atau mengkonfigurasi pengguna

Paket **FPSDemoData** memerlukan enam pengguna sedangkan paket **FPSMasterData** memerlukan satu pengguna. Lihat yang benar untuk paket data sampel Anda.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Membuat atau mengkonfigurasi pengguna - paket data referensi/konfigurasi

Paket **FPSMasterData** dirancang untuk menginstal dengan satu pengguna bernama Spencer Low dengan pengaturan yang diuraikan di sini. Untuk menginstal paket dengan benar, Anda harus membuat (atau sementara ganti nama) pengguna di lingkungan Anda dengan konfigurasi data sampel masuk.

Untuk membuat atau mengkonfigurasi pengguna, buka **pengaturan** > **Keamanan** > **pengguna**, dan melakukan hal berikut:

1. Atur UserFullname = "Spencer Low" dengan nama pengguna "spencerl" (**huruf kecil**) untuk peran manajer proyek dan manajer praktik.

2. Pilih pengguna **Spencer Low**, lalu pilih **Kelola peran**. Cari dan pilih peran **Administrator sistem**, dan kemudian pilih **OK** untuk memberikan hak penuh admin ke Spencer Low. Langkah ini diperlukan untuk memastikan bahwa sampel rekaman dibuat dengan kepemilikan pengguna yang benar dan oleh karena itu mengisi tampilan dengan benar.

3. Dari paket yang diunduh, Anda harus memperbarui file pemetaan data dengan alamat email dari konteks pengguna default. Untuk melakukannya, buka **PkgFolder**, lalu Cari dan membuka **ImportUserMapFile.xml** file di Notepad (atau Visual Studio atau editor XML lainnya). Atur bidang **DefaultUserToMapTo=** ke alamat email pengguna Spencer Low.

4. Jika Anda tidak menggunakan Spencer Low dengan nama pengguna **spencerl**, Anda harus memperbarui file tambahan. Buka **DemoDataPreImportConfig.xml** file, dan kemudian menemukan **userstocreateandconfigure** tag. Perbarui tag **\<login\>** dengan nama pengguna Anda pengguna Spencer Low. Untuk detail tambahan, lihat [catatan teknis](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Membuat atau mengkonfigurasi pengguna - paket data demo

Paket data demo memerlukan enam pengguna. Agar paket terinstal dengan benar, lakukan langkah berikut:

 1. Buat atau sementara ganti nama pengguna yang ada sesuai konfigurasi data sampel masuk dengan membuka **pengaturan** > **keamanan** > **pengguna**.
 
    Peran ini hanya diperlukan untuk demo berbasis persona.  
    - Nama Lengkap Pengguna = "David So" sebagai teknisi Field Service   
    - Fullname Pengguna = "Jamie Reding" sebagai operator Customer Service & Field Service   
    - Fullname Pengguna = "Molly Clark" sebagai manajer akun   
    - Fullname Pengguna = "Spencer Low" sebagai manajer praktik dan proyek  
    - Fullname Pengguna = "Veronica Quek" sebagai anggota tim   
    - Fullname Pengguna = "William Contoso"
  
2. Untuk tujuan impor data demo, tetapkan enam pengguna atas Peran Administrator sehingga sampel rekaman diimpor dengan benar. 

3. Buka **PkgFolder** lalu Cari dan membuka **ImportUserMapFile.xml**. Perbarui bidang **baru=** ke alamat email pengguna yang terkait di sistem.

   > [!div class="mx-imgBorder"]
   > ![Screenshot UserMapFile](media/sample-data-7.png)

4. Jika nama lengkap pengguna "Spencer Low" Anda memiliki ID pengguna yang berbeda dari **"spencerl"**, maka Anda harus memperbarui file tambahan. Buka **DemoDataPreImportConfig.xml** file, dan kemudian menemukan **userstocreateandconfigure** tag. Pembaruan tag **\<login\>** dengan loginId (peka huruf besar/kecil). 

5. Kalender pengguna pertama (di **userstocreateandconfigure** tag) digunakan untuk mengisi jam kerja untuk semua sumber daya yang dapat dipesan pada impor data demo. Navigasikan ke **pengaturan** > **keamanan** > **pengguna**, Cari pengguna "Spencer Low" Anda, dan buka pilihan "Jam kerja". Edit jam kerja yang ada, dengan memilih pilihan **seluruh jadwal mingguan berulang dari mulai hingga berakhir**. Pastikan **jam kerja ditetapkan untuk 8 pagi - 5 sore (9 jam), Senin hingga Jumat dan dengan zona waktu yang diatur ke waktu Pasifik (AS & Kanada)**. Hal ini diperlukan untuk memastikan bahwa proyek dan papan jadwal menunjukkan sebagaimana mestinya.

**Rekomendasi:** pertimbangkan untuk membuat cadangan organisasi Anda sekarang, jika Anda perlu Kembalikan ke titik awal jika terjadi kesalahan selama penginstalan data sampel. Untuk informasi lebih lanjut, lihat [instans pencadangan dan pemulihan](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Jalankan Package Deployer

1. Cari dan jalankan **PackageDeployer.exe** di folder **v902FPSMasterData** atau **PackageDeployer_FPSDemoData**.

2. Terima syarat dan ketentuan.

3. Pada jendela berikutnya:

   a. Pilih Jenis Penyebaran **Office 365**.

   b. Gunakan pengguna dan sandi pengguna administrator sistem yang dikonfigurasi dalam "Buat atau konfigurasi pengguna" ("Spencer Low" dengan nama pengguna "spencerl").

   c. Pastikan **tampilan daftar organisasi-organisasi yang tersedia** dipilih.

      > [!div class="mx-imgBorder"]
      > ![tangkapan layar jendela Package Deployer dengan "Tampilan daftar organisasi yang tersedia" dipilih](media/sample-data-2.png)

4. Pilih organisasi yang akan menginstal data sampel.

5. Pilih **berikutnya** hingga Anda melihat **konfigurasi Data Demo** dialog.

   > [!div class="mx-imgBorder"]
   > ![Ambil Screenshot dari jendela status Penginstal data demo](media/sample-data-3.png)

6. Sebelum melanjutkan, perhatikan bahwa menginstal data sampel dapat memerlukan waktu hingga satu jam (biasanya ~ 10 menit). Anda harus memastikan bahwa komputer tetap hidup dan tersambung ke jaringan selama seluruh proses penginstalan, dan bahwa sesi Anda tetap aktif.   

7. Saat Anda siap, klik **berikutnya** untuk memulai proses penginstalan data sampel. Setelah data sampel dimuat, klik **selesai**.

## <a name="verify-the-sample-data-installation"></a>Memverifikasi penginstalan data sampel

Untuk memeriksa kewajaran, pastikan bahwa jumlah rekaman dan jenis entitas yang tercantum di skenario fiktif Fabrikam Robotics muncul sebagaimana mestinya.

Setelah data sampel benar-benar terbuka, masuk sebagai pengguna Spencer Low dan konfirmasikan berikut:

- Jika aplikasi Project Service diinstal, buka **Project Service** > **Pengaturan** > **Daftar harga**. Konfirmasikan bahwa tingkat tagihan dan tingkat biaya ada dengan mata uang yang sesuai untuk setiap negara/kawasan dalam himpunan data.

- Jika aplikasi Project Service diinstal, buka **Universal Resource Scheduling** > **Pengaturan** > **Unit Organisasi**. Konfirmasikan bahwa daftar harga biaya dengan mata uang yang sesuai telah dikaitkan dengan masing-masing unit organisasi (termasuk entri kota). Jika ada yang hilang, Cari dan kaitkan daftar harga biaya yang benar.

- Jika aplikasi Field Service diinstal, buka **Project Service** > **Pengaturan** > **Daftar harga**. Konfirmasikan bahwa tingkat tagihan dan tingkat biaya sudah ada. Buka **Field Service** > **Pengaturan** > **Daftar harga** dan periksa bahwa tingkat tagihan dan biaya tingkat ada, dengan mata uang yang sesuai, untuk setiap negara/kawasan dalam himpunan data.

  > [!div class="mx-imgBorder"]
  > ![Screenshot dari daftar harga aktif](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Screenshot unit organisasional aktif](media/sample-data-5.png)

## <a name="technical-notes"></a>Catatan teknis

Lihat di bawah ini untuk lebih banyak rincian teknis tentang penginstalan data ini.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Menginstal data sampel di atas data yang ada (tidak disarankan)

Jika Anda harus menginstal data sampel di atas project service dan Field Service uji coba atau lingkungan demo yang ada yang sudah memiliki data, Anda harus menunda pra-pemeriksaan keamanan yang dilakukan oleh Penginstal.

Untuk melakukannya, buka **PkgFolder** folder untuk menemukan dan membuka **DemoDataPreImportConfig.xml** file dengan Notepad (atau editor XML lainnya).

Cari nilai berikut, dan kemudian mengubah pengaturan dari benar menjadi salah:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Perubahan ini menyebabkan Penginstal untuk memotong beberapa pemeriksaan penting keamanan, termasuk:

- Mengkonfirmasikan bahwa tidak lebih dari satu rekaman **Unit organisasi** aktif, dan kemudian mengganti nama ke **Fabrikam US**.

- Mengkonfirmasikan bahwa ada tidak lebih dari satu rekaman **Template kerja** aktif.

- Mengkonfirmasikan bahwa tidak lebih dari satu rekaman **Parameter Proyek** aktif, dan kemudian mengganti nama entri itu ke **Parameter**.

### <a name="configuration-components"></a>Komponen konfigurasi

Ada beberapa komponen konfigurasi lain di file pra-impor konfigurasi ini. Untuk pengguna teknis, sebagian di antaranya mencakup:

- **\<RequiredSolutions\>** menentukan penginstalan solusi prasyarat dan nomor versi mereka.

- **\<InstallSampleData\>** mengontrol apakah data sampel siap pakai untuk aplikasi diinstal.

    - false - melewati penginstalan data built-in ini (yang dapat dilepaskan)

    - True - menginstal data built-in bersamaan dengan penginstalan sampel data PSA dan FS

- **\<PreImportDataCollection\>** menentukan peta Data file rata dan rekaman terkait yang akan diimpor sebelum instalasi data sampel utama.

- **\<EntitiesToEnableScheduling\>** menentukan entitas yang harus diaktifkan untuk Pemesanan di Microsoft Dynamics Scheduling (alias Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** menentukan sumber daya dipesan yang akan dibuat (jika belum ada) sebelum mengeksekusi impor data sampel. Perlu diketahui bahwa data sampel sistem sumber daya dapat dipesan sesuai dengan target rekaman sumber daya sistem dapat dipesan pada FullName dan login setiap sumber daya. Oleh karena itu, TIDAK mungkin mengubah nama dalam file pra-konfigurasi ini kecuali jika Anda mengimpor data sampel ke sistem target menggunakan nama ini, lalu mengganti nama sumber daya dapat dipesan untuk nama yang Anda inginkan yang ditetapkan bersama rekaman pengguna yang diaktifkan, dan kemudian mengekspor data lagi untuk impor ke sistem tujuan akhir (memperbarui entri baru dan lama **ImportUserMapFile.xml** sesuai dengan itu).

- **\<PluginsToDisable\>** menentukan plug-in item baris yang sangat diskrit yang harus dinonaktifkan selama impor data sampel dan kemudian diaktifkan lagi setelahnya.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Skenario fiktif Fabrikam Robotics

Paket data referensi sampel Field Service dan Project Service menginstal **solusi Data induk Produksi Fabrikam (v3.0.0.0)**, bersama sekitar 4000 rekaman dan sekitar 40 entitas yang berbeda. Paket data sampel terpisah untuk Field Service atau project service berisi subset sampel data **v902FPSMasterData** untukaplikasi tersebut. Paket **Data Demo** menginstal **solusi Data Demo Fabrikam Manufacturing (v3.0.0.7)** dengan sekitar 22.000 rekaman di seluruh 148 entitas.

Perusahaan fiktif, Fabrikam Robotics, adalah produsen robot lini perakitan perangkat elektronik dan dikenal untuk kualitas produk, inovasi, dan layanan pelanggan yang kuat, termasuk perencanaan penginstalan, pelaksanaan dan Layanan pemeliharaan berkelanjutan. Fabrikam berkantor pusat di Amerika Serikat (Fabrikam U.S.), dan memiliki operasi layanan berbasis proyek di Prancis, India, Inggris, dan Swiss.

Operasi Field Service terpusat di Amerika Serikat, sebagian besar di area Seattle raya. Perusahaan berfokus pada memanfaatkan konektivitas Internet of Things (IoT) untuk memantau kinerja aset pelanggan dan memberikan layanan di lokasi yang semakin proaktif.

Ikhtisar tingkat tinggi data sampel adalah sebagai berikut:

- Elemen data sampel Umum (termasuk untuk kedua aplikasi)

    - 1 Pengguna

    - 71 Akun

    - 137 Kontak

    - Berbagai jenis transaksi dan kategori

    - 50 Produk dengan 1 daftar harga produk

    - 14 Daftar Harga/Biaya

    - 31 karakteristik (keahlian sumber daya) dalam 2 model peringkat dengan 3 tingkat (nilai peringkat)

- Project Service

    - 8 Unit Organisasi

    - 6 tingkat pemanfaatan khusus peran

    - 2,8 k+ spesifikasi peran-harga

- Field Service

    - 4 Wilayah

    - 5 Jenis Perintah Kerja

    - 22 Aset Pelanggan

    - 9 jenis insiden dengan berbagai karakteristik sumber daya terkait (9), Layanan (13) dan tugas Layanan (13)
   
Paket **Data Demo** menginstal sekitar 179 perintah kerja, 12 proyek, dan data transaksi terkait. 

### <a name="change-the-work-hours-for-sample-resources"></a>Ubah jam kerja untuk sumber daya sampel

Secara default, semua sumber daya yang dapat dipesan memiliki kalender 24 jam kerja.

Jika Anda ingin mengubah jam kerja untuk sampel sumber daya dapat dipesan, buka **Universal Resource Scheduling** > **Scheduling** > **Sumber daya**.

Pilih pengguna (misalnya, Spencer Low) dan Ubah jam kerja dari Spencer ke jam yang akan diterapkan ke beberapa pengguna. Buka **Universal Resource Scheduling** > **Pengaturan** > **Template Jam Kerja** dan edit rekaman **Template Kerja Default**. Di bidang **sumber daya Template**, pilih pengguna dengan jam kerja yang akan diterapkan ke sumber daya lainnya. Buka **Universal Resource Scheduling** > **Penjadwalan** > **Sumber daya** > **Sumber daya Dapat Dipesan Aktif**. Pilih sumber daya yang akan diubah, dan kemudian pilih **Atur kalender**. Pada **Template kerja** daftar drop-down, pilih **Default jam kerja** template atau template lain dengan sumber daya template yang benar. Saat Anda membuka papan jadwal, Anda dapat melihat bahwa sumber daya sekarang telah memperbarui jam kerja.

> [!div class="mx-imgBorder"]
> ![Tangkapan layar Sumber Daya yang Dapat Dipesan Aktif](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]