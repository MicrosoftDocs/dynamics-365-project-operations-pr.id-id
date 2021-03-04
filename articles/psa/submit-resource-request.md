---
title: Mengajukan permintaan sumber daya
description: Topik ini menyediakan informasi tentang pengajuan permintaan sumber daya proyek.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149727"
---
# <a name="submitting-a-resource-request"></a>Mengajukan permintaan sumber daya

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda dapat mengajukan persyaratan sumber daya yang dihasilkan sebagai permintaan sumber daya. Permintaan tersebut kemudian dikirim ke manajer sumber daya untuk pemenuhan.

1. Di Project Service Automation (PSA), pada halaman **proyek**, klik tab **tim** untuk melihat daftar sumber daya yang dapat dipesan. 
2. Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu klik **Ajukan Permintaan**.

![Mengajukan permintaan sumber daya](media/RM-how-to-18.png)

Status permintaan anggota tim umum akan berubah menjadi **Diajukan**.

Setelah permintaan terpenuhi oleh Manajer sumber daya, sumber daya generik akan digantikan dengan sumber daya bernama jika Manajer sumber daya memenuhi permintaan dengan Pemesanan sumber daya bernama. Jika tidak, sumber daya generik akan tetap berada di tim dan status permintaan akan berubah menjadi **Perlu Ditinjau**, jika Manajer sumber daya telah mengusulkan sumber daya bernama.
