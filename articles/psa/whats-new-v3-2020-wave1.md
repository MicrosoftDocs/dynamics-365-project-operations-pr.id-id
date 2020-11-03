---
title: Yang baru atau yang diubah di Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan informasi tentang apa yang baru dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078430"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="2477b-103">Yang baru atau yang diubah di Project Service Automation versi 3 gelombang 1 2020</span><span class="sxs-lookup"><span data-stu-id="2477b-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="2477b-104">Topik ini menyoroti pertimbangan peningkatan utama saat beralih ke rilis terbaru dari Project Service Automation (PSA) versi 3. x wave 1 2020.</span><span class="sxs-lookup"><span data-stu-id="2477b-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="2477b-105">Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="2477b-105">Time entry</span></span>
<span data-ttu-id="2477b-106">Pengalaman entri waktu diperpanjang untuk memberikan kemampuan untuk memperpanjang entri waktu ke skenario pelanggan lainnya.</span><span class="sxs-lookup"><span data-stu-id="2477b-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="2477b-107">Ini mencakup kemampuan untuk menambahkan jenis entri, yang sekarang mendorong perilaku tertentu berdasarkan nama skema bidang, **Pengaturan Entri Waktu** yang ditampilkan sebagai **sumber waktu**.</span><span class="sxs-lookup"><span data-stu-id="2477b-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings** , displayed as **Time Source**.</span></span> <span data-ttu-id="2477b-108">Solusi baru, disebut waktu, pengeluaran, Penstatusan, dan persetujuan (TESA) telah ditambahkan untuk mendukung fungsi ini.</span><span class="sxs-lookup"><span data-stu-id="2477b-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="2477b-109">Pertimbangan upgrade</span><span class="sxs-lookup"><span data-stu-id="2477b-109">Upgrade consideration</span></span>
<span data-ttu-id="2477b-110">Untuk mendukung fungsi ini, peran dalam PSA telah diperbarui untuk mencakup hak istimewa baru.</span><span class="sxs-lookup"><span data-stu-id="2477b-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="2477b-111">Hak istimewa ini memberikan akses baca ke entitas baru, **pengaturan entri waktu**.</span><span class="sxs-lookup"><span data-stu-id="2477b-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="2477b-112">Pengguna yang memerlukan kemampuan untuk mencatat waktu harus diberikan peran pengguna **Pengguna entri waktu** selain peran yang ada.</span><span class="sxs-lookup"><span data-stu-id="2477b-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="2477b-113">Peran ini mencakup fungsi baru dan memastikan bahwa entri waktu akan terus berfungsi.</span><span class="sxs-lookup"><span data-stu-id="2477b-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="2477b-114">Selain itu, jika Anda memiliki modul aplikasi kustom yang mencakup semua formulir untuk entitas entri waktu, Anda akan diminta untuk menghapus **formulir pembuatan cepat waktu TESA** dari modul.</span><span class="sxs-lookup"><span data-stu-id="2477b-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="2477b-115">Perubahan entri waktu perpanjangan saat ini</span><span class="sxs-lookup"><span data-stu-id="2477b-115">Currently extended time entry changes</span></span>
<span data-ttu-id="2477b-116">Untuk meminimalkan dampak terhadap pengguna waktu masuk saat ini, perubahan peran ini adalah satu-satunya persyaratan inti yang diperlukan untuk terus memanfaatkan entri waktu.</span><span class="sxs-lookup"><span data-stu-id="2477b-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="2477b-117">Jika Anda telah membuat tampilan kustom atau pengalaman entri waktu terpisah, Anda harus menetapkan bidang **pengaturan entri waktu** ke nilai PSA yang benar.</span><span class="sxs-lookup"><span data-stu-id="2477b-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
