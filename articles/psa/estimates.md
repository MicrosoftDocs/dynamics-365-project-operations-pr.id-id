---
title: Perkiraan
description: Topik ini menyediakan informasi tentang perkiraan di Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
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
ms.openlocfilehash: 95f739f0c724ff93c4d588776f9e49687bac2035
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132732"
---
# <a name="estimates"></a>Perkiraan

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pada kuotasi berbasis proyek, Anda dapat menggunakan entitas detail baris kuotasi untuk memperkirakan pekerjaan yang diperlukan untuk melaksanakan proyek. Selanjutnya Anda dapat berbagi perkiraan dengan pelanggan.

Baris kuotasi berbasis proyek tidak harus memiliki detail baris kuotasi. Atau, mereka dapat memiliki banyak detail baris kuotasi. Rincian baris kuotasi digunakan untuk memperkirakan waktu, pengeluaran, atau biaya. PSA tidak memungkinkan perkiraan material pada rincian baris kuotasi. Ini disebut kelas transaksi. Jumlah perkiraan pajak juga dapat dimasukkan pada kelas transaksi.

Selain kelas transaksi, rincian baris kuotasi memiliki jenis transaksi. PSA mendukung dua jenis transaksi untuk rincian baris kuotasi: **biaya** dan **kontrak proyek**.

## <a name="estimate-by-using-a-contract"></a>Perkirakan menggunakan kontrak

Jika Anda menggunakan kuotasi PSA saat membuat kontrak berbasis proyek, perkiraan yang Anda lakukan untuk setiap baris kuotasi pada kuotasi disalin ke kontrak proyek. Struktur kontrak proyek itu seperti struktur kuotasi proyek yang memiliki baris, rincian baris, dan jadwal faktur.

Perkiraan dapat dilakukan secara langsung dalam kontrak proyek, seperti dalam kuotasi proyek. Untuk kuotasi proyek, perkiraan dilakukan dengan menggunakan baris kontrak dan rincian baris kontrak. Rincian baris kontrak juga dapat dibuat dari rencana proyek yang dibuat dengan menggunakan pendekatan perkiraan bottom-up.

Rincian baris kontrak dapat digunakan untuk memperkirakan waktu, pengeluaran, atau biaya. Jumlah perkiraan pajak juga dapat dimasukkan pada rincian baris kontrak.

PSA tidak memungkinkan perkiraan material pada rincian baris kontrak.

Proses yang didukung pada kontrak proyek adalah pembuatan faktur dan konfirmasi. Pembuatan faktur membuat draf faktur berbasis proyek yang mencakup semua aktual penjualan yang tidak ditagih hingga tanggal saat ini.

Konfirmasi membuat kontrak hanya baca dan mengubah statusnya dari **draf** menjadi **dikonfirmasi**. Setelah melakukan tindakan ini, Anda tidak dapat mengurungkannya. Karena tindakan ini bersifat permanen, praktik terbaik adalah menjaga kontrak tetap dalam status **draf**.

Satu-satunya perbedaan antara kontrak draft dan kontrak yang dikonfirmasi adalah status mereka dan fakta bahwa kontrak draft dapat diedit sedangkan kontrak yang dikonfirmasi tidak dapat. Pembuatan faktur dan aktual pelacakan dapat dilakukan pada kontrak draf maupun kontrak yang dikonfirmasi.

PSA tidak mendukung perubahan perintah pada kontrak atau proyek.

## <a name="estimating-projects"></a>Perkiraan Proyek

Anda dapat memperkirakan waktu dan biaya pada proyek. PSA tidak memungkinkan perkiraan material atau biaya pada proyek.

Perkiraan waktu dihasilkan saat Anda membuat tugas dan mengidentifikasi atribut sumber daya umum yang diperlukan untuk melakukan tugas. Perkiraan waktu dihasilkan dari tugas jadwal. Perkiraan waktu tidak dibuat jika Anda membuat anggota tim generik di luar konteks jadwal.

Perkiraan biaya dimasukkan di kisi pada halaman **Perkiraan**.

## <a name="understanding-estimation"></a>Memahami estimasi

Gunakan tabel berikut sebagai panduan untuk memahami logika bisnis dalam fase estimasi.

| Skenario                                                                                                                                                                                                                                                                                                                                          | Rekaman Entitas                                                                                                                                                                                                       | Jenis Transaksi | Kelas Transaksi | Informasi tambahan                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Bila Anda perlu memperkirakan nilai penjualan waktu pada kuotasi                                                                                                                                                                                                                                                                                    | Rekaman detail baris kuotasi (QLD) dibuat                                                                                                                                                                               | Kontrak proyek | Time        | Bidang asal transaksi pada baris QLD sisi penjualan merujuk pada sisi biaya QLD |
|                                                                                                                                                                                                                                                                                     | Rekaman QLD kedua dibuat oleh sistem untuk menyimpan nilai biaya yang terkait. Semua bidang non-uang disalin dari penjualan QLD ke QLD biaya oleh sistem.                                                                                                                                                                               | Biaya | Time        | Bidang asal transaksi pada baris detail baris kuotasi (QLD) sisi penjualan merujuk pada sisi biaya QLD |
| Bila Anda perlu memperkirakan nilai penjualan waktu pada kontrak                                                                                                                                                                                                                                                                                 | Rekaman detail baris kontrak proyek (CLD) dibuat                                                                                                                                                                    | Kontrak Proyek | Time        | Bidang asal transaksi pada baris CLD sisi penjualan merujuk pada CLD biaya      |
|                                                                                                                                                                                                                                                                                  | Rekaman CLD kedua dibuat oleh sistem untuk menyimpan nilai biaya yang terkait. Semua bidang non-uang disalin dari penjualan CLD ke CLD biaya oleh sistem.                                                                                                                                                                    | Biaya | Time        | Bidang asal transaksi pada baris CLD sisi penjualan merujuk pada CLD biaya      |
| Bila pengguna menjelaskan sumber daya pada tugas proyek                                                                                                                                                                                                                                                                                            | Rekaman baris perkiraan untuk menampilkan nilai penjualan tugas dibuat saat tugas dibuat dengan semua dimensi harga yang diperlukan. Peran dan unit organisasi adalah dimensi harga project service OOB | Kontrak Proyek | Time        |                                                                                   |
|     | Rekaman baris perkiraan untuk menampilkan nilai biaya tugas dibuat saat tugas dibuat dengan semua dimensi harga yang diperlukan. Semua bidang non-uang disalin dari baris perkiraan penjualan ke baris perkiraan biaya oleh sistem. Peran dan unit organisasi adalah dimensi harga OOB PSA baik untuk biaya maupun tarif tagihan.                                                                                                                                                                                                                | Biaya             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Menyesuaikan detail baris kuotasi dan entitas detail baris kontrak

Jika Anda menambahkan bidang kustom pada detail baris kuotasi dan ingin sistem memasukkan nilai bidang sebagai nilai default pada baris biaya terkait yang dibuat, gunakan Alat registrasi plug-in PreOperationContractLineDetailUpdate dan PreOperationQuoteLineDetailUpdate. Plug-in ini harus didaftarkan ulang setelah detail baris kuotasi atau detail baris kontrak diubah. Untuk menyelesaikan proses ini, ikuti langkah berikut ini.

1. Buka PluginRegistrationTool, dan Sambungkan ke instans online Anda.
2. Pilih **pencarian**, dan Cari plug-in untuk memperbarui.

    ![Kotak dialog pohon pencarian](media/basic-guide-19.png)

3. Pilih plug-in, lalu, di halaman utama, pilih **pilih**.
4. Pilih langkah plug-in untuk memperbarui, klik kanan, lalu pilih **Perbarui**.

    ![Memilih langkah di plug-in](media/basic-guide-20.png)

5. Di kotak dialog **Perbarui langkah yang ada**, di bidang **atribut filter**, pilih tombol elipsis (**...**):
 
    ![Kotak dialog Perbarui langkah yang ada](media/basic-guide-21.png)

6. Di kotak dialog **Pilih atribut**, pilih kotak centang untuk atribut kustom.

    ![Kotak dialog Pilih atribut](media/basic-guide-22.png)

7. Pilih **OK** untuk menutup kotak dialog, lalu pilih **Perbarui langkah**.
 
    ![tombol Perbarui langkah](media/basic-guide-23.png)

8. Ulangi langkah 1 hingga 7 untuk plug-in kedua.
9. Tutup PluginRegistrationTool.
