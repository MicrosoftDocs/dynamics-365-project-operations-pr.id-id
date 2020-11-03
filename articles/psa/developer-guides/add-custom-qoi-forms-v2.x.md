---
title: Tambahkan formulir entitas kustom baru (Project Service Automation 2. x)
description: Topik ini menyediakan informasi tentang cara menambahkan formulir entitas kustom untuk peluang, kuotasi, pesanan, atau faktur di Dynamics 365 Project Service Automation 2. x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078678"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="f51bf-103">Tambahkan formulir entitas kustom baru (Project Service Automation 2. x)</span><span class="sxs-lookup"><span data-stu-id="f51bf-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="f51bf-104">Bidang Jenis</span><span class="sxs-lookup"><span data-stu-id="f51bf-104">Type field</span></span> 

<span data-ttu-id="f51bf-105">Dynamics 365 Project Service Automation bergantung pada bidang **jenis** ( **msdyn\_ordertype** ) pada entitas peluang, kuotasi, pesanan, dan faktur untuk membedakan versi **berbasis pekerjaan** entitas ini dari **berbasis item** dan versi **berbasis layanan**.</span><span class="sxs-lookup"><span data-stu-id="f51bf-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="f51bf-106">Versi berbasis pekerjaan dari entitas ini ditangani oleh PSA.</span><span class="sxs-lookup"><span data-stu-id="f51bf-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="f51bf-107">Banyak logika bisnis di sisi klien dan server solusi tergantung pada bidang **jenis**.</span><span class="sxs-lookup"><span data-stu-id="f51bf-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="f51bf-108">Oleh karena itu, penting bahwa bidang diinisialisasi dengan nilai yang benar saat entitas dibuat.</span><span class="sxs-lookup"><span data-stu-id="f51bf-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="f51bf-109">Nilai yang salah dapat menyebabkan perilaku yang tidak benar, dan beberapa logika bisnis mungkin tidak berjalan dengan benar.</span><span class="sxs-lookup"><span data-stu-id="f51bf-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="f51bf-110">Pengalihan formulir otomatis</span><span class="sxs-lookup"><span data-stu-id="f51bf-110">Automatic form switching</span></span>

<span data-ttu-id="f51bf-111">Untuk menghindari kerusakan data potensial dan perilaku tak terduga yang disebabkan oleh inisialisasi salah dan mengedit rekaman entitas penjualan, PSA sekarang mencakup logika untuk beralih formulir otomatis dalam formulir bawaan.</span><span class="sxs-lookup"><span data-stu-id="f51bf-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="f51bf-112">Logika ini akan membawa pengguna ke formulir yang benar untuk bekerja dengan versi berbasis pekerjaan atau jenis peluang, kuotasi, pesanan, atau entitas faktur lainnya.</span><span class="sxs-lookup"><span data-stu-id="f51bf-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="f51bf-113">Bila pengguna membuka versi berbasis pekerjaan peluang, kuotasi, pesanan, atau entitas faktur, formulir akan beralih ke **informasi proyek**.</span><span class="sxs-lookup"><span data-stu-id="f51bf-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="f51bf-114">Logika peralihan formulir otomatis tergantung pada pemetaan antara nilai **formId** dan bidang **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="f51bf-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="f51bf-115">Semua formulir bawaan telah ditambahkan ke pemetaan tersebut.</span><span class="sxs-lookup"><span data-stu-id="f51bf-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="f51bf-116">Namun, formulir kustom harus ditambahkan secara manual untuk menunjukkan versi entitas yang ditujukan untuk ditangani.</span><span class="sxs-lookup"><span data-stu-id="f51bf-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="f51bf-117">Ini didasarkan pada bidang **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="f51bf-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="f51bf-118">Jika peralihan formulir hilang dari pemetaan, logika akan beralih ke formulir bawaan, berdasarkan nilai yang disimpan dalam bidang entitas **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="f51bf-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="f51bf-119">Tambahkan formulir kustom dan Hidupkan logika beralih formulir</span><span class="sxs-lookup"><span data-stu-id="f51bf-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="f51bf-120">Contoh berikut menunjukkan cara menambahkan formulir kustom, **informasi proyek saya** , sehingga berfungsi pada peluang berbasis pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="f51bf-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="f51bf-121">Proses yang sama digunakan untuk menambahkan formulir kustom agar berfungsi dengan kuotasi, pesanan, dan faktur.</span><span class="sxs-lookup"><span data-stu-id="f51bf-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="f51bf-122">Ikuti langkah berikut untuk membuat formulir **informasi proyek** versi kustom.</span><span class="sxs-lookup"><span data-stu-id="f51bf-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="f51bf-123">Di entitas peluang, buka formulir **informasi proyek** , dan Simpan salinan dalam nama **informasi proyek saya**.</span><span class="sxs-lookup"><span data-stu-id="f51bf-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="f51bf-124">Buka formulir baru, dan kemudian, di properti, pastikan bahwa skrip inisialisasi formulir dari formulir **informasi proyek** ada.</span><span class="sxs-lookup"><span data-stu-id="f51bf-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="f51bf-125">Jangan hapus skrip.</span><span class="sxs-lookup"><span data-stu-id="f51bf-125">Don't remove the scripts.</span></span> <span data-ttu-id="f51bf-126">Jika tidak, beberapa data mungkin diinisialisasi dengan tidak benar.</span><span class="sxs-lookup"><span data-stu-id="f51bf-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="f51bf-127">Verifikasikan bahwa bidang **jenis** ( **msdyn\_ordertype** ) ada di formulir.</span><span class="sxs-lookup"><span data-stu-id="f51bf-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="f51bf-128">Jangan hapus bidang ini.</span><span class="sxs-lookup"><span data-stu-id="f51bf-128">Don't remove this field.</span></span> <span data-ttu-id="f51bf-129">Jika tidak, skrip inisiasi akan gagal.</span><span class="sxs-lookup"><span data-stu-id="f51bf-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="f51bf-130">Temukan nilai **formId** formulir baru.</span><span class="sxs-lookup"><span data-stu-id="f51bf-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="f51bf-131">Anda dapat menyelesaikan langkah ini dengan dua cara:</span><span class="sxs-lookup"><span data-stu-id="f51bf-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="f51bf-132">Mengekspor formulir **informasi proyek saya** sebagai bagian dari solusi tidak terkelola, lalu mencari nilai **formid** dalam file Customization.xml solusi yang diekspor.</span><span class="sxs-lookup"><span data-stu-id="f51bf-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="f51bf-133">Buka formulir **informasi proyek saya** di editor formulir, lalu cari pengidentifikasi unik global (GUID) di samping parameter **fromid** di URL, sebagaimana ditampilkan dalam ilustrasi berikut.</span><span class="sxs-lookup"><span data-stu-id="f51bf-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Nilai formId formulir baru di URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="f51bf-135">Buat pemetaan **msdyn\_ordertype** untuk nilai **formid** dengan mengedit sumber daya msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js</span><span class="sxs-lookup"><span data-stu-id="f51bf-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="f51bf-136">Hapus kode dari sumber daya, dan gantilah dengan kode berikut.</span><span class="sxs-lookup"><span data-stu-id="f51bf-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="f51bf-137">Simpan, lalu Publikasikan penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="f51bf-137">Save and then publish the customizations.</span></span>
