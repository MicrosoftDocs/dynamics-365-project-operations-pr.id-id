---
title: Tingkatkan dari Project Service Automation ke Project Operations
description: Artikel ini memberikan gambaran umum tentang proses untuk meningkatkan dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686979"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Tingkatkan dari Project Service Automation ke Project Operations

Kami sangat senang mengumumkan fase kedua dari tiga fase untuk peningkatan dari Microsoft Dynamics 365 Project Service Automation ke Microsoft Dynamics 365 Project Operations. Artikel ini memberikan gambaran umum bagi pelanggan yang memulai perjalanan yang mengasyikkan ini. 

Program pengiriman peningkatan akan dibagi menjadi tiga fase.

| Tingkatkan pengiriman | Tahap 1 (Januari 2022) | Tahap 2 (November 2022) | Tahap 3 (Gelombang April 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Tidak ada ketergantungan pada struktur rincian kerja (WBS) untuk proyek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam batas Operasi Proyek yang saat ini didukung | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar batas Operasi Proyek yang saat ini didukung, termasuk dukungan untuk klien desktop Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Fitur proses peningkatan 

Sebagai bagian dari proses peningkatan, kami telah menambahkan log pemutakhiran ke peta situs untuk memungkinkan administrator mendiagnosis kegagalan dengan lebih mudah. Selain antarmuka baru, aturan validasi baru akan ditambahkan untuk memastikan integritas data setelah peningkatan. Validasi berikut akan ditambahkan ke proses peningkatan.

| Validasi | Tahap 1 (Januari 2022) | Tahap 2 (November 2022) | Tahap 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan divalidasi terhadap pelanggaran integritas data umum (misalnya, penugasan sumber daya yang terkait dengan tugas induk yang sama tetapi memiliki proyek induk yang berbeda). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi terhadap batas Project for the Web yang [diketahui](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi terhadap batas yang diketahui dari klien desktop Proyek. | |  | :heavy_check_mark: |
| Sumber daya yang dapat dipesan dan kalender proyek akan dievaluasi terhadap pengecualian aturan kalender umum yang tidak kompatibel. | | :heavy_check_mark: | :heavy_check_mark: |

Pada fase 2, pelanggan yang meningkatkan ke Operasi Proyek akan meningkatkan proyek mereka yang sudah ada ke pengalaman baca-saja untuk perencanaan proyek. Dalam pengalaman baca-saja ini, WBS lengkap akan terlihat di grid pelacakan. Untuk mengedit WBS, manajer proyek dapat memilih [**Konversi**](/PSA-Upgrade-Project-Conversion.md) di halaman utama proyek. Proses latar belakang kemudian memperbarui proyek sehingga mendukung pengalaman penjadwalan proyek baru dari Project for the Web. Fase ini sesuai untuk pelanggan yang memiliki proyek yang sesuai dengan batas Project for the Web [yang](/project-for-the-web/project-for-the-web-limits-and-boundaries) diketahui.

Pada fase 3, dukungan untuk klien desktop Project akan ditambahkan, untuk kepentingan pelanggan yang ingin terus mengedit proyek mereka dari aplikasi tersebut. Namun, jika proyek yang ada dikonversi ke proyek baru untuk pengalaman Web, akses ke add-in akan dinonaktifkan untuk setiap proyek yang dikonversi.

## <a name="prerequisites"></a>Prasyarat

Agar memenuhi syarat untuk peningkatan Fase 1, Anda harus memenuhi kriteria berikut:

- Lingkungan target tidak boleh berisi rekaman apa pun di **entitas msdyn_projecttask**.
- Lisensi Operasi Proyek yang valid harus ditetapkan ke semua pengguna aktif. 
- Anda harus memvalidasi proses peningkatan di setidaknya satu lingkungan non-produksi yang berisi himpunan data representatif yang selaras dengan lingkungan produksi Anda.
- Lingkungan target harus diperbarui ke Project Service Automation Update Release 37 (V3.10.58.120) atau yang lebih baru.

Agar memenuhi syarat untuk peningkatan Fase 2, Anda harus memenuhi kriteria berikut:

- Lisensi Operasi Proyek yang valid harus ditetapkan ke semua pengguna aktif. 
- Anda harus memvalidasi proses peningkatan di setidaknya satu lingkungan non-produksi yang berisi himpunan data representatif yang selaras dengan lingkungan produksi Anda.
- Lingkungan target harus diperbarui ke Project Service Automation Update Release 37 (V3.10.58.120) atau yang lebih baru.
- Lingkungan yang berisi tugas (msdyn_projecttask) hanya didukung jika jumlah total tugas per proyek adalah 500 atau kurang.

Prasyarat untuk Fase 3 akan diperbarui saat tanggal ketersediaan umum mendekat.

## <a name="licensing"></a>Lisensi

Jika Anda memiliki lisensi aktif untuk Project Service Automation, Anda dapat menginstal dan menggunakan Operasi Proyek, yang mencakup semua kemampuan Project Service Automation dan banyak lagi. Anda kemudian dapat menguji kemampuan Operasi Proyek di lingkungan terpisah saat Anda terus menggunakan Project Service Automation dalam produksi. Setelah lisensi Project Service Automation Anda kedaluwarsa, Anda harus beralih ke Operasi Proyek. Saat merencanakan transisi ini, Anda harus memperhitungkan fakta bahwa lisensi Project Operations tidak menyertakan lisensi Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Menguji dan memfaktor ulang kustomisasi

Sebagai titik awal, impor semua penyesuaian ke dalam lingkungan Operasi Proyek (Lite) yang bersih untuk mengonfirmasi bahwa impor berhasil, dan bahwa operasi bisnis berperilaku seperti yang diharapkan.

Berikut adalah beberapa hal yang harus diperhatikan:

- Impor mungkin gagal karena dependensi yang hilang. Dengan kata lain, bidang referensi penyesuaian atau komponen lain yang telah dihapus dalam Operasi Proyek. Dalam hal ini, hapus dependensi ini dari lingkungan pengembangan.
- Jika solusi yang tidak dikelola dan dikelola menyertakan komponen yang tidak disesuaikan, hapus komponen tersebut dari solusi. Misalnya, saat Anda menyesuaikan **entitas Proyek**, tambahkan hanya header entitas ke solusi Anda. Jangan tambahkan semua bidang. Jika sebelumnya Anda telah menambahkan semua subkomponen, Anda mungkin harus membuat solusi baru secara manual dan menambahkan komponen yang relevan ke dalamnya.
- Formulir dan tampilan mungkin tidak muncul seperti yang diharapkan. Dalam beberapa keadaan, jika Anda telah menyesuaikan salah satu formulir atau tampilan out-of-box, penyesuaian mungkin mencegah pembaruan baru dalam Operasi Proyek berlaku. Untuk mengidentifikasi masalah ini, kami sarankan Anda melakukan tinjauan berdampingan tentang instalasi operasi proyek yang bersih dan instalasi operasi proyek yang mencakup penyesuaian Anda. Bandingkan formulir yang paling umum digunakan dalam bisnis Anda untuk mengonfirmasi bahwa versi formulir Anda masih masuk akal dan tidak melewatkan sesuatu dari versi formulir yang bersih. Lakukan jenis peninjauan berdampingan yang sama untuk setiap tampilan yang telah Anda sesuaikan.
- Logika bisnis mungkin gagal saat runtime. Karena referensi ke bidang di plug-in Anda tidak divalidasi pada saat impor, logika bisnis mungkin gagal karena referensi ke bidang yang tidak ada lagi, dan Anda mungkin menerima pesan kesalahan yang menyerupai contoh berikut: "Entitas 'Proyek' tidak berisi atribut dengan Nama = 'msdyn_plannedhours' dan NameMapping = 'Logis'." Dalam hal ini, ubah penyesuaian Anda sehingga mereka menggunakan bidang baru. Jika Anda menggunakan kelas proxy yang dibuat secara otomatis dan referensi tipe yang kuat dalam logika plug-in Anda, pertimbangkan untuk meregenerasi proxy tersebut dari instalasi yang bersih. Dengan cara ini, Anda dapat dengan mudah mengidentifikasi semua tempat di mana plug-in Anda bergantung pada bidang yang tidak digunakan lagi.

Setelah Anda memperbarui penyesuaian untuk mengimpor Operasi Proyek dengan bersih, lanjutkan ke langkah berikutnya.

## <a name="end-to-end-testing-in-development-environments"></a>Pengujian ujung ke ujung di lingkungan pengembangan

### <a name="initiate-upgrade"></a>Memulai peningkatan 

1. Di Power Platform pusat admin, temukan dan pilih lingkungan Anda. Kemudian, di aplikasi, temukan dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Instal** untuk memulai pemutakhiran. Pusat Power Platform admin akan menyajikan instalasi ini sebagai instalasi baru. Namun, keberadaan versi Project Service Automation yang lebih lama akan terdeteksi, dan instalasi yang ada akan ditingkatkan.

    Setelah pemutakhiran selesai, lingkungan harus menunjukkan bahwa Operasi Proyek diinstal, dan bahwa Project Service Automation tidak diinstal.

    Bergantung pada jumlah data di lingkungan, peningkatan mungkin memakan waktu beberapa jam. Tim inti yang mengelola peningkatan harus merencanakan dengan tepat dan menjalankan peningkatan selama non-jam kerja. Dalam beberapa kasus, jika volume data besar, peningkatan harus dijalankan selama akhir pekan. Keputusan tentang penjadwalan harus didasarkan pada hasil pengujian di lingkungan yang lebih rendah.

3. Tingkatkan solusi kustom yang sesuai. Pada titik ini, sebarkan perubahan apa pun yang Anda buat pada penyesuaian Anda di bagian Kustomisasi [pengujian dan pemfaktoran ulang di](#testing-and-refactoring-customizations) artikel ini.
4. **Buka Solusi Pengaturan** \> **·**, dan pilih untuk menghapus instalan **solusi Komponen Usang** Operasi Proyek.

    Solusi ini adalah solusi sementara yang menyimpan model data dan komponen yang ada yang ada selama peningkatan. Dengan menghapus solusi ini, Anda menghapus semua bidang dan komponen yang tidak lagi digunakan. Dengan cara ini, Anda membantu menyederhanakan antarmuka dan membuat integrasi dan ekstensi lebih mudah.
    
### <a name="upgrade-to-project-operations-lite"></a>Tingkatkan ke Project Operations Lite

Langkah-langkah berikut menjelaskan proses pemutakhiran dan pengelogan kesalahan terkait:

1. **Pemeriksaan Versi PSA:** Untuk menginstal Operasi Proyek, Anda harus memiliki V3.10.58.120 atau yang lebih tinggi.
1. **Pra-validasi:** Saat administrator memulai peningkatan, sistem menjalankan operasi pra-validasi pada setiap entitas yang merupakan inti dari solusi Operasi Proyek. Langkah ini memverifikasi bahwa semua referensi entitas valid, dan memastikan bahwa data yang terkait dengan WBS berada dalam batas yang diterbitkan Project for the Web.
1. **Peningkatan metadata:** Setelah pra-validasi berhasil, sistem memulai perubahan pada skema dan membuat solusi komponen yang tidak digunakan lagi. Anda dapat menghapus solusi yang tidak digunakan lagi ini setelah menyelesaikan semua pemfaktoran ulang penyesuaian yang diperlukan. Langkah ini adalah bagian terpanjang dari proses peningkatan dan dapat memakan waktu hingga empat jam untuk diselesaikan.
1. **Peningkatan data:** Setelah semua perubahan skema yang diperlukan telah diselesaikan dalam langkah peningkatan metadata, data Anda dimigrasikan ke skema baru, dan setiap default dan perhitungan ulang yang diperlukan dilakukan.
1. **Pembaruan mesin jadwal proyek:** Setelah pemutakhiran data berhasil, **tab Jadwal** di halaman utama diberi label **ulang Tugas**. Ketika pengguna memilih tab ini setelah peningkatan, mereka diarahkan untuk menavigasi ke kisi pelacakan untuk melihat versi baca-saja dari WBS. Untuk mengedit WBS, mereka harus memulai proses [konversi jadwal](/PSA-Upgrade-Project-Conversion.md). Semua proyek tanpa WBS yang sudah ada sebelumnya dapat menggunakan pengalaman penjadwalan baru secara langsung, tanpa konversi.
 
### <a name="validate-common-scenarios"></a>Memvalidasi skenario umum

Saat Anda memvalidasi penyesuaian spesifik, sebaiknya Anda juga meninjau proses bisnis yang didukung di seluruh aplikasi. Proses bisnis ini termasuk, tetapi tidak terbatas pada, penciptaan entitas penjualan seperti kutipan dan kontrak, dan pembuatan proyek yang mencakup WBS dan persetujuan aktual.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan besar antara Otomatisasi Layanan Proyek dan Operasi Proyek

Bagian ini memberikan ringkasan perubahan besar yang dapat Anda harapkan antara Project Service Automation dan Project Operations.

### <a name="project-planning"></a>Perencanaan proyek

Kemampuan perencanaan proyek dalam Operasi Proyek tidak lagi bergantung pada kombinasi logika sisi klien dan logika sisi server. Sebaliknya, Operasi Proyek menggunakan Project for the Web sebagai mesin penjadwalannya. Perubahan dalam kemampuan penjadwalan ini memungkinkan beberapa fitur baru, seperti tampilan Board dan Gantt, perencanaan berbasis sumber daya, item [daftar periksa tugas,](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) dan mode penjadwalan proyek. Kemampuan penjadwalan baru juga didukung oleh serangkaian antarmuka pemrograman aplikasi (API) [baru](../project-management/schedule-api-preview.md) yang kaya. API ini dimaksudkan untuk membantu memastikan bahwa tidak ada operasi terprogram untuk membuat, memperbarui, atau menghapus entitas di WBS yang merusak bidang terhitung dalam jadwal.

### <a name="billing-and-pricing"></a>Penagihan dan harga

Sebagai bagian dari investasi berkelanjutan dalam Operasi Proyek, beberapa kemampuan baru tersedia dalam Penagihan dan penetapan harga. Berikut adalah beberapa contoh:

- [Merekam penggunaan material pada proyek dan tugas proyek](../material/material-usage-log.md)
- [Manajemen subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berbasis uang muka dan panjar](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan validasi kontrak yang tidak melebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Penagihan berbasis tugas

### <a name="resource-management"></a>Manajemen sumber daya

Operasi Proyek menyediakan dukungan opsional untuk Universal Resource Scheduling papan (URS) dan asisten penjadwalan. Pengalaman baru ini akan menjadi wajib pada gelombang April 2023.

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penyebaran mana yang saat ini didukung untuk peningkatan?

| Sumber                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Layanan Proyek                             | Penyebaran Lite Operasi Proyek                        | Didukung               |
| Dynamics 365 Finance Manajemen Proyek dan Akuntansi | Penyebaran Lite Operasi Proyek                        | Saat ini tidak didukung |
| Manajemen Proyek Keuangan dan Akuntansi              | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Otomatisasi Layanan Proyek 3.x                         | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Proyek untuk Web (lingkungan khusus)            | Penyebaran Lite Operasi Proyek                        | Saat ini tidak didukung |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimana cara menginstal Operasi Proyek sebelum alat peningkatan tersedia?

Ada dua opsi untuk menginstal Operasi Proyek sebelum alat peningkatan tersedia:

- Menyediakan lingkungan baru.
- Sebarkan Operasi Proyek secara terpisah di organisasi penjualan mana pun di mana Project Service Automation tidak ada.

Jika Project Service Automation diinstal pada organisasi, tetapi tidak digunakan, itu dapat dihapus instalannya. Setelah Anda benar-benar menghapus Project Service Automation, Operasi Proyek dapat diinstal pada organisasi yang sama.
