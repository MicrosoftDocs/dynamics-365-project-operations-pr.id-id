---
title: Menentukan keterampilan dan kecakapan
description: Topik ini menyediakan informasi tentang cara mengonfigurasikan model kecakapan untuk menilai sumber daya.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078428"
---
# <a name="define-skills-and-proficiencies"></a>Menentukan keterampilan dan kecakapan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Keahlian adalah karakteristik sumber daya yang digunakan bersama antara Dynamics 365 Project Operations dan jika ada, Dynamics 365 Field Service. 

- Untuk mengelola repositori keahlian dalam Project Operations, buka **sumber daya** \> **Keahlian sumber daya**. 

## <a name="use-proficiency-models-to-rate-resources"></a>Gunakan model kecakapan untuk menilai sumber daya

Keahlian untuk sumber daya dinilai berdasarkan model kecakapan. Peringkat individual berada dalam model kemahiran. 

1. Untuk membuat model kecakapan, buka **sumber daya** \> **model kecakapan** , lalu pilih **baru**.
2. Di model peringkat baru, tentukan nilai peringkat minimum, nilai peringkat maksimum, dan entitas yang dinilai.
3. Di subkisi **nilai peringkat** , Anda dapat menentukan nilai peringkat yang berbeda, dari minimum hingga maksimum.


Nilai peringkat ini ditampilkan pada **persyaratan sumber daya** , **papan jadwal** , dan filter **asisten jadwal**.
