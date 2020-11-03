---
title: Memperbarui perkiraan saat penyelesaian
description: Topik ini menyediakan informasi tentang memperbarui proyeksi upaya pada proyek.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078667"
---
# <a name="update-estimate-at-completion"></a>Memperbarui perkiraan saat penyelesaian

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

biasanya manajer proyek merevisi perkiraan asli pada tugas. Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini. Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.

Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:

- Menimpa estimasi untuk menyelesaikan (ETC) default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas. 
- Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.

Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, estimasi untuk menyelesaikan (EAC) tugas, dan persentase progres, serta proyeksi varians upaya pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.
