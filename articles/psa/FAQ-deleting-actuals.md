---
title: Mengapa saya tidak dapat menghapus rekaman dari entitas Aktual?
description: Topik ini menyediakan informasi tentang alasan anda tidak dapat menghapus rekaman dari entitas aktual.
author: JPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ff2c951905324d5d05722f399057c03d22f1a1c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584416"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Mengapa saya tidak dapat menghapus rekaman dari entitas Aktual?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) tidak memungkinkan Anda menghapus aktual karena berfungsi sebagai sumber kebenaran untuk transaksi yang memiliki implikasi keuangan terhadap sistem hilir, seperti buku besar. Jika aktual dapat dihapus, integritas transaksi pelaporan keuangan dapat dipertanyakan. Untuk membuat jejak audit, pelanggan harus menggunakan jurnal untuk membuat transaksi kompensasi.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
