---
title: Mengajukan permintaan sumber daya
description: Topik ini menyediakan informasi tentang pengajuan permintaan sumber daya proyek.
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078577"
---
# <a name="submitting-a-resource-request"></a>Mengajukan permintaan sumber daya

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda dapat mengajukan persyaratan sumber daya yang dihasilkan sebagai permintaan sumber daya. Permintaan tersebut kemudian dikirim ke manajer sumber daya untuk pemenuhan.

1. Di Project Service Automation (PSA), pada halaman **proyek** , klik tab **tim** untuk melihat daftar sumber daya yang dapat dipesan. 
2. Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu klik **Ajukan Permintaan**.

![Mengajukan permintaan sumber daya](media/RM-how-to-18.png)

Status permintaan anggota tim umum akan berubah menjadi **Diajukan**.

Setelah permintaan terpenuhi oleh Manajer sumber daya, sumber daya generik akan digantikan dengan sumber daya bernama jika Manajer sumber daya memenuhi permintaan dengan Pemesanan sumber daya bernama. Jika tidak, sumber daya generik akan tetap berada di tim dan status permintaan akan berubah menjadi **Perlu Ditinjau** , jika Manajer sumber daya telah mengusulkan sumber daya bernama.
