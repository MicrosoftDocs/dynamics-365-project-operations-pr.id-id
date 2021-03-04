---
title: Memecahkan masalah penanganan kisi Tugas
description: Pembaruan topik memberikan informasi pemecahan masalah yang diperlukan saat menangani kisi Tugas.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031541"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Memecahkan masalah penanganan kisi Tugas 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Deskripsi topik menjelaskan cara memperbaiki masalah yang mungkin Anda temui saat menangani manajemen biaya.

## <a name="enable-cookies"></a>Aktifkan Cookie

Project Operations mengharuskan cookie pihak ketiga diaktifkan untuk membuat struktur perincian kerja. Bila cookie pihak ketiga tidak diaktifkan, bukan melihat tugas, Anda akan melihat halaman kosong saat memilih tab **Tugas** di halaman **Proyek**.

![Tab kosong bila cookie pihak ketiga tidak diaktifkan](media/blankschedule.png)


### <a name="workaround"></a>Solusi
Untuk Microsoft Edge atau browser Google Chrome, prosedur berikut menjelaskan cara memperbarui pengaturan browser Anda untuk mengaktifkan cookie pihak ketiga.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Buka browser Edge Anda.
2. Di sudut kanan atas, pilih **elipsis (...)**, lalu pilih **pengaturan**.
3. Dalam **Cookie dan izin situs**, pilih **Cookie dan data situs**.
4. Nonaktifkan **Blokir cookie pihak ketiga**.

#### <a name="google-chrome"></a>Google Chrome

1. Buka browser Chrome Anda.
2. Di sudut kanan atas, pilih tiga titik vertikal, lalu pilih **pengaturan**.
3. Dalam **Privasi dan keamanan**, pilih **Cookie dan data situs lainnya**.
4. Pilih **Izinkan semua cookie**.

> [!IMPORTANT]
> Jika Anda memblokir cookie pihak ketiga, semua cookie dan data situs dari situs lain akan diblokir, meskipun situs diizinkan pada daftar pengecualian Anda.

## <a name="pex-endpoint"></a>Titik Akhir PEX

Project Operations mengharuskan parameter proyek mereferensi titik akhir PEX. Titik akhir ini diperlukan untuk berkomunikasi dengan layanan yang digunakan untuk membuat struktur rincian kerja. Jika parameter tidak diaktifkan, Anda akan menerima kesalahan, "Parameter proyek tidak valid". 

### <a name="workaround"></a>Solusi
 ![Bidang titik akhir PEX pada parameter proyek](media/projectparameter.png)

1. Tambahkan bidang **titik akhir** PEX ke halaman **Parameter Proyek**.
2. Perbarui bidang dengan nilai berikut ini: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Hilangkan bidang dari halaman **Parameter Proyek**.

## <a name="privileges-for-project-for-the-web"></a>Hak istimewa untuk Proyek untuk Web

Project Operations mengandalkan layanan penjadwalan eksternal. Layanan mengharuskan pengguna memiliki beberapa peran yang ditetapkan untuk membaca dan menulis ke entitas yang terkait dengan struktur rincian kerja. Entitas ini mencakup tugas proyek, penugasan sumber daya, dan dependensi tugas. Jika pengguna tidak dapat menampilkan struktur rincian kerja saat membuka tab **Tugas**, kemungkinan karena Proyek untuk Project Operations belum diaktifkan. Pengguna mungkin menerima pesan kesalahan peran keamanan, atau kesalahan yang terkait dengan ditolaknya akses.


## <a name="workaround"></a>Solusi

1. Buka **Pengaturan > Keamanan > Pengguna > Pengguna Aplikasi**.  

   ![Pembaca aplikasi](media/applicationuser.jpg)
   
2. Klik dua kali rekaman pengguna aplikasi untuk memverifikasi berikut ini:

 - Pengguna memiliki akses ke proyek. Verifikasi ini biasanya dilakukan dengan memastikan bahwa pengguna memiliki peran keamanan **Manajer Proyek**.
 - Pengguna aplikasi Microsoft Project ada dan dikonfigurasi dengan benar.
 
3. Jika pengguna ini tidak ada, Anda dapat membuat rekaman pengguna yang baru. Pilih **pengguna baru**. Ubah formulir entri ke **Pengguna Aplikasi**, lalu tambahkan **ID Aplikasi**.

   ![Rincian pengguna aplikasi](media/applicationuserdetails.jpg)

4. Verifikasikan bahwa pengguna telah menerima lisensi yang benar dan layanan diaktifkan dalam rincian paket layanan lisensi.
5. Pastikan pengguna dapat membuka project.microsoft.com.
6. Verifikasikan melalui parameter proyek bahwa sistem mengarah ke titik akhir proyek yang benar.
7. Verifikasikan bahwa pengguna aplikasi proyek dibuat.
8. Terapkan peran keamanan berikut ke pengguna:

  - Pengguna Dataverse
  - Sistem Project Operations
  - Sistem proyek

## <a name="error-when-updating-the-work-breakdown-structure"></a>Kesalahan saat memperbarui struktur rincian kerja

Ketika satu atau beberapa pembaruan dibuat pada struktur rincian kerja, perubahan pada akhirnya gagal dan tidak disimpan. Kesalahan terjadi di kisi jadwal yang menyatakan bahwa "Perubahan terbaru yang anda buat tidak dapat disimpan".

### <a name="workaround"></a>Solusi

1. Verifikasikan bahwa pengguna telah menerima lisensi yang benar dan layanan diaktifkan dalam rincian paket layanan lisensi.
2. Pastikan pengguna dapat membuka project.microsoft.com.
3. Verifikasikan bahwa sistem mengarah ke titik akhir proyek yang benar.
4. Verifikasikan bahwa pengguna aplikasi proyek telah dibuat.
5. Terapkan peran keamanan berikut ke pengguna:
  
  - Pengguna dasar atau Pengguna Dataverse
  - Sistem Project Operations
  - Sistem proyek
  - Sistem Tulis Ganda Project Operations (Peran ini diperlukan jika Anda menyebarkan skenario berbasis sumber daya/non-stok Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]