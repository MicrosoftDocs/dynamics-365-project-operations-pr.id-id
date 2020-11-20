---
title: Tutup kuotasi
description: Topik ini memberikan informasi tentang menutup kuotasi proyek di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124687"
---
# <a name="close-a-quote"></a><span data-ttu-id="d2075-103">Tutup kuotasi</span><span class="sxs-lookup"><span data-stu-id="d2075-103">Close a quote</span></span>

<span data-ttu-id="d2075-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="d2075-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d2075-105">Kuotasi proyek dapat ditutup sebagai menang atau kalah.</span><span class="sxs-lookup"><span data-stu-id="d2075-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="d2075-106">Karena fungsi mengaktifkan dan merevisi tidak didukung pada kuotasi dalam Microsoft Dynamics 365 Project Operations, Anda dapat menutup draf kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d2075-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="d2075-107">Menutup kuotasi sebagai Menang</span><span class="sxs-lookup"><span data-stu-id="d2075-107">Close a quote as Won</span></span>

<span data-ttu-id="d2075-108">Penutupan kuotasi proyek sebagai menang akan menentukan status kuotasi ke **ditutup** dan alasan status ke **menang**.</span><span class="sxs-lookup"><span data-stu-id="d2075-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="d2075-109">Menutup kuotasi membuatnya hanya baca dan membuat kontrak proyek draf dengan semua informasi kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d2075-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="d2075-110">Karena kuotasi yang ditutup tidak dapat dibuka kembali, sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.</span><span class="sxs-lookup"><span data-stu-id="d2075-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="d2075-111">Kontrak proyek yang dibuat dari kuotasi proyek juga dibuat tersedia di modul manajemen proyek dan Akuntansi dari Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d2075-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="d2075-112">Jika kontrak proyek tidak dipetakan ke proyek pada salah satu baris, kontrak proyek ini dibuat tersedia sebagai kontrak proyek tidak aktif dan menjadi aktif segera setelah proyek dipetakan ke setidaknya satu baris kontraknya.</span><span class="sxs-lookup"><span data-stu-id="d2075-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="d2075-113">Jika kuotasi dilampirkan pada peluang, setiap proyek lain pada peluang ditutup secara otomatis sebagai Kalah.</span><span class="sxs-lookup"><span data-stu-id="d2075-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="d2075-114">Dampak keuangan menutup kuotasi sebagai menang</span><span class="sxs-lookup"><span data-stu-id="d2075-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="d2075-115">Jika ada aktual apa pun untuk waktu yang direkam pada proyek saat masih dilampirkan pada kuotasi draf, hanya biaya waktu atau pengeluaran yang tercatat.</span><span class="sxs-lookup"><span data-stu-id="d2075-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="d2075-116">Setelah kuotasi ditutup sebagai menang, aplikasi akan merefaktorisasi biaya dengan membalik aktual biaya yang lebih lama dan membuat ulang aktual biaya baru.</span><span class="sxs-lookup"><span data-stu-id="d2075-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="d2075-117">Aplikasi akan memproses aktual biaya ini berdasarkan metode penagihan pada baris kontrak proyek terkait.</span><span class="sxs-lookup"><span data-stu-id="d2075-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="d2075-118">Jika aktual biaya merujuk pada baris waktu dan kontrak material, sistem akan secara otomatis membuat aktual penjualan tidak tertagih yang sesuai saat kuotasi ditutup dan kontrak proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="d2075-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="d2075-119">Jika aktual biaya merujuk baris kontrak harga tetap, aplikasi akan menghentikan pemrosesan ulang aktual biaya berdasarkan aturan penagihan terpisah untuk pelanggan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="d2075-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="d2075-120">Semua aktual yang diproses ulang tersedia dalam modul manajemen proyek dan akuntansi agar akuntan proyek dapat meninjau, memperbarui, dan mengeposkan ke buku besar.</span><span class="sxs-lookup"><span data-stu-id="d2075-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="d2075-121">Menutup kuotasi sebagai kalah</span><span class="sxs-lookup"><span data-stu-id="d2075-121">Close a quote as Lost</span></span>

<span data-ttu-id="d2075-122">Penutupan kuotasi proyek sebagai kalah akan menentukan status ke **ditutup** dan alasan status ke **kalah**.</span><span class="sxs-lookup"><span data-stu-id="d2075-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="d2075-123">Menutup kuotasi membuatnya hanya baca.</span><span class="sxs-lookup"><span data-stu-id="d2075-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="d2075-124">Karena kuotasi yang ditutup tidak dapat dibuka kembali, dan sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.</span><span class="sxs-lookup"><span data-stu-id="d2075-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="d2075-125">Jika kuotasi proyek yang ditutup sebagai hilang kalah memiliki proyek yang dirujuk pada salah satu baris, proyek tersebut juga ditandai sebagai Ditutup dan setiap Pemesanan sumber daya dari hari itu ke depan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="d2075-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="d2075-126">Dalam Project Operations, penutupan kuotasi karena menang atau kalah tidak akan memengaruhi status peluang, yang akan tetap terbuka hingga ditutup secara manual.</span><span class="sxs-lookup"><span data-stu-id="d2075-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
