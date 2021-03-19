---
title: Proyek estimasi pendapatan harga tetap
description: Topik ini berisi informasi tentang pendapatan harga tetap dalam berbagai proyek.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278917"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="7bd7d-103">Proyek estimasi pendapatan harga tetap</span><span class="sxs-lookup"><span data-stu-id="7bd7d-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="7bd7d-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="7bd7d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7bd7d-105">Saat Anda membuat baris kontrak proyek dengan atribut berikut pada Dynamics 365 Project Operations di Microsoft Dataverse, sistem akan otomatis membuat proyek estimasi pendapatan harga tetap.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="7bd7d-106">Informasi dalam proyek ini berdasarkan pada item berikut:</span><span class="sxs-lookup"><span data-stu-id="7bd7d-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="7bd7d-107">Metode penagihan harga tetap.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="7bd7d-108">Proyek yang terkait.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-108">An associated project.</span></span>
  - <span data-ttu-id="7bd7d-109">Setidaknya satu tonggak pencapaian yang ditentukan di tab **Jadwal Faktur** pada halaman **Baris kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="7bd7d-110">Meninjau proyek estimasi pendapatan harga tetap</span><span class="sxs-lookup"><span data-stu-id="7bd7d-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="7bd7d-111">Untuk meninjau proyek estimasi pendapatan harga tetap, lakukan langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="7bd7d-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="7bd7d-112">Di lingkungan Dynamics 365 Finance, buka **Manajemen dan akuntansi proyek** > **Proyek** > **Proyek estimasi pendapatan harga tetap**.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="7bd7d-113">Pilih proyek yang ingin Anda lihat dan klik dua kali **ID proyek estimasi** untuk membuka record dan meninjau rincian proyek.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="7bd7d-114">Buka tab **Proyek**. Anda akan melihat satu proyek di kisi **Proyek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="7bd7d-115">Sistem menggunakan ini sebagai proyek default karena merupakan proyek yang terkait dengan baris kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="7bd7d-116">Untuk mengubah keterkaitan, pilih proyek tambahan dan tambahkan ke kisi **Proyek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="7bd7d-117">Jika beberapa proyek dipilih dalam kisi ini, persentase penyelesaian dan pendapatan proyek dihitung bersama untuk semua proyek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="7bd7d-118">Biaya proyek, profil pendapatan, template biaya, dan kode periode dapat diatur secara manual.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="7bd7d-119">Jika tidak diatur secara manual, nilai default selama perhitungan estimasi pertama untuk proyek menggunakan aturan yang dikonfigurasi untuk profil pendapatan dan biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="7bd7d-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]