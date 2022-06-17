---
title: Pemesanan vs Penugasan
description: Artikel ini memberikan informasi tentang perbedaan antara pemesanan sumber daya dan penetapan sumber daya.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918592"
---
# <a name="bookings-vs-assignments"></a>Pemesanan vs Penugasan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Pemesanan adalah alokasi sumber daya definitif atau tentatif ke proyek. Pemesanan definitif mengkonsumsi kapasitas sumber daya. Pemesanan mewakili konsep organisasi untuk tim sehingga mereka dapat memahami bagaimana sumber daya akan terlibat di berbagai proyek. Dynamics 365 Project Operations mempertimbangkan pemesanan sebagai konsep tingkat proyek. 

Tidak seperti pemesanan, penetapan adalah komitmen sumber daya untuk tugas proyek dalam jadwal proyek. Sumber daya dapat diberi nama atau generik.  Bila kebutuhan sumber daya diambil dari penetapan tugas proyek, Project Operations menggunakan kontur upaya penetapan sumber daya untuk membangun kontur detail kebutuhan sumber daya. Namun, referensi penetapan sumber daya tidak dipertahankan. Pembaruan pemesanan yang diambil dari persyaratan sumber daya tidak memperbarui penetapan sumber daya apa pun.

Biasanya, jumlah pemesanan untuk sumber daya akan sama dengan jumlah penetapan sumber daya di satu atau banyak tugas. Namun, Project Operations tidak menegakkan Perjanjian ini. Tampilan **rekonsiliasi** menunjukkan manajer proyek tempat di mana Pemesanan sumber daya dan penetapan tidak sesuai.




[!INCLUDE[footer-include](../includes/footer-banner.md)]