---
title: Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok
description: Topik ini memberikan informasi tentang cara berlangganan dan menyebarkan Project Operations untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334831"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Topik ini menjelaskan cara berlangganan penawaran uji coba dan menyebarkan lingkungan Project Operations untuk skenario berbasis sumber daya/non-persediaan.

## <a name="prerequisites"></a>Prasyarat
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure. Anda dapat membuat penyewa selama penukaran penawaran pertama. 
- Menyebarkan lingkungan Finance memerlukan langganan Azure valid yang akan ditagih per lingkungan. Anda dapat menggunakan langganan yang ada saat ini atau menggunakan [uji coba Azure](https://azure.microsoft.com/en-us/free/) untuk memulai. Lingkungan CDS akan disediakan gratis selama periode 30 hari terbatas.

> [!IMPORTANT]
> Hanya satu orang, administrator penyewa, dalam organisasi harus melakukan tugas ini. Jika Anda bukan pelanggan untuk rilis ini, tunggu hingga organisasi Anda telah terdaftar dan Anda telah menerima kredensial pengguna Anda.
> 
> Uji coba hanya digunakan satu kali dalam penyewa. Anda hanya dapat menjalankan uji coba satu kali. Sebaiknya buat penyewa baru untuk tujuan uji coba.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Uji Coba Pratinjau 

Sebelum memulai, pastikan Anda masuk ke browser dengan akun kerja pengguna di penyewa tempat Anda menginginkan pratinjau Project Operations.

1. Tukarkan kode penawaran pertama, , **Dynamics 365 Project Operations** di sini [Uji coba Project Operations](https://aka.ms/try-po).
2. Konfirmasikan pesanan.

  Anda akan melihat penawaran konfirmasi berhasil ditukarkan.

### <a name="dynamics-365-finance-preview-trial"></a>Uji coba pratinjau Dynamics 365 Finance

Buka [Uji Coba Pratinjau Dynamics 365 untuk Finance](https://aka.ms/trypoche), lalu ulangi langkah-langkah dari bagian sebelumnya dengan penawaran, Mendaftar untuk Lingkungan yang Di-Host Cloud.  

## <a name="assign-licenses"></a>Menetapkan lisensi

> [!IMPORTANT]
> Anda akan memerlukan akses administratif ke Portal Microsoft 365 organisasi Anda untuk menyelesaikan langkah-langkah berikut.

1. Buka [Pusat admin Microsoft 365](https://portal.office.com/) untuk menetapkan lisensi kepada pengguna.

2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.

3. Pastikan lisensi **Dynamics 365 Project Operations** telah dipilih, lalu pilih **Simpan perubahan**.

> [!NOTE]
> Penawaran uji coba Finance tidak perlu ditetapkan ke pengguna.

## <a name="start-a-new-project-in-lcs"></a>Memulai proyek baru di LCS

Membuat proyek lcs baru seperti yang dijelaskan di topik, [memulai proyek baru di LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Menambahkan langganan Azure ke proyek LCS

Untuk menyelesaikan tugas ini, ikuti langkah-langkah di topik, [tambahkan langganan Azure ke proyek LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Terapkan lingkungan demo Finance dengan Project Operations untuk skenario sumber daya/non-stok

Ikuti panduan di topik, [sediakan lingkungan baru](resource-provision-new-environment.md) untuk menyelesaikan penyebaran. Gunakan jenis penyebaran [lingkungan demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) untuk pratinjau. 

## <a name="install-cds-setup-and-configuration-data"></a>Menginstal data pengaturan dan konfigurasi CDS

Instal data pengaturan dan konfigurasi CDS sebagaimana dijelaskan dalam topik, [atur dan terapkan data konfigurasi di Common Data Service](resource-apply-pro-setup-config-data.md).
Selesaikan langkah ini hanya setelah lingkungan demo Finance disebarkan dan data demo siap.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
