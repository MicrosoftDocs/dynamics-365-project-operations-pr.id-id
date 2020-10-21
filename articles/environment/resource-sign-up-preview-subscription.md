---
title: Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok
description: Topik ini memberikan informasi tentang cara berlangganan dan menyebarkan Project Operations untuk skenario berbasis sumber daya/non-stok.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948922"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini menjelaskan tentang cara berlangganan pratinjau/penawaran mitra dan menyebarkan lingkungan Project Operations untuk sumber daya/non-stok berbasis skenario.

## <a name="prerequisites"></a>Prasyarat

- Anda akan menerima email yang mengundang Anda untuk berpartisipasi dalam pratinjau. Anda dapat meminta pratinjau di [situs web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure.
- Menyebarkan lingkungan Finance memerlukan langganan Azure valid yang akan ditagih per lingkungan. Anda dapat menggunakan langganan yang ada saat ini atau menggunakan [uji coba Azure](https://azure.microsoft.com/en-us/free/) untuk memulai. Lingkungan CDS akan disediakan gratis selama periode 30 hari terbatas.

## <a name="subscribe"></a>Berlangganan

Bila Anda menyetujui [permintaan pratinjau](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), Anda akan menerima dua tawaran dari Microsoft melalui email. Penawaran ini memungkinkan Anda menyebarkan pratinjau Project Operations:

- Dynamics 365 Project Operations – uji coba pratinjau
- Uji coba pratinjau Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Hanya satu orang, administrator penyewa, dalam organisasi harus melakukan tugas ini. Jika Anda bukan pelanggan untuk rilis ini, tunggu hingga organisasi Anda telah terdaftar dan Anda telah menerima kredensial pengguna Anda.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – uji coba pratinjau

1. Tukarkan tawaran pertama, **uji coba Dynamics 365 Project Operations** dengan URL yang diberikan dalam email Selamat datang Anda.

![Penawaran pertama](./media/1FirstOffer.png)

2. Verifikasikan bahwa Anda masuk sebagai pengguna yang termasuk dalam organisasi yang akan berlangganan layanan.
3. Lanjutkan dengan menukarkan Penawaran. 
4. Pilih **ya, tambahkan ke akun saya**.

![Tukarkan penawaran](./media/2RedeemFirstOffer.png)

![Konfirmasi Penawaran](./media/3ConfirmFirstOffer.png)

![Penawaran Ditukarkan](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Uji coba pratinjau Dynamics 365 Finance

Ulangi langkah yang sama dengan tawaran kedua dari email sambutan.

## <a name="assign-licenses"></a>Menetapkan lisensi

> [!IMPORTANT]
> Anda akan memerlukan akses administratif ke Portal Office 365 organisasi Anda untuk menyelesaikan langkah-langkah berikut.

1. Buka [Pusat admin Microsoft 365](https://portal.office.com/) untuk menetapkan lisensi kepada pengguna.

![Portal admin Office](./media/5OfficeAdminPortal.png)

2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.

![Menetapkan lisensi](./media/6AssignLicenses.png)

3. Periksa apakah lisensi Project Operations telah dipilih dan pilih **Simpan perubahan**. 

> [!NOTE]
> Penawaran uji coba Finance tidak perlu ditetapkan ke pengguna.

## <a name="start-a-new-project-in-lcs"></a>Memulai proyek baru di LCS

Membuat proyek lcs baru seperti yang dijelaskan di topik, [memulai proyek baru di LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Menambahkan langganan Azure ke proyek LCS

Untuk menyelesaikan tugas ini, ikuti langkah-langkah di topik, [tambahkan langganan Azure ke proyek LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Terapkan lingkungan demo Finance dengan Project Operations untuk skenario sumber daya/non-stok

Ikuti panduan di topik, [sediakan lingkungan baru](resource-provision-new-environment.md) untuk menyelesaikan penyebaran. Gunakan jenis penyebaran [lingkungan demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) untuk pratinjau.

## <a name="install-cds-setup-and-configuration-data"></a>Menginstal data pengaturan dan konfigurasi CDS

Instal data pengaturan dan konfigurasi CDS sebagaimana dijelaskan dalam topik, [atur dan terapkan data konfigurasi di Common Data Service](resource-apply-pro-setup-config-data.md).

