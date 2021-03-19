---
title: Jenis periode
description: Topik ini berisi informasi tentang cara mengonfigurasi jenis periode untuk estimasi pendapatan.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287287"
---
# <a name="period-types"></a><span data-ttu-id="1e804-103">Jenis periode</span><span class="sxs-lookup"><span data-stu-id="1e804-103">Period types</span></span>

<span data-ttu-id="1e804-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="1e804-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1e804-105">Jenis periode menentukan seberapa sering pendapatan pada satu proyek diperkirakan.</span><span class="sxs-lookup"><span data-stu-id="1e804-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="1e804-106">Topik ini berisi informasi tentang cara mengonfigurasi jenis periode untuk estimasi pendapatan.</span><span class="sxs-lookup"><span data-stu-id="1e804-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="1e804-107">Membuat dan menggunakan jenis periode</span><span class="sxs-lookup"><span data-stu-id="1e804-107">Create and work with period types</span></span>
<span data-ttu-id="1e804-108">Untuk membuat dan menggunakan jenis periode, lakukan langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="1e804-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="1e804-109">Di lingkungan Dynamics 365 Finance Anda, buka **Manajemen dan akuntansi proyek** > **Pengaturan** > **Estimasi** > **Jenis periode**.</span><span class="sxs-lookup"><span data-stu-id="1e804-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="1e804-110">Pilih **Baru** untuk membuat jenis perioden baru.</span><span class="sxs-lookup"><span data-stu-id="1e804-110">Select **New** to create new period type.</span></span> <span data-ttu-id="1e804-111">Masukkan nama dan deskripsi.</span><span class="sxs-lookup"><span data-stu-id="1e804-111">Enter a name and description.</span></span>
3. <span data-ttu-id="1e804-112">Di bidang **Frekuensi**, pilih nilai:</span><span class="sxs-lookup"><span data-stu-id="1e804-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="1e804-113">Jika Anda memilih **Minggu**, **Dua mingguan**, **Tengah-bulanan**, **Bulan**, **Hari**, **Kuartal**, atau **Tahun**, kalender akan digunakan untuk membuat periode.</span><span class="sxs-lookup"><span data-stu-id="1e804-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="1e804-114">Jika Anda memilih **Periode buku**, periode buku dari konfigurasi Buku besar akan digunakan untuk membuat periode.</span><span class="sxs-lookup"><span data-stu-id="1e804-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="1e804-115">Jika Anda memilih **Tidak terbatas**, Anda dapat menentukan periode kustom.</span><span class="sxs-lookup"><span data-stu-id="1e804-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="1e804-116">Pilih record jenis periode dan kemudian pilih **Buat periode** untuk membuat periode untuk jenis periode.</span><span class="sxs-lookup"><span data-stu-id="1e804-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="1e804-117">Berdasarkan frekuensi periode yang dipilih, Anda mungkin memiliki opsi untuk menentukan tanggal mulai atau jumlah periode yang akan dibuat.</span><span class="sxs-lookup"><span data-stu-id="1e804-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="1e804-118">Pilih **Periode** untuk meninjau periode yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="1e804-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]