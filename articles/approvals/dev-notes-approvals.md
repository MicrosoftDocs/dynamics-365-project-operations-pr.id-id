---
title: Catatan pengembang untuk persetujuan
description: Topik ini memberikan informasi pengembang tambahan tentang cara menangani persetujuan.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996795"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="8dc89-103">Catatan pengembang untuk persetujuan</span><span class="sxs-lookup"><span data-stu-id="8dc89-103">Developer notes for Approvals</span></span>

<span data-ttu-id="8dc89-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="8dc89-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8dc89-105">Dynamics 365 Project Operations mencakup logika validasi yang memastikan transisi rekaman yang benar melalui tahapan perjanjian.</span><span class="sxs-lookup"><span data-stu-id="8dc89-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="8dc89-106">Transisi rekaman yang benar memastikan:</span><span class="sxs-lookup"><span data-stu-id="8dc89-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="8dc89-107">Semua baris pendukung dibuat dalam tabel terkait, seperti jurnal dan aktual.</span><span class="sxs-lookup"><span data-stu-id="8dc89-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="8dc89-108">Pemberi izin ditandai sebagai **pemberi izin proyek** dalam proyek sebelum melanjutkan.</span><span class="sxs-lookup"><span data-stu-id="8dc89-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]