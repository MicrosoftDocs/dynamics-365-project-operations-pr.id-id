---
title: Pembayaran harian
description: Topik ini menyediakan informasi tentang aturan uang saku yang digunakan dalam manajemen pengeluaran.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078358"
---
# <a name="per-diems"></a><span data-ttu-id="581d8-103">Pembayaran harian</span><span class="sxs-lookup"><span data-stu-id="581d8-103">Per diems</span></span>

<span data-ttu-id="581d8-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="581d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="581d8-105">Uang saku adalah jatah uang yang dibayarkan kepada pekerja yang melakukan pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="581d8-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="581d8-106">Di manajemen pengeluaran, Anda dapat membuat aturan uang saku untuk berbagai situasi perjalanan.</span><span class="sxs-lookup"><span data-stu-id="581d8-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="581d8-107">Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya.</span><span class="sxs-lookup"><span data-stu-id="581d8-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="581d8-108">Saat membuat aturan uang saku, Anda dapat menentukan bahwa persentase tingkat uang saku diabaikan jika pekerja menerima makanan, atau layanan gratis.</span><span class="sxs-lookup"><span data-stu-id="581d8-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="581d8-109">Anda juga dapat menetapkan jumlah jam minimum dan maksimum yang dapat diterapkan dalam tarif uang saku untuk perjalanan pekerja.</span><span class="sxs-lookup"><span data-stu-id="581d8-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="581d8-110">Konfigurasi</span><span class="sxs-lookup"><span data-stu-id="581d8-110">Configuration</span></span> 

1. <span data-ttu-id="581d8-111">Untuk menambahkan lokasi uang saku, buka **Konfigurasikan** > **penghitungan dan kode** > **lokasi uang saku**.</span><span class="sxs-lookup"><span data-stu-id="581d8-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="581d8-112">Untuk setiap lokasi yang ditambahkan di atas, pilih tingkat uang saku, dan mata uang yang berlaku antara tanggal mulai, dan berakhir tertentu untuk hotel, makan, dan biaya lainnya.</span><span class="sxs-lookup"><span data-stu-id="581d8-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="581d8-113">Tarif uang saku dan mata uang dikonfigurasi dalam **Konfigurasikan** > **penghitungan dan kode** > **uang saku**.</span><span class="sxs-lookup"><span data-stu-id="581d8-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="581d8-114">Di halaman **lokasi uang saku** , konfigurasikan tingkatan tarif uang saku.</span><span class="sxs-lookup"><span data-stu-id="581d8-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="581d8-115">Tingkatan tarif uang saku memungkinkan Anda menentukan persentase pembagian penyisihan harian untuk hotel, makan, dan biaya lainnya.</span><span class="sxs-lookup"><span data-stu-id="581d8-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="581d8-116">Untuk menentukan pengurangan persentase makanan untuk sarapan, Makan Siang, atau makan malam, Perbarui bidang pada halaman **parameter manajemen pengeluaran** pada tab **uang saku**.</span><span class="sxs-lookup"><span data-stu-id="581d8-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="581d8-117">Ajukan pengeluaran menggunakan uang saku</span><span class="sxs-lookup"><span data-stu-id="581d8-117">Submit expenses using per diem</span></span>
<span data-ttu-id="581d8-118">Untuk mengajukan pengeluaran menggunakan uang saku, gunakan kategori pengeluaran **uang saku** saat membuat laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="581d8-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="581d8-119">Masukkan **uang saku dari tanggal** , **uang saku hingga tanggal** , dan **lokasi uang saku**.</span><span class="sxs-lookup"><span data-stu-id="581d8-119">Enter the **Per diem from date** , **Per diem to date** ,  and the **Per diem location**.</span></span> <span data-ttu-id="581d8-120">Jumlah tersebut akan dihitung berdasarkan harga uang saku untuk lokasi yang dipilih dan pengurangan makanan akan dihitung berdasarkan tingkatan tarif uang saku.</span><span class="sxs-lookup"><span data-stu-id="581d8-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
