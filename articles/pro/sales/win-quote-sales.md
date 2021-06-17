---
title: Menutup kuotasi - lite
description: Topik ini memberikan informasi tentang menutup kuotasi proyek di Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994140"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="9618a-103">Menutup kuotasi - lite</span><span class="sxs-lookup"><span data-stu-id="9618a-103">Close a quote - lite</span></span>

<span data-ttu-id="9618a-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="9618a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9618a-105">Kuotasi proyek dapat ditutup sebagai menang atau kalah.</span><span class="sxs-lookup"><span data-stu-id="9618a-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="9618a-106">Kuotasi draf dapat ditutup karena operasi Aktifkan dan Revisi pada kuotasi tidak didukung di Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9618a-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="9618a-107">Menutup kuotasi sebagai Menang</span><span class="sxs-lookup"><span data-stu-id="9618a-107">Close a quote as Won</span></span>

<span data-ttu-id="9618a-108">Bila Anda menutup kuotasi proyek sebagai Menang, status diatur ke Ditutup dan alasan status adalah Menang.</span><span class="sxs-lookup"><span data-stu-id="9618a-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="9618a-109">Menutup kuotasi membuat kuotasi proyek hanya bisa dibaca dan membuat kontrak proyek draf yang berisi informasi kuotasi.</span><span class="sxs-lookup"><span data-stu-id="9618a-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="9618a-110">Karena kuotasi tertutup tidak dapat dibuka kembali, dialog konfirmasi akan mengkonfirmasikan perubahan Anda.</span><span class="sxs-lookup"><span data-stu-id="9618a-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="9618a-111">Jika kuotasi dilampirkan pada peluang, setiap proyek lain pada peluang ditutup secara otomatis sebagai Kalah.</span><span class="sxs-lookup"><span data-stu-id="9618a-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="9618a-112">Dampak keuangan menutup kuotasi sebagai menang</span><span class="sxs-lookup"><span data-stu-id="9618a-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="9618a-113">Jika ada aktual selama waktu proyek saat masih terlampir pada draf kuotasi, hanya biaya waktu atau pengeluaran yang dicatat.</span><span class="sxs-lookup"><span data-stu-id="9618a-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="9618a-114">Setelah kuotasi ditutup sebagai menang, aplikasi akan merefaktorisasi biaya dengan membalik aktual biaya yang lebih lama dan membuat ulang aktual biaya baru.</span><span class="sxs-lookup"><span data-stu-id="9618a-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="9618a-115">Aplikasi akan memproses aktual biaya ini berdasarkan metode penagihan pada baris kontrak proyek terkait.</span><span class="sxs-lookup"><span data-stu-id="9618a-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="9618a-116">Jika aktual biaya mengacu ke waktu dan baris kontrak material, aktual penjualan tidak tertagih yang tidak terkait dibuat untuk saat kuotasi ditutup dan kontrak proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="9618a-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="9618a-117">Jika aktual biaya mengacu ke baris kontrak harga tetap, aplikasi akan berhenti memproses ulang aktual biaya yang didasarkan pada aturan penagihan terpisah untuk pelanggan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="9618a-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="9618a-118">Menutup kuotasi sebagai kalah:</span><span class="sxs-lookup"><span data-stu-id="9618a-118">Closing a quote as lost:</span></span>

<span data-ttu-id="9618a-119">Bila Anda menutup kuotasi proyek sebagai Kalah, status diatur ke Ditutup dan alasan status adalah Kalah.</span><span class="sxs-lookup"><span data-stu-id="9618a-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="9618a-120">Penutupan kuotasi membuat kuotasi proyek hanya bisa dibaca.</span><span class="sxs-lookup"><span data-stu-id="9618a-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="9618a-121">Karena kuotasi yang ditutup tidak dapat dibuka kembali, dan sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.</span><span class="sxs-lookup"><span data-stu-id="9618a-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="9618a-122">Jika kuotasi proyek yang ditutup sebagai Kalah mengacu ke proyek pada salah satu barisnya, proyek tersebut juga ditandai sebagai Ditutup.</span><span class="sxs-lookup"><span data-stu-id="9618a-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="9618a-123">Setiap Pemesanan sumber daya dari waktu itu ke depan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="9618a-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="9618a-124">Dalam Project Operations, penutupan kuotasi karena menang atau kalah tidak akan memengaruhi status peluang, yang akan tetap terbuka hingga ditutup secara manual.</span><span class="sxs-lookup"><span data-stu-id="9618a-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]