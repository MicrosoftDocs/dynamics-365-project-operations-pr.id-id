---
title: Mengembangkan template proyek dengan Salinan Proyek
description: artikel ini menyediakan informasi tentang cara membuat template proyek menggunakan tindakan kustom menyalin proyek.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923836"
---
# <a name="develop-project-templates-with-copy-project"></a>Mengembangkan template proyek dengan Salinan Proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mendukung kemampuan untuk menyalin proyek dan mengembalikan tugas apa pun ke sumber daya umum yang menunjukkan peran. Pelanggan dapat menggunakan fungsi ini untuk membuat template proyek dasar.

Bila Anda memilih **Salin proyek**, status proyek target diperbarui. Gunakan **alasan status** untuk menentukan kapan tindakan penyalinan selesai. Memilih **Salin proyek** juga memperbarui tanggal mulai proyek ke tanggal mulai saat ini jika tidak ada target tanggal terdeteksi di entitas proyek target.

## <a name="copy-project-custom-action"></a>Tindakan kustom Salin proyek

### <a name="name"></a>Nama 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parameter input

Terdapat tiga parameter input:

- **ReplaceNamedResources** atau **ClearTeamsAndAssignments** – Atur hanya salah satu pilihan. Jangan tetapkan keduanya.

    - **\{"ReplaceNamedResources":true\}** – Perilaku default untuk Project Operations. Sumber daya bernama apa pun digantikan dengan sumber daya generik.
    - **\{"ClearTeamsAndAssignments":true\}** – Perilaku default untuk Project for the Web. Semua penetapan dan anggota tim akan dihilangkan.

- **SourceProject** – Referensi entitas dari proyek sumber untuk disalin. Parameter ini tidak boleh null.
- **Target** – Referensi entitas dari proyek target untuk menyalin. Parameter ini tidak boleh null.

Tabel berikut memberikan ringkasan ketiga parameter.

| Parameter                | Tipe             | Nilai                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **True** atau **false** |
| ClearTeamsAndAssignments | Boolean          | **True** atau **false** |
| SourceProject            | Referensi Entitas | Proyek sumber    |
| Target                   | Referensi Entitas | Proyek target    |

Untuk default lebih lanjut tentang tindakan, lihat [menggunakan tindakan API Web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validasi

validasi berikut ini dilakukan.

1. Null memeriksa dan mengambil sumber dan proyek target untuk mengkonfirmasikan keberadaan kedua proyek di organisasi.
2. Sistem memvalidasi bahwa proyek target valid untuk disalin dengan memverifikasi kondisi berikut:

    - Tidak ada aktivitas sebelumnya pada proyek (termasuk pilihan tab **Tugas**), dan proyek baru dibuat.
    - Tidak ada salinan sebelumnya, tidak ada impor yang diminta pada proyek ini, dan proyek tidak memiliki status **Gagal**.

3. Operasi tidak dipanggil menggunakan HTTP.

## <a name="specify-fields-to-copy"></a>Menentukan bidang yang akan disalin

Saat tindakan dipanggil, **Salin proyek** akan melihat tampilan proyek **Kolom Salin proyek** untuk menentukan bidang yang akan disalin saat proyek disalin.

### <a name="example"></a>Contoh

Contoh berikut menunjukkan cara memanggil tindakan kustom **CopyProjectV3** dengan rangkaian parameter **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
