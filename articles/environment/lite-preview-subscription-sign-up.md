---
title: Mendaftar untuk berlangganan pratinjau - lite
description: Artikel ini menyediakan informasi tentang cara berlangganan dan menyebarkan penawaran penyebaran Project Operations lite ke faktur proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410037"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Mendaftar untuk berlangganan pratinjau - lite 

Artikel ini menjelaskan cara berlangganan penawaran uji coba dan menyebarkan penyebaran Dynamics 365 Project Operations lite - kesepakatan hingga faktur proforma.

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


1. Buka [Pusat admin Microsoft 365](https://portal.office.com/) untuk menetapkan lisensi kepada pengguna.
2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.
3. Pastikan lisensi **Dynamics 365 Project Operations** dipilih. 
4. Pilih **Simpan perubahan**.

## <a name="create-a-new-dataverse-environment"></a>Buat lingkungan Dataverse baru

1. Lakukan penyediaan lingkungan penyebaran Project Operations Dataverse baru dengan mengikuti petunjuk dalam artikel, [model penyebaran Dataverse](lite-deployment.md). Saat Anda memilih tipe lingkungan, pastikan untuk menggunakan **Uji coba (Berbasis langganan)**.

  ![Lingkungan baru.](./media/19CreateEnvironment.png)

2. Pilih pengaturan **Aktifkan aplikasi Dynamics 365** dan biarkan **Sebarkan Aplikasi ini secara otomatis** kosong.  
3. Pilih **Simpan** untuk membuat lingkungan.

  ![Tambahkan database.](./media/20CreateEnvironment1.png)

4. Setelah lingkungan dibuat, instal solusi **Microsoft Dynamics 365 Project Operations**. 

![Instal Solusi.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Konfigurasikan data demo

Konfigurasikan data demo dengan mengikuti petunjuk dalam artikel, [terapkan konfigurasi demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
