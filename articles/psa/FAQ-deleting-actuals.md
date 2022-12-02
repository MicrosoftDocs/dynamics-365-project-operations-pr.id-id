---
title: Mengapa saya tidak dapat menghapus rekaman dari entitas Aktual?
description: artikel ini menyediakan informasi tentang alasan anda tidak dapat menghapus rekaman dari entitas aktual.
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
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925584"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Mengapa saya tidak dapat menghapus rekaman dari entitas Aktual?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) tidak memungkinkan Anda menghapus aktual karena berfungsi sebagai sumber kebenaran untuk transaksi yang memiliki implikasi keuangan terhadap sistem hilir, seperti buku besar. Jika aktual dapat dihapus, integritas transaksi pelaporan keuangan dapat dipertanyakan. Untuk membuat jejak audit, pelanggan harus menggunakan jurnal untuk membuat transaksi kompensasi.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
