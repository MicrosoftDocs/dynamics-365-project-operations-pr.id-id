---
title: Pemesanan vs Penugasan
description: Topik ini memberikan informasi perbedaan antara pemesanan sumber daya dan penugasan sumber daya.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012770"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="11043-103">Pemesanan vs Penugasan</span><span class="sxs-lookup"><span data-stu-id="11043-103">Bookings vs assignments</span></span>

<span data-ttu-id="11043-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="11043-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="11043-105">Pemesanan adalah alokasi sumber daya definitif atau tentatif ke proyek.</span><span class="sxs-lookup"><span data-stu-id="11043-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="11043-106">Pemesanan definitif mengkonsumsi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="11043-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="11043-107">Pemesanan mewakili konsep organisasi untuk tim sehingga mereka dapat memahami bagaimana sumber daya akan terlibat di berbagai proyek.</span><span class="sxs-lookup"><span data-stu-id="11043-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="11043-108">Dynamics 365 Project Operations mempertimbangkan pemesanan sebagai konsep tingkat proyek.</span><span class="sxs-lookup"><span data-stu-id="11043-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="11043-109">Tidak seperti pemesanan, penetapan adalah komitmen sumber daya untuk tugas proyek dalam jadwal proyek.</span><span class="sxs-lookup"><span data-stu-id="11043-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="11043-110">Sumber daya dapat diberi nama atau generik.</span><span class="sxs-lookup"><span data-stu-id="11043-110">The resources can be named or generic.</span></span>  <span data-ttu-id="11043-111">Bila kebutuhan sumber daya diambil dari penetapan tugas proyek, Project Operations menggunakan kontur upaya penetapan sumber daya untuk membangun kontur detail kebutuhan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="11043-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="11043-112">Namun, referensi penetapan sumber daya tidak dipertahankan.</span><span class="sxs-lookup"><span data-stu-id="11043-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="11043-113">Pembaruan pemesanan yang diambil dari persyaratan sumber daya tidak memperbarui penetapan sumber daya apa pun.</span><span class="sxs-lookup"><span data-stu-id="11043-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="11043-114">Biasanya, jumlah pemesanan untuk sumber daya akan sama dengan jumlah penetapan sumber daya di satu atau banyak tugas.</span><span class="sxs-lookup"><span data-stu-id="11043-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="11043-115">Namun, Project Operations tidak menegakkan Perjanjian ini.</span><span class="sxs-lookup"><span data-stu-id="11043-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="11043-116">Tampilan **rekonsiliasi** menunjukkan manajer proyek tempat di mana Pemesanan sumber daya dan penetapan tidak sesuai.</span><span class="sxs-lookup"><span data-stu-id="11043-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]