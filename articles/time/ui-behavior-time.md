---
title: Perilaku UI entri waktu
description: Topik ini menyediakan informasi tentang perilaku UI untuk entri waktu.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078419"
---
# <a name="time-entry-ui-behavior"></a>Perilaku UI entri waktu

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Kisi **entri waktu mingguan** baru adalah kontrol kustom yang memiliki dua bagian utama, **dimensi** , dan **durasi**.

## <a name="dimensions"></a>Dimensi
Bagian **dimensi** menunjukkan dimensi yang waktunya dapat dimasukkan. Dimensi berikut didukung secara default:

  - Project
  - Tugas Proyek
  - Peran
  - Tipe
  - Status Entri

Bagian **dimensi** tidak memungkinkan pengeditan sebaris. Bagian ini didukung oleh tampilan yang memungkinkan bidang kustom ditambahkan ke kisi entri waktu mingguan.

## <a name="duration"></a>Durasi
Bagian durasi menampilkan hari dalam seminggu sebagai header kolom. Bagian ini memungkinkan pengeditan sebaris. Setelah baris entri waktu dibuat dengan dimensi yang sesuai, pengguna dapat dengan cepat memasukkan jumlah waktu yang dihabiskan pada dimensi tersebut.

## <a name="create-a-new-time-entry"></a>Buat entri waktu baru

1. Dalam kisi entri waktu, pilih **Baru**. 
2. Di kotak dialog **buat cepat entri waktu** , pilih tanggal entri waktu.
3. Masukkan data untuk dimensi **proyek** , **tugas proyek** , **peran** , dan **durasi**. Informasi ini harus ditambahkan dalam menit, jam, atau hari dengan mengetik **h** , **m** , atau **d** , bersama-sama dengan nomornya. 
4. Masukkan deskripsi untuk entri dan komentar yang dapat dibagikan secara eksternal terkait entri waktu. 

Bila Anda menyimpan entri, nilai yang dimasukkan akan muncul di Bagian **dimensi**. Informasi yang dimasukkan di bidang **durasi** akan muncul pada tanggal saat entri waktu dibuat.

Bidang pencarian didukung oleh tampilan sistem. Misalnya, setelah pengguna memasukkan proyek , bidang **tugas proyek** diatur ke tampilan **salinan** secara default. Untuk membuat entri waktu untuk tugas yang tidak ditetapkan ke pengguna, pilih **Ubah tampilan** di kotak dialog pencarian, lalu pilih tampilan **semua tugas proyek aktif**.

## <a name="edit-a-time-entry"></a>Editan Entri Waktu 
Rincian dari beberapa bidang pada halaman entri waktu, seperti **Deskripsi** dan **komentar eksternal** , tidak ditampilkan di kisi entri waktu mingguan. Sebaliknya, indikator segitiga kecil muncul di sel **durasi** yang memiliki rincian tambahan ini. 

1. Untuk mengedit entri waktu, pilih sel yang akan diperbarui di entri waktu.
2. Pilih **Edit rincian** untuk memperbarui data dalam panel **formulir utama entri waktu**. 

## <a name="copy-a-time-entry-row"></a>Salin baris Entri Waktu
Setelah baris dibuat, Anda dapat memilih **Salin baris** untuk menyalin seluruh baris ke baris baru. Bila baris disalin dengan cara ini, dimensi dan durasi juga disalin. Anda juga dapat memilih **Edit baris** untuk memperbarui nilai dimensi dan durasi di bagian **durasi**.

## <a name="open-a-time-entry-behavior"></a>Buka perilaku Entri Waktu
Untuk mendukung entri yang optimal dan cepat di bidang yang paling menonjol, kisi waktu mingguan menampilkan subkumpulan dimensi dan durasi waktu tertentu. Untuk melihat semua rincian entri satu kali, dalam **Edit entri** , pilih **buka**.

## <a name="submit-a-time-entry"></a>Ajukan entri waktu
Anda dapat mengirimkan entri satu kali atau grup entri waktu dengan memilih blok sel atau baris entri seluruh waktu, lalu memilih **Ajukan**. Entri waktu yang dikirim akan muncul sebagai entri yang menunggu persetujuan pada halaman **persetujuan** pemberi persetujuan. Setelah entri waktu berhasil diajukan, mereka tidak dapat diedit.

## <a name="recall-a-time-entry"></a>Tarik kembali entri waktu
Anda dapat menarik kembali entri waktu yang telah Anda ajukan. Anda dapat menanyakan entri satu kali, blok entri waktu, atau seluruh baris entri waktu. Entri waktu yang ditarik dapat diedit.

## <a name="time-entry-status"></a>Status Entri Waktu

- **Draf** : Entri waktu baru secara otomatis ditetapkan status **draf**. Hanya entri waktu yang memiliki status **draf** yang dapat dihapus.
- **Diajukan** : Bila entri waktu diajukan, status akan diperbarui ke **Diajukan**. 
- **Disetujui** : Bila entri waktu yang diajukan disetujui, status diperbarui ke **Disetujui**. 
- **Dikembalikan** : Jika entri waktu ditolak, status akan diperbarui ke **dikembalikan** , dan entri dapat dikoreksi dan diajukan kembali. 

## <a name="view-rejection-comments"></a>Lihat Komentar Penolakan
Bila entri waktu ditolak oleh pemberi izin, pemberi izin dapat menambahkan komentar untuk membantu sumber daya memahami alasan penolakan. Untuk melihat komentar penolakan untuk entri waktu, pilih **entri terbuka**. Komentar penolakan akan ditampilkan di Timeline. Pengguna dapat merespons komentar penolakan sebelum mereka mengirimkan ulang entri.

## <a name="copy-week"></a>Salin minggu
Setelah beberapa kali entri dibuat, pengguna dapat membuat beberapa entri waktu pada waktu yang sama.

1. Di formulir **entri waktu** , pilih **Salin pekan** ke buat entri waktu tambahan secara massal. 
2. Di kotak dialog **Salin** , bagian **dari periode** , gunakan bidang **tanggal mulai** dan **tanggal berakhir** untuk menentukan rentang tanggal untuk menyalin entri waktu. 
3. Di bagian **hingga periode** , di bidang **tanggal mulai** , tentukan tanggal untuk membuat entri waktu. 
4. Pilih **Salin**. Untuk tanggal yang ditentukan di **hingga periode** , salinan entri waktu untuk hari yang sesuai dalam pekan itu dalam **dari periode** dibuat. Misalnya, entri waktu Senin dari pekan lalu disalin ke hari Senin dalam pekan yang ditentukan sebagai **periode hingga**.

## <a name="import"></a>Impor
Proses dasar yang sama digunakan untuk mengimpor dari Pemesanan, tugas, dan pertukaran. Anda dapat menentukan rentang tanggal Pemesanan untuk diimpor, lalu secara eksplisit memilih Pemesanan yang harus disalin ke entri waktu draf. 
