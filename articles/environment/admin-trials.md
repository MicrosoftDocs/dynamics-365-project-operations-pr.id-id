---
title: Mendaftar ke uji coba Project Operations
description: Topik ini menyediakan informasi tentang cara menyebarkan uji coba Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/04/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c8ae111acffb45fef1c2e6435849471ae331796
ms.sourcegitcommit: 05ee415093d152b5b9e1203c3db0ea7f0c5a75a5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/04/2021
ms.locfileid: "7599217"
---
# <a name="sign-up-for-project-operations-trials"></a>Mendaftar ke uji coba Project Operations 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite - menangani faktur proforma, dan Project Operations untuk skenario berbasis stok/produksi_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Topik ini menjelaskan cara berlangganan penawaran mitra pratinjau dan menyebarkan lingkungan Dynamics 365 Project Operations.

Dengan uji coba Project Operations baru, Anda dapat secara otomatis menyebarkan salah satu dari tiga skenario penyebaran yang didukung dengan menyelesaikan daftar pertanyaan yang merekomendasikan pendekatan penyebaran terbaik. Topik ini menyediakan informasi tentang bagaimana:

- Menukarkan penawaran uji coba Anda.
- Memulai provisi.
- Mengonfigurasikan tulis ganda.
- Selengkapnya tentang Project Operations. 

Tabel berikut menjelaskan rincian penawaran uji coba baru.

| **Item penawaran**               | **Rincian**                                  |
|------------------------------|----------------------------------------------|
| Jenis Penawaran                   | Jenis penawaran ini adalah Prospek admin sehingga admin penyewa diperlukan untuk menukarkannya. |
| Penggunaan penawaran                    | Satu kali per penyewa                          |
| Durasi penawaran               | 30 hari kalender                             |
| Penukaran per penyewa       | 1                                            |
| Jumlah pengguna              | 25                                           |
| Ekstensi                    | 1 ekstensi, 30 hari kalender               |
| Jumlah lingkungan uji coba | 3                                            |


## <a name="admin-trial-details"></a>Rincian uji coba admin
Tabel berikut berisi rincian uji coba dan penerapannya untuk setiap jenis penyebaran.

| **Item**                      | **Lite**                                     | **Bahan tanpa stok** | **Bahan ber-stok** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Konfigurasi data yang diberikan           | Ya                                          | Ya                       | Ya (USSI)            |
| Data Transaksional            | No                                           | No                        | No                    |
| Waktu provisi dalam menit  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Prasyarat
Prasyarat berikut diperlukan untuk menyebarkan uji coba Dynamics 365 Project Operations.

- Mendaftar ke [Dynamics 365 Project Operations - uji coba pratinjau](https://www.aka.ms/try-po).
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure.

> [!IMPORTANT]
> Hanya satu orang dalam organisasi, administrator penyewa, yang harus melakukan tugas ini. Jika Anda bukan pelanggan untuk rilis ini, tunggu hingga organisasi Anda telah terdaftar dan Anda telah menerima kredensial pengguna Anda.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Uji coba pratinjau 

Sebelum Anda memulai, masuk ke browser dengan akun kerja pengguna di penyewa tempat Anda menginginkan pratinjau Project Operations.

1. Tukarkan kode penawaran pertama, **Dynamics 365 Project Operations - Uji Coba Pratinjau** dengan merekatkannya ke URL browser.

    ![Tukarkan penawaran](./media/16RedeemFirstOfferNew.png)

2. Konfirmasikan pesanan.

    ![Konfirmasi pesanan](./media/17ConfirmOrderNew.png)

  Anda akan melihat bahwa penawaran konfirmasi berhasil ditukarkan.

   ![Konfirmasi](./media/18OrderConfirmationNew.png)

  Anda akan diarahkan ke [pusat admin Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Kuesioner dan provisi

1.  Buka [pusat admin Power Platform](https://admin.powerplatform.com/projectoperationstrial) dan isi kuesioner.  
2.  Tinjau jenis penyebaran yang disarankan, lalu pilih **Mulai Konfigurasi** untuk memulai provisi.
3.  Periksa persyaratan dan ketentuan, dan kemudian pilih **Mulai**.

   Setelah provisi dimulai, Anda akan diarahkan ke daftar lingkungan di pusat admin Power Platform. Saat provisi sedang berlangsung, status lingkungan Anda adalah **PreparingInstance**.
 
  Setelah provisi selesai, status lingkungan Anda **Siap**. Penyediaan lingkungan mencakup penerapan data demo.
 
4.  Pilih URL Microsoft Dataverse dan URL aplikasi Finance and Operations terkait untuk memvalidasi penyebaran.

## <a name="configuring-dual-write"></a>Mengonfigurasikan tulis ganda
Untuk penyebaran bahan non-stok, konfigurasikan pemetaan tulis ganda Anda. Untuk informasi lebih lanjut, lihat [versi peta tulis ganda Project Operations](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Menetapkan lisensi

Anda akan memerlukan akses administratif ke Portal Microsoft 365 organisasi Anda untuk menyelesaikan langkah-langkah berikut.

1. Buka [pusat admin Microsoft 365](https://portal.office.com/) untuk menetapkan lisensi kepada pengguna.

   ![Halaman Beranda pusat Admin](./media/14AdminPortal.png)

2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.

   ![Menetapkan lisensi](./media/15AssignLicenses.png)

3. Pastikan lisensi **Dynamics 365 Project Operations Pratinjau**  telah dipilih, lalu pilih **Simpan perubahan**.

## <a name="additional-resources"></a>Sumber daya tambahan

Sumber daya berikut memberikan panduan bermanfaat saat Anda memulai perjalanan dengan Project Operations:

- [Rangkaian Video -Ikhtisar Project Operations, menyelami fitur dan peta jalan](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Menentukan jenis penyebaran Anda](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Tanya jawab

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Bagaimana jika saya memerlukan ALM atau ELM untuk lingkungan aplikasi Finance and Operations saya?

- Untuk mitra yang memerlukan kemampuan manajemen siklus hidup lingkungan lengkap, lihat [Permintaan Lisensi Sandbox Mitra](https://experience.dynamics.com/requestlicense) untuk meninjau penawaran mitra baru. 
- Untuk mitra yang mencari informasi lebih lanjut tentang Hak Penggunaan [Internal, lihat manfaat cloud dan perangkat lunak Hak Penggunaan Internal (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Dapatkah saya memperpanjang masa uji coba setelah 30 hari?
Untuk memperpanjang uji coba, selesaikan langkah-langkah berikut.

1. Di **pusat admin Microsoft 365**, buka **Penagihan** > **Produk Anda**.
2. Pilih **Dynamics 365 Project Operations (CE) - Uji Coba Pratinjau**.
3. Dalam **Tanggal Kedaluwarsa**, pilih **Perpanjang Tanggal**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Dapatkah saya meningkatkan dari penyebaran lite ke penyebaran skenario berbasis sumber daya/non-stok?
Saat ini, tidak ada dukungan untuk meningkatkan lingkungan dari versi lite ke penyebaran berbasis non-stok.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Dapatkah saya mengakses Lifecycle Services (LCS) untuk lingkungan Finance saya?  
Tidak. Untuk uji coba ini, penyebaran ditangani melalui Pusat Admin Power Platform. Akses ke lingkungan Finance dibatasi.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Dapatkah saya menginstal uji coba pada lingkungan yang ada?
Jika Anda memiliki lingkungan yang ada, Anda akan diizinkan untuk menginstal penyebaran lite di lingkungan Dataverse sales yang ada dari pusat Admin Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
