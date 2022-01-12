---
title: Kepegawaian proyek dengan pekerja kontrak dan kapasitas subkontrak
description: Ini topik menjelaskan bagaimana persyaratan proyek dapat dikelola menggunakan pekerja kontrak atau kapasitas subkontrak di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903695"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Kepegawaian proyek dengan pekerja kontrak dan kapasitas subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Anggota tim proyek generik dapat dikelola dengan karyawan atau pekerja kontrak. Saat mengelola proyek dengan pekerja kontrak, Anda dapat membatasi opsi kepegawaian Anda untuk pekerja kontrak tertentu yang ditugaskan ke jalur subkontrak. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cari persyaratan sumber daya staf dengan pekerja kontrak yang termasuk dalam jalur subkontrak tertentu

Untuk mencari dan persyaratan sumber daya staf dengan pekerja kontrak yang termasuk dalam garis subkontrak tertentu, ikuti langkah-langkah berikut:

1. Buat anggota tim proyek generik yang mereferensikan garis subkontrak dan subkontrak.
2. Hasilkan persyaratan sumber daya untuk anggota tim proyek generik ini dengan menggunakan **tombol Generate requirement pada sub grid anggota tim** proyek.
3. Pilih baris anggota tim lalu pilih **tombol Buku** pada sub-kisi. 
4. Ini membuka Papan Jadwal dengan konteks persyaratan. Seiring dengan atribut lain seperti tanggal, peran, dan bidang unit organisasi, filter Papan Jadwal juga secara otomatis diisi dengan bidang vendor, subkontrak, dan baris subkontrak dari kebutuhan sumber daya.
5. Sistem mencari sumber daya yang memenuhi kriteria filter dan mencantumkannya. 
6. Pilih salah satu sumber daya yang disaring dan pesan sumber daya untuk persyaratan. 
7. Anggota tim proyek dibuat dan diperbarui dengan referensi baris subkontrak dan subkontrak. Buka **Perkiraan Proyek** dan pilih **Perbarui harga untuk melihat biaya yang diperbarui** dari penugasan sumber daya. 

> [!NOTE]
> Memperbarui anggota tim proyek dengan referensi baris subkontrak dan subkontrak mungkin tidak selalu mungkin selama pemesanan jika sumber daya ditugaskan ke beberapa baris subkontrak. Jika sistem tidak dapat memperbarui anggota tim proyek dengan garis subkontrak dan subkontrak, maka buka catatan anggota tim proyek dan perbarui bidang-bidang ini secara manual sehingga perkiraan biaya keuangan secara akurat mencerminkan biaya subkontraktor.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Mencari dan persyaratan sumber daya staf dengan pekerja kontrak apa pun

Untuk mencari dan persyaratan sumber daya staf dengan pekerja kontrak, ikuti langkah-langkah berikut:

1. Buat anggota tim proyek generik.
2. Hasilkan persyaratan sumber daya untuk anggota tim proyek generik ini dengan menggunakan **tombol Generate requirement pada sub grid anggota tim** proyek.
3. Pilih baris anggota tim lalu pilih **tombol Buku** pada sub-kisi. 
4. Ini membuka Papan Jadwal dengan konteks persyaratan. Seiring dengan atribut lain seperti tanggal, peran, dan bidang unit organisasi, filter Papan Jadwal juga secara otomatis diisi dengan bidang vendor, subkontrak, dan baris subkontrak dari kebutuhan sumber daya. Karena persyaratan tidak memiliki nilai baris subkontrak atau subkontrak yang diisi, atribut ini akan kosong di panel filter.
5. Sistem mencari sumber daya yang memenuhi kriteria filter dan mencantumkannya.
6. Perbarui **bidang tipe Pekerja di panel filter ke Pekerja Kontrak untuk membatasi pencarian kepada pekerja** **kontrak**. Perbarui **Vendor pada panel filter untuk memilih vendor untuk membatasi pencarian hanya menampilkan pekerja kontrak milik perusahaan vendor** tertentu.
7. Pilih pekerja kontrak dari daftar dan pesan sumber daya untuk persyaratan.
8. Seorang anggota tim proyek dibuat. Namun, anggota tim proyek tidak diperbarui dengan baris subkontrak atau subkontrak dan oleh karena itu penugasan sumber daya tidak akan dikenakan biaya menggunakan harga subkontrak. Perbarui anggota tim proyek secara manual dengan baris subkontrak dan buka **Perkiraan Proyek dan pilih** **Perbarui harga untuk melihat biaya yang** diperbarui dari penugasan sumber daya.

> [!NOTE]
> Anggota tim proyek yang memiliki **tipe Pekerja sebagai pekerja Kontrak tetapi tidak memiliki referensi** **subkontrak** ditandai sebagai **Tidak Valid pada jaringan anggota tim** **Proyek**. Jika ada anggota tim proyek dengan status ini, buka catatan anggota tim proyek dan perbarui bidang garis subkontrak dan subkontrak secara manual sehingga perkiraan biaya keuangan secara akurat mencerminkan biaya subkontraktor pada **tab** Perkiraan. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
