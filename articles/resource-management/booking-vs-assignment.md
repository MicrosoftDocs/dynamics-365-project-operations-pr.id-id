---
title: Pemesanan vs Penugasan
description: Topik ini memberikan informasi perbedaan antara pemesanan sumber daya dan penugasan sumber daya.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841176"
---
# <a name="bookings-vs-assignments"></a>Pemesanan vs Penugasan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Pemesanan adalah alokasi sumber daya definitif atau tentatif ke proyek. Pemesanan definitif mengkonsumsi kapasitas sumber daya. Pemesanan mewakili konsep organisasi untuk tim sehingga mereka dapat memahami bagaimana sumber daya akan terlibat di berbagai proyek. Dynamics 365 Project Operations mempertimbangkan pemesanan sebagai konsep tingkat proyek. 

Tidak seperti pemesanan, penetapan adalah komitmen sumber daya untuk tugas proyek dalam jadwal proyek. Sumber daya dapat diberi nama atau generik.  Bila kebutuhan sumber daya diambil dari penetapan tugas proyek, Project Operations menggunakan kontur upaya penetapan sumber daya untuk membangun kontur detail kebutuhan sumber daya. Namun, referensi penetapan sumber daya tidak dipertahankan. Pembaruan pemesanan yang diambil dari persyaratan sumber daya tidak memperbarui penetapan sumber daya apa pun.

Biasanya, jumlah pemesanan untuk sumber daya akan sama dengan jumlah penetapan sumber daya di satu atau banyak tugas. Namun, Project Operations tidak menegakkan Perjanjian ini. Tampilan **rekonsiliasi** menunjukkan manajer proyek tempat di mana Pemesanan sumber daya dan penetapan tidak sesuai.




[!INCLUDE[footer-include](../includes/footer-banner.md)]