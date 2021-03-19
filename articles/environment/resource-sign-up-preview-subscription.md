---
title: Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok
description: Topik ini memberikan informasi tentang cara berlangganan dan menyebarkan Project Operations untuk skenario berbasis sumber daya/non-stok.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276847"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Topik ini menjelaskan tentang cara berlangganan pratinjau/penawaran mitra dan menyebarkan lingkungan Project Operations untuk sumber daya/non-stok berbasis skenario.

## <a name="prerequisites"></a>Prasyarat

- Anda akan menerima email yang mengundang Anda untuk berpartisipasi dalam pratinjau. Anda dapat meminta pratinjau di [situs web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure.
- Menyebarkan lingkungan Finance memerlukan langganan Azure valid yang akan ditagih per lingkungan. Anda dapat menggunakan langganan yang ada saat ini atau menggunakan [uji coba Azure](https://azure.microsoft.com/en-us/free/) untuk memulai. Lingkungan CDS akan disediakan gratis selama periode 30 hari terbatas.

## <a name="subscribe"></a>Berlangganan

Bila Anda menyetujui [permintaan pratinjau](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), Anda akan menerima tiga tawaran dari Microsoft melalui email. Penawaran ini memungkinkan Anda menyebarkan pratinjau Project Operations:

- Dynamics 365 Project Operations (CRM) - Uji Coba Pratinjau
- Office 365 Project Operations - Uji coba Pratinjau
- Dynamics 365 Finance -Uji coba pratinjau

> [!IMPORTANT]
> Hanya satu orang, administrator penyewa, dalam organisasi harus melakukan tugas ini. Jika Anda bukan pelanggan untuk rilis ini, tunggu hingga organisasi Anda telah terdaftar dan Anda telah menerima kredensial pengguna Anda.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - Uji Coba Pratinjau 

Sebelum memulai, pastikan Anda masuk ke browser dengan akun kerja pengguna di penyewa tempat Anda menginginkan pratinjau Project Operations.

1. Tukarkan kode penawaran pertama, **Dynamics 365 Project Operations (CRM) - Uji Coba Pratinjau** dengan merekatkannya ke URL browser.

![Tukarkan penawaran](./media/16RedeemFirstOfferNew.png)

2. Konfirmasikan pesanan.

![Konfirmasi pesanan](./media/17ConfirmOrderNew.png)

Anda akan melihat penawaran konfirmasi berhasil ditukarkan.

![Konfirmasi](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Uji coba Pratinjau

Ulangi langkah yang sama seperti dengan kode penawaran pertama. Pastikan untuk menambahkan kode penawaran kedua menggunakan akun pengguna yang sama yang digunakan dengan kode penawaran pertama.

### <a name="dynamics-365-finance-preview-trial"></a>Uji coba pratinjau Dynamics 365 Finance

Ulangi langkah yang sama dengan tawaran terakhir dari email sambutan.

## <a name="assign-licenses"></a>Menetapkan lisensi

> [!IMPORTANT]
> Anda akan memerlukan akses administratif ke Portal Microsoft 365 organisasi Anda untuk menyelesaikan langkah-langkah berikut.

1. Buka [Pusat admin Microsoft 365](https://portal.office.com/) untuk menetapkan lisensi kepada pengguna.

![Halaman Beranda pusat Admin](./media/14AdminPortal.png)

2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.

![Menetapkan lisensi](./media/15AssignLicenses.png)

3. Verifikasikan bahwa lisensi Pratinjau **Dynamics 365 Project Operations (CRM)** dan Project Operations **Office 365 - Pratinjau** telah dipilih, dan pilih **Simpan Perubahan**.

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
Selesaikan langkah ini hanya setelah lingkungan demo Finance disebarkan dan data demo di FO siap.


[!INCLUDE[footer-include](../includes/footer-banner.md)]