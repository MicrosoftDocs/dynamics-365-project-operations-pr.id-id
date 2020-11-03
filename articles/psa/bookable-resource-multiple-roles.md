---
title: Perkirakan penjualan proyek dan biaya saat sumber daya yang dapat dipesan memenuhi beberapa peran pada proyek
description: Topik ini menyediakan informasi tentang bagaimana dimensi harga dapat digunakan untuk mendukung harga dan biaya untuk sumber daya yang mengisi beberapa peran pada proyek.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078536"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Perkirakan penjualan proyek dan biaya saat sumber daya yang dapat dipesan memenuhi beberapa peran pada proyek 

Perusahaan berbasis proyek sering memiliki kebutuhan atas satu sumber daya untuk melakukan beberapa peran pada suatu proyek. Masing-masing peran ini dapat dihargai dan ditentukan biayanya dengan cara yang berbeda yang berarti waktu sumber daya yang sama pada proyek dapat memperoleh perkiraan keuangan yang berbeda tergantung pada tagihan dan tarif biaya untuk masing-masing peran. Project Service Automation memungkinkan konfigurasi nilai pada rekaman anggota tim untuk sumber daya bernama dan memungkinkan untuk penimpaan berbeda pada setiap tugas yang ditetapkan untuk anggota tim.

Contoh berikut menjelaskan bagaimana penimpaan sederhana nilai ini memungkinkan sumber daya untuk memiliki beberapa peran pada proyek dengan biaya dan tarif tagihan yang berbeda.

## <a name="create-tasks"></a>Membuat tugas
Buat dua tugas proyek untuk 40 jam masing-masing, tugas A dan tugas B. Pilih tugas A sebagai pendahulu tugas B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Konfigurasi peran dan unit organisasi untuk anggota tim proyek generik

1. Pada halaman **jadwal** , pilih baris **tugas** untuk tugas A. 
2. Di bidang **sumber daya** , pilih **buat** dalam daftar drop-down.
3. Pada halaman **Buat cepat anggota tim** , tentukan atribut anggota tim umum yang dapat melakukan tugas ini.
4. Pilih peran dan unit organisasi yang sesuai, lalu pilih **Simpan dan tutup**. Anggota tim umum dibuat dan ditetapkan ke tugas ini. 

Ulangi langkah ini untuk tugas B dan pastikan bahwa peran dan unit organisasi pada anggota tim umum yang dibuat untuk tugas B berbeda dari tugas A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Konfigurasi peran dan unit organisasi untuk tugas proyek

1. Setelah Anda membuat tugas A, pilih tugas, lalu pilih **Edit tugas**.
2. Pada halaman **rincian tugas** , temukan **peran** dan bidang **unit organisasi** , tambahkan nilai yang diperlukan dari sumber daya yang akan melakukan tugas ini. 

  > [!NOTE]
  > Jika Anda menyelesaikan skenario ini menggunakan data demo Project Service Automation, pilih **Pimpinan konsultasi** untuk peran, dan **fabrikam US** sebagai unit organisasi.

3. Pilih Tugas B, dan kemudian pilih **Edit tugas**.
4. Pada halaman **rincian tugas** , temukan **peran** dan bidang **unit organisasi** , tambahkan nilai yang diperlukan dari sumber daya yang akan melakukan tugas ini. Pastikan bahwa nilai di bidang **peran** dan **unit organisasi** berbeda untuk tugas B dari tugas A. 

  > [!NOTE]
  > Jika Anda menyelesaikan skenario ini menggunakan data demo Project Service Automation, pilih **Teknisi Jaringan** untuk peran, dan **fabrikam US** sebagai unit organisasi.

5. Simpan dan tutup halaman **Detail Tugas**. 

## <a name="team-member-and-estimates-behaviour"></a>Anggota tim dan perilaku perkiraan 

1. Pada halaman **rincian tugas** , pada **anggota tim** , pilih dua anggota tim umum, lalu pilih **buat persyaratan**. Ini akan membuat persyaratan sumber daya. 
2. Pilih baris anggota tim untuk **Pimpinan konsultasi** lalu pilih **Pesan**. Papan jadwal membuka dan memesan sumber daya untuk persyaratan tersebut.
3. Pilih baris anggota tim untuk **Teknisi Jaringan** lalu pilih **Pesan**. Papan jadwal membuka dan memesan sumber daya yang sama untuk persyaratan tersebut.

### <a name="team-member-grid"></a>Kisi anggota tim 
Pada kisi **anggota tim** , perhatikan bahwa dua rekaman anggota tim umum dihapus dan telah diganti menjadi satu sumber daya. Ada satu rangkaian nilai untuk sumber daya yang menampilkan rangkaian nilai default untuk **peran** dan **unit organisasi**.
Bila Anda memperluas baris rekaman anggota tim tersebut, Anda dapat melihat tugas yang berbeda pada rekaman anggota tim untuk kedua tugas tersebut. Setiap baris tugas memiliki nilai spesifik tugas untuk **peran** dan **unit organisasi**. 

### <a name="estimates-grid"></a>Kisi Perkiraan 
Saat menavigasi kisi **Estimasi** , Anda akan melihat bahwa kedua tugas untuk sumber daya yang sama harganya berbeda.
Tugas untuk sumber daya pada tugas A harganya menggunakan nilai atribut **peran** **Pimpinan konsultasi**. Tugas untuk sumber daya yang sama pada tugas B harganya menggunakan nilai atribut **peran** **Teknisi Jaringan**.





