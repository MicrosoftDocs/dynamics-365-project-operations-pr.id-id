---
title: Pesan sumber daya bernama dari persyaratan sumber daya.
description: Topik ini menyediakan informasi tentang pemesanan sumber daya bernama untuk persyaratan sumber daya generik.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291038"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="c924e-103">Pesan sumber daya bernama dari persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="c924e-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c924e-104">Anda dapat memesan sumber daya bernama untuk menggantikan sumber daya generik yang memiliki persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="c924e-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c924e-105">Di Project Service Automation (PSA), di halaman **proyek**, klik tab **tim**.</span><span class="sxs-lookup"><span data-stu-id="c924e-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="c924e-106">Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu klik **pesan**.</span><span class="sxs-lookup"><span data-stu-id="c924e-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="c924e-107">Atau, buka persyaratan sumber daya, lalu klik **pesan**.</span><span class="sxs-lookup"><span data-stu-id="c924e-107">Or, open the resource requirement and then click **Book**.</span></span>


![Memesan anggota tim generik](media/RM-how-to-14.png)


3. <span data-ttu-id="c924e-109">Di halaman **asisten jadwal**, pilih sumber daya bernama untuk melakukan pemesanan ke tim proyek, lalu klik **pesan**.</span><span class="sxs-lookup"><span data-stu-id="c924e-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Memesan anggota tim generik menggunakan Asisten jadwal](media/RM-how-to-15.png)

<span data-ttu-id="c924e-111">Bila Pemesanan selesai dan dipenuhi oleh sumber daya bernama, sumber daya generik digantikan dengan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="c924e-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Anggota tim bernama menggantikan anggota tim generik](media/RM-how-to-16.png)

<span data-ttu-id="c924e-113">Tugas pada jadwal diperbarui dengan sumber daya bernama juga.</span><span class="sxs-lookup"><span data-stu-id="c924e-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Anggota tim bernama ditetapkan ke tugas proyek](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c924e-115">Penuhi sumber daya generik dengan beberapa sumber daya bernama</span><span class="sxs-lookup"><span data-stu-id="c924e-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c924e-116">Memenuhi persyaratan untuk sumber daya generik dengan beberapa sumber daya bernama serupa dengan menetapkan satu sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="c924e-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c924e-117">Misalnya, ada tugas dengan durasi lima hari dan 120 jam upaya.</span><span class="sxs-lookup"><span data-stu-id="c924e-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c924e-118">Tugas ini tidak dapat diselesaikan dengan satu sumber daya yang bekerja selama delapan jam sehari selama lima hari seminggu.</span><span class="sxs-lookup"><span data-stu-id="c924e-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Sebuah tugas memerlukan 120 jam kerja selama lima hari](media/RM-how-to-21.png)

<span data-ttu-id="c924e-120">Persyaratannya adalah untuk 120 jam rekayasa Robotika selama lima hari, yang merupakan 24 jam per hari.</span><span class="sxs-lookup"><span data-stu-id="c924e-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Persyaratan per hari](media/RM-how-to-22.png)

<span data-ttu-id="c924e-122">Ini adalah contoh bila beberapa sumber daya bernama diperlukan untuk memenuhi permintaan sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="c924e-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c924e-123">Anda perlu memesan beberapa sumber daya untuk memenuhi persyaratan.</span><span class="sxs-lookup"><span data-stu-id="c924e-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Pemesanan beberapa sumber daya untuk memenuhi persyaratan](media/RM-how-to-23.png)

<span data-ttu-id="c924e-125">Perbedaan utama dalam skenario ini adalah bahwa sumber daya generik tetap pada tim yang ditetapkan untuk tugas, dan anggota tim sumber daya bernama yang dipesan tidak ditetapkan sebagai bagian dari posisi.</span><span class="sxs-lookup"><span data-stu-id="c924e-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c924e-126">Manajer proyek dapat menetapkan pekerjaan yang sesuai dengan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="c924e-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c924e-127">Tampilan **rekonsiliasi** dapat membantu manajer proyek dalam memecah Pemesanan di beberapa sumber daya menjadi penetapan tugas.</span><span class="sxs-lookup"><span data-stu-id="c924e-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c924e-128">Hal ini tidak dilakukan secara otomatis karena dalam skenario apa pun yang lebih rumit daripada contoh sederhana di atas, seperti di mana Anda memiliki bundel tugas yang membuat persyaratan, maksud dari bagaimana manajer proyek ingin menugaskan, harus diasumsikan oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="c924e-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c924e-129">Karena sistem tidak dapat memahami maksud, kemungkinannya adalah asumsi yang akan berbeda dari yang dimaksudkan dan hasil yang tidak tepat atau tidak terduga akan terjadi.</span><span class="sxs-lookup"><span data-stu-id="c924e-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="c924e-130">Hasil yang dapat diprediksi adalah bahwa sumber daya generik tetap ditugaskan hingga manajer proyek dengan sengaja membuat tugas, dengan bantuan tampilan **rekonsiliasi**.</span><span class="sxs-lookup"><span data-stu-id="c924e-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]