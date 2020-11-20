---
title: Mengembangkan template proyek dengan Salinan Proyek
description: Topik ini menyediakan informasi tentang cara membuat template proyek menggunakan tindakan kustom menyalin proyek.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131617"
---
# <a name="develop-project-templates-with-copy-project"></a>Mengembangkan template proyek dengan Salinan Proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mendukung kemampuan untuk menyalin proyek dan mengembalikan tugas apa pun kembali ke sumber daya generik yang menunjukkan peran. Pelanggan dapat menggunakan fungsi ini untuk membuat template proyek dasar.

Bila Anda memilih **Salin proyek**, status proyek target diperbarui. Gunakan **alasan status** untuk menentukan kapan tindakan penyalinan selesai. Memilih **Salin proyek** juga memperbarui tanggal mulai proyek ke tanggal mulai saat ini jika tidak ada target tanggal terdeteksi di entitas proyek target.

## <a name="copy-project-custom-action"></a>Tindakan kustom Salin proyek 

### <a name="name"></a>Nama 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parameter input
Terdapat tiga parameter input:

| Parameter          | Tipe   | Values                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referensi Entitas | Proyek Sumber |
| Target             | Referensi Entitas | Proyek target |


- **{"clearTeamsAndAssignments":true}**: perilaku default Anda untuk proyek untuk web, dan akan menghapus semua tugas dan anggota tim.
- **{"removeNamedResources":true}** perilaku default untuk Project Operations, dan akan mengembalikan tugas ke sumber daya generik.

Untuk default lebih lanjut tentang tindakan, lihat [menggunakan tindakan API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Menentukan bidang yang akan disalin 
Saat tindakan dipanggil, **Salin proyek** akan melihat tampilan proyek **Kolom Salin proyek** untuk menentukan bidang yang akan disalin saat proyek disalin.
