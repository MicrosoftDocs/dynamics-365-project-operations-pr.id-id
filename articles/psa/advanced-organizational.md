---
title: Unit Organisasi
description: Topik ini menyediakan informasi tentang unit organisasi di Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 755eee6ab9993c72ff1db46e0993527ac0826bfe
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130627"
---
# <a name="organizational-units"></a>Unit Organisasi 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, unit organisasi adalah grup atau divisi berbeda di perusahaan layanan profesional yang menggunakan sumber daya dapat ditagih yang memiliki tingkat biaya.

Untuk perusahaan layanan profesional yang menggunakan sumber daya teknis di berbagai area praktik atau lini bisnis, biaya untuk mengisi peran di satu area praktik atau lini bisnis mungkin berbeda dari biaya untuk mengisi peran di area praktik atau lini bisnis lainnya. Unit organisasi konsep membantu dalam skenario ini dengan menyediakan cara untuk mengelompokkan sekumpulan peran yang dapat ditagih dalam divisi dari perusahaan yang memiliki struktur biaya yang berbeda untuk peran ini.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Atribut kunci dan Asosiasi unit organisasi

Dalam PSA, unit organisasi dalam PSA memiliki mata uang spesifik dan daftar harga biaya tertentu.

Mata uang unit organisasi adalah mata uang utama yang digunakan untuk melacak biaya.

Satu atau beberapa daftar harga biaya dapat dilampirkan ke setiap unit organisasi. PSA menempatkan batasan berikut pada daftar harga yang dapat dilampirkan ke unit organisasi:

- Daftar harga harus dalam mata uang unit organisasi
- Daftar harga harus dari daftar harga biaya

Selain itu, ada atribut untuk unit organisasi pada entitas sumber daya. Setiap sumber daya dapat ditetapkan ke satu unit organisasi.

## <a name="roles-of-organizational-units"></a>Peran Unit Organisasi

Unit organisasi memainkan dua peran dalam PSA:

- **Unit kontrak** – unit organisasi yang mewakili grup perusahaan atau divisi yang terutama bertanggung jawab untuk memenangkan penjualan dan mengelola pengiriman pekerjaan dan layanan kepada pelanggan. Unit kontrak diidentifikasi oleh bidang **unit kontrak** di bagian header **peluang**, **kuotasi**, **kontrak proyek**, dan halaman **proyek**.
- **Unit sumber daya** - unit organisasi yang memiliki atau ditetapkan sumber daya. Unit organisasi ini dapat menyediakan sumber daya untuk beberapa peran pada pernyataan kerja (SOW) dan proyek yang dimiliki oleh unit kontrak.

> ![Unit kontrak dan unit sumber daya](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Tanya-Jawab Unit Organisasi

Berikut adalah beberapa pertanyaan yang paling sering diajukan tentang unit organisasi.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Bagaimana keterkaitan entitas unit organisasi di PSA dengan entitas organisasi yang sudah ada di Dynamics 365?

Entitas organisasi di Microsoft Dynamics 365 mewakili nama instans Dynamics 365 global. Nama ini biasanya adalah nama perusahaan global.

Entitas unit organisasi mewakili grup atau divisi di perusahaan global. Grup atau divisi ini memiliki seperangkat peran dan daftar harga biaya untuk peran tersebut, dan peran serta daftar harga berbeda dari peran dan daftar harga grup atau divisi lain di perusahaan.

Bila PSA diinstal, unit organisasi default dibuat berdasarkan organisasi. Semua sumber daya yang ada ditetapkan ke unit organisasi default. Jika pengguna direktori aktif atau sumber daya baru diimpor ke Dynamics 365, proses impor pengguna menetapkan mereka ke unit organisasi default di PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Apa perbedaan entitas unit organisasi dengan entitas unit bisnis?

Di Dynamics 365, entitas unit bisnis adalah konstruk keamanan. Asosiasi pengguna dengan unit bisnis menentukan entitas dan rekaman entitas yang dapat diakses pengguna. Ia juga menentukan izin (buat, baca, tulis, Hapus, lampirkan, Lampirkan ke, tetapkan, atau bagikan) yang dimiliki pengguna untuk rekaman entitas tersebut.

Entitas unit organisasi mewakili grup perusahaan atau divisi yang memiliki tingkat biaya yang berbeda untuk karyawan yang ditetapkan untuknya. Asosiasi sumber daya dengan unit organisasi menentukan biaya sumber daya untuk keterlibatan proyek.

Bila Anda menerapkan Dynamics 365, Optimalkan otorisasi keamanan untuk hierarki unit bisnis dan penetapan pengguna ke unit bisnis. Tetapkan semua pengguna yang biasanya harus mengakses kumpulan rekaman yang sama ke unit bisnis yang sama. Unit organisasi tidak berpengaruh pada otorisasi keamanan atau akses.

#### <a name="example-of-organizational-units-and-business-units"></a>Contoh unit organisasi dan unit bisnis

Aswono, Ltd. memiliki praktik Teknologi Microsoft yang berkembang. Panji dan Nirmala adalah pengembang C\#, namun Nirmala berada di Amerika Serikat, sedangkan Panji berada di India. Sebagian besar keterlibatan proyek memerlukan sumber daya dari Aswono India dan Aswono US, dan Panji serta Nirmala memerlukan tingkat keamanan akses yang sama ke proyek di area praktik ini. Namun, biaya pengembang dari Aswono India berbeda secara signifikan dari biaya pengembang dari Aswono US.

Berikut adalah cara optimal untuk merancang skenario ini menggunakan Dynamics 365 dan PSA.

1. Buat praktik Teknologi Microsoft sebagai unit bisnis, dan kaitkan Panji dan Nirmala dengannya. Dengan cara ini, Anda membantu menjamin bahwa karyawan memiliki tingkat keamanan akses yang sama ke setiap proyek di area praktik tersebut. Mereka berdua akan dapat memeriksa kemajuan dan waktu laporan, pengeluaran, dan pembaruan tugas. 
2. Buat dua unit organisasi untuk membantu menjamin bahwa biaya untuk proyek tercermin dengan benar. 
3. Kaitkan Nirmala dengan Aswono US dan kaitkan Panji dengan Aswono India.
4. Tetapkan daftar harga biaya yang sesuai ke kedua unit organisasi. Dengan dengan cara ini, Anda membantu menjamin bahwa biaya yang tercatat pada proyek untuk Panji dan Nirmala secara akurat mencerminkan selisih biaya antara Aswono US dan Aswono India.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Apakah unit organisasi terkait dengan wilayah penjualan di Dynamics 365?

Tidak ada keterkaitan atau relasi antara wilayah penjualan dan unit organisasi. Wilayah penjualan biasanya merupakan area geografis tempat penjualan terjadi. Daftar harga penjualan dapat dikaitkan dengan setiap wilayah penjualan.

Unit organisasi adalah grup internal atau divisi di perusahaan yang melacak biaya untuk sekumpulan peran yang mereka Jual ke divisi lain atau ke pelanggan eksternal.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Contoh unit organisasi dan unit bisnis dan wilayah penjualan

Aswono, Ltd memiliki dua pusat pengembangan: Aswono US dan Aswono India. Biaya sumber daya sangat berbeda antara dua pusat pengembangan ini.

Aswono menjual layanan TI di banyak pasar internasional, seperti Amerika Latin, Amerika Utara, Asia-Pasifik, Eropa Barat, dan Timur Tengah. Tarif tagihan untuk peran proyek yang sama dapat berbeda secara luas di pasar ini.

Aswono AS dan Aswono India harus diatur sebagai unit organisasi, dan setiap unit organisasi harus memiliki daftar harga biaya sendiri. Asia-Pasifik, Amerika Latin, Amerika Utara, Eropa Barat, dan Timur Tengah harus disiapkan sebagai wilayah penjualan, dan masing-masing wilayah penjualan harus memiliki daftar harga penjualan sendiri.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Mengapa ada pembatasan pada Asosiasi daftar harga dengan unit organisasi? 

Harga penjualan biasanya unik untuk area geografis atau pasar di mana Layanan dijual. Divisi internal perusahaan biasanya tidak memiliki harga penjualan mereka sendiri untuk jenis layanan yang sama. Namun, Divisi internal memiliki biaya yang berbeda dari barang yang dijual (COGS), tergantung pada keterampilan orang yang mereka pekerjakan dan kondisi kerja di kawasan di mana mereka beroperasi. Karena unit organisasi dimodelkan sebagai divisi internal perusahaan, mereka hanya dapat memiliki daftar harga biaya.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Mengapa kita tidak dapat mengaitkan daftar harga penjualan ke unit organisasi?

Dalam PSA, daftar harga penjualan dapat dikaitkan dengan pelanggan dan wilayah penjualan. Entitas transaksional seperti peluang, kuotasi, kontrak proyek, dan proyek menggunakan daftar harga penjualan yang dilampirkan ke akun pelanggan atau wilayah penjualan untuk menentukan tingkat tagihan dan potensi pendapatan pada keterlibatan proyek.

Daftar harga biaya dikaitkan dengan unit organisasi. Entitas transaksional seperti peluang, kuotasi, kontrak proyek, dan proyek menggunakan daftar harga biaya yang dilampirkan ke unit kontrak untuk menentukan biaya ke keterlibatan proyek.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Apakah unit organisasi bersifat hierarkis dalam PSA?

Tidak. Dalam rilis PSA saat ini, unit organisasi tidak hierarkis. Ini berarti bahwa Anda tidak dapat:

- Mengonfigurasikan pola untuk harga biaya default yang melintas ke atas hierarki. 
- Melaporkan pendapatan atau biaya yang diakumulasikan pada tingkat yang berbeda dari hierarki unit organisasi.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Kami adalah perusahaan multinasional besar dengan hierarki bertingkat kompleks dari pusat biaya, divisi, dan kantor penagihan. Bagaimana cara membuat penggunaan terbaik dari konsep unit organisasi dalam versi aplikasi Project Service ini?

Bila Anda memiliki hierarki kompleks Pusat biaya, divisi, kantor penagihan, dll., konfigurasikan node leaf hierarki tersebut sebagai unit organisasi yang berbeda.
Contoh berikut menunjukkan hierarki pada umumnya:

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
 
Jika hierarki serupa, Anda harus mengaturnya sebagai daftar datar, seperti ditunjukkan di sini:
- Aswono India-Praktik SAP-konsultan teknis 
- Aswono India-Praktik SAP-konsultan Fungsional       
- Aswono India-Praktik Teknologi Microsoft-konsultan Fungsional 
- Aswono India-Praktik Teknologi Microsoft-konsultan Fungsional 
- Aswono AS-Praktik SAP-konsultan teknis  
- Aswono AS-Praktik SAP-konsultan Fungsional  
- Aswono AS-Praktik Teknologi Microsoft-konsultan Teknis 
- Aswono AS-Praktik Teknologi Microsoft-konsultan Fungsional

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Kami adalah perusahaan layanan profesional kecil yang beroperasi hanya sebagai satu divisi. Bagaimana cara terbaik menggunakan konsep unit organisasi dalam versi PSA saat ini?

Jika perusahaan Anda beroperasi sebagai satu unit yang memiliki satu daftar harga biaya, Anda tidak perlu mengkonfigurasi unit organisasi apa pun. Selama penginstalan PSA, Dynamics 365 membuat satu unit organisasi default yang memiliki nama sama dengan organisasi. Secara default, semua sumber daya ditetapkan ke unit organisasi ini. Bila sistem memerlukan unit organisasi untuk dipilih, unit organisasi ini dipilih secara default.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Saat proyek dibuat dari baris kuotasi atau kontrak proyek, unit kontrak default berasal dari kuotasi atau kontrak proyek. Jika proyek dibuat sebelum entitas penjualan seperti kuotasi atau kontrak proyek, apa unit kontrak default-nya?

Saat proyek dibuat sendiri, unit kontrak default dari proyek didasarkan pada pengguna yang membuatnya. Pengguna tersebut juga merupakan manajer proyek default. Jika proyek dipetakan ke entitas penjualan seperti kuotasi atau kontrak proyek, unit kontrak pada proyek didasarkan pada entitas penjualan sebagai gantinya. Dalam kasus ini, perkiraan proyek dapat dihitung ulang, karena daftar harga biaya digunakan untuk menghitung perubahan perkiraan biaya jika unit kontrak diubah. Daftar harga penjualan digunakan untuk menghitung perkiraan penjualan yang akan diubah sehingga mereka tersinkronisasi dengan daftar harga proyek pada kuotasi.

Bidang **unit kontrak** dan **mata uang** pada proyek dikunci dan tidakbisa diedit, karena harus diselaraskan dengan nilai pada entitas penjualan (kuotasi atau kontrak proyek) yang dipetakan ke proyek.
