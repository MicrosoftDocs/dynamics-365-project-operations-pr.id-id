---
title: Memahami status proyek
description: Halaman topik ini menyediakan informasi tentang status yang ditetapkan ke proyek di Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286477"
---
# <a name="understand-project-status"></a>Memahami status proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Bagian **status** pada halaman **entitas proyek** memberikan ringkasan tentang kesehatan suatu proyek berdasarkan biaya dan usaha.


## <a name="status-summary-fields"></a>Bidang ringkasan status

- Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek. Bidang ini menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko. 
- Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status. 
- Bidang **Status diperbarui pada** tidak dapat diedit. Nilai dalam bidang ini adalah stempel waktu yang menunjukkan waktu pembaruan status terakhir.
- Bidang **performa jadwal** dan **performa biaya** ditetapkan dari kisi pelacakan. Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat memperbarui bidang ini ke **depan**. Bila jadwal dan varians biaya untuk node root negatif, bidang ini diatur ke **belakang**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]