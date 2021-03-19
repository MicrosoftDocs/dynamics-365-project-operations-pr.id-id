---
title: Lacak status proyek
description: Cara melacak status proyek di Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281932"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="2f49d-103">Melacak status proyek (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2f49d-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2f49d-104">Gunakan [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] untuk melacak kemajuan proyek klien.</span><span class="sxs-lookup"><span data-stu-id="2f49d-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="2f49d-105">Seiring perkembangan keterlibatan, tahap proyek diperbarui untuk mencerminkan tahap keterlibatan:</span><span class="sxs-lookup"><span data-stu-id="2f49d-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="2f49d-106">**Baru**</span><span class="sxs-lookup"><span data-stu-id="2f49d-106">**New**</span></span>    | <span data-ttu-id="2f49d-107">Bila Anda membuat sebuah proyek, tahapan diatur ke **Baru**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="2f49d-108">Jika Anda membuat proyek dari template, pada tahap ini proyek mungkin memiliki jadwal, perkiraan dan data tim.</span><span class="sxs-lookup"><span data-stu-id="2f49d-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="2f49d-109">Jika tidak, itu akan menjadi garis besar proyek dan Anda harus secara manual memasukkan seluruh komponen proyek.</span><span class="sxs-lookup"><span data-stu-id="2f49d-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="2f49d-110">**Kuotasi**</span><span class="sxs-lookup"><span data-stu-id="2f49d-110">**Quote**</span></span>   |      <span data-ttu-id="2f49d-111">Ketika Anda menghubungkan sebuah proyek dengan kuotasi atau membuatnya dari kuotasi, tahapan proyek diatur ke **kuotasi**, dan perkiraan awal dan akhir tanggal juga diperbarui.</span><span class="sxs-lookup"><span data-stu-id="2f49d-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="2f49d-112">Ketika proyek pada tahapan kuotasi, rincian pada kuotasi ditampilkan pada tab **Sales** pada halaman **proyek**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="2f49d-113">**Rencana**</span><span class="sxs-lookup"><span data-stu-id="2f49d-113">**Plan**</span></span>   |                                     <span data-ttu-id="2f49d-114">Ketika Anda memenangkan kuotasi yang berkaitan dengan proyek, dan ketika keterlibatan berkembang ke tahapan kontrak, tahapan proyek diperbarui ke **rencana**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="2f49d-115">Rincian kontrak ditampilkan pada tab **Sales** pada halaman **proyek**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="2f49d-116">**Selesai**</span><span class="sxs-lookup"><span data-stu-id="2f49d-116">**Complete**</span></span> |                    <span data-ttu-id="2f49d-117">Ketika pekerjaan proyek selesai, Anda dapat mengubah tahapan ke **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="2f49d-118">Ketika tahapan proyek diatur ke selesai, dapat dipahami bahwa pekerjaan 100% selesai tetapi proyek dibiarkan terbuka untuk waktu yang tertunda atau entri pengeluaran direkam.</span><span class="sxs-lookup"><span data-stu-id="2f49d-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="2f49d-119">**Tutup**</span><span class="sxs-lookup"><span data-stu-id="2f49d-119">**Close**</span></span>   |           <span data-ttu-id="2f49d-120">Ketika semua transaksi telah tercatat pada proyek dan Anda tidak berharap lagi untuk login, Anda dapat secara manual mengatur tahapan ke **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="2f49d-121">Ketika proyek diatur ke **Tutup**, Anda tidak dapat mencatat lebih banyak transaksi pada proyek dan proyek akan menjadi hanya baca.</span><span class="sxs-lookup"><span data-stu-id="2f49d-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="2f49d-122">Untuk melacak status proyek</span><span class="sxs-lookup"><span data-stu-id="2f49d-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="2f49d-123">Pergi ke **Project Service > Proyek**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="2f49d-124">Klik proyek yang ingin Anda kerjakan.</span><span class="sxs-lookup"><span data-stu-id="2f49d-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="2f49d-125">Di bar di bagian atas layar, pilih panah bawah di sebelah nama proyek, dan kemudian klik **Pelacakan Proyek**.</span><span class="sxs-lookup"><span data-stu-id="2f49d-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="2f49d-126">Pilih **pelacakan usaha** atau **pelacakan biaya** dalam daftar drop-down di atas daftar tugas.</span><span class="sxs-lookup"><span data-stu-id="2f49d-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="2f49d-127">Klik dua kali setiap tugas untuk mengeditnya.</span><span class="sxs-lookup"><span data-stu-id="2f49d-127">Double-click any task to edit it.</span></span> <span data-ttu-id="2f49d-128">Anda juga dapat memindahkan atau mengubah ukuran Bar di Gantt chart untuk mengubah waktu dan kemajuan untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="2f49d-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="2f49d-129">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="2f49d-129">See Also</span></span>  
 [<span data-ttu-id="2f49d-130">Panduan Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="2f49d-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]