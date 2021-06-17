---
title: Menyebarkan Project Operations - lite
description: Topik ini menyediakan informasi tentang cara menginstal penawaran penyebaran Project operation lite ke faktur proforma.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995535"
---
# <a name="deploy-project-operations---lite"></a>Menyebarkan Project Operations - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations mendukung beberapa model penyebaran. Untuk menentukan model penyebaran terbaik, lihat [jenis penyebaran](determine-deployment-type.md).


> [!IMPORTANT]
> Penyebaran ini, penawaran penyebaran sederhana-untuk faktur proforma, menghasilkan **penyebaran Project Operations Common Data Service saja**.

- [Menginstal Project Operations ke lingkungan CDS baru](#new)
- [Instal ke lingkungan CDS yang ada](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Menginstal Project Operations ke lingkungan CDS baru

1. Sebagai [administrator global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, buat lingkungan CDS baru di [Pusat admin powerplatform](https://admin.powerplatform.com). Pastikan bahwa **database CDS** dan **aplikasi Dynamics 365** diaktifkan. Untuk informasi lebih lanjut, lihat [membuat dan mengelola lingkungan di pusat admin Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pilih **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Menginstal Project Operations ke lingkungan CDS lama

1. Sebagai [administrator Power Platform atau global](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, Cari lingkungan di [Pusat admin powerplatform](https://admin.powerplatform.com) tempat Anda ingin menginstal Project Operations.
2. Instal **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365. Untuk informasi lebih lanjut, lihat [Kelola aplikasi Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]