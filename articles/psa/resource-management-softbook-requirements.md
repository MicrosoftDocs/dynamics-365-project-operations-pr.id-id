---
title: Persyaratan pesanan tentatif
description: Topik ini menyediakan informasi tentang cara memenuhi persyaratan pesanan tentatif.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282922"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="485bb-103">Persyaratan pesanan tentatif</span><span class="sxs-lookup"><span data-stu-id="485bb-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="485bb-104">Persyaratan sumber daya dapat dipesan secara definitif.</span><span class="sxs-lookup"><span data-stu-id="485bb-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="485bb-105">Pemesanan definitif membuat proposal yang menghabiskan kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="485bb-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="485bb-106">Usulan ini kemudian dikirim kembali ke pemohon untuk disetujui.</span><span class="sxs-lookup"><span data-stu-id="485bb-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="485bb-107">Pemesanan tentatif menambahkan sumber daya ke tim proyek dan memiliki status yang berbeda di papan jadwal, namun tidak mengkonsumsi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="485bb-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="485bb-108">Untuk melakukan pesanan tentatif sumber daya dari papan jadwal, atur bidang **status Pemesanan** menjadi **tentatif**.</span><span class="sxs-lookup"><span data-stu-id="485bb-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Status pemesanan diatur ke tentatif](media/Resource-Management-image77.png)

<span data-ttu-id="485bb-110">Saat tab **tim** berada di tampilan **anggota tim bernama**, sumber daya ditampilkan di sana.</span><span class="sxs-lookup"><span data-stu-id="485bb-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="485bb-111">Jam yang dipesan dengan tentatif dilaporkan di kolom **jam pesanan tentatif**.</span><span class="sxs-lookup"><span data-stu-id="485bb-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Jam pesanan tentatif di tampilan anggota tim bernama](media/Resource-Management-image78.png)

<span data-ttu-id="485bb-113">Anggota tim dipesan terlebih dulu tidak dapat ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="485bb-113">Soft-booked team members can be assigned to tasks.</span></span>

![Anggota tim dipesan tentatif ditetapkan ke tugas.](media/Resource-Management-image79.png)

<span data-ttu-id="485bb-115">Pada tab **rekonsiliasi**, tidak ada Pemesanan yang ditampilkan untuk sumber daya pesanan tentatif, karena tab **rekonsiliasi** hanya mempertimbangkan Pemesanan definitif.</span><span class="sxs-lookup"><span data-stu-id="485bb-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Sumber daya yang dipesan dengan tentatif tanpa pemesanan pada tab rekonsiliasi](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="485bb-117">Anda tidak dapat memesan sumber daya secara tentatif dari persyaratan yang dihasilkan dari anggota tim generik.</span><span class="sxs-lookup"><span data-stu-id="485bb-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="485bb-118">Di papan jadwal, pewarnaan yang berbeda digunakan untuk pemesanan tentatif untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="485bb-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Melakukan pemesanan tentatif di papan jadwal](media/Resource-Management-image81.png)

<span data-ttu-id="485bb-120">Untuk mengkonversi Pemesanan tentatif ke Pemesanan definitif, di papan jadwal, klik kanan Pemesanan tentatif, lalu pilih **Ubah status** \> **Pesanan definitif** \> **Definitif**.</span><span class="sxs-lookup"><span data-stu-id="485bb-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Mengubah status pemesanan menjadi Definitif](media/Resource-Management-image82.png)

<span data-ttu-id="485bb-122">Pemesanan diubah, dan status berubah di papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="485bb-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="485bb-123">Karena status pemesanan sekarang **Definitif**, sumber daya ditampilkan sebagai dipesan, dan kapasitas serta ketersediaannya disesuaikan.</span><span class="sxs-lookup"><span data-stu-id="485bb-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="485bb-124">Anda dapat menggunakan metode yang sama untuk membatalkan pemesanan definitif atau Pemesanan tentatif dari papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="485bb-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="485bb-125">Untuk mengkonversi sumber daya yang dipesan dengan tentatif ke definitif pada tab **tim** proyek, pilih sumber daya, lalu pilih **konfirmasikan**.</span><span class="sxs-lookup"><span data-stu-id="485bb-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Perintah Konfirmasi](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]