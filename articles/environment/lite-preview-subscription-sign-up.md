---
title: Mendaftar untuk berlangganan pratinjau - lite
description: Artikel ini menyediakan informasi tentang cara berlangganan dan menyebarkan penyebaran Project Operations lite - berurusan dengan faktur proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6953956c0b3401a6c64ee597f966ba4a4c0d07b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921260"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Mendaftar untuk berlangganan pratinjau - lite 

Artikel ini menjelaskan cara berlangganan penawaran uji coba dan menyebarkan Dynamics 365 Project Operations penyebaran lite - berurusan dengan faktur proforma.

> [!NOTE]
> Proses ini akan berubah di rilis mendatang Project Operations.

## <a name="prerequisites"></a>Prasyarat
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure. Anda dapat membuat penyewa selama penukaran penawaran pertama.

> [!IMPORTANT]
> Hanya satu orang, administrator penyewa, dalam organisasi harus melakukan tugas ini. Jika Anda bukan pelanggan untuk rilis ini, tunggu hingga organisasi Anda telah terdaftar dan Anda telah menerima kredensial pengguna Anda.
> 
> Uji coba hanya digunakan satu kali dalam penyewa. Anda hanya dapat menjalankan uji coba satu kali. Sebaiknya buat penyewa baru untuk tujuan uji coba.

### <a name="dynamics-365-project-operations-trial"></a>Uji Coba Dynamics 365 Project Operations 

Sebelum memulai, pastikan Anda masuk ke browser dengan akun kerja pengguna di penyewa tempat Anda menginginkan pratinjau Project Operations.

1. Buka [Uji coba Project Operations](https://aka.ms/try-po) untuk menukarkan kode penawaran pertama, **Dynamics 365 Project Operations**.
2. Konfirmasikan pesanan.

  Anda akan melihat penawaran konfirmasi berhasil ditukarkan.

## <a name="assign-licenses"></a>Menetapkan lisensi

> [!IMPORTANT]
> Anda akan memerlukan akses administratif ke Portal Microsoft 365 organisasi Anda untuk menyelesaikan langkah-langkah berikut.


1. Buka [Microsoft 365 pusat](https://portal.office.com/) admin untuk menetapkan lisensi kepada pengguna Anda.
2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.
3. Pastikan lisensi **Dynamics 365 Project Operations** dipilih. 
4. Pilih **Simpan perubahan**.

## <a name="create-a-new-dataverse-environment"></a>Buat lingkungan Dataverse baru

1. Sediakan lingkungan penyebaran Operasi Dataverse Proyek baru dengan mengikuti instruksi dalam artikel, [Dataverse model penyebaran](lite-deployment.md). Saat Anda memilih tipe lingkungan, pastikan untuk menggunakan **Uji coba (Berbasis langganan)**.

  ![Lingkungan baru.](./media/19CreateEnvironment.png)

2. Pilih pengaturan **Aktifkan aplikasi Dynamics 365** dan biarkan **Sebarkan Aplikasi ini secara otomatis** kosong.  
3. Pilih **Simpan** untuk membuat lingkungan.

  ![Tambahkan database.](./media/20CreateEnvironment1.png)

4. Setelah lingkungan dibuat, instal solusi **Microsoft Dynamics 365 Project Operations**. 

![Instal Solusi.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instal konfigurasi CDS dan data demo konfigurasi

Instal konfigurasi CDS dan atur data demo dengan mengikuti instruksi dalam artikel, [Terapkan pengaturan demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
