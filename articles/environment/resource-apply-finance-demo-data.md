---
title: Menerapkan data demo ke lingkungan di-host Finance cloud
description: Artikel ini menjelaskan cara menerapkan data demo dari Project Operations ke lingkungan yang Dynamics 365 Finance dihosting Cloud.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 4ce53c171929f0610c53025becaebea46d902c90
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924664"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Menerapkan data demo ke lingkungan di-host Finance cloud

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

> [!IMPORTANT]
> Artikel ini hanya berlaku untuk Microsoft Dynamics 365 Finance versi 10.0.13 dan hanya dapat dilakukan di lingkungan yang dihosting Cloud. Selesaikan langkah-langkah dalam artikel **ini SEBELUM** Anda menerapkan pembaruan kualitas ke lingkungan.

1. Di proyek LCS, buka halaman **rincian lingkungan**. Perhatikan bahwa ini mencakup rincian yang diperlukan untuk menyambung ke lingkungan dengan menggunakan Remote Desktop Protocol (RDP).

![Rincian lingkungan.](./media/1EnvironmentDetails.png)

Set pertama kredensial yang disorot adalah kredensial akun lokal dan berisi hyperlink ke sambungan desktop jarak jauh. Kredensial mencakup nama pengguna dan sandi admin lingkungan. Rangkaian kredensial kedua digunakan untuk masuk ke SQL Server di lingkungan ini.

2. Sambungkan ke lingkungan dengan hyperlink di **akun lokal**, dan gunakan **kredensial akun lokal** untuk mengautentikasi.
3. Buka **layanan informasi Internet** > **kumpulan aplikasi** > **AOSService** dan Hentikan layanan. Anda menghentikan layanan pada titik ini sehingga Anda dapat melanjutkan untuk mengganti database SQL.

![Hentikan AOS.](./media/2StopAOS.png)

4. Buka **Layanan** dan Hentikan dua item berikut:

- Microsoft Dynamics 365 Unified Operations: Layanan Manajemen batch
- Microsoft Dynamics 365 Unified Operations: kerangka impor ekspor data

![Hentikan Layanan.](./media/3StopServices.png)

5. Buka Microsoft SQL Server Management Studio. Masuk dengan kredensial SQL Server dan gunakan pengguna dan sandi axdbadmin dari halaman **rincian lingkungan** LCS.

![SQL Server Management Studio.](./media/4SSMS.png)

6. Di object Explorer, **database** dan Cari **AXDB**. Anda akan mengganti database dengan database baru yang terletak di [pusat Unduh](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Salin file zip ke VM yang mana Anda terhubung dari jarak jauh dan ekstrak konten zip.
8. Di SQL Server Management Studio, klik kanan **axdb**, dan kemudian pilih **tugas** > **Pulihkan** > **database**.

![Mengembalikan database.](./media/5RestoreDatabase.png)

9. Pilih **perangkat sumber** dan navigasikan ke file yang diekstrak dari zip yang disalin.

![Perangkat sumber.](./media/6SourceDevice.png)

10. Pilih **pilihan**, lalu pilih **Timpa database yang ada** dan **tutup koneksi yang ada ke database tujuan**. 
11. Pilih **OK**.

![Pulihkan Pengaturan.](./media/7RestoreSetting.png)

Anda akan menerima konfirmasi bahwa pemulihan AXDB berhasil. Setelah menerima konfirmasi ini, Anda dapat menutup SQL Services Management Studio.

12. Kembali ke **layanan informasi Internet** > **kumpulan aplikasi** > **AOSService** dan mulai AOSService.
13. Buka **Layanan** dan mulai dua layanan yang Anda Hentikan sebelumnya.

14. Cari alat AdminUserProvisioning pada VM ini. Lihat ke bawah, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Jalankan file .ext menggunakan alamat pengguna di bidang **alamat email**. 
16. Pilih **kirim**.

![Penyediaan Sandi Admin.](./media/8AdminUserProvisioning.png)

Hal ini berlangsung selama beberapa menit. Anda akan menerima pesan konfirmasi bahwa pengguna admin berhasil diperbarui.

17. Terakhir, Jalankan Command Prompt sebagai administrator dan lakukan iisreset

![Reset IIS.](./media/9IISReset.png)

18. Tutup sesi desktop jarak jauh dan gunakan halaman **rincian lingkungan** LCS untuk masuk ke lingkungan untuk mengkonfirmasi sudah berfungsi seperti yang diharapkan.

![Keuangan dan Operasi.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]