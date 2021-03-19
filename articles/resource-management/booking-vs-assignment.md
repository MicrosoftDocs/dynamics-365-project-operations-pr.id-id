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
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279907"
---
# <a name="bookings-vs-assignments"></a>Pemesanan vs Penugasan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Pemesanan adalah alokasi sumber daya definitif atau tentatif ke proyek. Pemesanan definitif mengkonsumsi kapasitas sumber daya. Pemesanan mewakili konsep organisasi untuk tim sehingga mereka dapat memahami bagaimana sumber daya akan terlibat di berbagai proyek. Dynamics 365 Project Operations mempertimbangkan pemesanan sebagai konsep tingkat proyek. 

Tidak seperti pemesanan, penetapan adalah komitmen sumber daya untuk tugas proyek dalam jadwal proyek. Sumber daya dapat diberi nama atau generik.  Bila kebutuhan sumber daya diambil dari penetapan tugas proyek, Project Operations menggunakan kontur upaya penetapan sumber daya untuk membangun kontur detail kebutuhan sumber daya. Namun, referensi penetapan sumber daya tidak dipertahankan. Pembaruan pemesanan yang diambil dari persyaratan sumber daya tidak memperbarui penetapan sumber daya apa pun.

Biasanya, jumlah pemesanan untuk sumber daya akan sama dengan jumlah penetapan sumber daya di satu atau banyak tugas. Namun, Project Operations tidak menegakkan Perjanjian ini. Tampilan **rekonsiliasi** menunjukkan manajer proyek tempat di mana Pemesanan sumber daya dan penetapan tidak sesuai.




[!INCLUDE[footer-include](../includes/footer-banner.md)]