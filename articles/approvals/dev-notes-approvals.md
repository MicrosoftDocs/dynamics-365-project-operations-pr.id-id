---
title: Catatan pengembang untuk persetujuan
description: Topik ini memberikan informasi pengembang tambahan tentang cara menangani persetujuan.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579724"
---
# <a name="developer-notes-for-approvals"></a>Catatan pengembang untuk persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mencakup logika validasi yang memastikan transisi rekaman yang benar melalui tahapan perjanjian. Transisi rekaman yang benar memastikan: 

  - Semua baris pendukung dibuat dalam tabel terkait, seperti jurnal dan aktual.
  - Pemberi izin ditandai sebagai **pemberi izin proyek** dalam proyek sebelum melanjutkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]