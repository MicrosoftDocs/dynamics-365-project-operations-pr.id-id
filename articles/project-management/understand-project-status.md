---
title: Memahami status proyek
description: Artikel ini ini menyediakan informasi tentang status yang ditetapkan ke proyek di Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 86cb60b634b62af23f39720c0452dca82ff3ad26
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923606"
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