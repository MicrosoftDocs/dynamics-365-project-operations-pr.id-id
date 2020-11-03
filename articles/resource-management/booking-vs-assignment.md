---
title: Pemesanan vs Penugasan
description: Topik ini memberikan informasi perbedaan antara pemesanan sumber daya dan penugasan sumber daya.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078333"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="554f1-103">Pemesanan vs Penugasan</span><span class="sxs-lookup"><span data-stu-id="554f1-103">Bookings vs assignments</span></span>

<span data-ttu-id="554f1-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="554f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="554f1-105">Pemesanan adalah alokasi sumber daya definitif atau tentatif ke proyek.</span><span class="sxs-lookup"><span data-stu-id="554f1-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="554f1-106">Pemesanan definitif mengkonsumsi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="554f1-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="554f1-107">Penetapan adalah Penetapan sumber daya untuk tugas proyek dalam jadwal proyek.</span><span class="sxs-lookup"><span data-stu-id="554f1-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="554f1-108">Sumber daya dapat riil atau generik.</span><span class="sxs-lookup"><span data-stu-id="554f1-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="554f1-109">Idealnya, untuk sumber daya riil, Pemesanan dan penetapan harus sesuai, karena tidak berbeda.</span><span class="sxs-lookup"><span data-stu-id="554f1-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="554f1-110">Namun, Microsoft Dynamics Project Operations tidak menegakkan Perjanjian ini.</span><span class="sxs-lookup"><span data-stu-id="554f1-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="554f1-111">Tampilan **rekonsiliasi** menunjukkan manajer proyek tempat di mana Pemesanan sumber daya dan penetapan tidak sesuai.</span><span class="sxs-lookup"><span data-stu-id="554f1-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
