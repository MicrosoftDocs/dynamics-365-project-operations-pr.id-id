---
title: Memecahkan masalah penanganan kisi Tugas
description: Artikel ini menyediakan informasi pemecahan masalah yang diperlukan saat bekerja di kisi Tugas.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911048"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Memecahkan masalah penanganan kisi Tugas 


_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-persediaan, penyebaran Lite - faktur penawaran hingga proforma, Project for the Web_

Kisi tugas yang dimanfaatkan adalah Dynamics 365 Project Operations adalah iframe yang di-host dalam Microsoft Dataverse. Oleh karena itu, persyaratan khusus harus dipenuhi untuk memastikan otentikasi dan otorisasi berfungsi dengan benar. Artikel ini menguraikan masalah umum yang dapat memengaruhi kemampuan untuk merender grid atau mengelola tugas dalam struktur rincian kerja (WBS).

Masalah umum mencakup:

- Tab **Tugas** di kisi Tugas kosong.
- Saat membuka proyek, proyek tidak dimuat dan antarmuka (UI) pengguna terjebak pada spinner.
- Administrasi hak istimewa untuk **Project for the Web**.
- Perubahan tidak disimpan saat Anda membuat, memperbarui, atau menghapus tugas.

## <a name="issue-the-task-tab-is-empty"></a>Masalah: Tab Tugas kosong

### <a name="mitigation-1-enable-cookies"></a>Mitigasi 1: Aktifkan cookie

Project Operations mengharuskan cookie pihak ketiga diaktifkan untuk membuat struktur rincian kerja. Bila cookie pihak ketiga tidak diaktifkan, bukan melihat tugas, Anda akan melihat halaman kosong saat memilih tab **Tugas** di halaman **Proyek**.

Untuk Microsoft Edge atau browser Google Chrome, prosedur berikut menjelaskan cara memperbarui pengaturan browser Anda untuk mengaktifkan cookie pihak ketiga.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Buka browser Edgé Anda.
2. Di sudut kanan atas, pilih **elipsis (...)**, lalu pilih **pengaturan**.
3. Dalam **Cookie dan izin situs**, pilih **Cookie dan data situs**.
4. Nonaktifkan **Blokir cookie pihak ketiga**.
5. Refresh browser Anda. 

#### <a name="google-chrome"></a>Google Chrome

1. Buka browser Chrome Anda.
2. Di sudut kanan atas, pilih tiga titik vertikal, lalu pilih **pengaturan**.
3. Dalam **Privasi dan keamanan**, pilih **Cookie dan data situs lainnya**.
4. Pilih **Izinkan semua cookie**.
5. Refresh browser Anda. 

> [!NOTE]
> Jika Anda memblokir cookie pihak ketiga, semua cookie dan data situs dari situs lain akan diblokir, meskipun situs diizinkan pada daftar pengecualian Anda.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mitigasi 2: Validasikan titik akhir PEX telah dikonfigurasi dengan benar

Project Operations mengharuskan parameter proyek mereferensi titik akhir PEX. Titik akhir diperlukan untuk berkomunikasi dengan layanan yang digunakan untuk membuat struktur rincian kerja. Jika parameter tidak diaktifkan, Anda akan menerima kesalahan, "Parameter proyek tidak valid". Untuk memperbarui titik akhir PEX, selesaikan langkah-langkah berikut.

1. Tambahkan bidang **titik akhir** PEX ke halaman **Parameter Proyek**.
2. Identifikasikan jenis produk yang Anda gunakan. Nilai ini digunakan saat titik akhir PEX diatur. Setelah pengambilan, jenis produk sudah ditentukan di titik akhir PEX. Pertahankan nilai tersebut.
3. Perbarui bidang dengan nilai berikut ini: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Tabel berikut menyediakan parameter jenis yang harus digunakan berdasarkan jenis produk.

      | **Jenis Produk**                     | **Jenis Parameter** |
      |--------------------------------------|--------------------|
      | Project for the Web di organisasi Default   | type=0             |
      | Project for the Web di organisasi bernama CDS | type=1             |
      | Project Operations                   | type=2             |

4. Hilangkan bidang dari halaman **Parameter Proyek**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Mitigasi 3: masuk ke project.microsoft.com
Di browser Anda Microsoft Edge, buka tab baru, buka project.microsoft.com, dan masuk dengan menggunakan peran pengguna yang Anda gunakan untuk mengakses Operasi Proyek.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Masalah: Proyek tidak dimuat dan UI terjebak pada spinner

Untuk tujuan otentikasi, pop-up harus diaktifkan agar kisi Tugas dapat dimuat. Jika pop-up tidak diaktifkan, layar akan terjebak pada spinner pemuatan. Grafis berikut menunjukkan URL dengan label pop-up diblokir di bilah alamat yang mengakibatkan spinner terjebak mencoba memuat halaman. 

   ![Spinner terjebak dan blokir pop-up.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mitigasi 1: Aktifkan pop-up

Bila proyek Anda terjebak pada spinner, kemungkinan pop-up tidak diaktifkan.

#### <a name="microsoft-edge"></a>Microsoft Edge

Ada dua cara untuk mengaktifkan pop-up di browser Edge Anda.

1. Di browser Edge, pilih pemberitahuan di kanan atas browser.
2. Pilih **Selalu izinkan popup dan pengalihan dari** lingkungan Dataverse tertentu.
 
     ![Jendela pop-up diblokir.](media/enablepopups.png)

Selain itu, Anda dapat menyelesaikan langkah-langkah berikut.

1. Buka browser Edgé Anda.
2. Di sudut kanan atas, pilih **elipsis** (...), lalu pilih **Pengaturan** > **Izin situs** > **Pop-up dan pengalihan**.
3. Matikan **Pop-up dan pengalihan** untuk memblokir pop-up atau hidupkan izinkan pop-up di perangkat Anda.
4. Setelah mengaktifkan pop-up, refresh browser Anda. 

#### <a name="google-chrome"></a>Google Chrome
1. Buka browser Chrome Anda.
2. Telusuri ke halaman dengan pop-up diblokir.
3. Di bilah alamat, pilih **Pop-up diblokir**.
4. Pilih tautan untuk pop-up yang ingin dilihat.
5. Setelah mengaktifkan pop-up, refresh browser Anda. 

> [!NOTE]
> Untuk selalu melihat pop-up situs, pilih **Selalu izinkan pop-up dan pengalihan dari [situs]** dan kemudian pilih **Selesai**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Masalah 3: Administrasi hak istimewa untuk Project for the Web

Project Operations mengandalkan layanan penjadwalan eksternal. Layanan mengharuskan pengguna memiliki beberapa peran yang ditetapkan yang memungkinkan mereka membaca dan menulis ke entitas yang terkait dengan WBS. Entitas ini mencakup tugas proyek, penugasan sumber daya, dan dependensi tugas. Jika pengguna tidak dapat menampilkan WBS saat mereka menelusuri ke tab **Tugas**, kemungkinan karena **Proyek** for **Project Operations** belum diaktifkan. Pengguna mungkin menerima pesan kesalahan peran keamanan, atau kesalahan yang terkait dengan ditolaknya akses.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mitigasi 1: Memvalidasi peran keamanan pengguna dan pengguna akhir aplikasi

1. Buka **Pengaturan** > **Keamanan** > **Pengguna** > **Pengguna Aplikasi**.  

   ![Pembaca aplikasi.](media/applicationuser.jpg)
   
2. Klik dua kali rekaman pengguna aplikasi untuk memverifikasi:

     - Pengguna memiliki akses ke proyek. Anda dapat melakukannya dengan memverifikasi bahwa pengguna memiliki peran keamanan **Manajer Proyek**.
     - Pengguna aplikasi Microsoft Project ada dan dikonfigurasi dengan benar.
 
3. Jika pengguna ini tidak ada, buat rekaman pengguna baru. 
4. Pilih **Pengguna Baru**, ubah formulir entri ke **Pengguna Aplikasi**, lalu tambahkan **ID Aplikasi**.

   ![Rincian pengguna aplikasi.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Masalah 4: Perubahan tidak disimpan saat Anda membuat, memperbarui, atau menghapus tugas

Bila Anda membuat satu atau beberapa pembaruan ke WBS, perubahan tersebut akan gagal dan tidak disimpan. Kesalahan terjadi di kisi jadwal dengan pesan yang mengatakan, "Perubahan terakhir yang Anda buat tidak dapat disimpan".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mitigasi 1: Validasikan penetapan lisensi

1. Verifikasikan bahwa pengguna telah menerima lisensi yang benar dan layanan diaktifkan dalam rincian paket layanan lisensi.  
2. Pastikan pengguna dapat membuka **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mitigasi 2: Konfigurasi validasi pengguna aplikasi Project
1. Verifikasikan bahwa pengguna aplikasi proyek telah dibuat.
2. Terapkan peran keamanan berikut ke pengguna:
  
  - Pengguna Dataverse atau Pengguna dasar
  - Sistem Project Operations
  - Sistem proyek
  - Sistem Penulisan Ganda Project Operations. Peran ini diperlukan untuk skenario berbasis sumber daya/tanpa stok Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
