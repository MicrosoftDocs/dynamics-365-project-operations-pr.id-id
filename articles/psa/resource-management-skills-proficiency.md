---
title: Model keahlian dan kecakapan
description: Topik ini menyediakan informasi tentang cara menggunakan keahlian dan model kecakapan.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008675"
---
# <a name="skills-and-proficiency-models"></a>Model keahlian dan kecakapan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Keahlian adalah karakteristik sumber daya yang digunakan bersama antara Dynamics 365 Project Service Automation dan jika ada, Dynamics 365 Field Service. 

Untuk mengelola repositori keahlian dalam Project Service Automation, buka **sumber daya** \> **Keahlian sumber daya**. 

> ![Keterampilan Sumber Daya](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Gunakan model kecakapan untuk menilai sumber daya

Keahlian untuk sumber daya dinilai berdasarkan model kecakapan. Peringkat individual berada dalam model kemahiran. 

1. Untuk membuat model kecakapan, buka **sumber daya** \> **model kecakapan**, lalu pilih **baru**.
2. Di model peringkat baru, tentukan nilai peringkat minimum, nilai peringkat maksimum, dan entitas yang dinilai.
3. Di subkisi **nilai peringkat**, Anda dapat menentukan nilai peringkat yang berbeda, dari minimum hingga maksimum.

> ![Peringkat minimum dan maksimum ditentukan](media/Resource-Management-image85.png)

Nilai peringkat ini ditampilkan pada **persyaratan sumber daya**, **papan jadwal**, dan filter **asisten jadwal**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]