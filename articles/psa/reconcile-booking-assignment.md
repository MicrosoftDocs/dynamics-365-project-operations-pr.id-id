---
title: Rekonsiliasi pemesanan dan penetapan
description: Topik ini menyediakan informasi tentang nilai aktual.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 7ca6f4bb69322db08c413e076860e2ee9fdcc412
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078530"
---
# <a name="reconcile-bookings-and-assignments"></a>Rekonsiliasi pemesanan dan penetapan

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pemesanan proyek anggota tim proyek dan penetapan tugas proyek terkait secara longgar. Oleh karena itu, sumber daya dapat memiliki penetapan tugas yang tidak sesuai dengan Pemesanan dan Pemesanan yang tidak sesuai dengan penetapan tugas. Idealnya, Pemesanan proyek dan penetapan selaras, sehingga sumber daya memiliki kapasitas untuk melakukan penetapan tugas mereka. Namun, kenyataannya adalah bahwa Pemesanan dapat terjadi berdasarkan ketersediaan, dan waktu tugas dapat berubah di sepanjang siklus hidup proyek. Oleh karena itu, hubungan longgar memungkinkan fleksibilitas.

Karena hubungan onggar dari Pemesanan proyek dan penetapan tugas, tab **rekonsiliasi** disertakan pada entitas proyek. Tab ini membantu manajer proyek merekonsiliasi Pemesanan anggota tim dan tugas mereka untuk tim proyek mereka.

Tab **rekonsiliasi** menampilkan Pemesanan dan tugas hingga penetapan tugas individual untuk setiap anggota tim. Ini menunjukkan jam di sel yang dapat mewakili periode waktu dari bulan ke hari.

Di bidang **skala waktu** , Anda dapat memilih **bulan** , **Pekan** , atau **hari**. Secara default, **Pekan** dipilih. Namun, Anda dapat mengubah nilai default dengan memilih tombol **pengaturan**. Bila tab **rekonsiliasi** dibuka, maka akan ditampilkan tanggal saat ini, namun Anda dapat menggunakan kontrol kalender untuk maju atau mundur dalam waktu. Saat proyek memiliki tanggal mulai di masa mendatang, tab menampilkan tanggal tersebut saat dibuka. Kontrol kalender juga memiliki pilihan yang memungkinkan Anda beralih ke tanggal mulai dan selesai proyek.

Anda dapat menggunakan kontrol perluasan pada setiap sumber daya untuk menampilkan rincian pemesanan sumber daya. Anda juga dapat memperluas tugas setiap sumber daya ke tingkat tugas individual.

Bagian bawah tab **rekonsiliasi** menunjukkan Total keseluruhan bersih untuk proyek, dan tab juga mencakup kolom total. Untuk setiap sumber daya, tab menghitung perbedaan antara Pemesanan anggota tim pada proyek dan Rollup tugas anggota tim. Idealnya, perbedaan ini harus 0 (nol). Dengan kata lain, tidak ada perbedaan antara Pemesanan sumber daya dan penetapan tugasnya. Perbedaan ditunjukkan dengan warna dan arsir untuk memanggil menunjukkan dua kondisi:

- **Kekurangan Pemesanan** – kekurangan Pemesanan terjadi bila sumber daya memiliki lebih banyak tugas daripada Pemesanan. Karena kapasitas ini belum dicadangkan, manajer proyek dapat memperbaiki kondisi ini dengan memperluas Pemesanan sumber daya untuk mengatasi kekurangan.
- **Pemesanan berlebih** – kelebihan Pemesanan terjadi saat sumber daya telah dipesan ke proyek namun belum ditetapkan ke tugas. Kondisi ini dapat diterima jika, misalnya, sumber daya telah dipesan sebelum penetapan tugas terjadi. Namun, dalam kasus lain, sumber daya mungkin tidak direncanakan untuk ditetapkan. Dalam kasus ini, manajer proyek harus mempertimbangkan membatalkan pemesanan sumber daya, sehingga kapasitas dapat digunakan untuk proyek lain.

> [!NOTE]
> Legenda untuk kondisi ini mungkin tersembunyi untuk meninggalkan lebih banyak ruang untuk kisi. Dalam kasus ini, Anda dapat membuat legenda terlihat dengan memilih tombol **pengaturan**.

Dalam kasus tertentu, bila bidang **skala waktu** diatur ke tingkat yang lebih tinggi dari **hari** , perbedaan dapat dihitung sebagai 0 (nol). Misalnya, pada tingkat **bulan** , perbedaan bersih untuk sumber daya mungkin 0 (nol) untuk menunjukkan bahwa Pemesanan sama dengan penetapan. Namun, jika Anda melihat waktu di tingkat **Pekan** , Anda mungkin melihat bahwa ada tugas yang dilakukan 0 (nol) jam dan Pemesanan 40 jam di minggu pertama dalam bulan itu, namun penetapan 40 jam dan Pemesanan dalam 0 (nol) jam di minggu kedua dalam bulan itu. Meskipun total pemesanan dan penugasan untuk bulan tersebut sama, mereka berbeda pekan.

Bila Anda melihat tingkat waktu yang lebih tinggi, sel dalam tab **rekonsiliasi** menunjukkan indikator sel untuk menginformasikan bahwa ada perbedaan pada tingkat waktu yang lebih rendah. Misalnya, dalam ilustrasi berikut, indikator sel muncul di sel untuk bulan Oktober 2018 untuk sumber daya yang bernama Cakrawati Dewani. Oleh karena itu, Anda dapat melihat bahwa, meskipun Pemesanan dan penetapan sumber daya sama saat digabungkan pada tingkat **bulan** , namun tidak sesuai dengan tingkat yang lebih rendah.

![Pemesanan dan penugasan yang tidak cocok di tingkat bulanan](media/reconcile-assignments-01.JPG)

Klik dua kali sel untuk memperbesar ke tingkat lebih rendah berikutnya dan melihat perbedaannya. Misalnya, jika Anda mengeklik dua kali perbedaan oktober 2018 untuk Cakrawati Dewani, Anda telusuri hingga detail ke tingkat **Pekan**. Selanjutnya, Anda dapat melihat bahwa sumber daya memiliki Pemesanan 16 jam, namun tidak ada tugas dalam dua pekan pertama Oktober, dan 16 jam penugasan, namun tidak ada Pemesanan dalam minggu ketiga Oktober.

![Pemesanan dan penugasan yang tidak cocok di tingkat pekanan](media/reconcile-assignments-02.JPG)

Anda dapat mengklik kanan sel untuk memperkecil tingkat yang lebih tinggi berikutnya. Anda juga dapat mematikan indikator sel dengan memilih tombol **pengaturan**. 

Anda juga dapat menggunakan tombol **sebelumnya** dan **berikutnya** di atas kisi untuk bergerak melalui perbedaan apa pun dalam proyek Anda. Untuk menggunakan tombol ini, Anda harus memilih sumber daya terlebih dulu. Pilih **berikutnya** untuk beralih ke perbedaan berikutnya antara Pemesanan dan tugas untuk sumber daya tersebut. Untuk membuka perbedaan sebelumnya, pilih **Sebelumnya**.

Dalam situasi Anda memiliki penetapan tugas untuk sumber daya, namun tidak ada pemesanan, Anda dapat memilih kekurangan pemesanan itu, lalu pilih **Perluas Pemesanan**. Selanjutnya Anda dapat melihat Pemesanan yang diperlukan untuk mengatasi kekurangan sumber daya. Anda juga dapat melihat Pemesanan sumber daya pada proyek saat ini dan proyek lainnya. Pilih **OK** untuk membuat pemesanan untuk sumber daya tanpa memperhatikan ketersediaan saat ini. Manajer proyek atau manajer sumber daya kemudian dapat menggunakan papan jadwal untuk mengelola situasi dengan sumber daya yang dipesan berlebihan di luar kapasitasnya karena pemesanannya diperluas.

## <a name="managing-with-time-zones"></a>Mengelola dengan zona waktu
Untuk memastikan hasil yang akurat dan dapat diprediksi saat menggunakan perpanjangan Pemesanan, ada dua prasyarat penting yang harus dipenuhi:  

- Pengguna harus mengkonfigurasi zona waktu perangkat mereka untuk mencocokkan zona waktu yang ditentukan di Pengaturan personalisasi sistem Anda.
 
  ![Pengaturan zona waktu di Windows 10](media/reconcile-assignments-03.png)

  ![Pengaturan zona waktu di Pengaturan personalisasi](media/reconcile-assignments-04.png)
 
- Sumber daya yang dapat dipesan harus memiliki minimal satu menit waktu kerja yang tumpang tindih dengan kontur yang digunakan untuk menentukan ekstensi yang diminta. Contohnya, contoh berikut menunjukkan sumber daya ulasan dengan jam kerja yang jatuh antara 9:00 dan 19:00. 

  ![Perbandingan kontur sumber daya](media/reconcile-assignments-05.png)

Tabel berikut menampilkan:

- Template kalender Proyek.
- Sumber daya A: sumber daya ini memiliki kalender yang sama dan berada di zona waktu yang sama dengan proyek. Waktu mulai pemesanan adalah 9:00.
- Sumber daya B: sumber daya ini terletak di zona waktu yang berbeda dari proyek dan oleh karena itu dimulai pada 19:00 di zona waktu mereka. Namun, Pemesanan akan dimulai pada pukul 9:00 karena itu adalah waktu mulai terawal kontur tugas.
- Sumber daya C dan D: sumber daya juga terletak di zona waktu yang berbeda, keduanya berbeda dari satu sama lain dan proyek, dan Pemesanan mereka tidak dimulai lebih awal dari waktu mulai masing-masing yang tersedia.

|Entitas  |Kalender  |
|-|-|
|Template kalender Proyek   | ![Kalender Proyek](media/reconcile-assignments-06.png) |
|Sumber Daya A  | ![Kalender Sumber Daya A](media/reconcile-assignments-06.png) |
|Sumber Daya B  |  ![Kalender Sumber Daya B](media/reconcile-assignments-07.png) |
|Sumber Daya C  |  ![Kalender Sumber Daya C](media/reconcile-assignments-08.png) |
|Sumber Daya D  | ![Kalender Sumber Daya D](media/reconcile-assignments-09.png)  |
 
Bila Anda menavigasi ke tampilan rekonsiliasi, tugas sumber daya dan kekurangan Pemesanan terkait akan ditampilkan.
 ![Tampilan rekonsiliasi sebelum perpanjangan](media/reconcile-assignments-10.png)

Setelah fungsi perpanjangan Pemesanan telah dieksekusi pada setiap sumber daya, Pemesanan berhasil diperpanjang untuk setiap sumber daya. Hal ini dikarenakan setiap jam kerja sumber daya saling tumpang tindih dengan kontur kekurangan.
 ![Tampilan rekonsiliasi setelah ekstensi pemesanan](media/reconcile-assignments-11.png) 

Namun, jika dilihat lebih dekat pada rincian pemesanan, tampak adanya perbedaan dalam waktu mulai pemesanan. Pemesanan tidak akan dimulai lebih awal dari waktu mulai kontur tugas dan tidak lebih awal dari waktu mulai sumber daya yang tersedia.
 ![Pemesanan baru sumber daya di papan jadwal](media/reconcile-assignments-12.png)
