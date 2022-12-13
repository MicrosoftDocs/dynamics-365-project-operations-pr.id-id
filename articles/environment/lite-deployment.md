---
title: Menyebarkan Lite Operasi Proyek
description: Artikel ini menyediakan informasi tentang cara menginstal penawaran penyebaran Project Operations lite ke faktur proforma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810982"
---
# <a name="deploy-project-operations-lite"></a>Menyebarkan Lite Operasi Proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_



Project Operations mendukung beberapa model penyebaran. Untuk menentukan model penyebaran terbaik, lihat [jenis penyebaran](determine-deployment-type.md).


> [!IMPORTANT]
> Penyebaran ini, penawaran penyebaran sederhana-untuk faktur proforma, menghasilkan **penyebaran Project Operations Dataverse saja**.

- [Menginstal Project Operations ke lingkungan Dataverse baru](#new)
- [Instal ke lingkungan Dataverse yang ada](#existing)
- [Instal ke lingkungan yang ada Dataverse yang memiliki komponen tulis ganda](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Instal Project Operations Lite ke lingkungan baru Dataverse 

1. Sebagai [administrator global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, buat lingkungan Dataverse baru di [Pusat admin PowerPlatform](https://admin.powerplatform.com). Pastikan **Buat database untuk lingkungan ini** dan **Aplikasi Dynamics 365** diaktifkan. Untuk informasi lebih lanjut, lihat [membuat dan mengelola lingkungan di pusat admin Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Pilih **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instal Project Operations Lite ke lingkungan yang sudah ada Dataverse  
1. Sebagai [administrator Power Platform atau global](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, Cari lingkungan di [Pusat admin powerplatform](https://admin.powerplatform.com) tempat Anda ingin menginstal Project Operations.
1. Instal **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365. Untuk informasi lebih lanjut, lihat [Kelola aplikasi Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Instal Project Operations Lite ke lingkungan yang ada di mana solusi tulis ganda sudah ada Dataverse 

Jika Anda ingin terus menjalankan Operasi Proyek dalam mode Penyebaran Lite, Anda harus mengikuti langkah-langkah berikut:

1. Sebagai [administrator Power Platform atau global](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, Cari lingkungan di [Pusat admin powerplatform](https://admin.powerplatform.com) tempat Anda ingin menginstal Project Operations.
1. Instal **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365. Untuk informasi lebih lanjut, lihat [Kelola aplikasi Dynamics 365](/power-platform/admin/manage-apps).
1. Karena lingkungan Anda memiliki komponen tulis ganda yang membantu integrasi ke aplikasi keuangan dan operasi yang diinstal, penginstalan Operasi Proyek juga akan menginstal kemampuan dan ekstensi yang diperlukan untuk mengintegrasikan data terkait Proyek ke aplikasi keuangan dan operasi. Karena Anda ingin menjalankan Operasi Proyek dalam penyebaran Lite, komponen integrasi ini harus dihapus karena akan membuat batasan dan overhead untuk skenario penyebaran Lite. Hapus instalan solusi **Dynamics 365 Project Operations Dual Write dan** Dual Write **Dynamics 365 Project Operations Entity Maps** secara manual untuk menghapus komponen ini.
1.  **Buka Operasi Proyek -> Pengaturan -> Parameter**.  **Buka halaman Detail Parameter Proyek** dan atur **bidang Perilaku** Peningkatan Solusi ke **Hanya** Ringan. Ini memastikan bahwa setiap peningkatan Operasi Proyek berikutnya tidak akan mengembalikan komponen integrasi ke dalam Operasi Proyek.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
