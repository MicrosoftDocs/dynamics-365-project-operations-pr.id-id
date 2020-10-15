---
title: Memahami status proyek
description: Topik ini menyediakan informasi tentang status yang ditetapkan ke proyek di Dynamics 365 Project operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965680"
---
# <a name="understand-project-status"></a><span data-ttu-id="bed66-103">Memahami status proyek</span><span class="sxs-lookup"><span data-stu-id="bed66-103">Understand project status</span></span>

<span data-ttu-id="bed66-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="bed66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="bed66-105">Bagian **status** pada halaman **entitas proyek** memberikan ringkasan tentang kesehatan suatu proyek berdasarkan biaya dan usaha.</span><span class="sxs-lookup"><span data-stu-id="bed66-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="bed66-106">Bidang ringkasan status</span><span class="sxs-lookup"><span data-stu-id="bed66-106">Status summary fields</span></span>

- <span data-ttu-id="bed66-107">Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek.</span><span class="sxs-lookup"><span data-stu-id="bed66-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="bed66-108">Bidang ini menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="bed66-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="bed66-109">Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status.</span><span class="sxs-lookup"><span data-stu-id="bed66-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="bed66-110">Bidang **Status yang diperbarui pada** tidak dapat diedit.</span><span class="sxs-lookup"><span data-stu-id="bed66-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="bed66-111">Nilai dalam bidang ini adalah stempel waktu yang menunjukkan waktu pembaruan status terakhir.</span><span class="sxs-lookup"><span data-stu-id="bed66-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="bed66-112">Bidang **performa jadwal** dan **performa biaya** ditetapkan dari kisi pelacakan.</span><span class="sxs-lookup"><span data-stu-id="bed66-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="bed66-113">Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, bidang ini diperbarui **ke depan**.</span><span class="sxs-lookup"><span data-stu-id="bed66-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="bed66-114">Bila jadwal dan varians biaya untuk node root negatif, bidang ini diatur ke **belakang**.</span><span class="sxs-lookup"><span data-stu-id="bed66-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
