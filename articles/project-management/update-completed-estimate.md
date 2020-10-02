---
title: Memperbarui perkiraan saat penyelesaian
description: Topik ini menyediakan informasi tentang memperbarui proyeksi upaya pada proyek.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897770"
---
# <a name="update-estimate-at-completion"></a>Memperbarui perkiraan saat penyelesaian

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

biasanya manajer proyek merevisi perkiraan asli pada tugas. Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini. Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.

Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:

- Menimpa estimasi untuk menyelesaikan (ETC) default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas. 
- Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.

Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, estimasi untuk menyelesaikan (EAC) tugas, dan persentase progres, serta proyeksi varians upaya pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.
