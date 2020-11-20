---
title: Mengapa saya tidak dapat menghapus rekaman dari entitas Aktual?
description: Topik ini menyediakan informasi tentang alasan anda tidak dapat menghapus rekaman dari entitas aktual.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127162"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="26aa2-103">Mengapa saya tidak dapat menghapus rekaman dari entitas Aktual?</span><span class="sxs-lookup"><span data-stu-id="26aa2-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="26aa2-104">Project Service Automation (PSA) tidak memungkinkan Anda menghapus aktual karena berfungsi sebagai sumber kebenaran untuk transaksi yang memiliki implikasi keuangan terhadap sistem hilir, seperti buku besar.</span><span class="sxs-lookup"><span data-stu-id="26aa2-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="26aa2-105">Jika aktual dapat dihapus, integritas transaksi pelaporan keuangan dapat dipertanyakan.</span><span class="sxs-lookup"><span data-stu-id="26aa2-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="26aa2-106">Untuk membuat jejak audit, pelanggan harus menggunakan jurnal untuk membuat transaksi kompensasi.</span><span class="sxs-lookup"><span data-stu-id="26aa2-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

