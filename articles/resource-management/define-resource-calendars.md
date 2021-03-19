---
title: Menentukan kalender sumber daya
description: Topik ini menyediakan informasi tentang cara menentukan kalender jam kerja untuk sumber daya dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279817"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="4f9a0-103">Menentukan kalender sumber daya</span><span class="sxs-lookup"><span data-stu-id="4f9a0-103">Define resource calendars</span></span>

<span data-ttu-id="4f9a0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="4f9a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4f9a0-105">Setiap sumber daya dapat dipesan yang mengerjakan proyek harus memiliki kalender jam kerja untuk menentukan ketersediaan mereka.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="4f9a0-106">Jam kerja untuk sumber daya dapat didefinisikan dengan dua cara:</span><span class="sxs-lookup"><span data-stu-id="4f9a0-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="4f9a0-107">Menentukan aturan kalender individual untuk sumber daya</span><span class="sxs-lookup"><span data-stu-id="4f9a0-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="4f9a0-108">Menerapkan template kalender yang ada untuk sumber daya</span><span class="sxs-lookup"><span data-stu-id="4f9a0-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="4f9a0-109">Menentukan jam kerja sumber daya</span><span class="sxs-lookup"><span data-stu-id="4f9a0-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="4f9a0-110">Pada menu **sumber daya**, pilih **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="4f9a0-111">Dari tampilan kisi, pilih **sumber daya dapat dipesan** yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="4f9a0-112">Pada halaman **rincian sumber daya**, pilih tab **jam kerja**. Secara default, kalender sumber daya yang dapat dipesan akan default ke jam kerja template jam kerja default yang ditentukan untuk organisasi.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="4f9a0-113">Untuk memperbarui jam kerja, klik kanan pada tanggal mulai aturan kalender yang diusulkan yang akan ditentukan.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="4f9a0-114">Gunakan menu aturan kalender untuk menentukan aturan kalender untuk hari tertentu, sisa rangkaian, atau seluruh kalender.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="4f9a0-115">Setelah pilihan dipilih, Anda kemudian dapat menentukan:</span><span class="sxs-lookup"><span data-stu-id="4f9a0-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="4f9a0-116">Hari kerja dalam sepekan di mana jam kerja akan berlaku.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="4f9a0-117">Waktu kerja dalam setiap hari.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-117">The working times within each day.</span></span>
    - <span data-ttu-id="4f9a0-118">Zona waktu lokal untuk aturan kalender.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="4f9a0-119">Jika berlaku, waktu non-kerja juga dapat ditentukan untuk aturan.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="4f9a0-120">Menerapkan template kalender ke sumber daya</span><span class="sxs-lookup"><span data-stu-id="4f9a0-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="4f9a0-121">Pada menu **sumber daya**, pilih **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="4f9a0-122">Dari tampilan kisi, pilih hingga 25 **sumber daya dapat dipesan** untuk diperbarui.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="4f9a0-123">Pilih **Atur kalender** dan dialog akan meminta Anda daftar template jam kerja yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="4f9a0-124">Pilih template yang ingin Anda gunakan, kemudian pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="4f9a0-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]