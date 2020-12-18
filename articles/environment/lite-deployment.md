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
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642187"
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

1. Sebagai [administrator global atau Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, buat lingkungan CDS baru di [Pusat admin powerplatform](https://admin.powerplatform.com). Pastikan bahwa **database CDS** dan **aplikasi Dynamics 365** diaktifkan. Untuk informasi lebih lanjut, lihat [membuat dan mengelola lingkungan di pusat admin Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pilih **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Menginstal Project Operations ke lingkungan CDS lama

1. Sebagai [administrator Power Platform atau global](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, Cari lingkungan di [Pusat admin powerplatform](https://admin.powerplatform.com) tempat Anda ingin menginstal Project Operations.
2. Instal **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365. Untuk informasi lebih lanjut, lihat [Kelola aplikasi Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).


