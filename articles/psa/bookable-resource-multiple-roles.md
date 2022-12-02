---
title: Buat estimasi penjualan dan biaya proyek apabila sumber daya yang dapat dipesan mengisi beberapa peran untuk suatu proyek
description: artikel ini memberikan informasi tentang cara menggunakan dimensi harga untuk mendukung harga dan biaya untuk sumber daya yang mengisi beberapa peran pada satu proyek.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5adaa7b83aae69c15aa268e723417172f1b56f42
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916154"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Buat estimasi penjualan dan biaya proyek apabila sumber daya yang dapat dipesan mengisi beberapa peran untuk suatu proyek 

[!include [banner](../includes/psa-now-project-operations.md)]

Perusahaan berbasis proyek sering memiliki kebutuhan akan satu sumber daya untuk melakukan beberapa peran dalam suatu proyek. Masing-masing peran ini dapat dihargai dan ditentukan biayanya dengan cara yang berbeda yang berarti waktu sumber daya yang sama pada proyek dapat memperoleh perkiraan keuangan yang berbeda tergantung pada tagihan dan tarif biaya untuk masing-masing peran. Project Service Automation memungkinkan konfigurasi nilai pada rekaman anggota tim untuk sumber daya bernama dan memungkinkan untuk penimpaan berbeda pada setiap tugas yang ditetapkan untuk anggota tim.

Contoh berikut menjelaskan bagaimana penimpaan sederhana nilai ini memungkinkan sumber daya untuk memiliki beberapa peran pada proyek dengan biaya dan tarif tagihan yang berbeda.

## <a name="create-tasks"></a>Membuat tugas
Buat dua tugas proyek untuk 40 jam masing-masing, tugas A dan tugas B. Pilih tugas A sebagai pendahulu tugas B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Konfigurasi peran dan unit organisasi untuk anggota tim proyek generik

1. Pada halaman **jadwal**, pilih baris **tugas** untuk tugas A. 
2. Di bidang **sumber daya**, pilih **buat** dalam daftar drop-down.
3. Pada halaman **Buat cepat anggota tim**, tentukan atribut anggota tim umum yang dapat melakukan tugas ini.
4. Pilih peran dan unit organisasi yang sesuai, lalu pilih **Simpan dan tutup**. Anggota tim umum dibuat dan ditetapkan ke tugas ini. 

Ulangi langkah ini untuk tugas B dan pastikan bahwa peran dan unit organisasi pada anggota tim umum yang dibuat untuk tugas B berbeda dari tugas A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Konfigurasi peran dan unit organisasi untuk tugas proyek

1. Setelah Anda membuat tugas A, pilih tugas, lalu pilih **Edit tugas**.
2. Pada halaman **rincian tugas**, temukan **peran** dan bidang **unit organisasi**, tambahkan nilai yang diperlukan dari sumber daya yang akan melakukan tugas ini. 

  > [!NOTE]
  > Jika Anda menyelesaikan skenario ini menggunakan data demo Project Service Automation, pilih **Pimpinan konsultasi** untuk peran, dan **fabrikam US** sebagai unit organisasi.

3. Pilih Tugas B, dan kemudian pilih **Edit tugas**.
4. Pada halaman **rincian tugas**, temukan **peran** dan bidang **unit organisasi**, tambahkan nilai yang diperlukan dari sumber daya yang akan melakukan tugas ini. Pastikan bahwa nilai dalam bidang **Peran** dan **Unit Organisasi** berbeda untuk Tugas B dari nilai untuk Tugas A. 

  > [!NOTE]
  > Jika Anda menyelesaikan skenario ini menggunakan data demo Project Service Automation, pilih **Teknisi Jaringan** untuk peran, dan **fabrikam US** sebagai unit organisasi.

5. Simpan dan tutup halaman **Rincian Tugas**. 

## <a name="team-member-and-estimates-behavior"></a>Anggota tim dan estimasi perilaku 

1. Pada halaman **rincian tugas**, pada **anggota tim**, pilih dua anggota tim umum, lalu pilih **buat persyaratan**. 
2. Pilih baris anggota tim untuk **Pimpinan konsultasi** lalu pilih **Pesan**. Papan jadwal membuka dan memesan sumber daya untuk persyaratan tersebut.
3. Pilih baris anggota tim untuk **Teknisi Jaringan** lalu pilih **Pesan**. Papan jadwal membuka dan memesan sumber daya yang sama untuk persyaratan tersebut.

### <a name="team-member-grid"></a>Kisi anggota tim 
Pada kisi **anggota tim**, perhatikan bahwa dua rekaman anggota tim umum dihapus dan telah diganti menjadi satu sumber daya. Ada satu rangkaian nilai untuk sumber daya yang menampilkan rangkaian nilai default untuk **peran** dan **unit organisasi**.
Bila Anda memperluas baris rekaman anggota tim tersebut, Anda dapat melihat tugas yang berbeda pada rekaman anggota tim untuk kedua tugas tersebut. Setiap baris tugas memiliki nilai spesifik tugas untuk **Peran** dan **Unit Organisasi**. 

### <a name="estimates-grid"></a>Kisi Perkiraan 
Saat menavigasi kisi **Estimasi**, Anda akan melihat bahwa kedua tugas untuk sumber daya yang sama harganya berbeda.
Tugas untuk sumber daya pada tugas A harganya menggunakan nilai atribut **peran** **Pimpinan konsultasi**. Tugas untuk sumber daya yang sama pada tugas B harganya menggunakan nilai atribut **peran** **Teknisi Jaringan**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
