---
title: Catatan pengembang untuk persetujuan
description: Topik ini memberikan informasi pengembang tambahan tentang cara menangani persetujuan.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483952"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="e1fae-103">Catatan pengembang untuk persetujuan</span><span class="sxs-lookup"><span data-stu-id="e1fae-103">Developer notes for Approvals</span></span>

<span data-ttu-id="e1fae-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="e1fae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1fae-105">Dynamics 365 Project Operations mencakup logika validasi yang memastikan transisi rekaman yang benar melalui tahapan perjanjian.</span><span class="sxs-lookup"><span data-stu-id="e1fae-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="e1fae-106">Transisi rekaman yang benar memastikan:</span><span class="sxs-lookup"><span data-stu-id="e1fae-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="e1fae-107">Semua baris pendukung dibuat dalam tabel terkait, seperti jurnal dan aktual.</span><span class="sxs-lookup"><span data-stu-id="e1fae-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="e1fae-108">Pemberi izin ditandai sebagai **pemberi izin proyek** dalam proyek sebelum melanjutkan.</span><span class="sxs-lookup"><span data-stu-id="e1fae-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
