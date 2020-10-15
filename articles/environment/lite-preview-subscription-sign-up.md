---
title: Mendaftar untuk berlangganan pratinjau
description: Topik ini menyediakan informasi tentang cara berlangganan dan menyebarkan penawaran penyebaran Project operation lite ke faktur proforma.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948919"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Mendaftar ke langganan pratinjau untuk penyebaran sederhana – menangani faktur proforma

Topik ini menjelaskan cara berlangganan penawaran mitra pratinjau dan menyebarkan Dynamics 365 Project operation lite ke faktur proforma.

> [!NOTE]
> Proses ini akan berubah di rilis mendatang Project Operations.

## <a name="prerequisites"></a>Prasyarat

- Anda akan menerima email yang mengundang Anda untuk berpartisipasi dalam pratinjau. Anda dapat meminta pratinjau di [situs web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure.
- Pengguna yang menerapkan pratinjau akan memerlukan nomor telepon dan kartu kredit yang valid. Saat mendaftar, tidak akan ada biaya untuk kartu selama enam bulan. Setelah enam bulan, Anda harus membatalkan langganan. 
- Tinjau semua persyaratan dan ketentuan.

## <a name="subscribe"></a>Berlangganan

Bila Anda menerima persetujuan [permintaan pratinjau](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), Anda akan menerima dua tawaran dari Microsoft melalui email. Penawaran ini memungkinkan Anda menyebarkan pratinjau Project Operations:

- Uji coba pratinjau Dynamics 365 Customer Service – kode penggunaan tunggal
- Dynamics 365 Project Operations – uji coba pratinjau

### <a name="dynamics-365-customer-service-paid-offer"></a>Penawaran berbayar Dynamics 365 Customer Service

1. Menggunakan jendela penyamaran /Incognito browser, menukarkan kode penawaran pertama untuk Dynamics 365 Customer Service. Untuk mendaftar ke Customer Service, anda akan memerlukan:

- Nomor Telepon
- Kartu Kredit. Saat mendaftar, tidak akan ada biaya untuk kartu selama enam bulan. Setelah enam bulan, Anda harus membatalkan langganan.
- Tinjau semua persyaratan dan ketentuan.

2. Berikan informasi kontak Anda.

![Informasi Kontak](./media/1ContactInformation.png)

3. Berikan rincian penyewa baru.

![Buat ID pengguna](./media/2CreateUserID.png)

4. Verifikasikan identitas Anda, Simpan ID pengguna baru, lalu pilih **Atur**.

![Simpan informasi](./media/3SaveInfo.png)

5. Lengkapi pendaftaran kartu kredit dan Tinjau semua persyaratan dan ketentuan. 

![Selesaikan kartu kredit](./media/4CompleteCreditCard.png)

![Pembayaran dengan kartu kredit](./media/5CreditCardCheckout.png)

![Simpan pesanan](./media/6SaveOrder.png)

![Konfirmasi kartu kredit](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Batalkan penawaran Dynamics 365 Customer Service enterprise

Penawaran Dynamics 365 Customer Service Enterprise diberikan gratis selama enam bulan. Penawaran akan diperpanjang dengan tarif penuh pada akhir periode enam bulan. Untuk membatalkan sebelum tanggal perpanjangan, selesaikan petunjuk berikut. 

> [!NOTE]
> Setelah Anda menyelesaikan langkah-langkah ini, Anda tidak akan dapat lagi menggunakan lingkungan pratinjau publik Project Operations.

1. Buka [portal admin](https://admin.microsoft.com/), dan dalam **penagihan**, pilih **produk Anda**.

![Portal admin, halaman produk Anda](./media/8AdminPortal.png)

2. Batalkan **penawaran Dynamics 365 Customer Service enterprise**.

![Batalkan langganan](./media/9CancelSubscription.png)

3. Pilih **pengaturan** > **tindakan** > **membatalkan langganan**.
4. Pada formulir **pembatalan langganan**, masukkan informasi di bidang wajib.
5. Pilih **Batalkan** > **langganan.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – uji coba pratinjau

1. Tukarkan tawaran kedua, uji coba Dynamics 365 Project Operations dengan URL yang diberikan dalam email Selamat datang Anda.

![Tukarkan penawaran 2](./media/10RedeemOffer2.png)

2. Verifikasikan bahwa Anda masuk sebagai pengguna yang termasuk dalam organisasi yang sama yang berlangganan menggunakan kode Penawaran pertama, lalu lanjutkan dengan penukaran Penawaran. 
3. Pilih **ya, tambahkan ke akun saya**.

![Tambahkan ke akun](./media/11AddToAccount.png)

![Coba layar sekarang](./media/12TryNow.png)

![Detail pesanan](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Menetapkan lisensi

> [!IMPORTANT]
> Anda akan memerlukan akses administratif ke Portal Office 365 organisasi Anda untuk menyelesaikan langkah-langkah berikut.

1. Buka [Pusat admin Microsoft 365](https://portal.office.com/) untuk menetapkan lisensi kepada pengguna.

![Halaman Beranda pusat Admin](./media/14AdminPortal.png)

2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.

![Menetapkan lisensi](./media/15AssignLicenses.png)

3. Periksa apakah lisensi **Customer Service Enterprise** dan **Project Operations** telah dipilih dan pilih **simpan perubahan**.

## <a name="create-a-new-cds-environment"></a>Buat lingkungan CDS baru

LakukanPara Pihakenyediaan lingkungan penyebaran cds Project Operations baru dengan mengikuti petunjuk dalam topik, [model penyebaran cds](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instal konfigurasi CDS dan data demo konfigurasi

Instal konfigurasi CDS dan konfigurasikan data demo dengan mengikuti petunjuk dalam topik, [terapkan konfigurasi demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).
