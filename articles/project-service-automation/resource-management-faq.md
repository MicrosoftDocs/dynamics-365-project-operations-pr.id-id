---
title: Tanya-Jawab Manajemen sumber daya
description: Topik ini memberikan jawaban atas pertanyaan umum tentang manajemen sumber daya.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752487"
---
# <a name="resource-management-faq"></a><span data-ttu-id="44093-103">Tanya-Jawab Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="44093-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="44093-104">Apa perbedaan antara persyaratan anggota tim dan sumber daya?</span><span class="sxs-lookup"><span data-stu-id="44093-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="44093-105">Anggota tim proyek dapat ditetapkan ke tugas, memesan atau memesan berlebihan, dan diatur sebagai pemberi izin.</span><span class="sxs-lookup"><span data-stu-id="44093-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="44093-106">Persyaratan sumber daya dapat ada tanpa anggota tim proyek, sebagai catatan draf permintaan.</span><span class="sxs-lookup"><span data-stu-id="44093-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="44093-107">Apa perbedaan antara jam yang diusulkan dan dipesan tentatif?</span><span class="sxs-lookup"><span data-stu-id="44093-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="44093-108">Jam yang diusulkan dan jam yang dipesan tentatif berbeda dalam hal visibilitas.</span><span class="sxs-lookup"><span data-stu-id="44093-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="44093-109">Jam yang diusulkan hanya dapat dilihat oleh Manajer sumber daya dan manajer proyek yang memulai permintaan menggunakan permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="44093-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="44093-110">Jam pesanan tentatif dapat dilihat oleh siapa pun yang memiliki akses ke papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="44093-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="44093-111">Bagaimana cara melihat jam pesanan tentatif untuk sumber daya pada tim?</span><span class="sxs-lookup"><span data-stu-id="44093-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="44093-112">Pesanan tentatif dapat dilakukan ketika melakukan pemesanan persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="44093-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="44093-113">Sumber daya yang dipesan dengan tentatif pada tim proyek akan muncul sebagai anggota tim yang memiliki jam yang telah dipesan dengan tentatif.</span><span class="sxs-lookup"><span data-stu-id="44093-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="44093-114">Mereka juga akan ditampilkan di papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="44093-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="44093-115">Bagaimana cara mengubah jam yang diperlukan, dan tanggal mulai dan berakhir, untuk sumber daya (generik atau bernama) yang saya pesan?</span><span class="sxs-lookup"><span data-stu-id="44093-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="44093-116">Setelah sumber daya dipesan, pilih **Kelola Pemesanan** untuk melakukan perubahan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="44093-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="44093-117">Jenis sumber daya Apakah yang didukung oleh dukungan Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="44093-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="44093-118">**Pengguna** dan **kontak** adalah satu-satunya jenis sumber daya yang didukung Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="44093-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="44093-119">Walaupun Anda dapat membuat jenis sumber daya lain (misalnya, **perlengkapan**, dan **grup**), tidak ada penggunaan ujung ke ujung yang didukung.</span><span class="sxs-lookup"><span data-stu-id="44093-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="44093-120">Apa antara penetapan dan Pemesanan?</span><span class="sxs-lookup"><span data-stu-id="44093-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="44093-121">Penetapan adalah Penetapan sumber daya untuk tugas proyek dalam jadwal proyek.</span><span class="sxs-lookup"><span data-stu-id="44093-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="44093-122">Sumber daya dapat merupakan sumber daya riil atau generik.</span><span class="sxs-lookup"><span data-stu-id="44093-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="44093-123">Pemesanan adalah alokasi sumber daya definitif atau tentatif ke proyek.</span><span class="sxs-lookup"><span data-stu-id="44093-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="44093-124">Pemesanan definitif mengkonsumsi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="44093-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="44093-125">Idealnya, untuk sumber daya riil, Pemesanan dan penetapan harus sesuai, karena tidak berbeda.</span><span class="sxs-lookup"><span data-stu-id="44093-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="44093-126">Namun, PSA tidak menegakkan Perjanjian ini.</span><span class="sxs-lookup"><span data-stu-id="44093-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="44093-127">Tampilan rekonsiliasi menunjukkan manajer proyek tempat di mana Pemesanan sumber daya dan penetapan tidak sesuai.</span><span class="sxs-lookup"><span data-stu-id="44093-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
