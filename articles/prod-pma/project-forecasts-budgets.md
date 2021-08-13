---
title: Perkiraan proyek dan anggaran
description: Microsoft Dynamics 365 Finance memberikan perkiraan proyek dan anggaran proyek untuk mengelola dan mengontrol proyek Anda.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47ea4c49a76a2bb0a1855fce2e9a874b4044e429d963c08392ec0ab471f89329
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988070"
---
# <a name="project-forecasts-and-budgets"></a>Perkiraan proyek dan anggaran

[!include [banner](../includes/banner.md)]

Ada dua cara untuk mengelola dan mengontrol proyek Anda: perkiraan proyek dan anggaran proyek. 

Gunakan peramalan proyek jika organisasi Anda memiliki perspektif operasional, dan jika berfokus pada pendapatan dan biaya yang berasal dari transaksi tertentu. Gunakan penganggaran proyek jika organisasi Anda lebih berfokus pada jumlah keuangan. 

Perkiraan proyek dan anggaran proyek menggunakan model perkiraan untuk menahan jumlah proyeksi transaksi. 

Setiap metode memiliki keuntungannya. Anda harus mempertimbangkan poin berikut sebelum memilih metode untuk organisasi Anda.

|   Metode alokasi       |           Peramalan proyek            |        Penganggaran proyek                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Alokasi periode**     | Anda tidak dapat mengalokasikan transaksi secara eksplisit melalui periode fiskal. Sebaliknya, perkiraan, dan kontrol perkiraan, didasarkan pada masa berlaku proyek. Karena perkiraan didasarkan pada tanggal tertentu, Anda harus menyimpulkan periode dari tanggal. | Anda tidak dapat mengalokasikan melalui keseluruhan proyek atau periode fiskal. Jika anda mengalokasikan lebih dari satu periode, anda dapat membawa jumlah yang tidak terpakai ke depan ke periode fiskal berikutnya. |
| **Melihat transaksi**  | Anda dapat melihat transaksi dalam formulir perkiraan, di mana Anda melihat perkiraan untuk seluruh perusahaan dan untuk semua proyek, terlepas dari hierarki. Untuk fokus pada proyek tertentu, Anda harus memfilter data.                                       | Anda dapat melihat transaksi yang dianggarkan untuk satu hierarki proyek. Oleh karena itu, Anda dapat melihat rincian transaksi untuk proyek induk atau subproyeknya.                 |
| **Variabel transaksi** | Saat Anda memasukkan transaksi perkiraan, Anda dapat menggunakan setiap atribut yang ada untuk transaksi aktual. Hal ini memungkinkan untuk lebih rinci dalam perkiraan. Misalnya, Anda dapat memasukkan rincian untuk kuantitas, pekerja, item, atau properti baris.         | Bila Anda memasukkan rincian anggaran, Anda hanya dapat menggunakan jumlah, kategori, dan aktivitas.                    |
| **Keamanan**              | Peramalan didasarkan pada transaksi yang Anda masukkan dalam formulir perkiraan dan tidak melibatkan mekanisme kontrol proses. Setiap pekerja yang memiliki izin untuk formulir perkiraan dapat merevisi informasi tanpa persetujuan.                                        | Penganggaran menggunakan alur kerja sistem, yang memungkinkan manajemen perubahan dan memungkinkan Anda menyimpan Riwayat revisi.         |
| **Jenis Entitas**           | Entri transaksi perkiraan didasarkan pada jumlah unit, dan biaya dan harga unit penjualan.  | Rincian anggaran didasarkan pada jumlah, yang dibagi antara biaya dan pendapatan.                                          |
| **Model perkiraan**       | Karena setiap perkiraan harus dikaitkan dengan model, Anda dapat membuat beberapa model perkiraan dan juga mengkonfigurasi submodel.           | Anggaran proyek Membatasi model perkiraan yang digunakan untuk penganggaran. Model perkiraan yang lebih sedikit dapat membantu meningkatkan konsistensi dalam proyeksi.                           |
| **Pembengkakan biaya**         | Anda hanya dapat membolehkan atau menolak masuknya transaksi yang akan menyebabkan Pembengkakan biaya.   | Penganggaran proyek memberikan pilihan kontrol tambahan untuk pengguna. Anda dapat mengizinkan peringatan dan Pembengkakan.                    |
| **Kontrol**               | Kontrol perkiraan dilakukan dengan menggunakan pengurangan perkiraan. Jumlah aktual dikurangkan dari saldo transaksi perkiraan tanpa jejak audit. Hal ini dapat membuat lebih sulit untuk melacak di mana transaksi aktual terjadi.                   | Dalam kontrol anggaran proyek, jumlah aktual dikurangkan dari jumlah anggaran yang tersisa. Hal ini memungkinkan untuk jalur audit yang lebih jelas.                                   |

## <a name="project-forecasts"></a>Perkiraan proyek
Bila Anda menggunakan peramalan proyek, Anda dapat memasukkan transaksi perkiraan dalam formulir perkiraan untuk setiap jenis transaksi. Setiap atribut yang tersedia untuk transaksi aktual dapat digunakan untuk transaksi perkiraan, misalnya, profitabilitas baris, atribut baris, pekerja, atau deskripsi. Anda juga dapat memproyeksikan berapa lama setelah dikenakan biaya, Anda akan menagih pelanggan. 

Transaksi perkiraan proyek didasarkan pada unit dan jumlah. 

Anda harus mengaitkan setiap perkiraan proyek dengan model perkiraan. Saat Anda memasukkan transaksi perkiraan, model perkiraan akan secara otomatis disarankan. Model perkiraan bertindak sebagai wadah untuk transaksi perkiraan. 

Anda dapat menetapkan model perkiraan sebagai submodel untuk model. Hal ini memungkinkan Anda memperkirakan berdasarkan kawasan, periode waktu, atau Departemen. Anda dapat menyalin transaksi perkiraan dalam model untuk membuat model baru, dan Anda juga dapat mentransfer transaksi ke buku besar. Karena ada relasi satu lawan satu antara perkiraan dan model, setiap model perkiraan membuat anggaran terpisah untuk proyek. 

Model perkiraan dapat menggunakan pengurangan perkiraan sebagai mekanisme kontrol untuk proyek. Di pengurangan perkiraan, transaksi aktual mengurangi saldo transaksi perkiraan. Namun, karena pengurangan perkiraan diterapkan ke proyek tertinggi dalam hierarki, maka akan memberikan tampilan terbatas perubahan dalam perkiraan. Misalnya, jika pekerja terkait dengan subproyek, transaksi aktual untuk pekerja diposting ke proyek induk. Hal ini dapat menyulitkan untuk melacak perubahan, karena Anda tidak dapat dengan mudah menentukan transaksi di mana subproyek menyebabkan pengurangan jumlah perkiraan. Oleh karena itu, sebaiknya Buat salinan model perkiraan untuk pengurangan perkiraan yang akan digunakan. Selanjutnya Anda dapat menggunakan laporan untuk melihat apa yang awalnya diperkirakan. 

Anda dapat merevisi, menyalin, menghapus, atau mengalihkan perkiraan proyek ke anggaran buku besar. Namun, tidak ada kontrol proses. Setiap pekerja yang memiliki izin untuk formulir perkiraan dapat merevisi tanpa ulasan.

-   **Revisi** – Anda dapat merevisi transaksi perkiraan dalam formulir tempat entri asli dimasukkan.
-   **Salin atau Hapus** – bila Anda menyalin transaksi perkiraan, Anda menyalin baris transaksi satu model perkiraan ke model perkiraan lainnya. Bila Anda menghapus perkiraan, Anda akan menghapus transaksi perkiraan dari model perkiraan. Untuk membatasi transaksi perkiraan yang disalin atau dihapus, pilih jenis transaksi dan tanggal tertentu. Hal ini memungkinkan Anda menyalin atau menghapus hanya bagian tertentu dari perkiraan.
-   **Transfer**– saat Anda mentransfer perkiraan proyek ke anggaran buku besar, Anda mentransfer transaksi perkiraan model perkiraan ke anggaran buku besar. Anda dapat menimpa transaksi yang ditransfer sebelumnya dalam anggaran buku besar yang Anda transfer perkiraan proyeknya.

## <a name="project-budgets"></a>Anggaran proyek
Penganggaran proyek adalah metode yang lebih sederhana daripada peramalan, meskipun berintegrasi dengan model perkiraan. Ia menggunakan formulir entri tunggal untuk rincian dan revisi anggaran yang asli, dan memungkinkan untuk proyeksi yang hanya didasarkan pada jumlah, kategori, atau aktivitas. 

Dalam penganggaran proyek, Semua anggaran asli dan revisi harus dikirim ke alur kerja proyek untuk disetujui. Alur kerja memberi Anda kontrol yang lebih besar atas proses dan membuat rekaman Riwayat perubahan. 

Penganggaran proyek menyerupai penganggaran buku besar, namun lebih cepat dan lebih mudah diatur. Banyak pilihan di penganggaran buku besar, seperti urutan nomor atau mata uang, tidak harus diatur secara terpisah untuk proyek.

Anggaran proyek secara otomatis terkait dengan dua model perkiraan, satu untuk anggaran asli dan satu untuk anggaran tersisa. Oleh karena itu, laporan yang didasarkan pada model perkiraan dapat menggunakan data anggaran. Bila anggaran proyek dilakukan, sistem membuat transaksi perkiraan berdasarkan model terkait, yang digunakan untuk tujuan pelaporan dan kontrol.

## <a name="forecast-models"></a>Model perkiraan
Model perkiraan memiliki hierarki lapisan tunggal. Ini berarti bahwa satu proyek perkiraan harus dikaitkan dengan satu model perkiraan .

Jika Anda menggunakan peramalan proyek, Anda dapat mengidentifikasi model sebagai submodel. Anda kemudian dapat membuat perkiraan menurut departemen, periode waktu, atau kawasan. Misalnya, Anda dapat membuat model perkiraan selama satu tahun, lalu membuat submodel untuk perkiraan Regional timur laut, Tenggara, barat laut, dan barat daya yang diajukan oleh kepala wilayah. Dengan memilih pilihan yang berbeda dalam laporan yang tersedia, Anda dapat melihat informasi berdasarkan perkiraan Total atau submodel.





[!INCLUDE[footer-include](../includes/footer-banner.md)]