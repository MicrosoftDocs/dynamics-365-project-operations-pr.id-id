---
title: Menentukan kalender sumber daya
description: Topik ini menyediakan informasi tentang cara menentukan kalender jam kerja untuk sumber daya dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078332"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="5c408-103">Menentukan kalender sumber daya</span><span class="sxs-lookup"><span data-stu-id="5c408-103">Define resource calendars</span></span>

<span data-ttu-id="5c408-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="5c408-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c408-105">Setiap sumber daya dapat dipesan yang mengerjakan proyek harus memiliki kalender jam kerja untuk menentukan ketersediaan mereka.</span><span class="sxs-lookup"><span data-stu-id="5c408-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="5c408-106">Jam kerja untuk sumber daya dapat didefinisikan dengan dua cara:</span><span class="sxs-lookup"><span data-stu-id="5c408-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="5c408-107">Menentukan aturan kalender individual untuk sumber daya</span><span class="sxs-lookup"><span data-stu-id="5c408-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="5c408-108">Menerapkan template kalender yang ada untuk sumber daya</span><span class="sxs-lookup"><span data-stu-id="5c408-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="5c408-109">Menentukan jam kerja sumber daya</span><span class="sxs-lookup"><span data-stu-id="5c408-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="5c408-110">Pada menu **sumber daya** , pilih **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="5c408-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5c408-111">Dari tampilan kisi, pilih **sumber daya dapat dipesan** yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="5c408-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="5c408-112">Pada halaman **rincian sumber daya** , pilih tab **jam kerja**. Secara default, kalender sumber daya yang dapat dipesan akan default ke jam kerja template jam kerja default yang ditentukan untuk organisasi.</span><span class="sxs-lookup"><span data-stu-id="5c408-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="5c408-113">Untuk memperbarui jam kerja, klik kanan pada tanggal mulai aturan kalender yang diusulkan yang akan ditentukan.</span><span class="sxs-lookup"><span data-stu-id="5c408-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="5c408-114">Gunakan menu aturan kalender untuk menentukan aturan kalender untuk hari tertentu, sisa rangkaian, atau seluruh kalender.</span><span class="sxs-lookup"><span data-stu-id="5c408-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="5c408-115">Setelah pilihan dipilih, Anda kemudian dapat menentukan:</span><span class="sxs-lookup"><span data-stu-id="5c408-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="5c408-116">Hari kerja dalam sepekan di mana jam kerja akan berlaku.</span><span class="sxs-lookup"><span data-stu-id="5c408-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="5c408-117">Waktu kerja dalam setiap hari.</span><span class="sxs-lookup"><span data-stu-id="5c408-117">The working times within each day.</span></span>
    - <span data-ttu-id="5c408-118">Zona waktu lokal untuk aturan kalender.</span><span class="sxs-lookup"><span data-stu-id="5c408-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="5c408-119">Jika berlaku, waktu non-kerja juga dapat ditentukan untuk aturan.</span><span class="sxs-lookup"><span data-stu-id="5c408-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="5c408-120">Menerapkan template kalender ke sumber daya</span><span class="sxs-lookup"><span data-stu-id="5c408-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="5c408-121">Pada menu **sumber daya** , pilih **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="5c408-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="5c408-122">Dari tampilan kisi, pilih hingga 25 **sumber daya dapat dipesan** untuk diperbarui.</span><span class="sxs-lookup"><span data-stu-id="5c408-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="5c408-123">Pilih **Atur kalender** dan dialog akan meminta Anda daftar template jam kerja yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="5c408-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="5c408-124">Pilih template yang ingin Anda gunakan, kemudian pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="5c408-124">Select the template you want to use, and then select **Apply**.</span></span>
