---
title: Menambahkan bidang kustom ke pengaturan harga dan entitas transaksi
description: Topik ini memberikan informasi tentang menambahkan bidang kustom ke pengaturan harga dan entitas transaksi.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: af2256e77c3ceeee9638f57d971137df1658687b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148467"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Menambahkan bidang kustom ke pengaturan harga dan entitas transaksi 

[!include [banner](../includes/psa-now-project-operations.md)]

Topik ini mengasumsikan bahwa anda telah menyelesaikan prosedur di topik, [membuat entitas dan bidang kustom](create-custom-fields-entities.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan selesaikan dan kemudian kembali ke topik ini. 

Dalam topik ini, prosedur akan menunjukkan cara menambahkan referensi bidang kustom yang diperlukan ke entitas dan elemen antarmuka pengguna (UI) seperti formulir dan tampilan.

## <a name="add-custom-pricing-dimension-fields"></a>Menambahkan bidang dimensi harga kustom 
Setelah bidang kustom dan entitas telah dibuat, langkah selanjutnya adalah membuat pengaturan harga dan entitas transaksi yang mengetahui entitas kustom atau rangkaian pilihan dengan membuat bidang referensi. Tergantung pada apakah daftar dimensi harga mencakup dimensi rangkaian pilihan atau dimensi entitas atau keduanya, ikuti hanya langkah di **dimensi harga kustom berbasis rangkaian pilihan** atau **Dimensi harga kustom berbasis entitas**, atau keduanya.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensi harga kustom berbasis rangkaian pilihan
Bila dimensi harga kustom adalah rangkaian pilihan, tambahkan sebagai bidang ke entitas Project Service penting. Dalam prosedur berikut , **lokasi kerja sumber daya** dan **jam kerja sumber daya** digunakan sebagai pilihan dimensi harga berbasis rangkaian pilihan. Ini harus terlebih dahulu ditambahkan sebagai bidang untuk entitas harga, **harga peran**, dan **markup harga peran**.

1. Dalam Project Service Automation, klik **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas > Harga Peran**.
3. Perluas entitas **Harga Peran**, lalu pilih **Bidang**.
4. Klik **baru** untuk membuat bidang baru yang disebut **lokasi kerja sumber daya** dan pilih **rangkaian pilihan** sebagai jenis bidang. 
5. Pilih **gunakan rangkaian pilihan yang ada**, pilih rangkaian pilihan **lokasi kerja sumber daya**, lalu klik **Simpan**.
6. Ulangi langkah 1-5 untuk menambahkan bidang ini ke entitas **markup harga peran**. 
7. Ulangi langkah 1-5 untuk rangkaian pilihan **jam kerja sumber daya**.

> [!IMPORTANT]
> Bila Anda menambahkan bidang ke lebih dari satu entitas, gunakan nama bidang yang sama di semua entitas. 

> ![Menambahkan lokasi kerja sumber daya ke harga peran](media/RWL-Field.png)

Dalam fase penjualan dan estimasi untuk suatu proyek, perkiraan upaya kerja yang diperlukan untuk menyelesaikan pekerjaan **lokal** dan **onsite**, di **jam reguler** dan **jam lembur**  digunakan untuk perkirakan nilai kuotasi/proyek. Bidang **lokasi kerja sumber daya** dan **jam kerja sumber daya** akan ditambahkan ke entitas estimasi, **detail baris kuotasi**, **detail baris kontrak**, **Tugas Proyek**, **anggota tim proyek**, dan **baris Estimasi**.

1. Di PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas > Detail Baris kuotasi**.
3. Perluas entitas **detail baris kuotasi**, dan pilih **bidang**.
4. Klik **baru** untuk membuat bidang baru yang disebut **lokasi kerja sumber daya** dan pilih jenis bidang, **rangkaian pilihan**. 
5. Pilih **gunakan rangkaian pilihan yang ada** dan **lokasi kerja sumber daya**, lalu klik **Simpan**.
6. Ulangi langkah 1-5 untuk menambahkan bidang ini ke **detail baris kontrak proyek**,**Tugas Proyek**, **anggota tim proyek**, dan entitas **baris Estimasi**.
7. Ulangi langkah 1-6 untuk rangkaian pilihan **jam kerja sumber daya**. 

> ![Menambahkan lokasi kerja sumber daya ke baris perkiraan](media/RWL-Default-Value.png)


Untuk pengiriman dan faktur, pekerjaan yang diselesaikan harus dengan harga akurat untuk memilih apakah dilakukan **lokal** atau **onsite**, dan apakah selesai selama **jam reguler** atau **lembur** pada aktual proyek. Bidang **lokasi kerja sumber daya** dan **jam kerja sumber daya** akan ditambahkan ke entitas **entri waktu**, **aktual**, **detail baris faktur**, dan **baris jurnal**.

1. Di PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**.
2. Di penelusur solusi, di panel navigasi kiri, pilih  **Entitas > Entri waktu**.
3. Perluas entitas **detail baris kuotasi**, kemudian pilih **bidang**.
4. Klik **baru** untuk membuat bidang baru yang disebut **lokasi kerja sumber daya** dan pilih **rangkaian pilihan** sebagai jenis bidang. 
5. Pilih **gunakan rangkaian pilihan yang ada**, pilih rangkaian pilihan **lokasi kerja sumber daya**, lalu klik **Simpan**.
6. Ulangi langkah 1-5 untuk menambahkan bidang ini ke entitas baris **aktual**, **detail baris faktur**, dan **baris jurnal**.
7. Ulangi langkah 1-6 untuk rangkaian pilihan **jam kerja sumber daya**. 

> ![Menambahkan lokasi kerja sumber daya ke Entri waktu](media/RWL-time-entry.png)

Ini melengkapi perubahan skema yang diperlukan untuk dimensi kustom berbasis rangkaian pilihan.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensi harga kustom berbasis entitas

Bila dimensi harga kustom adalah entitas, anda akan menambahkan Relasi 1:N antara entitas dimensi dan entitas Project Service utama. Menggunakan contoh jabatan standar dari atas, masuk akal untuk mengharapkan bahwa setiap karyawan ditetapkan jabatan standar. Hasil SAs, Anda akan memerlukan relasi 1:N dari jabatan standar menjadi sumber daya yang dapat dipesan, atau relasi N:1 jika dibuat dari sumber daya yang dapat dipesan ke jabatan standar.

1. Di PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**. 
2. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas > Jabatan Standar**.
3. Perluas entitas **jabatan standar** dan pilih **Relasi 1:N**.
4. Klik **baru** untuk membuat relasi 1: N baru yang disebut **jabatan standar ke sumber daya yang dapat dipesan**. Masukkan informasi yang diperlukan dan kemudian klik **Simpan**.

> ![Menambahkan jabatan standar sebagai bidang referensi untuk sumber daya yang dapat dipesan](media/ST-BR.png)

Jabatan stAndar juga harus ditambahkan ke entitas harga project service, **harga peran**, dan **markup harga peran**. Ini juga diselesaikan menggunakan Relasi 1: N antara entitas **jabatan standar** dan entitas **harga peran** serta entitas **jabatan standar** dan **Markup harga peran**.

1. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas > Jabatan Standar**.
2. Perluas entitas **jabatan standar** dan pilih **Relasi 1:N**.
3. Klik **baru** untuk membuat relasi 1: N baru yang disebut **jabatan standar ke Harga Peran**. Masukkan informasi yang diperlukan dan kemudian klik **Simpan**.
4. Ulangi langkah 1-4 untuk membuat Relasi 1: N antara entitas **jabatan standar** dan **Markup harga peran**,

Dalam tahapan penjualan dan estimasi untuk proyek, untuk harga kuotasi/proyek, perkiraan upaya kerja diperlukan untuk setiap jabatan standar. Ini berarti bahwa Relasi 1: N dari jabatan standar untuk masing-masing entitas estimasi dalam Project Service diperlukan: 

- **Rincian Baris Kuotasi**
- **Detail Baris Kontrak Proyek**
- **Tugas Proyek**
- **Anggota Tim Proyek**
- **Baris Perkiraan**

5. Ulangi langkah 1-5 untuk membuat Relasi 1: N dari **jabatan standar** ke **detail baris kuotasi**, **detail baris kontrak proyek**, **Tugas Proyek**, **anggota tim proyek**, dan **Baris Estimasi**.

> ![Menambahkan jabatan standar sebagai bidang referensi untuk baris estimasi](media/ST-Estimate-Line.png)

Dalam fase pengiriman dan faktur, pekerjaan yang diselesaikan oleh setiap jabatan standar harus dengan harga yang akurat pada aktual proyek. Ini berarti bahwa harus ada Relasi 1: N dari **jabatan standar** ke **entri waktu**, **aktual**, **Rincian baris faktur**, dan **entitas baris jurnal**.

6. Ulangi langkah 1-6 untuk membuat Relasi 1: N dari **jabatan standar** ke **entri waktu**, **aktual**, **Rincian baris faktur**, dan **entitas baris jurnal**.

> ![Menambahkan jabatan standar sebagai bidang referensi untuk entri waktu](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Konfigurasikan nilai dimensi default dengan menggunakan fitur pemetaan platform
Untuk entri waktu, akan sangat membantu untukmemiliki sistem default jabatan standar pada entri waktu dari sumber daya dapat dipesan yang merekam entri waktu. Gunakan langkah berikut untuk menambahkan pemetaan bidang pada relasi 1: N dari **sumber daya yang dapat dipesan** ke **entri waktu**.

1. Di penelusur solusi, di panel navigasi kiri, pilih **Entitas > Jabatan Standar**.
2. Perluas entitas **jabatan standar** dan pilih **Relasi 1:N**.
3. Klik dua kali **sumber daya yang dapat dipesan ke entri waktu**. Pada halaman **relasi**, klik **gunakan pemetaan bidang**. 
4. Klik **baru** untuk membuat pemetaan bidang baru antara bidang **jabatan standar** pada entitas **sumber daya yang dapat dipesan** ke bidang referensi **jabatan standar** pada entitas **entri waktu**. 

> ![Konfigurasi Pemetaan bidang untuk memungkinkan default jabatan standar dari sumber dapat dipesan ke entri waktu](media/ST-Mapping2.png)


Ini melengkapi perubahan skema yang diperlukan untuk dimensi kustom berbasis entitas.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Menambahkan bidang kustom ke formulir, tampilan, dan aturan bisnis

Setelah Anda membuat semua perubahan skema yang diperlukan, langkah selanjutnya adalah membuat bidang terlihat di UI dengan menambahkan bidang ke formulir dan tampilan.

1. Buka formulir atau tampilan. Di panel navigasi kanan, pilih bidang dan tarik pada ke kanvas formulir. 
2. Jika Anda mengedit tampilan, gunakan panel navigasi kanan, klik **Tambah bidang**, dan di kotak dialog **daftar bidang**, pilih bidang yang Anda butuhkan, lalu klik **OK**.

Tabel berikut ini memberikan daftar lengkap dari tampilan dan formulir bawaan, menurut entitas, yang perlu diperbarui dengan bidang baru. Jika Anda memiliki tampilan tambahan atau formulir dalam penyesuaian Anda pada entitas tersebut, tambahkan bidang baru ke bidang tersebut juga.

| Entitas Project Service        | Formulir yang memerlukan bidang baru   |Tampilan yang memerlukan bidang baru      |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peran|• Informasi |• Harga Kategori Sumber Daya Aktif<br> • Tampilan Terkait Harga Kategori Sumber Daya|
|  Markup Harga Peran|• Informasi|• Markup Harga Peran Aktif<br>• Tampilan Terkait Markup Harga Peran|
|  Rincian baris kuotasi|• Informasi Proyek<br>• Pembuatan Cepat Proyek|• Rincian Baris Kuotasi Aktif<br>• Gabungan Rincian Baris Kuotasi<br>• Tampilan Terkait Rincian Baris Kuotasi|
|  Rincian Baris Kontrak Proyek|• Informasi Proyek<br>• Pembuatan Cepat Proyek|• Rincian Baris Kontrak Gabungan<br>• Rincian Baris Kontrak Aktif<br>• Tampilan Terkait Rincian Baris Kontrak|
|  Tugas Proyek|• Informasi<br>• Formulir Baru||
|  Anggota Tim Proyek|• Informasi<br>• Formulir Baru|• Anggota Tim Proyek Aktif<br>• Anggota Tim Proyek<br>• Tampilan Terkait Anggota Tim Proyek|
|  Entri Waktu|• Informasi<br>• Buat Entri Waktu|• Entri Waktu Saya Menurut Tanggal<br>• Entri Waktu Saya untuk pekan Ini<br>• Entri waktu untuk persetujuan|
|  Lini Jurnal|• Informasi<br>• Buat Cepat|• Lini Jurnal Aktif<br>• Tampilan Terkait Lini Jurnal|
|  Rincian Baris Faktur|• Informasi<br>• Buat Cepat|• Rincian Baris Faktur Aktif<br>• Transaksi Faktur Kena Biaya<br>• Transaksi Faktur Gratis<br>• Tampilan Terkait Rincian Baris Faktur<br>• Transaksi Faktur Tidak Kena Biaya|
|  Aktual|• Informasi<br>• Aktual Aktif|• Tampilan Terkait Aktual|

Bidang kustom juga mungkin harus ditambahkan pada aturan Bisnis, tergantung pada yang Anda tentukan. Satu instans Bawaan adalah untuk **editabilitas aturan bisnis dari entri waktu berdasarkan status**. Aturan ini menentukan bidang yang harus dikunci saat entri waktu berada dalam status tidak dapat diedit seperti **disetujui**. Tambahkan bidang ke aturan bisnis ini sehingga bidang terkunci untuk diedit saat entri waktu berada dalam status selain **draf** atau **Dikembalikan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]