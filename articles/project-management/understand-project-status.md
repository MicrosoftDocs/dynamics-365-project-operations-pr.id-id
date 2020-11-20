---
title: Memahami status proyek
description: Topik ini menyediakan informasi tentang status yang ditetapkan ke proyek di Dynamics 365 Project operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127297"
---
# <a name="understand-project-status"></a>Memahami status proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Bagian **status** pada halaman **entitas proyek** memberikan ringkasan tentang kesehatan suatu proyek berdasarkan biaya dan usaha.


## <a name="status-summary-fields"></a>Bidang ringkasan status

- Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek. Bidang ini menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko. 
- Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status. 
- Bidang **Status diperbarui pada** tidak dapat diedit. Nilai dalam bidang ini adalah stempel waktu yang menunjukkan waktu pembaruan status terakhir.
- Bidang **performa jadwal** dan **performa biaya** ditetapkan dari kisi pelacakan. Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat memperbarui bidang ini ke **depan**. Bila jadwal dan varians biaya untuk node root negatif, bidang ini diatur ke **belakang**.
