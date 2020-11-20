---
title: Menutup kuotasi - lite
description: Topik ini memberikan informasi tentang menutup kuotasi proyek di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175715"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="451a2-103">Menutup kuotasi - lite</span><span class="sxs-lookup"><span data-stu-id="451a2-103">Close a quote - lite</span></span>

<span data-ttu-id="451a2-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="451a2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="451a2-105">Kuotasi proyek dapat ditutup sebagai menang atau kalah.</span><span class="sxs-lookup"><span data-stu-id="451a2-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="451a2-106">Operasi mengaktifkan dan merevisi pada kuotasi tidak didukung dalam Microsoft Dynamics 365 Project Operations, sehingga Anda dapat menutup draf kuotasi.</span><span class="sxs-lookup"><span data-stu-id="451a2-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="451a2-107">Menutup kuotasi sebagai Menang</span><span class="sxs-lookup"><span data-stu-id="451a2-107">Close a quote as Won</span></span>

<span data-ttu-id="451a2-108">Penutupan kuotasi proyek sebagai menang akan menutup kuotasi dengan status diatur ke ditutup dan alasan status ke menang.</span><span class="sxs-lookup"><span data-stu-id="451a2-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="451a2-109">Menutup kuotasi membuat kuotasi proyek hanya bisa dibaca dan membuat kontrak proyek draf yang berisi informasi kuotasi.</span><span class="sxs-lookup"><span data-stu-id="451a2-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="451a2-110">Karena kuotasi yang ditutup tidak dapat dibuka kembali, ada dialog konfirmasi sebelum perubahan dilakukan karena kuotasi yang ditutup tidak dapat dibuka kembali dan perubahannya tidak dapat diubah.</span><span class="sxs-lookup"><span data-stu-id="451a2-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="451a2-111">Jika kuotasi dilampirkan pada peluang, setiap proyek lain pada peluang ditutup secara otomatis sebagai Kalah.</span><span class="sxs-lookup"><span data-stu-id="451a2-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="451a2-112">Dampak keuangan menutup kuotasi sebagai menang</span><span class="sxs-lookup"><span data-stu-id="451a2-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="451a2-113">Jika ada aktual apa pun untuk waktu yang direkam pada proyek saat masih dilampirkan pada kuotasi draf, hanya biaya waktu atau pengeluaran yang tercatat.</span><span class="sxs-lookup"><span data-stu-id="451a2-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="451a2-114">Setelah kuotasi ditutup sebagai menang, aplikasi akan merefaktorisasi biaya dengan membalik aktual biaya yang lebih lama dan membuat ulang aktual biaya baru.</span><span class="sxs-lookup"><span data-stu-id="451a2-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="451a2-115">Aplikasi akan memproses aktual biaya ini berdasarkan metode penagihan pada baris kontrak proyek terkait.</span><span class="sxs-lookup"><span data-stu-id="451a2-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="451a2-116">Jika aktual biaya merujuk pada baris waktu dan kontrak material, sistem akan secara otomatis membuat aktual penjualan tidak tertagih yang sesuai saat kuotasi ditutup dan kontrak proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="451a2-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="451a2-117">Jika aktual biaya merujuk baris kontrak harga tetap, aplikasi akan menghentikan pemrosesan ulang aktual biaya berdasarkan aturan penagihan terpisah untuk pelanggan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="451a2-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="451a2-118">Menutup kuotasi sebagai kalah:</span><span class="sxs-lookup"><span data-stu-id="451a2-118">Closing a quote as lost:</span></span>

<span data-ttu-id="451a2-119">Penutupan kuotasi proyek sebagai kalah akan menentukan status ke ditutup dan alasan status ke kalah.</span><span class="sxs-lookup"><span data-stu-id="451a2-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="451a2-120">Penutupan kuotasi membuat kuotasi proyek hanya bisa dibaca.</span><span class="sxs-lookup"><span data-stu-id="451a2-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="451a2-121">Karena kuotasi yang ditutup tidak dapat dibuka kembali, dan sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.</span><span class="sxs-lookup"><span data-stu-id="451a2-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="451a2-122">Jika kuotasi proyek yang ditutup sebagai hilang kalah memiliki proyek yang dirujuk pada salah satu baris, proyek tersebut juga ditandai sebagai Ditutup dan setiap Pemesanan sumber daya dari hari itu ke depan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="451a2-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="451a2-123">Dalam Project Operations, penutupan kuotasi karena menang atau kalah tidak akan memengaruhi status peluang, yang akan tetap terbuka hingga ditutup secara manual.</span><span class="sxs-lookup"><span data-stu-id="451a2-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
