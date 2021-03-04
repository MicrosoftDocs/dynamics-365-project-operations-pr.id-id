---
title: Mendaftar untuk berlangganan pratinjau - lite
description: Topik ini menyediakan informasi tentang cara berlangganan dan menyebarkan penawaran penyebaran Project operation lite ke faktur proforma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175895"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Mendaftar untuk berlangganan pratinjau - lite 

Topik ini menjelaskan cara berlangganan penawaran mitra pratinjau dan menyebarkan Dynamics 365 Project operation lite ke faktur proforma.

> [!NOTE]
> Proses ini akan berubah di rilis mendatang Project Operations.

## <a name="prerequisites"></a>Prasyarat

- Anda akan menerima email yang mengundang Anda untuk berpartisipasi dalam pratinjau. Anda dapat meminta pratinjau di [situs web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure.
- Tinjau semua persyaratan dan ketentuan.

## <a name="subscribe"></a>Berlangganan

Bila Anda menerima persetujuan [permintaan pratinjau](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), Anda akan menerima dua tawaran dari Microsoft melalui email. Penawaran ini memungkinkan Anda menyebarkan pratinjau Project Operations:

- Dynamics 365 Project Operations (CRM) - Uji coba Pratinjau
- Office 365 Project Operations - Uji coba Pratinjau

> [!IMPORTANT]
> Hanya satu orang, administrator penyewa, dalam organisasi harus melakukan tugas ini. Jika Anda bukan pelanggan untuk rilis ini, tunggu hingga organisasi Anda telah terdaftar dan Anda telah menerima kredensial pengguna Anda.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - Uji coba Pratinjau 

Sebelum memulai, pastikan Anda masuk ke browser dengan akun kerja pengguna di penyewa tempat Anda menginginkan pratinjau Project Operations.

1. Tukarkan kode penawaran pertama, **Dynamics 365 Project Operations (CRM) - Uji Coba Pratinjau** dengan menempelkannya ke URL browser.

![Tukarkan penawaran](./media/16RedeemFirstOfferNew.png)

2. Konfirmasikan pesanan.
![Konfirmasi pesanan](./media/17ConfirmOrderNew.png)

Anda akan melihat penawaran konfirmasi berhasil ditukarkan.

![Konfirmasi](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Uji coba Pratinjau

Ulangi langkah yang sama seperti dengan kode penawaran pertama. Pastikan untuk menambahkan kode penawaran kedua menggunakan akun pengguna yang sama yang digunakan dengan kode penawaran pertama.

## <a name="assign-licenses"></a>Menetapkan lisensi

> [!IMPORTANT]
> Anda akan memerlukan akses administratif ke Portal Microsoft 365 organisasi Anda untuk menyelesaikan langkah-langkah berikut.


1. Buka [Pusat admin Microsoft 365](https://portal.office.com/) untuk menetapkan lisensi kepada pengguna.

![Halaman Beranda pusat Admin](./media/14AdminPortal.png)

2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.

![Menetapkan lisensi](./media/15AssignLicenses.png)

3. Verifikasi bahwa Lisensi **Pratinjau Dynamics 365 Project Operations (CRM)** dan **Office 365 Project Operations - pratinjau** dipilih. 
4. Pilih **Simpan perubahan**.

## <a name="create-a-new-cds-environment"></a>Buat lingkungan CDS baru

1. LakukanPara Pihakenyediaan lingkungan penyebaran cds Project Operations baru dengan mengikuti petunjuk dalam topik, [model penyebaran cds](lite-deployment.md). Saat Anda memilih tipe lingkungan, pastikan untuk menggunakan **Uji coba (Berbasis langganan)**.
![Lingkungan baru](./media/19CreateEnvironment.png)

2. Pilih pengaturan **Aktifkan aplikasi Dynamics 365** dan biarkan **Sebarkan Aplikasi ini secara otomatis** kosong.  
3. Pilih **Simpan** untuk membuat lingkungan.

![Tambahkan database](./media/20CreateEnvironment1.png)

4. Setelah lingkungan dibuat, instal solusi **Microsoft Dynamics 365 Project Operations**. 

![Instal Solusi](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instal konfigurasi CDS dan data demo konfigurasi

Instal konfigurasi CDS dan konfigurasikan data demo dengan mengikuti petunjuk dalam topik, [terapkan konfigurasi demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]