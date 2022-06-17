---
title: Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang cara berlangganan dan menyebarkan Operasi Proyek untuk skenario berbasis resouce/non-stocked.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fb196a50b4cb9e8533db52414e8536d77a30e425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920110"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Mendaftar ke langganan pratinjau Project Operations untuk skenario sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_



Artikel ini menjelaskan cara berlangganan penawaran uji coba dan menyebarkan lingkungan Operasi Proyek untuk skenario berbasis sumber daya/non-stok.

## <a name="prerequisites"></a>Prasyarat
- Pengguna yang menerapkan pratinjau harus memiliki hak administrator global Penyewa Azure. Anda dapat membuat penyewa selama penukaran penawaran pertama. 
- Menyebarkan lingkungan Finance memerlukan langganan Azure valid yang akan ditagih per lingkungan. Anda dapat menggunakan langganan yang ada saat ini atau menggunakan [uji coba Azure](https://azure.microsoft.com/free/) untuk memulai. Lingkungan CDS akan disediakan gratis selama periode 30 hari terbatas.

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

1. Buka [Microsoft 365 pusat](https://portal.office.com/) admin untuk menetapkan lisensi kepada pengguna Anda.

2. Pada halaman **pengguna aktif**, pilih pengguna yang akan ditetapkan lisensinya.

3. Pastikan lisensi **Dynamics 365 Project Operations** telah dipilih, lalu pilih **Simpan perubahan**.

> [!NOTE]
> Penawaran uji coba Finance tidak perlu ditetapkan ke pengguna.

## <a name="start-a-new-project-in-lcs"></a>Memulai proyek baru di LCS

Buat proyek LCS baru seperti yang dijelaskan dalam artikel, [Mulai proyek baru di LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Menambahkan langganan Azure ke proyek LCS

Untuk menyelesaikan tugas ini, ikuti langkah-langkah dalam artikel, [Menambahkan langganan Azure ke proyek LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Terapkan lingkungan demo Finance dengan Project Operations untuk skenario sumber daya/non-stok

Ikuti panduan dalam artikel, Menyediakan [lingkungan](resource-provision-new-environment.md) baru untuk menyelesaikan penyebaran. Gunakan jenis penyebaran [lingkungan demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) untuk pratinjau. 

## <a name="install-cds-setup-and-configuration-data"></a>Menginstal data pengaturan dan konfigurasi CDS

Instal data pengaturan dan konfigurasi CDS seperti yang dijelaskan dalam artikel, [Siapkan dan terapkan data konfigurasi dalam Common Data Service](resource-apply-pro-setup-config-data.md) file.
Selesaikan langkah ini hanya setelah lingkungan demo Finance disebarkan dan data demo siap.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
