---
title: Menambahkan langganan Azure ke proyek LCS
description: Topik ini menyediakan informasi tentang cara menyambungkan langganan Azure ke proyek lcs.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000620"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Menambahkan langganan Azure ke proyek LCS

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Lingkungan host Cloud harus disebarkan menggunakan langganan Azure yang ada. Topik ini menjelaskan cara menyambungkan langganan Azure yang ada ke proyek lcs. 

## <a name="grant-admin-consent"></a>Memberikan izin admin

1. Di proyek LCS, di Bagian **lingkungan**, pilih **pengaturan Microsoft Azure**.

![Pengaturan Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Pada halaman **pengaturan proyek**, pada tab **konektor Azure**, pilih **otorisasi**. Hal ini memungkinkan lingkungan akan disebarkan ke proyek ini.

![Azure Connectors](./media/2AzureConnectors.png)

3. Pilih **otorisasi** lagi untuk memberikan izin admin.

![Memberikan izin admin](./media/3GrantAdminConsent.png)

4. Terima permintaan izin.

![Terima permintaan izin](./media/4AcceptPermissionRequest.png)

Otorisasi sekarang selesai. 

![Otorisasi berhasil](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Berikan akses layanan penyebaran Dynamics ke langganan Azure Anda

1. Pergi ke [penagihan Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) dan pilih langganan Anda. Dynamics Deployment Services harus mengakses langganan ini agar dapat menerapkan lingkungan.

![Rincian Langganan Azure](./media/6AzureSubscription.png)

2. Pilih **kontrol akses (iam)** di panel navigasi, lalu pilih **Tambah penetapan peran**.
3. Di penggeser di sisi kanan, pilih **kontributor peran**, dan di daftar yang tersedia, cari dan pilih **Dynamics Deployment Services**. 
4. Pilih **Simpan**.

![Akses Langganan](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Menambahkan konektor langganan ke proyek LCS

1. Di proyek LCS, pada halaman **pengaturan Microsoft Azure**, pilih **Tambah** untuk menambahkan konektor baru.
2. Masukkan ID langganan Azure Anda. Anda dapat menemukan ID langganan Azure di [portal Azure](https://ms.portal.azure.com/), dalam  **pengaturan**  di kiri bawah layar.
3. Di bidang **Konfigurasikan untuk menggunakan Azure Resource Manager**, pilih **ya**.
4. Pastikan domain penyewa AAD langganan Azure cocok dengan langganan Azure pemilik domain yang Anda gunakan, lalu pilih **berikutnya**.
5. Di layar **konfigurasi Microsoft Azure**, pilih **berikutnya** untuk mengonfirmasi. Jika Anda menerima kesalahan pada layar ini, kembali ke bagian [menyediakan akses Dynamics Deployment Services ke langganan Azure](#provide) di topik ini, dan pastikan Anda telah menyelesaikan semua langkah.
6. Unduh Sertifikat Manajemen Azure ke folder lokal di komputer Anda. Minta administrator langganan Azure untuk mengunggah sertifikat ke Portal Manajemen Azure dengan memilih langganan dan masuk ke **Pengaturan** > **Manajemen Sertifikat**. Sertifikat ini memungkinkan LCS berkomunikasi dengan Azure atas nama Anda. Anda dapat melewatkan langkah ini jika pengguna Anda memiliki akses ke langganan.
7. Pilih  **Selanjutnya**.
8. Pilih kawasan Azure untuk disebarkan, lalu pilih pusat data yang dekat dengan lokasi Anda berencana menggunakan sistem ini.
9.  Pilih  **Sambungkan**.

Anda telah berhasil terhubung langganan Azure Anda. Anda sekarang dapat menyebarkan lingkungan host Cloud Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
