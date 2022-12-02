---
title: Menyebarkan Project Operations - lite
description: Artikel ini menyediakan informasi tentang cara menginstal penawaran penyebaran Project Operations lite ke faktur proforma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930322"
---
# <a name="deploy-project-operations---lite"></a>Menyebarkan Project Operations - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_



Project Operations mendukung beberapa model penyebaran. Untuk menentukan model penyebaran terbaik, lihat [jenis penyebaran](determine-deployment-type.md).


> [!IMPORTANT]
> Penyebaran ini, penawaran penyebaran sederhana-untuk faktur proforma, menghasilkan **penyebaran Project Operations Dataverse saja**.

- [Menginstal Project Operations ke lingkungan Dataverse baru](#new)
- [Instal ke lingkungan Dataverse yang ada](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Menginstal Project Operations ke lingkungan Dataverse baru

1. Sebagai [administrator global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, buat lingkungan Dataverse baru di [Pusat admin PowerPlatform](https://admin.powerplatform.com). Pastikan **Buat database untuk lingkungan ini** dan **Aplikasi Dynamics 365** diaktifkan. Untuk informasi lebih lanjut, lihat [membuat dan mengelola lingkungan di pusat admin Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pilih **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Menginstal Project Operations ke lingkungan Dataverse lama
1. Pastikan lingkungan belum dikonfigurasi dengan [penulisan ganda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) saat penginstalan kemudian akan menginstal kemampuan [Project Operations untuk skenario berbasis sumber daya/non-stok](project-operations-integrated-deployment-overview.md).
2. Sebagai [administrator Power Platform atau global](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, Cari lingkungan di [Pusat admin powerplatform](https://admin.powerplatform.com) tempat Anda ingin menginstal Project Operations.
3. Instal **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365. Untuk informasi lebih lanjut, lihat [Kelola aplikasi Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
