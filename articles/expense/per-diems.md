---
title: Pembayaran harian
description: Topik ini menyediakan informasi tentang aturan uang saku yang digunakan dalam manajemen pengeluaran.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276307"
---
# <a name="per-diems"></a><span data-ttu-id="af3c4-103">Pembayaran harian</span><span class="sxs-lookup"><span data-stu-id="af3c4-103">Per diems</span></span>

<span data-ttu-id="af3c4-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="af3c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="af3c4-105">Uang saku adalah jatah uang yang dibayarkan kepada pekerja yang melakukan pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="af3c4-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="af3c4-106">Di manajemen pengeluaran, Anda dapat membuat aturan uang saku untuk berbagai situasi perjalanan.</span><span class="sxs-lookup"><span data-stu-id="af3c4-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="af3c4-107">Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya.</span><span class="sxs-lookup"><span data-stu-id="af3c4-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="af3c4-108">Saat membuat aturan uang saku, Anda dapat menentukan bahwa persentase tingkat uang saku diabaikan jika pekerja menerima makanan, atau layanan gratis.</span><span class="sxs-lookup"><span data-stu-id="af3c4-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="af3c4-109">Anda juga dapat menetapkan jumlah jam minimum dan maksimum yang dapat diterapkan dalam tarif uang saku untuk perjalanan pekerja.</span><span class="sxs-lookup"><span data-stu-id="af3c4-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="af3c4-110">Konfigurasi</span><span class="sxs-lookup"><span data-stu-id="af3c4-110">Configuration</span></span> 

1. <span data-ttu-id="af3c4-111">Untuk menambahkan lokasi uang saku, buka **Konfigurasikan** > **penghitungan dan kode** > **lokasi uang saku**.</span><span class="sxs-lookup"><span data-stu-id="af3c4-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="af3c4-112">Untuk setiap lokasi yang ditambahkan di atas, pilih tingkat uang saku, dan mata uang yang berlaku antara tanggal mulai, dan berakhir tertentu untuk hotel, makan, dan biaya lainnya.</span><span class="sxs-lookup"><span data-stu-id="af3c4-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="af3c4-113">Tarif uang saku dan mata uang dikonfigurasi dalam **Konfigurasikan** > **penghitungan dan kode** > **uang saku**.</span><span class="sxs-lookup"><span data-stu-id="af3c4-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="af3c4-114">Di halaman **lokasi uang saku**, konfigurasikan tingkatan tarif uang saku.</span><span class="sxs-lookup"><span data-stu-id="af3c4-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="af3c4-115">Tingkatan tarif uang saku memungkinkan Anda menentukan persentase pembagian penyisihan harian untuk hotel, makan, dan biaya lainnya.</span><span class="sxs-lookup"><span data-stu-id="af3c4-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="af3c4-116">Untuk menentukan pengurangan persentase makanan untuk sarapan, Makan Siang, atau makan malam, Perbarui bidang pada halaman **parameter manajemen pengeluaran** pada tab **uang saku**.</span><span class="sxs-lookup"><span data-stu-id="af3c4-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="af3c4-117">Ajukan pengeluaran menggunakan uang saku</span><span class="sxs-lookup"><span data-stu-id="af3c4-117">Submit expenses using per diem</span></span>
<span data-ttu-id="af3c4-118">Untuk mengajukan pengeluaran menggunakan uang saku, gunakan kategori pengeluaran **uang saku** saat membuat laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="af3c4-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="af3c4-119">Masukkan **uang saku dari tanggal**, **uang saku hingga tanggal**, dan **lokasi uang saku**.</span><span class="sxs-lookup"><span data-stu-id="af3c4-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="af3c4-120">Jumlah tersebut akan dihitung berdasarkan harga uang saku untuk lokasi yang dipilih dan pengurangan makanan akan dihitung berdasarkan tingkatan tarif uang saku.</span><span class="sxs-lookup"><span data-stu-id="af3c4-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]