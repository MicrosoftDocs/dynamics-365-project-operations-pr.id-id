---
title: Menyebarkan Project Operations - lite
description: Topik ini menyediakan informasi tentang cara menginstal penawaran penyebaran Project operation lite ke faktur proforma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580736"
---
# <a name="deploy-project-operations---lite"></a>Menyebarkan Project Operations - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_



Project Operations mendukung beberapa model penyebaran. Untuk menentukan model penyebaran terbaik, lihat [jenis penyebaran](determine-deployment-type.md).


> [!IMPORTANT]
> Penyebaran ini, penawaran penyebaran sederhana-untuk faktur proforma, menghasilkan **penyebaran Project Operations Dataverse saja**.

- [Menginstal Operasi Proyek ke lingkungan baru Dataverse](#new)
- [Instal ke lingkungan yang Dataverse sudah ada](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Menginstal Operasi Proyek ke lingkungan baru Dataverse

1. [Sebagai Global atau Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Operasi Proyek, buat lingkungan baru Dataverse di [pusat](https://admin.powerplatform.com) admin PowerPlatform. Pastikan Membuat **database untuk lingkungan** ini dan **Aplikasi** Dynamics 365 diaktifkan. Untuk informasi lebih lanjut, lihat [membuat dan mengelola lingkungan di pusat admin Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pilih **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Menginstal Operasi Proyek ke lingkungan yang Dataverse sudah ada
1. Pastikan bahwa lingkungan belum dikonfigurasi dengan [dual-write](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) karena instalasi kemudian akan menginstal [Operasi Proyek untuk kemampuan skenario](project-operations-integrated-deployment-overview.md) berbasis sumber daya / non-stocked.
2. Sebagai [administrator Power Platform atau global](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, Cari lingkungan di [Pusat admin powerplatform](https://admin.powerplatform.com) tempat Anda ingin menginstal Project Operations.
3. Instal **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365. Untuk informasi lebih lanjut, lihat [Kelola aplikasi Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
