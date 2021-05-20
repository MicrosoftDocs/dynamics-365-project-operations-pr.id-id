---
title: Menyebarkan Project Operations - lite
description: Topik ini menyediakan informasi tentang cara menginstal penawaran penyebaran Project operation lite ke faktur proforma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950268"
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