---
title: Tingkatkan dari Otomatisasi Layanan Proyek ke Operasi Proyek
description: Artikel ini memberikan gambaran umum tentang proses untuk memutakhirkan dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446039"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Tingkatkan dari Otomatisasi Layanan Proyek ke Operasi Proyek

Kami sangat senang mengumumkan yang pertama dari tiga fase untuk upgrade dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations. Artikel ini memberikan gambaran umum bagi pelanggan yang memulai perjalanan yang mengasyikkan ini. Artikel mendatang akan mencakup pertimbangan pengembang dan detail tentang peningkatan fitur. Mereka tidak hanya akan memberikan panduan untuk membantu Anda mempersiapkan peningkatan ke Operasi Proyek, tetapi juga menjelaskan apa yang dapat Anda harapkan setelah Anda meningkatkan.

Program pengiriman peningkatan akan dibagi menjadi tiga fase.

| Tingkatkan pengiriman | Tahap 1 (Januari 2022) | Tahap 2 (November 2022) | Tahap 3 (Gelombang April 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Tidak ada ketergantungan pada struktur rincian kerja (WBS) untuk proyek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam batas Operasi Proyek yang saat ini didukung | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar batas Operasi Proyek yang saat ini didukung, termasuk dukungan untuk klien desktop Proyek | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Fitur proses peningkatan 

Sebagai bagian dari proses peningkatan, kami telah menambahkan log peningkatan ke peta situs, sehingga administrator dapat lebih mudah mendiagnosis kegagalan. Selain antarmuka baru, aturan validasi baru akan ditambahkan untuk memastikan integritas data setelah peningkatan. Validasi berikut akan ditambahkan ke proses peningkatan.

| Validasi | Tahap 1 (Januari 2022) | Tahap 2 (November 2022) | Tahap 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan divalidasi terhadap pelanggaran integritas data umum (misalnya, penugasan sumber daya yang terkait dengan tugas induk yang sama tetapi memiliki proyek induk yang berbeda). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi [terhadap batas proyek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi terhadap batas yang diketahui dari klien desktop Project. | |  | :heavy_check_mark: |
| Sumber daya yang dapat dipesan dan kalender proyek akan dievaluasi terhadap pengecualian aturan kalender umum yang tidak kompatibel. | | :heavy_check_mark: | :heavy_check_mark: |

Pada fase 2, pelanggan yang meningkatkan ke Operasi Proyek akan meningkatkan proyek yang ada ke pengalaman baca-saja untuk perencanaan proyek. Dalam pengalaman baca-saja ini, WBS lengkap akan terlihat di grid pelacakan. Untuk mengedit WBS, manajer proyek dapat memilih **Konversi** di halaman Proyek **utama**. Proses latar belakang kemudian akan memperbarui proyek sehingga mendukung pengalaman penjadwalan proyek baru dari Project for the Web. Fase ini sesuai untuk pelanggan yang memiliki proyek yang sesuai dengan [batas proyek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Pada fase 3, dukungan untuk klien desktop Project akan ditambahkan, untuk kepentingan pelanggan yang ingin terus mengedit proyek mereka dari aplikasi tersebut. Namun, jika proyek yang ada dikonversi ke pengalaman Project for the Web baru, akses ke add-in akan dinonaktifkan untuk setiap proyek yang dikonversi.

## <a name="prerequisites"></a>Prasyarat

Agar memenuhi syarat untuk peningkatan fase 1, pelanggan harus memenuhi kriteria berikut:

- Lingkungan target tidak boleh berisi catatan apa pun di **entitas msdyn_projecttask**.
- Lisensi Operasi Proyek yang valid harus ditetapkan ke semua pengguna aktif pelanggan. 
- Pelanggan harus memvalidasi proses peningkatan di setidaknya satu lingkungan non-produksi yang memiliki himpunan data representatif yang selaras dengan data produksi.
- Lingkungan target harus diperbarui ke Project Service Automation Update Release 41 (3.10.62.162) atau yang lebih baru.

Prasyarat untuk fase 2 dan fase 3 akan diperbarui saat tanggal ketersediaan umum semakin dekat.

## <a name="licensing"></a>Lisensi

Jika Anda memiliki lisensi aktif untuk Project Service Automation, Anda dapat menginstal dan menggunakan Project Operations, yang mencakup semua kemampuan Project Service Automation dan lainnya. Dengan cara ini, Anda dapat menguji kemampuan Operasi Proyek saat Anda terus menggunakan Project Service Automation dalam produksi. Setelah lisensi Project Service Automation Anda berakhir, Anda harus beralih ke Operasi Proyek. Saat Anda merencanakan transisi ini, Anda harus memperhitungkan fakta bahwa lisensi Operasi Proyek tidak menyertakan lisensi Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Menguji dan memfaktorkan ulang penyesuaian

Sebagai titik awal, impor semua penyesuaian ke lingkungan Project Operations (Lite) yang bersih untuk mengonfirmasi bahwa impor berhasil, dan bahwa operasi bisnis berperilaku seperti yang diharapkan.

Berikut adalah beberapa hal yang harus diwaspadai:

- Impor mungkin gagal karena dependensi yang hilang. Dengan kata lain, bidang referensi penyesuaian atau komponen lain yang telah dihapus dalam Operasi Proyek. Dalam hal ini, hapus dependensi ini dari lingkungan pengembangan.
- Jika solusi yang tidak dikelola dan dikelola anda menyertakan komponen yang tidak disesuaikan, hapus komponen tersebut dari solusi. Misalnya, saat Anda menyesuaikan **entitas Project**, tambahkan hanya header entitas ke solusi Anda. Jangan tambahkan semua bidang. Jika sebelumnya Anda telah menambahkan semua subkomponen, Anda mungkin harus membuat solusi baru secara manual dan menambahkan komponen yang relevan ke dalamnya.
- Formulir dan tampilan mungkin tidak muncul seperti yang diharapkan. Dalam beberapa keadaan, jika Anda telah menyesuaikan salah satu formulir atau tampilan out-of-box, penyesuaian mungkin mencegah pembaruan baru dalam Operasi Proyek diterapkan. Untuk mengidentifikasi masalah ini, kami sarankan Anda melakukan tinjauan berdampingan tentang instalasi bersih Operasi Proyek dan instalasi Operasi Proyek yang menyertakan penyesuaian Anda. Bandingkan formulir yang paling umum digunakan dalam bisnis Anda untuk mengonfirmasi bahwa versi formulir Anda masih masuk akal dan tidak melewatkan sesuatu dari versi formulir yang bersih. Lakukan jenis peninjauan berdampingan yang sama untuk setiap tampilan yang telah Anda sesuaikan.
- Logika bisnis mungkin gagal saat runtime. Karena referensi ke bidang di plug-in Anda tidak divalidasi pada saat impor, logika bisnis mungkin gagal karena referensi ke bidang yang sudah tidak ada lagi, dan Anda mungkin menerima pesan kesalahan yang menyerupai contoh berikut: "Entitas 'Proyek' tidak berisi atribut dengan Name = 'msdyn_plannedhours' dan NameMapping = 'Logical'." Dalam hal ini, ubah penyesuaian Anda sehingga mereka menggunakan bidang baru. Jika Anda menggunakan kelas proxy yang dibuat secara otomatis dan referensi tipe yang kuat dalam logika plug-in Anda, pertimbangkan untuk meregenerasi proxy tersebut dari instalasi yang bersih. Dengan cara ini, Anda dapat dengan mudah mengidentifikasi semua tempat di mana plug-in Anda bergantung pada bidang yang tidak digunakan lagi.

Setelah Anda memperbarui penyesuaian untuk mengimpor Operasi Proyek dengan bersih, lanjutkan ke langkah berikutnya.

## <a name="end-to-end-testing-in-development-environments"></a>Pengujian end-to-end di lingkungan pengembangan

### <a name="initiate-upgrade"></a>Memulai peningkatan 

1. Di Power Platform pusat admin, temukan dan pilih lingkungan Anda. Kemudian, dalam aplikasi, temukan dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Instal** untuk memulai pemutakhiran. Pusat Power Platform admin akan menyajikan instalasi ini sebagai instalasi baru. Namun, keberadaan versi Project Service Automation yang lebih lama akan terdeteksi, dan instalasi yang ada akan ditingkatkan.

    Setelah pemutakhiran selesai, lingkungan harus menunjukkan bahwa Operasi Proyek diinstal, dan bahwa Project Service Automation tidak diinstal.

    > [!NOTE]
    > Bergantung pada jumlah data di lingkungan, peningkatan mungkin memakan waktu beberapa jam. Tim inti yang mengelola peningkatan harus merencanakan dengan tepat dan menjalankan peningkatan selama jam non-kerja. Dalam beberapa kasus, jika volume data besar, peningkatan harus dijalankan selama akhir pekan. Keputusan tentang penjadwalan harus didasarkan pada hasil pengujian di lingkungan yang lebih rendah.

3. Tingkatkan solusi khusus yang sesuai. Pada titik ini, sebarkan perubahan apa pun yang Anda buat pada penyesuaian Anda di [bagian Pengujian dan pemfaktoran ulang penyesuaian](#testing-and-refactoring-customizations) di artikel ini.
4. Buka **Solusi** Pengaturan \>**·**, dan pilih untuk menghapus instalan **solusi Komponen yang Tidak Digunakan Lagi** Operasi Proyek.

    Solusi ini adalah solusi sementara yang menyimpan model data dan komponen yang ada yang ada selama peningkatan. Dengan menghapus solusi ini, Anda menghapus semua bidang dan komponen yang tidak lagi digunakan. Dengan cara ini, Anda membantu menyederhanakan antarmuka dan membuat integrasi dan ekstensi lebih mudah.
    
### <a name="validate-common-scenarios"></a>Memvalidasi skenario umum

Saat Anda memvalidasi penyesuaian spesifik Anda, kami sarankan Anda juga meninjau proses bisnis yang didukung di seluruh aplikasi. Proses bisnis ini termasuk, tetapi tidak terbatas pada, penciptaan entitas penjualan seperti kutipan dan kontrak, dan pembuatan proyek yang mencakup WBN dan persetujuan aktual.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan besar antara Otomatisasi Layanan Proyek dan Operasi Proyek

Bagian ini menyediakan ringkasan perubahan besar yang dapat Anda harapkan antara Otomatisasi Layanan Proyek dan Operasi Proyek.

### <a name="project-planning"></a>Perencanaan proyek

Kemampuan perencanaan proyek dalam Project Operations tidak lagi bergantung pada kombinasi logika sisi klien dan logika sisi server. Sebagai gantinya, Operasi Proyek menggunakan Project for the Web sebagai mesin penjadwalannya. Perubahan kemampuan penjadwalan ini memungkinkan beberapa fitur baru, seperti tampilan Board dan Gantt, perencanaan berbasis sumber daya, [item](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) daftar periksa tugas, dan mode penjadwalan proyek. Kemampuan penjadwalan baru juga didukung oleh serangkaian antarmuka pemrograman aplikasi (API [) baru](../project-management/schedule-api-preview.md) yang kaya. API ini dimaksudkan untuk membantu memastikan bahwa tidak ada operasi terprogram untuk membuat, memperbarui, atau menghapus entitas di WBS yang merusak bidang terhitung dalam jadwal.

## <a name="billing-and-pricing"></a>Penagihan dan harga

Sebagai bagian dari investasi berkelanjutan dalam Operasi Proyek, beberapa kemampuan baru tersedia dalam Penagihan dan harga. Berikut adalah beberapa contoh:

- [Merekam penggunaan materi pada proyek dan tugas proyek](../material/material-usage-log.md)
- [Manajemen subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berbasis uang muka dan panjar](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan validasi kontrak tidak melebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Penagihan berbasis tugas

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penyebaran mana yang saat ini didukung untuk peningkatan?

| Sumber                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Layanan Proyek                             | Penyebaran Lite Operasi Proyek                        | Didukung               |
| Dynamics 365 Finance Manajemen proyek dan Akuntansi | Penyebaran Lite Operasi Proyek                        | Saat ini tidak didukung |
| Manajemen dan Akuntansi Proyek Keuangan              | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Otomatisasi Layanan Proyek 3.x                         | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Proyek untuk Web (lingkungan khusus)            | Penyebaran Lite Operasi Proyek                        | Saat ini tidak didukung |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimana cara menginstal Operasi Proyek sebelum alat peningkatan tersedia?

Ada dua opsi untuk menginstal Operasi Proyek sebelum alat peningkatan tersedia:

- Menyediakan lingkungan baru.
- Sebarkan Operasi Proyek secara terpisah di organisasi penjualan mana pun di mana Project Service Automation tidak ada.

> [!NOTE]
> Jika Project Service Automation diinstal pada organisasi, tetapi tidak digunakan, itu dapat dihapus instalannya. Setelah Anda benar-benar menghapus Project Service Automation, Operasi Proyek dapat diinstal pada organisasi yang sama.
