---
title: Tingkatkan dari Project Service Automation ke Project Operations
description: Artikel ini memberikan ikhtisar proses untuk ditingkatkan dari ke Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736670"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Tingkatkan dari Project Service Automation ke Project Operations

Dengan bangga kami umumkan bagian kedua dari tiga fase untuk ditingkatkan dari Microsoft Dynamics 365 Project Service Automation ke Microsoft Dynamics 365 Project Operations. Artikel ini memberikan ikhtisar untuk pelanggan yang sedang melakukan perjalanan menarik ini. 

Program pelaksanaan peningkatan akan dibagi menjadi tiga fase.

| Pelaksanaan peningkatan | Fase 1 (Januari 2022) | Fase 2 (November 2022) | Fase 3 (Gelombang April 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Tidak ada dependensi pada struktur perincian kerja (WBS) untuk proyek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS tercakup dalam batas Project Operations yang saat ini didukung | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar batas Project Operations yang saat ini didukung, termasuk dukungan untuk Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Fitur proses peningkatan 

Sebagai bagian dari proses peningkatan, kami telah menambahkan log peningkatan ke peta situs untuk memungkinkan administrator mendiagnosis kegagalan dengan lebih mudah. Setelah antarmuka baru, aturan validasi baru akan ditambahkan untuk memastikan integritas data setelah peningkatan. Validasi berikut akan ditambahkan ke proses peningkatan.

| Validasi | Fase 1 (Januari 2022) | Fase 2 (November 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan divalidasi terhadap pelanggaran integritas data umum (misalnya, penetapan sumber daya yang terkait dengan tugas induk yang sama tetapi memiliki proyek induk yang berbeda). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi terhadap [batas yang diketahui dari Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi terhadap batas yang diketahui dari Project Desktop Client. | |  | :heavy_check_mark: |
| Sumber daya yang dapat dipesan dan kalender proyek akan dievaluasi terhadap pengecualian aturan kalender umum tidak kompatibel. | | :heavy_check_mark: | :heavy_check_mark: |

Pada fase 2, pelanggan yang meningkatkan ke Project Operations akan mendapatkan peningkatan proyek yang ada menjadi pengalaman hanya baca untuk perencanaan proyek. Dalam pengalaman hanya baca ini, WBS lengkap akan terlihat di kisi pelacakan. Untuk mengedit WBS, manajer proyek dapat memilih [**Konversi**](/PSA-Upgrade-Project-Conversion.md) pada halaman utama proyek. Proses latar belakang kemudian memperbarui proyek supaya dapat mendukung pengalaman penjadwalan proyek baru dari Project for the Web. Fase ini sesuai untuk pelanggan yang memiliki proyek yang sesuai dengan [batas yang diketahui dalam Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Pada fase 3, dukungan untuk Project Desktop Client akan ditambahkan, untuk keuntungan pelanggan yang ingin terus mengedit proyek mereka dari aplikasi tersebut. Namun, jika proyek yang ada dikonversi ke pengalaman baru Project for the Web, akses ke add-in akan dinonaktifkan untuk setiap proyek yang dikonversi.

## <a name="prerequisites"></a>Prasyarat

Agar memenuhi syarat untuk peningkatan Fase 1, Anda harus memenuhi kriteria berikut:

- Lingkungan target tidak boleh berisi rekaman apa pun dalam entitas **msdyn_projecttask**.
- Lisensi Project Operations yang valid harus ditetapkan ke semua pengguna aktif. 
- Anda harus memvalidasi proses peningkatan paling tidak satu lingkungan non-produksi yang berisi himpunan data perwakilan yang selaras dengan lingkungan produksi Anda.
- Lingkungan target harus diperbarui ke Project Service Automation Rilis Pembaruan 37 (V3.10.58.120) atau versi yang lebih baru.

Agar memenuhi syarat untuk peningkatan Fase 2, Anda harus memenuhi kriteria berikut:

- Lisensi Project Operations yang valid harus ditetapkan ke semua pengguna aktif. 
- Anda harus memvalidasi proses peningkatan paling tidak satu lingkungan non-produksi yang berisi himpunan data perwakilan yang selaras dengan lingkungan produksi Anda.
- Lingkungan target harus diperbarui ke Project Service Automation Rilis Pembaruan 37 (V3.10.58.120) atau versi yang lebih baru.
- Lingkungan yang berisi tugas (msdyn_projecttask) didukung hanya jika total jumlah tugas per proyek adalah 500 atau kurang.

Prasyarat untuk Fase 3 akan diperbarui saat tanggal ketersediaan umum sudah mendekati.

## <a name="licensing"></a>Lisensi

Jika Anda memiliki lisensi aktif untuk Project Service Automation, Anda dapat menginstal dan menggunakan Project Operations, yang mencakup semua kemampuan Project Service Automation dan lainnya. Dengan cara ini, Anda dapat menguji kemampuan Project Operations sementara terus menggunakan Project Service Automation dalam produksi. Setelah lisensi Project Service Automation berakhir, Anda nantinya harus melakukan transisi ke Project Operations. Saat merencanakan transisi ini, Anda harus menjelaskan fakta bahwa lisensi Project Operations tidak mencakup lisensi Project Service Automation. Pelanggan yang memiliki skenario di mana mereka telah menyebarkan Project Service Automation dan harus terus menggunakan atau meningkatkan lisensinya untuk PSA sedangkan mereka berencana beralih ke Project Operations, dapat meminta lisensi PSA sementara berdasarkan lisensi yang dibeli Project Operations. Satu lisensi Project Service Automation akan dikeluarkan untuk satu lisensi Project Operations. Lisensi PSA sementara mungkin diminta menggunakan tautan ini: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Menguji dan merestorasi penyesuaian

Sebagai titik awal, impor semua penyesuaian ke lingkungan Project Operations (Lite) yang bersih untuk mengkonfirmasikan bahwa impor berhasil dan operasi bisnis berperilaku seperti yang diharapkan.

Berikut adalah beberapa hal yang harus diperhatikan:

- Impor mungkin gagal karena dependensi yang tidak ada. Dengan kata lain, bidang referensi penyesuaian atau komponen lain yang telah dihapus di Project Operations. Dalam kasus ini, hapus dependensi ini dari lingkungan pengembangan.
- Jika solusi yang tidak terkelola dan terkelola Anda mencakup komponen yang tidak disesuaikan, hapus komponen tersebut dari solusi. Contohnya, bila Anda menyesuaikan entitas **Proyek**, cukup tambahkan header entitas ke solusi Anda. Jangan tambahkan semua bidang. Jika sebelumnya Anda menambahkan semua subkomponen, Anda mungkin harus membuat solusi baru secara manual dan menambahkan komponen yang relevan ke dalamnya.
- Formulir dan tampilan mungkin tidak muncul seperti yang diharapkan. Dalam kondisi tertentu, jika Anda telah menyesuaikan formulir atau tampilan versi out-of-box, penyesuaian mungkin akan mencegah pembaruan baru di Project Operations berlaku. Untuk mengidentifikasi masalah ini, sebaiknya Anda melakukan tinjauan berdampingan penginstalan Project Operations yang selesai dan penginstalan Project Operations yang mencakup penyesuaian Anda. Bandingkan formulir yang paling umum digunakan dalam bisnis Anda untuk mengkonfirmasikan bahwa versi formulir Anda tetap masuk akal dan tidak kehilangan sesuatu dari versi formulir yang jelas. Lakukan jenis peninjauan berdampingan yang sama untuk tampilan yang Anda sesuaikan.
- Logika bisnis mungkin gagal saat runtime. Karena referensi ke bidang di plug-in tidak divalidasi pada saat impor, logika bisnis mungkin gagal karena referensi ke bidang yang sudah tidak ada lagi, dan Anda mungkin menerima pesan kesalahan yang mirip contoh berikut: entitas "'Proyek' tidak berisi atribut dengan Nama = 'msdyn_plannedhours' dan NameMapping = 'Logical'." Dalam kasus ini, modifikasi penyesuaian agar dapat menggunakan bidang baru. Jika Anda menggunakan kelas proksi yang dibuat secara otomatis dan referensi jenis kuat pada logika plug-in, pertimbangkan untuk meregenerasi proksi tersebut dari penginstalan yang selesai. Dengan cara ini, Anda dapat dengan mudah mengidentifikasi semua tempat plug-in tergantung pada bidang yang tidak digunakan lagi.

Setelah Anda memperbarui penyesuaian untuk mengimpor Project Operations dengan mulus, silakan pindah ke langkah selanjutnya.

## <a name="end-to-end-testing-in-development-environments"></a>Pengujian end-to-end di lingkungan pengembangan

### <a name="initiate-upgrade"></a>Memulai peningkatan 

1. Dalam pusat admin Power Platform, temukan dan pilih lingkungan Anda. Lalu, dalam aplikasi, temukan dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Instal** untuk memulai peningkatan. Pusat admin Power Platform akan menyajikan penginstalan ini sebagai penginstalan baru. Namun, kehadiran Project Service Automation versi sebelumnya akan terdeteksi, dan penginstalan yang ada akan ditingkatkan.

    Setelah peningkatan selesai, lingkungan harus menunjukkan bahwa Project Operations telah diinstal, dan Project Service Automation tidak diinstal.

    Tergantung jumlah data yang ada di lingkungan, peningkatan mungkin butuh waktu beberapa jam. Tim inti yang mengelola peningkatan harus merencanakannya dengan tepat dan menjalankan peningkatan di luar jam kerja. Dalam kasus tertentu, jika volume data besar, peningkatan harus dijalankan selama akhir pekan. Keputusan tentang penjadwalan harus didasarkan pada hasil pengujian di lingkungan yang lebih rendah.

3. Tingkatkan solusi kustom jika diperlukan. Pada titik ini, terapkan perubahan yang Anda buat pada penyesuaian pada bagian [Penyesuaian Pengujian dan restorasi](#testing-and-refactoring-customizations) di artikel ini.
4. Buka **make.powerapps.com**, pilih lingkungan Anda dari drop down pada sisi kanan atas portal, pilih **Solusi** dari menu kiri, pilih solusi **Komponen Project Operations yang Tidak Digunakan Lagi** dan **Hapus Instalan**.

    Solusi ini adalah solusi sementara yang menyimpan model dan komponen data yang ada saat peningkatan. Dengan menghapus solusi ini, Anda menghapus semua bidang dan kompone yang tidak digunakan lagi. Dengan cara ini, Anda akan membantu menyederhanakan antarmuka dan membuat integrasi dan ekstensi menjadi lebih mudah.
    
### <a name="upgrade-to-project-operations-lite"></a>Meningkatkan Project Operations Lite

Langkah-langkah berikut menjelaskan proses peningkatan dan pengelogan kesalahan terkait:

1. **Pemeriksaan Versi PSA:** Untuk menginstal Project Operations, Anda harus memiliki V3.10.58.120 atau yang lebih tinggi.
1. **Pra-validasi:** Bila administrator memulai peningkatan, sistem menjalankan operasi pra-validasi pada setiap entitas yang intinya ke solusi Project Operations. Langkah ini akan memverifikasi bahwa semua entitas referensi valid dan memastikan bahwa data yang terkait dengan WBS berada dalam batas yang dipublikasikan Project for the Web.
1. **Peningkatan metadata:** Setelah pra-validasi yang berhasil, sistem memulai perubahan pada skema dan membuat solusi komponen yang tidak digunakan lagi. Anda dapat menghapus solusi yang tidak digunakan setelah Anda menyelesaikan semua restorasi penyesuaian yang diperlukan. Langkah ini adalah bagian terlama dari proses peningkatan dan dapat berlangsung selama empat jam.
1. **Peningkatan data:** Setelah semua perubahan skema yang diperlukan telah diselesaikan pada langkah peningkatan metadata, data Anda dimigrasi ke skema baru, dan setiap default dan penghitungan ulang yang diperlukan dilakukan.
1. **Pembaruan mesin jadwal proyek:** Setelah peningkatan data yang berhasil, tab **Jadwal** pada halaman utama berlabel **Tugas**. Bila pengguna memilih tab ini setelah peningkatan, mereka akan diarahkan untuk menavigasi ke kisi pelacakan untuk melihat versi WBS hanya baca. Untuk mengedit WBS, mereka harus memulai [proses konversi jadwal](/PSA-Upgrade-Project-Conversion.md). Semua proyek tanpa WBS yang sudah ada sebelumnya dapat menggunakan pengalaman penjadwalan baru secara langsung, tanpa konversi.
 
### <a name="validate-common-scenarios"></a>Validasi skenario umum

Saat Anda memvalidasi penyesuain khusus, sebaiknya Anda juga meninjau proses bisnis yang didukung di seluruh aplikasi. Proses bisnis ini mencakup, namun tidak terbatas pada pembuatan entitas penjualan seperti kuotasi dan kontrak, serta pembuatan proyek yang mencakup WBS dan persetujuan aktual.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan besar antara Project Service Automation dan Project Operations

Bagian ini memberikan ringkasan perubahan besar yang dapat Anda harapkan antara Project Service Automation dan Project Operations.

### <a name="project-planning"></a>Perencanaan proyek

Kemampuan perencanaan proyek dalam Project Operations tidak lagi mengandalkan kombinasi logika sisi klien dan logika sisi server. Sebaliknya, Project Operations menggunakan Project for the Web sebagai mesin penjadwalannya. Perubahan kemampuan penjadwalan ini memungkinkan beberapa fitur baru, seperti tampilan Board and Gantt, perencanaan berdasarkan sumber daya, [item daftar periksa tugas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c), dan mode penjadwalan proyek. Kemampuan penjadwalan baru juga didukung oleh kumpulan [antarmuka program aplikasi (API) baru yang kaya](../project-management/schedule-api-preview.md). API ini ditujukan untuk membantu memastikan tidak ada operasi programmatis untuk membuat, memperbarui, atau menghapus entitas di WBS yang akan rusak pada bidang terhitung dalam jadwal.

### <a name="billing-and-pricing"></a>Penagihan dan harga

Sebagai bagian dari melanjutkan investasi dalam Project Operations, beberapa kemampuan baru tersedia dalam Penagihan dan harga. Berikut adalah beberapa contoh:

- [Merekam penggunaan bahan pada proyek dan tugas proyek](../material/material-usage-log.md)
- [Manajemen subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berbasis uang muka dan panjar](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontrak tidak melebihi status dan validasi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Penagihan berdasarkan tugas

### <a name="resource-management"></a>Manajemen sumber daya

Project Operations memberikan dukungan opsional untuk board Universal Resource Scheduling (URS) dan asisten penjadwalan. Pengalaman baru ini akan menjadi wajib pada gelombang April 2023.

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penyebaran mana yang saat ini didukung untuk peningkatan?

| Sumber                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Layanan Proyek                             | Penyebaran Project Operations Lite                        | Didukung               |
| Manajemen Proyek dan Akuntasi Dynamics 365 Finance | Penyebaran Project Operations Lite                        | Saat ini tidak didukung |
| Manajemen Proyek dan Akuntansi Finance              | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Project Service Automation 3.x                         | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Project for the Web (lingkungan khusus)            | Penyebaran Project Operations Lite                        | Saat ini tidak didukung |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimana cara menginstal Project Operations sebelum tooling peningkatan tersedia?

Ada dua pilihan untuk menginstal Project Operations sebelum tooling peningkatan tersedia:

- Penyediaan lingkungan baru.
- Sebarkan Project Operations secara terpisah di organisasi penjualan mana pun yang tidak ada Project Service Automation.

Jika Project Service Automation diinstal pada organisasi, namun tidak digunakan, kemungkinan bisa dihapus instalannya. Setelah Anda benar-benar menghapus Project Service Automation, Project Operations dapat diinstal di organisasi yang sama.
