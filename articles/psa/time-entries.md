---
title: Buat Entri Waktu
description: Topik ini menyediakan informasi tentang cara membuat entri waktu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149682"
---
# <a name="create-time-entries"></a>Buat Entri Waktu

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Di versi sebelumnya Dynamics 365 Project Service Automation, entri waktu dimasukkan secara mingguan. Di versi 3 dari Project Service Automation, entri waktu dimasukkan setiap hari. Namun, setelah beberapa entri waktu dibuat, Anda dapat massal membuat atau menyalinnya.

## <a name="create-a-time-entry"></a>Buat Entri Waktu

Ikuti langkah berikut untuk membuat entri waktu.

1. Pada halaman **Entri waktu**, pilih **baru**.
2. Di kotak dialog **buat cepat: entri waktu**, masukkan durasi entri waktu dalam menit, jam, atau hari. Durasi harus dimasukkan dalam format berikut: *x* menit, *x* jam, atau *x* hari. Jam dan hari juga dapat dimasukkan dalam nilai desimal, misalnya, *x,x* jam atau *x,x* hari.
3. Pilih jenis entri waktu dan proyek yang Anda masukkan entri waktunya.
4. Di bidang **tugas proyek**, Cari tugas untuk entri waktu ini.

    > [!NOTE]
    > Jika Anda membuat entri waktu untuk tugas yang tidak ditetapkan ke pengguna, di bidang **tugas proyek**, pilih tombol **pencarian**, pilih **Ubah tampilan**, lalu pilih **semua tugas proyek yang aktif** untuk mencantumkan semua tugas.

5. Masukkan deskripsi, jika Deskripsi diperlukan, lalu pilih **Simpan dan tutup**.

Setelah entri waktu dibuat dan disimpan, Anda dapat mengeditnya di kisi entri waktu . Kisi entri waktu mendukung dua format:

- Anda dapat memasukkan entri waktu dalam Format **hh:mm**. Format ini kemudian dikonversi ke jam dan pecahan.
- Anda dapat memasukkan jam dan pecahan secara langsung.

Perhatikan bahwa pecahan jam bukan menit. Oleh karena itu, 1,5 jam mewakili 1 jam 30 menit. Aturan yang sama berlaku untuk pecahan sehari. Satu hari adalah 24 Jam, dan 0,5 hari menunjukkan 12 jam.

## <a name="bulk-create-time-entries"></a>Buat Entri Waktu secara massal

Setelah beberapa entri waktu dibuat, Anda dapat menyalinnya untuk membuat entri waktu tambahan secara massal.

1. Pada halaman **Entri waktu**, pilih **Salin Pekan**.
2. Di grup bidang **dari periode** di bidang **tanggal mulai** dan **tanggal berakhir**, tentukan rentang tanggal untuk menyalin entri waktu.
3. Di grup bidang **hingga periode**, di bidang **tanggal mulai**, tentukan tanggal untuk membuat entri waktu.
4. Pilih **salin** untuk membuat salinan entri waktu yang sesuai dengan hari dalam minggu yang ditentukan dalam grup bidang **hingga periode**. Misalnya, entri waktu untuk hari Senin pekan lalu disalin ke hari Senin dalam pekan yang ditentukan dalam grup bidang **hingga periode**.

## <a name="import-data-for-time-entries"></a>Impor data untuk Entri Waktu

Anda dapat mengimpor data dari Pemesanan dan tugas proyek. Saat mengimpor data, Anda dapat menentukan rentang tanggal Pemesanan untuk diimpor, lalu secara eksplisit memilih Pemesanan yang harus dibuat sebagai entri waktu **draf**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Kemampuan Kelompokkan berdasarkan, Urutkan, pencarian, dan filter

Anda dapat mengelompokkan dan memfilter entri waktu berdasarkan dimensi yang ditentukan di kolom. Di bidang **Kelompokkan berdasarkan**, pilih dimensi yang akan digunakan untuk memfilter entri waktu. Anda juga dapat mengurutkan rekaman entri waktu dalam urutan naik atau turun menggunakan panah urut pada heading kolom. Selain itu, Anda dapat menampilkan atau menyembunyikan entri dengan memilih tombol **filter** pada heading kolom, lalu, di kotak **pencarian**, memasukkan teks yang akan digunakan untuk mencari entri waktu berdasarkan nama proyek, tugas proyek, waktu entri, atau sumber daya.
