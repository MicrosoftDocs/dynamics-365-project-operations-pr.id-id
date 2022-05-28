---
title: Mengatur template biaya
description: Topik ini berisi informasi tentang cara membuat dan menggunakan template biaya di Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9e163dc3180d2b35ddf9b15aa0577bf51e3b72ce
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594214"
---
# <a name="set-up-cost-templates"></a>Mengatur template biaya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Topik ini berisi informasi tentang cara membuat dan menggunakan template biaya di Project Operations. Template biaya menentukan:

- Kategori proyek untuk transaksi prakiraan dan aktual untuk disertakan dalam persentase perhitungan penyelesaian proyek. Nilai persen-selesai kemudian digunakan untuk menghitung jumlah pendapatan yang diakui.
- Apakah persentase penyelesaian dapat dimodifikasi jika dihitung secara otomatis.
- Apakah persentase selesai dihitung berdasarkan jumlah atau unit.

## <a name="cost-template-example"></a>Contoh template biaya

Anda sedang mengerjakan proyek desain situs web untuk pelanggan yang Anda kenakan biaya tetap sebesar USD 10.000. Anda memprakirakan bahwa dibutuhkan waktu 100 jam (USD 5.000) untuk menyelesaikan proyek tersebut. Anda juga memperkirakan dua tiket pesawat dan akomodasi empat malam di hotel untuk perjalanan ke lokasi pelanggan (USD 1.800). Seluruhnya membutuhkan biaya dengan perkiraan sebesar USD 6.800.

Saat Anda menjalankan proses pengakuan pendapatan harga tetap untuk membuat estimasi di akhir bulan, Anda akan menemukan bahwa Anda telah bekerja sebanyak 35 jam di proyek tersebut. Biaya ini belum termasuk tiket pesawat atau hotel. Anda juga memiliki asisten yang melakukan lima jam penelitian untuk proyek dengan biaya USD 100, yang belum pernah Anda rencanakan.

Bila Anda menghitung nilai persen selesai untuk proyek ini, Anda dapat menentukan pilihan sebagai berikut:

- Apakah Anda ingin menyertakan semua biaya (jam dan pengeluaran) atau hanya beberapa jam?
- Apakah Anda ingin menyertakan seluruh jam atau hanya jumlah jam yang direncanakan?
- Apakah Anda ingin menghitung persen selesai berdasarkan biaya tunai dari jam yang direncanakan (USD 5.000) atau hanya berdasarkan jumlah jam (100)?

Jawaban Anda untuk pertanyaan ini menentukan pilihan yang akan Anda tetapkan pada template biaya dan kategori yang Anda pilih pada baris template biaya.

Tabel berikut ini menjelaskan hasil dari metode yang berbeda untuk menghitung nilai persen selesai untuk skenario ini.

| Penyelesaian berdasarkan | Biaya tunai atau unit | Persen selesai | Penghitungan |
| --- | --- | --- | --- |
| Semua jam, tidak ada biaya | Biaya tunai | 37% 35 x USD 50 + USD 100 = USD 1.850 USD 1.850/USD 5.000 |
| Semua jam, tidak ada biaya | Unit | 40% | 40 jam/100 jam (termasuk lima jam yang tidak direncanakan) |
| Jam yang direncanakan, tidak ada biaya | Biaya tunai atau unit | 35% | 35/100 jam atau 35 x USD 50/5.000 |
| Semua jam dan biaya | Biaya tunai | 27,2% | USD 1.850/USD 6.800 |

Memutuskan pendekatan yang akan dilakukan untuk membuat template biaya dapat bergantung pada beberapa pertimbangan:

- Jika Anda menyertakan jam tidak terencana dalam template biaya, Anda berisiko mencapai 100 persen selesai sebelum proyek selesai. Hal ini dikarenakan jam kerja yang sebenarnya akan lebih besar daripada jam yang direncanakan. Jika Anda menggunakan salah satu dari dua metode pertama yang tercantum dalam tabel, Anda harus mengubah rencana (unit prakira) bila Anda mengetahui penyimpangannya. Dalam kasus ini, Anda akan menambah atau mengurangi jam berdasarkan pengetahuan Anda tentang apa yang diperlukan untuk menyelesaikan proyek. Jika proyek akan memerlukan 65 jam lagi untuk menyelesaikan, Anda perlu menambahkan lima jam pada rencana untuk total 105. Jika Anda tahu bahwa asisten Anda akan melakukan penelitian lima jam lagi, total akan menjadi 110 jam.
- Jika Anda menggunakan metode ketiga yang tercantum dalam tabel, Anda hanya perlu memperbarui jam yang direncanakan untuk waktu Anda sendiri untuk menjaga perhitungan persen selesai yang akurat. Profitabilitas Anda akan berubah saat jam yang tidak direncanakan dicatat, namun Anda akan tetap berada di jalur persen selesai yang diketahui.
- Jika Anda menggunakan metode keempat yang tercantum dalam tabel, risikonya adalah bahwa biaya akan muncul pada waktu yang tidak teratur dan mungkin tidak tercermin dalam kemajuan penyelesaian Anda. Oleh karena itu, jika biaya disertakan, biaya tersebut dapat menyebabkan persen selesai Anda berfluktuasi lebih daripada yang diinginkan. Misalnya, karena Anda tidak melakukan penerbangan, persen selesai Anda adalah 27 persen, bukan 35 persen atau 37 persen jika Anda menghitung hanya berdasarkan waktu. Jika Anda telah melakukan satu perjalanan selama dua malam dan memperkirakan biaya penerbangan dan hotel secara akurat, persen selesai akan menjadi 40,4 persen (USD 1850 untuk tenaga kerja dan USD 900 untuk pengeluaran = USD 2750/USD 6800 = 40,4 persen). Oleh karena itu, menimbulkan biaya hanya untuk satu perjalanan pesawat akan mengubah persen selesai dari 27 persen menjadi 40 persen.

## <a name="create-cost-templates"></a>Membuat template biaya
Untuk membuat template biaya, ikuti langkah-langkah berikut:

1. Untuk mengakses templat biaya, di lingkungan Dynamics 365 Finance, buka **Templat Biaya Perkiraan** > **Penyiapan** > **manajemen proyek dan akuntansi** > **·**.
2. Pilih **Baru** untuk membuat template biaya baru. Masukkan nama dan deskripsi.
3. Cantumkan ID baris biaya untuk setiap jenis transaksi.
4. Pilih metode penyelesaian default:

  - **Otomatis**: Persentase penyelesaian dihitung secara otomatis untuk satu proyek. Nilai yang diperoleh tidak dapat diubah.
  - **Manual**: Persentase penyelesaian dihitung secara otomatis untuk satu proyek. Nilai yang diperoleh dapat diubah.

  > [!NOTE]
  > Untuk penghitungan manual, persentase penyelesaian dikelola dalam **Penghitungan manual** di tab **Umum** pada halaman **Estimasi**.

5. Di **Selesai berdasarkan**, pilih salah satu nilai berikut:

  - **Jumlah**: Jumlah dalam mata uang akuntansi menghitung persentase penyelesaian.
  - **Unit**: Kuantitas menghitung persentase penyelesaian.
  - **Garis lurus**: Sistem menghitung persentase penyelesaian secara proporsional dengan menggunakan tanggal mulai dan berakhir proyek untuk menentukan durasi proyek.

6. Pilih **Baris biaya** untuk meninjau baris biaya template biaya. Minimal satu baris biaya diperlukan untuk setiap jenis transaksi. Namun, Anda dapat membuat beberapa baris biaya untuk jenis transaksi yang sama dan mengatur atribut yang diinginkan untuk baris ini.
7. Di tab **Kategori**, pilih kategori proyek yang akan disertakan pada baris template biaya.
8. Di tab **Umum**, pilih apakah baris ini akan disertakan dalam persentase perhitungan penyelesaian.
9. Pilih biaya untuk menyelesaikan metode yang akan digunakan saat menghitung persentase penyelesaian.


[!INCLUDE[footer-include](../includes/footer-banner.md)]