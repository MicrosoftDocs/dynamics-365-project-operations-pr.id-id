---
title: Pemenuhan persyaratan sumber daya generik
description: Topik ini menyediakan informasi tentang cara pemesanan sumber daya bernama untuk persyaratan sumber daya generik.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279592"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="26ca6-103">Pemenuhan persyaratan sumber daya generik</span><span class="sxs-lookup"><span data-stu-id="26ca6-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="26ca6-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="26ca6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26ca6-105">Anda dapat memesan sumber daya bernama untuk menggantikan sumber daya generik yang memiliki persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="26ca6-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="26ca6-106">Pada halaman **proyek**, pilih tab **Tim**.</span><span class="sxs-lookup"><span data-stu-id="26ca6-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="26ca6-107">Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu pilih **pesan**.</span><span class="sxs-lookup"><span data-stu-id="26ca6-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="26ca6-108">Atau, buka persyaratan sumber daya, lalu pilih **pesan**.</span><span class="sxs-lookup"><span data-stu-id="26ca6-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="26ca6-109">Di halaman **asisten jadwal**, pilih sumber daya bernama untuk melakukan pemesanan ke tim proyek, lalu pilih **pesan**.</span><span class="sxs-lookup"><span data-stu-id="26ca6-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="26ca6-110">Bila Pemesanan selesai dan dipenuhi oleh sumber daya bernama, sumber daya generik digantikan dengan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="26ca6-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="26ca6-111">Tugas pada jadwal diperbarui dengan sumber daya bernama juga.</span><span class="sxs-lookup"><span data-stu-id="26ca6-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="26ca6-112">Penuhi sumber daya generik dengan beberapa sumber daya bernama</span><span class="sxs-lookup"><span data-stu-id="26ca6-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="26ca6-113">Memenuhi persyaratan untuk sumber daya generik dengan beberapa sumber daya bernama serupa dengan menetapkan satu sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="26ca6-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="26ca6-114">Misalnya, ada tugas dengan durasi lima hari dan 120 jam upaya.</span><span class="sxs-lookup"><span data-stu-id="26ca6-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="26ca6-115">Tugas ini tidak dapat diselesaikan dengan satu sumber daya yang bekerja selama delapan jam sehari selama lima hari seminggu.</span><span class="sxs-lookup"><span data-stu-id="26ca6-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="26ca6-116">Persyaratannya adalah untuk 120 jam rekayasa Robotika selama lima hari, yang merupakan 24 jam per hari.</span><span class="sxs-lookup"><span data-stu-id="26ca6-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="26ca6-117">Ini adalah contoh bila beberapa sumber daya bernama diperlukan untuk memenuhi permintaan sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="26ca6-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="26ca6-118">Anda perlu memesan beberapa sumber daya untuk memenuhi persyaratan.</span><span class="sxs-lookup"><span data-stu-id="26ca6-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="26ca6-119">Perbedaan utama dalam skenario ini adalah bahwa sumber daya generik tetap pada tim yang ditetapkan untuk tugas, dan anggota tim sumber daya bernama yang dipesan tidak ditetapkan sebagai bagian dari posisi.</span><span class="sxs-lookup"><span data-stu-id="26ca6-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="26ca6-120">Manajer proyek dapat menetapkan pekerjaan yang sesuai dengan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="26ca6-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="26ca6-121">Tampilan **rekonsiliasi** dapat membantu manajer proyek dalam memecah Pemesanan di beberapa sumber daya menjadi penetapan tugas.</span><span class="sxs-lookup"><span data-stu-id="26ca6-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="26ca6-122">Hal ini tidak dilakukan secara otomatis karena dalam skenario apa pun yang lebih rumit daripada contoh sederhana di atas, seperti di mana Anda memiliki bundel tugas yang membuat persyaratan atau maksud dari bagaimana manajer proyek ingin menugaskan, harus diasumsikan oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="26ca6-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="26ca6-123">Karena sistem tidak dapat memahami maksud, mungkin asumsi cenderung akan berbeda dari yang dimaksudkan dan hasil yang tidak tepat atau tidak terduga akan terjadi.</span><span class="sxs-lookup"><span data-stu-id="26ca6-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="26ca6-124">Hasil yang dapat diprediksi adalah bahwa sumber daya generik tetap ditugaskan hingga manajer proyek dengan sengaja membuat tugas, dengan bantuan tampilan **rekonsiliasi**.</span><span class="sxs-lookup"><span data-stu-id="26ca6-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]