---
title: Tambahkan formulir entitas kustom baru (Project Service Automation 2. x)
description: Topik ini menyediakan informasi tentang cara menambahkan formulir entitas kustom untuk peluang, kuotasi, pesanan, atau faktur di Dynamics 365 Project Service Automation 2. x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008000"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Tambahkan formulir entitas kustom baru (Project Service Automation 2. x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Bidang Jenis 

Dynamics 365 Project Service Automation bergantung pada bidang **jenis** (**msdyn\_ordertype**) pada entitas peluang, kuotasi, pesanan, dan faktur untuk membedakan versi **berbasis pekerjaan** entitas ini dari **berbasis item** dan versi **berbasis layanan**. Versi berbasis pekerjaan dari entitas ini ditangani oleh PSA. Banyak logika bisnis di sisi klien dan server solusi tergantung pada bidang **jenis**. Oleh karena itu, penting bahwa bidang diinisialisasi dengan nilai yang benar saat entitas dibuat. Nilai yang salah dapat menyebabkan perilaku yang tidak benar, dan beberapa logika bisnis mungkin tidak berjalan dengan benar.

## <a name="automatic-form-switching"></a>Pengalihan formulir otomatis

Untuk menghindari kerusakan data potensial dan perilaku tak terduga yang disebabkan oleh inisialisasi salah dan mengedit rekaman entitas penjualan, PSA sekarang mencakup logika untuk beralih formulir otomatis dalam formulir bawaan. Logika ini akan membawa pengguna ke formulir yang benar untuk bekerja dengan versi berbasis pekerjaan atau jenis peluang, kuotasi, pesanan, atau entitas faktur lainnya. Bila pengguna membuka versi berbasis pekerjaan peluang, kuotasi, pesanan, atau entitas faktur, formulir akan beralih ke **informasi proyek**.

Logika peralihan formulir otomatis tergantung pada pemetaan antara nilai **formId** dan bidang **msdyn\_ordertype**. Semua formulir bawaan telah ditambahkan ke pemetaan tersebut. Namun, formulir kustom harus ditambahkan secara manual untuk menunjukkan versi entitas yang ditujukan untuk ditangani. Ini didasarkan pada bidang **msdyn\_ordertype**. Jika peralihan formulir hilang dari pemetaan, logika akan beralih ke formulir bawaan, berdasarkan nilai yang disimpan dalam bidang entitas **msdyn\_ordertype**.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Tambahkan formulir kustom dan Hidupkan logika beralih formulir

Contoh berikut menunjukkan cara menambahkan formulir kustom, **informasi proyek saya**, sehingga berfungsi pada peluang berbasis pekerjaan. Proses yang sama digunakan untuk menambahkan formulir kustom agar berfungsi dengan kuotasi, pesanan, dan faktur.

Ikuti langkah berikut untuk membuat formulir **informasi proyek** versi kustom.

1. Di entitas peluang, buka formulir **informasi proyek**, dan Simpan salinan dalam nama **informasi proyek saya**.
2. Buka formulir baru, dan kemudian, di properti, pastikan bahwa skrip inisialisasi formulir dari formulir **informasi proyek** ada. 

    > [!IMPORTANT]
    > Jangan hapus skrip. Jika tidak, beberapa data mungkin diinisialisasi dengan tidak benar.

3. Verifikasikan bahwa bidang **jenis** (**msdyn\_ordertype**) ada di formulir. 

    > [!IMPORTANT]
    > Jangan hapus bidang ini. Jika tidak, skrip inisiasi akan gagal.

4. Temukan nilai **formId** formulir baru. Anda dapat menyelesaikan langkah ini dengan dua cara:

    - Mengekspor formulir **informasi proyek saya** sebagai bagian dari solusi tidak terkelola, lalu mencari nilai **formid** dalam file Customization.xml solusi yang diekspor.
    - Buka formulir **informasi proyek saya** di editor formulir, lalu cari pengidentifikasi unik global (GUID) di samping parameter **fromid** di URL, sebagaimana ditampilkan dalam ilustrasi berikut.

    ![Nilai formId formulir baru di URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Buat pemetaan **msdyn\_ordertype** untuk nilai **formid** dengan mengedit sumber daya msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js Hapus kode dari sumber daya, dan gantilah dengan kode berikut.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Simpan, lalu Publikasikan penyesuaian.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]