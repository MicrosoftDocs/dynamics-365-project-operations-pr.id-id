---
title: Mengisi staf proyek dengan pekerja kontrak dan kapasitas subkontrak
description: Ini topik menjelaskan bagaimana persyaratan proyek dapat dikelola menggunakan pekerja kontrak atau kapasitas subkontrak di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574646"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Mengisi staf proyek dengan pekerja kontrak dan kapasitas subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Anggota tim proyek generik dapat dikelola dengan karyawan atau pekerja kontrak. Saat mengelola proyek dengan pekerja kontrak, Anda dapat membatasi opsi kepegawaian Anda untuk pekerja kontrak tertentu yang ditugaskan ke jalur subkontrak. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Mencari persyaratan sumber daya staf dengan pekerja kontrak yang termasuk dalam jalur subkontrak tertentu

Untuk mencari dan persyaratan sumber daya staf dengan pekerja kontrak yang termasuk dalam jalur subkontrak tertentu, ikuti langkah-langkah berikut:

1. Buat anggota tim proyek generik yang merujuk pada subkontrak dan subkontrak.
2. Buat persyaratan sumber daya untuk anggota tim proyek generik ini dengan **menggunakan tombol Hasilkan persyaratan** pada sub kisi anggota tim proyek.
3. Pilih baris anggota tim lalu pilih tombol **Buku** di sub kisi. 
4. Ini membuka Papan Jadwal dengan konteks persyaratan. Seiring dengan atribut lain seperti tanggal, peran, dan bidang unit organisasi, filter Papan Jadwal juga secara otomatis diisi dengan bidang vendor, subkontrak, dan subkontrak dari kebutuhan sumber daya.
5. Sistem mencari sumber daya yang memenuhi kriteria filter dan mencantumkannya. 
6. Pilih salah satu sumber daya yang difilter dan pesan sumber daya untuk persyaratan tersebut. 
7. Anggota tim proyek dibuat dan diperbarui dengan referensi subkontrak dan subkontrak. Buka **Perkiraan** Proyek dan pilih **Perbarui harga** untuk melihat biaya penetapan sumber daya yang diperbarui. 

> [!NOTE]
> Memperbarui anggota tim proyek dengan referensi subkontrak dan subkontrak mungkin tidak selalu dimungkinkan selama pemesanan jika sumber daya ditugaskan ke beberapa jalur subkontrak. Jika sistem tidak dapat memperbarui anggota tim proyek dengan jalur subkontrak dan subkontrak, maka buka catatan anggota tim proyek dan perbarui bidang ini secara manual sehingga perkiraan biaya keuangan secara akurat mencerminkan biaya subkontraktor.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Mencari dan persyaratan sumber daya staf dengan pekerja kontrak mana pun

Untuk mencari dan persyaratan sumber daya staf dengan pekerja kontrak mana pun, ikuti langkah-langkah berikut:

1. Buat anggota tim proyek generik.
2. Buat persyaratan sumber daya untuk anggota tim proyek generik ini dengan **menggunakan tombol Hasilkan persyaratan** pada sub kisi anggota tim proyek.
3. Pilih baris anggota tim lalu pilih tombol **Buku** di sub kisi. 
4. Ini membuka Papan Jadwal dengan konteks persyaratan. Seiring dengan atribut lain seperti tanggal, peran, dan bidang unit organisasi, filter Papan Jadwal juga secara otomatis diisi dengan bidang vendor, subkontrak, dan subkontrak dari kebutuhan sumber daya. Karena persyaratan tidak memiliki nilai subkontrak atau subkontrak baris yang diisi, atribut ini akan kosong di panel filter.
5. Sistem mencari sumber daya yang memenuhi kriteria filter dan mencantumkannya.
6. **Perbarui bidang tipe** Pekerja di panel filter ke **Pekerja** Kontrak untuk membatasi pencarian kepada pekerja kontrak. Perbarui **Vendor** di panel filter untuk memilih vendor untuk membatasi pencarian agar hanya menampilkan pekerja kontrak milik perusahaan vendor tertentu.
7. Pilih pekerja kontrak dari daftar dan pesan sumber daya untuk kebutuhan tersebut.
8. Anggota tim proyek dibuat. Namun, anggota tim proyek tidak diperbarui dengan subkontrak atau subkontrak dan oleh karena itu penugasan sumber daya tidak akan dikenakan biaya menggunakan harga subkontrak. Perbarui anggota tim proyek secara manual dengan jalur subkontrak dan buka **Perkiraan** Proyek dan pilih **Perbarui harga** untuk melihat biaya penugasan sumber daya yang diperbarui.

> [!NOTE]
> Anggota tim proyek yang memiliki **tipe** Pekerja sebagai **pekerja** Kontrak tetapi tidak memiliki referensi subkontrak ditandai sebagai **Tidak Valid** pada **kisi anggota** tim Proyek. Jika ada anggota tim proyek dengan status ini, buka catatan anggota tim proyek dan perbarui bidang jalur subkontrak dan subkontrak secara manual sehingga perkiraan biaya keuangan secara akurat mencerminkan biaya subkontraktor pada **tab Perkiraan**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
