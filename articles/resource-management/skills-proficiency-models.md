---
title: Keterampilan dan sertifikasi
description: Topik ini memberikan informasi tentang menambahkan karakteristik keterampilan dan sertifikasi ke sumber daya.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4c814754e68b3a1a8bf8784434d45010bf8d0123
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908243"
---
# <a name="skills-and-certifications"></a><span data-ttu-id="dc71f-103">Keterampilan dan sertifikasi</span><span class="sxs-lookup"><span data-stu-id="dc71f-103">Skills and certifications</span></span>
<span data-ttu-id="dc71f-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="dc71f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc71f-105">Karakteristik digunakan untuk memperkaya atribut yang digunakan untuk mendeskripsikan kemampuan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="dc71f-105">Characteristics are used to enrich the attributes used to describe the abilities of a resource.</span></span> <span data-ttu-id="dc71f-106">Setiap karakteristik sumber daya dapat digambarkan sebagai **keterampilan** atau **sertifikasi**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-106">Each characteristic of a resource can be described as a **Skill** or a **Certification**.</span></span>

<span data-ttu-id="dc71f-107">Menambahkan karakteristik pada persyaratan sumber daya memungkinkan Anda mendokumentasikan pengetahuan keterampilan yang diperlukan oleh sumber daya untuk menyelesaikan tugas pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="dc71f-107">Adding characteristics to resource requirements lets you document the knowledge or expertise needed by a resource to complete tasks on a project.</span></span> <span data-ttu-id="dc71f-108">Karakteristik memungkinkan Anda memfilter daftar sumber daya yang tersedia untuk sumber daya yang memiliki karakteristik yang diperlukan saat menjadwalkan persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="dc71f-108">Characteristics let you filter the list of available resources to those resources that have the required characteristics when scheduling the resource requirement.</span></span>

## <a name="add-characteristics"></a><span data-ttu-id="dc71f-109">Tambahkan Karakteristik</span><span class="sxs-lookup"><span data-stu-id="dc71f-109">Add characteristics</span></span>

1. <span data-ttu-id="dc71f-110">Dari menu utama, buka **sumber daya** dan di Bagian **sumber daya**, pilih **keterampilan**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-110">From the main menu, open **Resources** and in the **Resources** section, select **Skills**.</span></span>
2. <span data-ttu-id="dc71f-111">Pilih **baru** untuk menambahkan karakteristik.</span><span class="sxs-lookup"><span data-stu-id="dc71f-111">Select **New** to add characteristics.</span></span>
3. <span data-ttu-id="dc71f-112">Isi bidang wajib, lalu pilih **Jenis karakteristik**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-112">Fill in the required fields and select the **Characteristic Type**.</span></span>

## <a name="assign-characteristics-to-resources"></a><span data-ttu-id="dc71f-113">Menetapkan karakteristik ke sumber daya</span><span class="sxs-lookup"><span data-stu-id="dc71f-113">Assign characteristics to resources</span></span>

1. <span data-ttu-id="dc71f-114">Dari menu utama, pilih **Sumber daya** > **Sumber daya yang dapat dipesan**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-114">From the main menu, select **Resources** > **Bookable Resources**.</span></span> <span data-ttu-id="dc71f-115">Halaman **sumber daya aktif yang dapat dipesan** akan terbuka dan Anda dapat melihat daftar semua sumber daya yang tersedia dalam sistem.</span><span class="sxs-lookup"><span data-stu-id="dc71f-115">The **Active Bookable Resources** page opens and you can view a list of all available resources in the system.</span></span>
2. <span data-ttu-id="dc71f-116">Dari daftar, pilih nama sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="dc71f-116">From the list, select the name of a bookable resource.</span></span>
3. <span data-ttu-id="dc71f-117">Di bagian **Project Service**, pilih **+ Tambahkan rekaman karakteristik sumber daya yang dapat dipesan**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-117">In the **Project Service** section, select **+Add Bookable Resource Characteristics record**.</span></span>
4. <span data-ttu-id="dc71f-118">Di jendela pop-up yang terbuka, temukan dan pilih karakteristik yang diperlukan dan menambahkan **nilai Rating** untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="dc71f-118">In the pop-up window that opens, find and select the required characteristics, and add a **Rating Value** for the resource.</span></span>
5. <span data-ttu-id="dc71f-119">Pilih **Simpan & Tutup**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-119">Select **Save & Close**.</span></span>

## <a name="assign-characteristics-to-resource-requirements"></a><span data-ttu-id="dc71f-120">Menetapkan karakteristik ke persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="dc71f-120">Assign characteristics to resource requirements</span></span>

1. <span data-ttu-id="dc71f-121">Di kisi anggota tim, Cari dan klik dua kali anggota tim generik dengan karakteristik yang perlu diperbarui.</span><span class="sxs-lookup"><span data-stu-id="dc71f-121">In the team member grid, find and double-click the generic team member with the characteristics that need to be updated.</span></span>
2. <span data-ttu-id="dc71f-122">Di detail **anggota tim proyek**, pilih tab **persyaratan sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-122">In the **Project Team member Detail**, select the **Resource Requirement** tab.</span></span>
3. <span data-ttu-id="dc71f-123">Di subkisi **keterampilan**, pilih **+ Tambah karakteristik persyaratan baru.**</span><span class="sxs-lookup"><span data-stu-id="dc71f-123">In the **Skills** subgrid, select **+Add new Requirement Characteristic.**</span></span>
4. <span data-ttu-id="dc71f-124">Di panel buat cepat, Cari dan pilih karakteristik yang diperlukan dan tambahkan **nilai rating**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-124">In the quick create pane, find and select the required characteristics and add a **Rating Value**.</span></span>
5. <span data-ttu-id="dc71f-125">Pilih **Simpan & Tutup**.</span><span class="sxs-lookup"><span data-stu-id="dc71f-125">Select **Save & Close**.</span></span>