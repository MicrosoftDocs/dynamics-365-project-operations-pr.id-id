---
title: Mengisi staf proyek dengan pekerja kontrak dan kapasitas subkontrak
description: Artikel ini menjelaskan bagaimana persyaratan proyek dapat dikelola menggunakan pekerja kontrak atau kapasitas subkontrak di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522439"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Mengisi staf proyek dengan pekerja kontrak dan kapasitas subkontrak

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anggota tim proyek umum dapat dikelola dengan karyawan atau pekerja kontrak. Bila mengelola proyek dengan pekerja kontrak, Anda dapat membatasi pilihan pengelolaan pada pekerja kontrak tertentu yang ditetapkan ke baris subkontrak. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Mencari persyaratan sumber daya pengelolaan dengan pekerja kontrak yang memiliki baris subkontrak tertentu

Untuk mencari lan mengelola persyaratan sumber daya dengen pekerja yang dalam baris subkontrak tertentu, ikuti langkah-langkah ini:

1. Membuat anggota tim proyek generik yang mereferensikan subkontrak dan baris subkontrak.
2. Buat persyaratan sumber daya untuk anggota tim proyek generik ini dengan menggunakan tombol **Buat persyatatan** pada subkisi anggota tim proyek.
3. Pilih baris anggota tim, lalu pilih tombol **Buku** pada subkisi. 
4. Ini membuka Papan Jadwal dengan konteks persyatatan. Bersama atribut lainnya seperti tanggal, peran, dan bidang unit organisasi, filter Papan Jadwal juga secara otomatis diisi dengan bidang vendor, subkontrak, dan baris subkontrak dari persyaratan sumber daya.
5. Sistem mencari sumber daya yang memenuhi kriteria filter dan mencantumkannya. 
6. Pilih salah satu sumber daya terfilter dan pesan sumber daya untuk persyaratan. 
7. Anggota tim proyek yang dibuat dan diperbarui dengan referensi subkontrak dan baris subkontrak. Buka **Estimasi Proyek** dan pilih **Perbarui harga** untuk melihat biaya penugasan sumber daya yang diperbarui.. 

> [!NOTE]
> Memperbarui anggota tim proyek dengan referensi subkontrak dan baris subkontrak mungkin tidak selalu dapat dilakukan selama pemesanan jika sumber daya ditetapkan ke beberapa baris subkontrak. Jika sistem tidak dapat memperbarui anggota tim proyek dengan subkontrak dan baris subkontrak, buka rekaman anggota tim proyek dan perbarui bidang ini secara manual sehingga estimasi biaya keuangan mencerminkan biaya subkontraktor secara akurat.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Mencari dan mengelola persyaratan sumber daya dengan pekerja kontrak mana pun

Untuk mencari dan mengelola persyaratan sumber daya dengan setiap pekerja kontrak, ikuti langkah-langkah berikut:

1. Buat anggota tim proyek generik.
2. Buat persyaratan sumber daya untuk anggota tim proyek generik ini dengan menggunakan tombol **Buat persyatatan** pada subkisi anggota tim proyek.
3. Pilih baris anggota tim, lalu pilih tombol **Buku** pada subkisi. 
4. Ini membuka Papan Jadwal dengan konteks persyatatan. Bersama atribut lainnya seperti tanggal, peran, dan bidang unit organisasi, filter Papan Jadwal juga secara otomatis diisi dengan bidang vendor, subkontrak, dan baris subkontrak dari persyaratan sumber daya. Karena persyaratan tidak memiliki nilai subkontrak atau baris subkontrak yang diisi, atribut ini akan kosong di panel filter.
5. Sistem mencari sumber daya yang memenuhi kriteria filter dan mencantumkannya.
6. Perbarui bidang **Jenis pekerja** pada panel filter ke **Pekerja Kontrak** untuk membatasi pencarian pada pekerja kontrak. Perbarui **Vendor** pada panel filter untuk memilih vendor untuk membatasi pencarian agar hanya menampilkan pekerja kontrak milik perusahaan vendor tertentu.
7. Pilih pekerja kontrak dari daftar dan pesan sumber daya untuk persyaratan.
8. Anggota tim proyek telah dibuat. Namun, anggota tim proyek tidak diperbarui dengan subkontrak atau baris subkontrak apa pun dan karena itu penetapan sumber daya tidak akan dikenakan biaya menggunakan harga subkontrak. Perbarui anggota tim proyek dengan baris subkontrak secara manual, lalu buka **Estimasi Proyek**, lalu pilih **Perbarui harga** untuk melihat biaya penugasan sumber daya yang diperbarui.

> [!NOTE]
> Anggota tim proyek yang memiliki **Jenis pekerja** sebagai **Pekerja Kontrak** tetapi tidak memiliki referensi subkontrak ditandai sebagai **Tidak Valid** pada kisi **Anggota tim proyek**. Jika jika ada anggota tim proyek dengan status ini, buka rekaman anggota tim proyek dan secara manual memperbarui bidang subkontrak dan baris subkontrak sehingga estimasi biaya keuangan bisa secara akurat mencerminkan biaya subkontraktor pada tab **Estimasi**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
