---
title: Mengapa harga diatur default ke nol pada biaya waktu aktual?
description: Pemecahan masalah mengapa harga diatur default ke nol pada biaya waktu aktual.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ffe915a48f088bde457121a323325ba490c24e45
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993060"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="02564-103">Mengapa harga diatur default ke nol pada biaya waktu aktual?</span><span class="sxs-lookup"><span data-stu-id="02564-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="02564-104">FAQ ini berlaku untuk nilai aktual di mana kelas transaksi diatur ke waktu dan jenis transaksi adalah biaya.</span><span class="sxs-lookup"><span data-stu-id="02564-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="02564-105">Tiga pemeriksaan berikut akan membantu Anda memecahkan masalah mengapa harga diatur default ke 0 pada biaya waktu aktual.</span><span class="sxs-lookup"><span data-stu-id="02564-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="02564-106">Periksa 1: Mengidentifikasi daftar harga biaya untuk proyek</span><span class="sxs-lookup"><span data-stu-id="02564-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="02564-107">Temukan proyek dari bidang proyek aktual lalu buka halaman proyek.</span><span class="sxs-lookup"><span data-stu-id="02564-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="02564-108">Klik link unit kontrak pada bidang.</span><span class="sxs-lookup"><span data-stu-id="02564-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="02564-109">Pada halaman Unit kontrak, periksa apakah unit kontrak memiliki daftar harga dalam kisi daftar harga biaya.</span><span class="sxs-lookup"><span data-stu-id="02564-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="02564-110">Jika lebih dari satu daftar harga, Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="02564-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="02564-111">Project Service hanya mendukung satu daftar harga per unit organisasional.</span><span class="sxs-lookup"><span data-stu-id="02564-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="02564-112">Hapus semua daftar harga dari entitas ini hingga ada hanya satu daftar harga yang terlampir di kisi daftar harga biaya unit organisasional.</span><span class="sxs-lookup"><span data-stu-id="02564-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="02564-113">Jika tidak ada daftar harga yang dilampirkan ke Unit organisasional, catat mata uang unit organisasional.</span><span class="sxs-lookup"><span data-stu-id="02564-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="02564-114">Buka project service dan parameter, lalu buka tab daftar harga. Centang jika ada daftar harga dengan konteks diatur ke biaya dan mata uang yang sesuai dengan mata uang Unit organisasional.</span><span class="sxs-lookup"><span data-stu-id="02564-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="02564-115">Jika tidak ada daftar harga yang sesuai dengan kriteria tersebut, Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="02564-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="02564-116">Pastikan Anda memiliki minimal satu daftar harga dengan konteks yang diatur ke biaya dan mata uang yang sesuai dengan mata uang Unit organisasional.</span><span class="sxs-lookup"><span data-stu-id="02564-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="02564-117">Jika terdapat lebih dari satu daftar harga yang cocok dengan kriteria, Lanjutkan membaca dokumen ini untuk membuat lebih banyak pemeriksaan.</span><span class="sxs-lookup"><span data-stu-id="02564-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="02564-118">Centang 2: Apakah salah satu daftar harga yang tercantum di atas berlaku untuk tanggal tertentu biaya waktu aktual?</span><span class="sxs-lookup"><span data-stu-id="02564-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="02564-119">Agar project service mempertimbangkan daftar harga untuk default harga, daftar harga tersebut harus berlaku untuk tanggal di biaya waktu aktual.</span><span class="sxs-lookup"><span data-stu-id="02564-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="02564-120">Periksa berikut untuk melihat apakah daftar harga yang tercantum di atas berlaku:</span><span class="sxs-lookup"><span data-stu-id="02564-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="02564-121">Periksa apakah tanggal mulai dan berakhir pada tab Umum untuk daftar harga yang terlampir tidak kosong.</span><span class="sxs-lookup"><span data-stu-id="02564-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="02564-122">Jika tanggal mulai dan berakhir pada harga yang tercantum di atas daftar kosong, Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="02564-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="02564-123">Buat catatan dari bidang tanggal mulai pada biaya waktu aktual dan periksa apakah salah satu daftar harga yang tercantum berlaku untuk tanggal itu.</span><span class="sxs-lookup"><span data-stu-id="02564-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="02564-124">Misalnya, tanggal biaya waktu aktual harus berada dalam tanggal mulai dan tanggal berakhir pada daftar harga.</span><span class="sxs-lookup"><span data-stu-id="02564-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="02564-125">Jika tidak ada daftar harga yang mencakup tanggal di biaya waktu aktual, Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="02564-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="02564-126">Modifikasi tanggal mulai dan berakhir daftar harga untuk memastikan bahwa daftar harga mencakup tanggal biaya waktu aktual.</span><span class="sxs-lookup"><span data-stu-id="02564-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="02564-127">Jika lebih dari atu daftar harga yang mencakup tanggal di biaya waktu aktual, Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="02564-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="02564-128">Anda dapat memperbaiki ini dengan mengedit tanggal berakhir dan mulai dari daftar harga sehingga ada hanya satu daftar harga yang mencakup tanggal biaya waktu aktual.</span><span class="sxs-lookup"><span data-stu-id="02564-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="02564-129">Jika ada hanya satu daftar harga yang mencakup tanggal waktu biaya aktual, beralih ke Centang berikutnya dalam dokumen.</span><span class="sxs-lookup"><span data-stu-id="02564-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="02564-130">Setelah Anda membuat perbaikan diperlukan, buat ulang entri waktu, setujui, dan verifikasi bahwa biaya waktu aktual menunjukkan harga yang valid.</span><span class="sxs-lookup"><span data-stu-id="02564-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="02564-131">Periksa 3: Apakah ada harga dalam daftar harga untuk dimensi harga pada biaya waktu aktual?</span><span class="sxs-lookup"><span data-stu-id="02564-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="02564-132">Jika Anda telah berhasil menyelesaikan Centang 1 dan Centang 2, sekarang Anda seharusnya memiliki hanya satu daftar harga yang dapat diterapkan pada tanggal biaya waktu aktual.</span><span class="sxs-lookup"><span data-stu-id="02564-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="02564-133">Buka daftar harga proyek dan buka tab Harga Peran. Pastikan bahwa terdapat baris di kisi untuk dimensi harga pada biaya waktu aktual.</span><span class="sxs-lookup"><span data-stu-id="02564-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="02564-134">Jika tidak ada baris di kisi harga peran untuk dimensi harga pada waktu biaya aktual, Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="02564-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="02564-135">Buat baris di kisi harga peran untuk dimensi harga pada biaya waktu aktual Anda.</span><span class="sxs-lookup"><span data-stu-id="02564-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="02564-136">Setelah ini dilakukan, buat ulang entri waktu, setujui, dan verifikasi bahwa biaya waktu aktual menunjukkan harga yang valid.</span><span class="sxs-lookup"><span data-stu-id="02564-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="02564-137">Jika Anda tetap tidak melihat harga yang valid pada biaya waktu aktual setelah melakukan pemeriksaan tiga di atas, buat log tiket dukungan.</span><span class="sxs-lookup"><span data-stu-id="02564-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]