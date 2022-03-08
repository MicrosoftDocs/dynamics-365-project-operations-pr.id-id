---
title: Upgrade dari Project Service Automation ke Project Operations
description: Ini topik memberikan gambaran umum tentang proses untuk meningkatkan dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954294"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Upgrade dari Project Service Automation ke Project Operations

Kami sangat antusias untuk mengumumkan yang pertama dari tiga fase untuk upgrade dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations. Ini topik memberikan gambaran umum bagi pelanggan yang memulai perjalanan yang mengasyikkan ini. Topik masa depan akan mencakup pertimbangan pengembang dan rincian tentang peningkatan fitur. Mereka tidak hanya akan memberikan panduan untuk membantu Anda mempersiapkan upgrade Anda ke Operasi Proyek tetapi juga menjelaskan apa yang dapat Anda harapkan setelah Anda meningkatkan.

Program pengiriman upgrade akan dibagi menjadi tiga fase.

| Tingkatkan pengiriman | Tahap 1 (Januari 2022) | Fase 2 (Gelombang April 2022) | Fase 3 (Gelombang April 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Tidak ada ketergantungan pada struktur rincian kerja (WBS) untuk proyek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam batas operasi proyek yang saat ini didukung | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar batas Operasi Proyek yang didukung saat ini, termasuk dukungan untuk klien desktop Proyek | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Memutakhirkan fitur proses 

Sebagai bagian dari proses upgrade, kami telah menambahkan log upgrade ke peta situs, sehingga administrator dapat lebih mudah mendiagnosis kegagalan. Selain antarmuka baru, aturan validasi baru akan ditambahkan untuk memastikan integritas data setelah upgrade. Validasi berikut akan ditambahkan ke proses upgrade.

| Validasi | Tahap 1 (Januari 2022) | Fase 2 (Gelombang April 2022) | Fase 3 (Gelombang April 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan divalidasi terhadap pelanggaran integritas data umum (misalnya, tugas sumber daya yang terkait dengan tugas induk yang sama tetapi memiliki proyek induk yang berbeda). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi terhadap [batas-batas Proyek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan divalidasi terhadap batas yang diketahui dari klien desktop Proyek. | | :heavy_check_mark: | :heavy_check_mark: |
| Sumber daya yang dapat dipesan dan kalender proyek akan dievaluasi terhadap pengecualian aturan kalender yang tidak kompatibel umum. | | :heavy_check_mark: | :heavy_check_mark: |

Pada fase 2, pelanggan yang meng-upgrade ke Operasi Proyek akan memiliki proyek yang ada ditingkatkan menjadi pengalaman read-only untuk perencanaan proyek. Dalam pengalaman baca-saja ini, WBS penuh akan terlihat di grid pelacakan. Untuk mengedit WBS, manajer proyek dapat memilih **Konversi pada halaman Proyek** **utama**. Proses latar belakang kemudian akan memperbarui proyek sehingga mendukung pengalaman penjadwalan proyek baru dari Project for the Web. Fase ini sesuai untuk pelanggan yang memiliki proyek yang sesuai dengan [batas Proyek untuk Web yang](/project-for-the-web/project-for-the-web-limits-and-boundaries) diketahui.

Pada fase 3, dukungan untuk klien desktop Project akan ditambahkan, untuk kepentingan pelanggan yang ingin terus mengedit proyek mereka dari aplikasi itu. Namun, jika proyek yang ada dikonversi ke Proyek baru untuk pengalaman Web, akses ke add-in akan dinonaktifkan untuk setiap proyek yang dikonversi.

## <a name="prerequisites"></a>Prasyarat

Agar memenuhi syarat untuk upgrade fase 1, pelanggan harus memenuhi kriteria berikut:

- Lingkungan target tidak boleh berisi catatan apa pun dalam **entitas** msdyn_projecttask.
- Lisensi Operasi Proyek yang Valid harus diberikan kepada semua pengguna aktif pelanggan. 
- Pelanggan harus memvalidasi proses upgrade di setidaknya satu lingkungan non-produksi yang memiliki dataset representatif yang selaras dengan data produksi.
- Lingkungan target harus diperbarui ke Project Service Automation Update Release 38 atau yang lebih baru.

Prasyarat untuk fase 2 dan fase 3 akan diperbarui saat tanggal ketersediaan umum mendekat.

## <a name="licensing"></a>Lisensi

Jika Anda memiliki lisensi aktif untuk Otomatisasi Layanan Proyek, Anda dapat menginstal dan menggunakan Operasi Proyek, yang mencakup semua kemampuan Otomatisasi Layanan Proyek dan banyak lagi. Dengan cara ini, Anda dapat menguji kemampuan Operasi Proyek saat Anda terus menggunakan Project Service Automation dalam produksi. Setelah lisensi Otomatisasi Layanan Proyek Kedaluwarsa, Anda harus beralih ke Operasi Proyek. Ketika Anda merencanakan transisi ini, Anda harus menjelaskan fakta bahwa lisensi Operasi Proyek tidak menyertakan lisensi Otomatisasi Layanan Proyek.

## <a name="testing-and-refactoring-customizations"></a>Pengujian dan refactoring kustomisasi

Sebagai titik awal, impor semua kustomisasi ke dalam lingkungan Operasi Proyek bersih (lite) untuk mengkonfirmasi bahwa impor berhasil, dan bahwa operasi bisnis berperilaku seperti yang diharapkan.

Berikut adalah beberapa hal yang harus diperhatikan:

- Impor mungkin gagal karena ketergantungan yang hilang. Dengan kata lain, bidang referensi kustomisasi atau komponen lain yang telah dihapus dalam Operasi Proyek. Dalam hal ini, hapus dependensi ini dari lingkungan pembangunan.
- Jika solusi Anda yang tidak dikelola dan dikelola mencakup komponen yang tidak disesuaikan, hapus komponen tersebut dari solusi. Misalnya, saat Anda mengkustomisasi **entitas** Proyek, tambahkan hanya header entitas ke solusi Anda. Jangan menambahkan semua bidang. Jika sebelumnya Anda telah menambahkan semua subkomponen, Anda mungkin harus membuat solusi baru secara manual dan menambahkan komponen yang relevan ke dalamnya.
- Bentuk dan pandangan mungkin tidak tampak tidak terduga. Dalam beberapa keadaan, jika Anda telah menyesuaikan salah satu formulir atau tampilan di luar kotak, kustomisasi mungkin mencegah pembaruan baru dalam Operasi Proyek mulai berlaku. Untuk mengidentifikasi masalah ini, kami sarankan Anda melakukan tinjauan berdampingan tentang instalasi Operasi Proyek yang bersih dan instalasi Operasi Proyek yang mencakup kustomisasi Anda. Bandingkan formulir yang paling umum digunakan dalam bisnis Anda untuk mengonfirmasi bahwa versi formulir Anda masih masuk akal dan tidak kehilangan sesuatu dari versi bersih formulir. Lakukan jenis ulasan berdampingan yang sama untuk setiap tampilan yang telah Anda sesuaikan.
- Logika bisnis mungkin gagal saat runtime. Karena referensi ke bidang di plug-in Anda tidak divalidasi pada saat impor, logika bisnis mungkin gagal karena referensi ke bidang yang tidak ada lagi, dan Anda mungkin menerima pesan kesalahan yang menyerupai contoh berikut: entitas "'Proyek' tidak berisi atribut dengan Nama = 'msdyn_plannedhours' dan NameMapping = 'Logis'. Dalam hal ini, ubah kustomisasi Anda sehingga mereka menggunakan bidang baru. Jika Anda menggunakan kelas proxy yang dihasilkan secara otomatis dan referensi tipe yang kuat dalam logika plug-in Anda, pertimbangkan untuk meregenerasi proxy tersebut dari instalasi yang bersih. Dengan cara ini, Anda dapat dengan mudah mengidentifikasi semua tempat di mana plug-in Anda bergantung pada bidang yang sudah usang.

Setelah Anda memperbarui kustomisasi untuk mengimpor Operasi Proyek dengan bersih, lanjutkan ke langkah selanjutnya.

## <a name="end-to-end-testing-in-lower-environments"></a>Pengujian end-to-end di lingkungan yang lebih rendah

### <a name="run-the-upgrade-in-production"></a>Menjalankan peningkatan produksi

1. Di Power Platform pusat admin, temukan dan pilih lingkungan Anda. Kemudian, dalam aplikasi, temukan dan **Dynamics 365 Project Operations** pilih.
2. Pilih **Instal untuk memulai** upgrade. Power Platform Pusat admin akan menyajikan instalasi ini sebagai instalasi baru. Namun, kehadiran versi sebelumnya dari Project Service Automation akan terdeteksi, dan instalasi yang ada akan ditingkatkan.

    Setelah upgrade selesai, lingkungan harus menunjukkan bahwa Operasi Proyek diinstal, dan bahwa Otomatisasi Layanan Proyek tidak diinstal.

    > [!NOTE]
    > Tergantung pada jumlah data di lingkungan, upgrade mungkin memakan waktu beberapa jam. Tim inti yang mengelola upgrade harus merencanakan sesuai dan menjalankan upgrade selama jam non-bisnis. Dalam beberapa kasus, jika volume data besar, upgrade harus dijalankan selama akhir pekan. Keputusan tentang penjadwalan harus didasarkan pada hasil pengujian di lingkungan yang lebih rendah.

3. Tingkatkan solusi kustom yang sesuai. Pada titik ini, terapkan perubahan apa pun yang Anda buat pada kustomisasi Anda di [bagian Pengujian dan refactoring kustomisasi](#testing-and-refactoring-customizations) topik ini.
4. Buka **·** \> **Solusi** Pengaturan, dan pilih untuk menghapus instalasi **solusi Komponen Usang Operasi** Proyek.

    Solusi ini adalah solusi sementara yang memegang model data dan komponen yang ada yang hadir selama upgrade. Dengan menghapus solusi ini, Anda menghapus semua bidang dan komponen yang tidak lagi digunakan. Dengan cara ini, Anda membantu menyederhanakan antarmuka dan membuat integrasi dan ekstensi lebih mudah.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan besar antara Otomatisasi Layanan Proyek dan Operasi Proyek

Bagian ini memberikan ringkasan perubahan besar yang dapat Anda harapkan antara Otomatisasi Layanan Proyek dan Operasi Proyek.

### <a name="project-planning"></a>Perencanaan proyek

Kemampuan perencanaan proyek dalam Operasi Proyek tidak lagi bergantung pada kombinasi logika sisi klien dan logika sisi server. Sebagai gantinya, Operasi Proyek menggunakan Proyek untuk Web karena mesin penjadwalannya. Perubahan kemampuan penjadwalan ini memungkinkan beberapa fitur baru, seperti tampilan Board dan Gantt, perencanaan berbasis sumber daya, [item daftar](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) tugas, dan mode penjadwalan proyek. Kemampuan penjadwalan baru juga didukung oleh satu set antarmuka pemrograman aplikasi baru [(API) yang](../project-management/schedule-api-preview.md) kaya. API ini dimaksudkan untuk membantu memastikan bahwa tidak ada operasi terprogram untuk membuat, memperbarui, atau menghapus entitas di WBS yang merusak bidang yang dihitung dalam jadwal.

## <a name="billing-and-pricing"></a>Penagihan dan harga

Sebagai bagian dari investasi berkelanjutan dalam Operasi Proyek, beberapa kemampuan baru tersedia dalam Penagihan dan harga. Berikut adalah beberapa contoh:

- [Merekam penggunaan material pada proyek dan tugas proyek](../material/material-usage-log.md)
- [Manajemen subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berbasis uang muka dan panjar](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan validasi kontrak yang tidak melebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Tagihan berbasis tugas

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penyebaran apa yang saat ini didukung untuk upgrade?

| Sumber                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Layanan Proyek                             | Penyebaran Project Operations Lite                        | Didukung               |
| Dynamics 365 Finance Manajemen Proyek dan Akuntansi | Penyebaran Project Operations Lite                        | Saat ini tidak didukung |
| Manajemen Proyek Keuangan dan Akuntansi              | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Manajemen Proyek Keuangan dan Akuntansi              | Project Operations untuk skenario pesanan dengan stok/produksi | Saat ini tidak didukung |
| Otomatisasi Layanan Proyek 3.x                         | Project Operations untuk skenario sumber daya/tanpa stok     | Saat ini tidak didukung |
| Proyek untuk Web (lingkungan khusus)            | Penyebaran Project Operations Lite                        | Saat ini tidak didukung |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimana cara menginstal Operasi Proyek sebelum perkakas peningkatan tersedia?

Ada dua opsi untuk menginstal Operasi Proyek sebelum perkakas peningkatan tersedia:

- Menyediakan lingkungan baru.
- Terapkan Operasi Proyek secara terpisah pada setiap organisasi penjualan di mana Project Service Automation tidak hadir.

> [!NOTE]
> Jika Project Service Automation diinstal pada organisasi, tetapi tidak digunakan, itu dapat dihapus. Setelah Anda benar-benar menghapus Otomatisasi Layanan Proyek, Operasi Proyek dapat diinstal pada organisasi yang sama.
