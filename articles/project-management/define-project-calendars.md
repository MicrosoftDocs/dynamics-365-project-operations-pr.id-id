---
title: Menentukan kalender proyek
description: Topik ini menyediakan informasi tentang penggunaan kalender proyek untuk melacak jadwal proyek.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897995"
---
# <a name="define-project-calendars"></a><span data-ttu-id="57bd1-103">Menentukan kalender proyek</span><span class="sxs-lookup"><span data-stu-id="57bd1-103">Define project calendars</span></span>

<span data-ttu-id="57bd1-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="57bd1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="57bd1-105">Untuk membuat jadwal proyek, Anda membuat template kalender proyek yang mendefinisikan jumlah jam kerja setiap hari dan penutupan bisnis apapun.</span><span class="sxs-lookup"><span data-stu-id="57bd1-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="57bd1-106">Untuk membuat template kalender proyek, Anda mengaitkan template kerja dengan bidang **template kalender** untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="57bd1-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="57bd1-107">Ikuti langkah berikut untuk membuat template kerja.</span><span class="sxs-lookup"><span data-stu-id="57bd1-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="57bd1-108">Pilih **Sumber daya** di panel navigasi kiri.</span><span class="sxs-lookup"><span data-stu-id="57bd1-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="57bd1-109">Di halaman daftar **sumber daya**, buka rekaman pengguna, lalu pilih **Tampilkan Jam Kerja**.</span><span class="sxs-lookup"><span data-stu-id="57bd1-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="57bd1-110">Pastikan Anda mengizinkan pop-up di halaman browser.</span><span class="sxs-lookup"><span data-stu-id="57bd1-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="57bd1-111">Dengan demikian, Anda dapat melihat jam kerja yang ditetapkan untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="57bd1-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="57bd1-112">Pada tab **tampilan bulanan**, pilih **Atur**.</span><span class="sxs-lookup"><span data-stu-id="57bd1-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="57bd1-113">Daftar tiga pilihan muncul:</span><span class="sxs-lookup"><span data-stu-id="57bd1-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="57bd1-114">Jadwal Mingguan Baru</span><span class="sxs-lookup"><span data-stu-id="57bd1-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="57bd1-115">Jadwal Kerja untuk Satu Hari</span><span class="sxs-lookup"><span data-stu-id="57bd1-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="57bd1-116">Waktu Nonaktif</span><span class="sxs-lookup"><span data-stu-id="57bd1-116">Time Off</span></span>

4. <span data-ttu-id="57bd1-117">Pilih **jadwal mingguan baru**, lalu Atur pilihan untuk jadwal sumber daya ini.</span><span class="sxs-lookup"><span data-stu-id="57bd1-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="57bd1-118">Anda dapat mengatur jadwal mingguan yang berulang, parameter jam harian, penutupan bisnis, dan banyak lagi.</span><span class="sxs-lookup"><span data-stu-id="57bd1-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="57bd1-119">Atur rentang tanggal, pilih **Simpan**, lalu pilih **tutup**.</span><span class="sxs-lookup"><span data-stu-id="57bd1-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="57bd1-120">Kembali ke halaman daftar **sumber daya**, dan pilih sumber daya yang Anda tetapkan jam kerja.</span><span class="sxs-lookup"><span data-stu-id="57bd1-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="57bd1-121">Pilih **Atur kalender sebagai** untuk mengatur template kerja.</span><span class="sxs-lookup"><span data-stu-id="57bd1-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="57bd1-122">Di kotak dialog **template kerja**, masukkan nama untuk template kerja, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="57bd1-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="57bd1-123">Sekarang Anda dapat mengaitkan template kerja dengan template kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="57bd1-123">You can now associate the work template with a project calendar template.</span></span>
