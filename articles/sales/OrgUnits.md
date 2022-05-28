---
title: Unit organisasi
description: Ini topik menjelaskan konsep unit organisasi, dan menjelaskan cara membuat dan memelihara unit organisasi di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581380"
---
# <a name="organizational-units-overview"></a>Gambaran umum unit organisasi

Di Microsoft Dynamics 365 Project Operations, *unit* organisasi adalah kelompok atau divisi yang berbeda dalam perusahaan jasa profesional yang menggunakan sumber daya yang dapat ditagih yang memiliki tarif biaya.

Untuk perusahaan jasa profesional yang menggunakan sumber daya teknis di berbagai bidang praktik atau lini bisnis, biaya untuk mengisi peran dapat bervariasi, tergantung pada area praktik atau lini bisnis tempat peran tersebut diisi. Dalam skenario ini, konsep unit organisasi membantu dengan menyediakan cara untuk mengelompokkan satu set peran yang dapat ditagih dalam divisi perusahaan yang memiliki struktur biaya yang berbeda untuk peran tersebut.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Konsep unit organisasi dalam Operasi Proyek

Dalam Operasi Proyek, unit organisasi memiliki mata uang tertentu dan daftar harga biaya tertentu.

Mata uang unit organisasi adalah mata uang utama yang digunakan untuk melacak biaya.

Satu atau beberapa daftar harga biaya dapat dilampirkan ke setiap unit organisasi. Operasi Proyek menempatkan batasan berikut pada daftar harga yang dapat dilampirkan ke unit organisasi:

- Daftar harga harus dalam mata uang unit organisasi.
- Daftar harga harus berupa daftar harga biaya.

Selain itu, entitas Sumber Daya menyertakan atribut untuk unit organisasi. Setiap sumber daya dapat ditetapkan ke satu unit organisasi.

### <a name="roles-of-organizational-units"></a>Peran Unit Organisasi

Unit organisasi memainkan dua peran dalam Operasi Proyek:

- **Unit kontrak** – unit organisasi yang mewakili grup perusahaan atau divisi yang terutama bertanggung jawab untuk memenangkan penjualan dan mengelola pengiriman pekerjaan dan layanan kepada pelanggan. Unit kontrak diidentifikasi oleh bidang **unit kontrak** di bagian header **peluang**, **kuotasi**, **kontrak proyek**, dan halaman **proyek**.
- **Unit sumber daya** - unit organisasi yang memiliki atau ditetapkan sumber daya. Unit organisasi ini dapat menyediakan sumber daya untuk beberapa peran pada pernyataan kerja (SOW) dan proyek yang dimiliki oleh unit kontrak.

![Unit kontrak dan unit sumber daya.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>FAQ unit organisasi

Berikut adalah beberapa pertanyaan yang paling sering diajukan tentang unit organisasi.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Bagaimana entitas Unit Organisasi dalam Operasi Proyek terkait dengan entitas Organisasi yang sudah ada di Dynamics 365?

Entitas Organisasi di Dynamics 365 mewakili nama instans Dynamics 365 global. Nama ini biasanya adalah nama perusahaan global.

Entitas unit organisasi mewakili grup atau divisi di perusahaan global. Grup atau divisi ini memiliki seperangkat peran dan daftar harga biaya untuk peran tersebut, dan peran serta daftar harga berbeda dari peran dan daftar harga grup atau divisi lain di perusahaan.

Saat Operasi Proyek diinstal, unit organisasi default dibuat berdasarkan organisasi. Semua sumber daya yang ada ditetapkan ke unit organisasi default. Jika ada pengguna atau sumber daya Active Directory baru yang diimpor ke Dynamics 365, proses impor pengguna menetapkannya ke unit organisasi default dalam Operasi Proyek.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Bagaimana entitas Unit Organisasi berbeda dari entitas Unit Bisnis?

Di Dynamics 365, entitas unit bisnis adalah konstruk keamanan. Asosiasi pengguna dengan unit bisnis menentukan entitas dan rekaman entitas yang dapat diakses pengguna. Ia juga menentukan izin (buat, baca, tulis, Hapus, lampirkan, Lampirkan ke, tetapkan, atau bagikan) yang dimiliki pengguna untuk rekaman entitas tersebut.

Entitas unit organisasi mewakili grup perusahaan atau divisi yang memiliki tingkat biaya yang berbeda untuk karyawan yang ditetapkan untuknya. Asosiasi sumber daya dengan unit organisasi menentukan biaya sumber daya untuk keterlibatan proyek.

Bila Anda menerapkan Dynamics 365, Optimalkan otorisasi keamanan untuk hierarki unit bisnis dan penetapan pengguna ke unit bisnis. Tetapkan semua pengguna yang biasanya harus mengakses kumpulan rekaman yang sama ke unit bisnis yang sama. Unit organisasi tidak berpengaruh pada otorisasi keamanan atau akses.

**Contoh yang menunjukkan satu potensi perbedaan dalam pemodelan unit organisasi dan unit bisnis**

Aswono, Ltd. memiliki praktik Teknologi Microsoft yang berkembang. Panji dan Nirmala adalah pengembang C\#, namun Nirmala berada di Amerika Serikat, sedangkan Panji berada di India. Sebagian besar keterlibatan proyek membutuhkan sumber daya dari Contoso India dan Contoso AS, dan Prakash dan Tricia memerlukan tingkat akses keamanan yang sama ke proyek-proyek di area praktik ini. Namun, biaya pengembang dari Aswono India berbeda secara signifikan dari biaya pengembang dari Aswono US.

Berikut adalah cara optimal untuk merancang skenario ini dengan menggunakan Dynamics 365 dan Project Operations.

1. Buat praktik Teknologi Microsoft sebagai unit bisnis, dan kaitkan Panji dan Nirmala dengannya. Dengan cara ini, Anda membantu memastikan bahwa kedua karyawan memiliki tingkat akses keamanan yang sama ke proyek apa pun di area praktik tersebut. Keduanya akan dapat memeriksa kemajuan dan melaporkan waktu, biaya, penggunaan material, dan pembaruan tugas.
2. Buat dua unit organisasi untuk membantu memastikan bahwa biaya untuk proyek tercermin dengan benar.
3. Kaitkan Tricia dengan Contoso AS dan Prakash dengan Contoso India.
4. Tetapkan daftar harga biaya yang sesuai ke kedua unit organisasi. Dengan cara ini, Anda membantu memastikan bahwa biaya yang dicatat pada proyek untuk Prakash dan Tricia secara akurat mencerminkan perbedaan biaya antara Contoso AS dan Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Apakah unit organisasi terkait dengan wilayah penjualan di Dynamics 365?

Tidak ada keterkaitan atau relasi antara wilayah penjualan dan unit organisasi. Wilayah penjualan biasanya merupakan area geografis tempat penjualan terjadi. Daftar harga penjualan dapat dikaitkan dengan setiap wilayah penjualan.

Unit organisasi adalah grup internal atau divisi di perusahaan yang melacak biaya untuk sekumpulan peran yang mereka Jual ke divisi lain atau ke pelanggan eksternal.

**Contoh yang menunjukkan satu perbedaan potensial dalam pemodelan unit organisasi dan wilayah penjualan**

Aswono, Ltd memiliki dua pusat pengembangan: Aswono US dan Aswono India. Biaya sumber daya sangat berbeda antara kedua pusat pengembangan ini. Contoso menjual layanan teknologi informasi (TI) di banyak pasar internasional, seperti Amerika Latin, Amerika Utara, Asia-Pasifik, Eropa Barat, dan Timur Tengah. Tarif tagihan untuk peran proyek yang sama dapat berbeda secara luas di pasar ini. Aswono AS dan Aswono India harus diatur sebagai unit organisasi, dan setiap unit organisasi harus memiliki daftar harga biaya sendiri. Asia-Pasifik, Amerika Latin, Amerika Utara, Eropa Barat, dan Timur Tengah harus disiapkan sebagai wilayah penjualan, dan masing-masing wilayah penjualan harus memiliki daftar harga penjualan sendiri.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Mengapa ada pembatasan pada Asosiasi daftar harga dengan unit organisasi?

Harga penjualan biasanya unik untuk area geografis atau pasar di mana Layanan dijual. Divisi internal perusahaan biasanya tidak memiliki harga penjualan mereka sendiri untuk jenis layanan yang sama. Namun, Divisi internal memiliki biaya yang berbeda dari barang yang dijual (COGS), tergantung pada keterampilan orang yang mereka pekerjakan dan kondisi kerja di kawasan di mana mereka beroperasi. Karena unit organisasi dimodelkan sebagai divisi internal perusahaan, mereka hanya dapat memiliki daftar harga biaya.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Mengapa kita tidak dapat mengaitkan daftar harga penjualan dengan unit organisasi?

Dalam Operasi Proyek, daftar harga penjualan dapat dikaitkan dengan pelanggan dan wilayah penjualan. Entitas transaksional seperti Peluang, Penawaran, Kontrak Proyek, dan Proyek menggunakan daftar harga penjualan yang dilampirkan ke akun pelanggan atau wilayah penjualan untuk menentukan tarif tagihan dan potensi pendapatan untuk keterlibatan proyek.

Daftar harga biaya dikaitkan dengan unit organisasi. Entitas transaksional seperti Peluang, Penawaran, Kontrak Proyek, dan Proyek menggunakan daftar harga biaya yang dilampirkan ke unit kontraktor untuk menentukan biaya untuk keterlibatan proyek.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Apakah unit organisasi hierarki dalam Operasi Proyek?

Tidak. Dalam rilis Operasi Proyek saat ini, unit organisasi tidak hierarki. Oleh karena itu, Anda tidak dapat melakukan tugas-tugas berikut:

- Konfigurasikan pola untuk memasukkan harga biaya default yang melintasi hierarki.
- Melaporkan pendapatan atau biaya yang digulung pada tingkat hierarki unit organisasi yang berbeda.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kami adalah perusahaan multinasional besar yang memiliki hierarki pusat biaya, divisi, dan kantor penagihan yang kompleks dan bertingkat. Bagaimana kita bisa menggunakan konsep unit organisasi dengan sebaik-baiknya dalam versi Operasi Proyek saat ini?

Ketika Anda memiliki hierarki kompleks pusat biaya, divisi, kantor penagihan, dan sebagainya, siapkan simpul daun hierarki itu sebagai unit organisasi yang berbeda.

Contoh berikut menunjukkan hierarki tipikal.

**Aswono India**

- Praktek SAP

    - Konsultan teknis
    - Konsultan fungsional

- Praktik Teknologi Microsoft

    - Konsultan teknis
    - Konsultan fungsional

**Contoso AS**

- Praktek SAP

    - Konsultan teknis
    - Konsultan fungsional

- Praktik Teknologi Microsoft

    - Konsultan teknis
    - Konsultan fungsional

Jika hierarki Anda menyerupai contoh ini, Anda harus mengaturnya sebagai daftar datar, seperti yang ditunjukkan di sini:

- Aswono India-Praktik SAP-konsultan teknis
- Aswono India-Praktik SAP-konsultan Fungsional
- Aswono India-Praktik Teknologi Microsoft-konsultan Fungsional
- Aswono India-Praktik Teknologi Microsoft-konsultan Fungsional
- Aswono AS-Praktik SAP-konsultan teknis
- Aswono AS-Praktik SAP-konsultan Fungsional
- Aswono AS-Praktik Teknologi Microsoft-konsultan Teknis
- Aswono AS-Praktik Teknologi Microsoft-konsultan Fungsional

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kami adalah perusahaan layanan profesional kecil yang beroperasi hanya sebagai satu divisi. Bagaimana kita bisa menggunakan konsep unit organisasi dengan sebaik-baiknya dalam versi Operasi Proyek saat ini?

Jika perusahaan Anda beroperasi sebagai satu unit yang memiliki satu daftar harga biaya, Anda tidak perlu mengkonfigurasi unit organisasi apa pun. Instalasi Operasi Proyek membuat satu unit organisasi default yang memiliki nama yang sama dengan organisasi. Secara default, semua sumber daya ditetapkan ke unit organisasi ini. Bila sistem memerlukan unit organisasi untuk dipilih, unit organisasi ini dipilih secara default.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Saat proyek dibuat dari baris kuotasi atau kontrak proyek, unit kontrak default berasal dari kuotasi atau kontrak proyek. Apa itu unit kontrak default jika proyek dibuat sebelum entitas penjualan seperti Penawaran atau Kontrak Proyek?

Saat proyek dibuat sendiri, unit kontrak default dari proyek didasarkan pada pengguna yang membuatnya. Pengguna tersebut juga merupakan manajer proyek default. Jika proyek dipetakan ke entitas penjualan seperti penawaran atau kontrak proyek, unit kontraktor proyek didasarkan pada entitas penjualan sebagai gantinya. Dalam kasus ini, perkiraan proyek dapat dihitung ulang, karena daftar harga biaya digunakan untuk menghitung perubahan perkiraan biaya jika unit kontrak diubah. Daftar harga jual digunakan untuk menghitung estimasi penjualan yang akan diubah sehingga sinkron dengan daftar harga proyek penawaran.

Bidang **Unit** Kontrak dan **Mata Uang** proyek dikunci untuk diedit, karena harus sinkron dengan nilai entitas penjualan (kutipan atau kontrak proyek) tempat proyek dipetakan.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Membuat dan memelihara unit organisasi dalam Operasi Proyek

Untuk membuat unit organisasi dalam Operasi Proyek, ikuti langkah-langkah berikut.

1. **Buka Pengaturan \> Unit** Organisasi.
2. Pilih **baru**.
3. Di **area Umum**, di **bidang Nama**, masukkan nama untuk unit organisasi. Kemudian atur bidang lainnya sesuai kebutuhan.
4. Pilih **Simpan** untuk membuat rekaman sehingga Anda dapat terus mengeditnya.
5. Di bawah **Daftar** Harga Biaya, pilih tanda plus (**+**) untuk menambahkan daftar harga. Anda hanya dapat menambahkan daftar harga yang memiliki konteks Biaya **di** sini.
6. **Di bidang Nama**, pilih tombol **Pencarian**, dan pilih daftar harga yang ingin Anda sediakan untuk unit organisasi. Terus tambahkan daftar harga sesuai kebutuhan.
7. Setelah selesai menambahkan daftar harga, pilih **Simpan** di sudut kanan bawah halaman.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
