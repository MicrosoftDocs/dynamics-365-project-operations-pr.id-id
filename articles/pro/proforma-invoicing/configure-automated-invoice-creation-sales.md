---
title: Mengonfigurasi pembuatan faktur otomatis - lite
description: Topik ini menyediakan informasi tentang mengonfigurasikan pembuatan otomatis faktur proforma.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176570"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Mengonfigurasi pembuatan faktur otomatis - lite
 
_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Anda dapat mengkonfigurasi pembuatan faktur otomatis dalam Dynamics 365 Project Operations. Sistem membuat draf faktur proforma berdasarkan jadwal faktur untuk setiap baris kontrak dan kontrak proyek. Jadwal faktur dikonfigurasi pada tingkat baris kontrak. Setiap baris pada kontrak dapat memiliki jadwal faktur yang berbeda, atau jadwal faktur yang sama dapat disertakan pada setiap baris kontrak.

Bila Anda membuat faktur, sistem selalu membuat minimal satu faktur per kontrak proyek. Dalam kasus tertentu, mungkin terdapat beberapa faktur yang dibuat.

Misalnya, jika kontrak memiliki beberapa pelanggan, jumlah faktur yang sama akan dibuat sebagai jumlah pelanggan yang memiliki transaksi yang dapat ditagih ke faktur pada kontrak proyek tersebut.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Memahami bagaimana transaksi disertakan dalam faktur 

Terkadang, setiap baris kontrak berbasis proyek menentukan jadwal faktur terpisah. Misalnya, Layanan penerapan kontrak Adatum memiliki baris kontrak berikut:

- Pekerjaan prototipe yang merupakan harga tetap dengan dua tonggak yang dibuat secara manual.
- Pekerjaan penerapan yang mencakup waktu dan akan ditagih dwi-mingguan pada hari Senin.
- Pengeluaran yang timbul yang harus ditagih per bulan pada hari Senin pertama setiap bulannya.

Jadwal faktur yang ditentukan pada masing-masing dari dua baris item ini terlihat seperti tabel berikut:

| Baris Kontrak | Tanggal pembuatan faktur | Tanggal penutupan transaksi | Tanggal tonggak | Jumlah tonggak |
| --- | --- | --- | --- | --- |
| Pekerjaan Prototipe | 5 Oktober Senin | - | 5 Oktober Senin | 5000 USD |
| - | Selasa, 3 November | - | Selasa, 3 November | 12,000 USD |
| Pekerjaan Penerapan | 5 Oktober Senin | 4 Oktober Ahad | - | - |
| - | 19 Oktober Senin | 18 Oktober Ahad | - | - |
| - | 2 November, Senin | 1 November, Ahad | - | - |
| - | 16 November, Senin | 15 November, Ahad | - | - |
| Pengeluaran yang dikeluarkan | 5 Oktober Senin | 4 Oktober Ahad | - | - |
| - | 2 November, Senin | 1 November, Ahad | - | - |

Dalam contoh ini ketika faktur otomatis berjalan pada:

- **4 Oktober atau tanggal sebelum itu** : tidak ada faktur yang dihasilkan untuk kontrak ini karena tabel **jadwal faktur** untuk masing-masing baris kontrak ini tidak memanggil 4 Oktober, minggu sebagai tanggal Jalankan faktur.
- **5 Oktober Senin**: satu faktur dibuat untuk:

    - Pekerjaan prototipe yang mencakup tonggak, jika ditandai sebagai **siap untuk faktur**.
    - Pekerjaan penerapan yang mencakup semua transaksi waktu yang dibuat sebelum tanggal batas transaksi 4 Oktober minggu yang ditandai sebagai **siap faktur**.
    - Pengeluaranyang dikeluarkan yang mencakup semua transaksi pengeluaran yang dibuat sebelum tanggal batas transaksi 4 Oktober minggu yang ditandai sebagai **siap faktur**.
  
- **Pada 6 Oktober atau tanggal sebelum 19 Oktober**: tidak ada faktur yang dihasilkan untuk kontrak ini karena tabel **jadwal faktur** untuk masing-masing baris kontrak ini tidak memanggil 6 Oktober atau tanggal sebelum 19 Oktober sebagai tanggal Jalankan faktur.
- **19 Oktober, Senin**: Satu faktur dihasilkan untuk pekerjaan penerapan yang mencakup semua transaksi waktu yang dibuat sebelum tanggal batas transaksi 18 Oktober minggu yang ditandai sebagai **siap faktur**.
- **2 November Senin**: satu faktur dibuat untuk:

    - Pekerjaan penerapan yang mencakup semua transaksi waktu yang dibuat sebelum tanggal batas transaksi 1 November minggu yang ditandai sebagai **siap faktur**.
    - Pengeluaranyang dikeluarkan yang mencakup semua transaksi pengeluaran yang dibuat sebelum tanggal batas transaksi 1 November minggu yang ditandai sebagai **siap faktur**.

- **3 November, Selasa**: satu faktur dibuat untuk pekerjaan prototipe yang mencakup tonggak untuk 12000 USD, jika ditandai sebagai **siap untuk faktur**.

## <a name="configure-automatic-invoicing"></a>Konfigurasikan faktur Otomatis

Selesaikan langkah berikut untuk mengkonfigurasi faktur otomatis yang berjalan.

1. Di **Project Operations**, buka **pengaturan** > **persiapan faktur rutin**.
2. Membuat batch pekerjaan, dan namai **Project operations buat faktur**. Nama pekerjaan batch harus mencakup kata "Buat faktur".
3. Di bidang **jenis pekerjaan**, pilih **tidak ada**. Secara default, bidang **frekuensi harian** dan opsi **aktif** diatur ke **ya**.
4. Pilih **Jalankan alur kerja**. Di kotak dialog **mencari rekaman**, Anda akan melihat tiga alur kerja:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Pilih **ProcessRunCaller** dan kemudian pilih **Tambahkan**.
6. Pilih **OK** di kotak dialog berikutnya. Alur kerja **tidur** diikuti dengan alur kerja **proses**. 

> [!NOTE]
> Anda juga dapat memilih **ProcessRunner** di langkah 5. Kemudian, bila Anda memilih **OK**, alur kerja **proses** diikuti dengan alur kerja **tidur**.

Alur kerja **ProcessRunCaller** dan **ProcessRunner** membuat faktur. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** adalah alur kerja yang benar-benar membuat faktur. Alur kerja melalui semua baris kontrak pembuatan faktur, dan membuat faktur untuk baris tersebut. Untuk menentukan baris kontrak yang harus dibuat faktur, pekerjaan akan melihat tanggal faktur berjalan untuk baris kontrak. Jika baris kontrak milik satu kontrak memiliki tanggal yang sama saat menjalankan faktur, transaksi digabungkan menjadi satu faktur yang memiliki dua baris faktur. Jika tidak ada transaksi untuk membuat faktur, pekerjaan akan melompati pembuatan faktur.

Setelah **ProcessRunner** selesai berjalan, maka ia memanggil **ProcessRunCaller**, menyediakan waktu berakhir, dan ditutup. **ProcessRunCaller** kemudian memulai timer yang berjalan selama 24 jam dari waktu berakhir yang ditentukan. Di akhir timer, **ProcessRunCaller** ditutup.

Pekerjaan proses batch untuk membuat faktur adalah pekerjaan berulang. Jika proses batch ini dijalankan berkali-kali, beberapa instans pekerjaan dibuat dan menyebabkan kesalahan. Oleh karena itu, Anda harus memulai proses batch hanya satu kali, kemudian me-restart hanya jika berhenti berjalan.

> [!NOTE]
> Faktur bets di Project Operations hanya berjalan untuk baris kontrak proyek yang dikonfigurasi dengan jadwal faktur. Baris kontrak dengan metode penagihan harga tetap harus mengonfigurasikan tonggak waktu. Baris kontrak proyek dengan metode waktu dan materi penagihan akan memerlukan pengaturan jadwal faktur berdasarkan tanggal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]