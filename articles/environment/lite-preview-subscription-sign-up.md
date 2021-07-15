---
title: Mendaftar untuk berlangganan pratinjau - lite
description: Topik ini menyediakan informasi tentang cara berlangganan dan menyebarkan penawaran penyebaran Project operation lite ke faktur proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334786"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Mendaftar untuk berlangganan pratinjau - lite 

Topik ini menjelaskan cara berlangganan penawaran uji coba dan menyebarkan penyebaran Dynamics 365 Project Operations lite - kesepakatan hingga faktur proforma.

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

1. Lakukan penyediaan lingkungan penyebaran Project Operations Dataverse baru dengan mengikuti petunjuk dalam topik, [model penyebaran Dataverse](lite-deployment.md). Saat Anda memilih tipe lingkungan, pastikan untuk menggunakan **Uji coba (Berbasis langganan)**.

  ![Lingkungan baru](./media/19CreateEnvironment.png)

2. Pilih pengaturan **Aktifkan aplikasi Dynamics 365** dan biarkan **Sebarkan Aplikasi ini secara otomatis** kosong.  
3. Pilih **Simpan** untuk membuat lingkungan.

  ![Tambahkan database](./media/20CreateEnvironment1.png)

4. Setelah lingkungan dibuat, instal solusi **Microsoft Dynamics 365 Project Operations**. 

![Instal Solusi](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instal konfigurasi CDS dan data demo konfigurasi

Instal konfigurasi CDS dan konfigurasikan data demo dengan mengikuti petunjuk dalam topik, [terapkan konfigurasi demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
