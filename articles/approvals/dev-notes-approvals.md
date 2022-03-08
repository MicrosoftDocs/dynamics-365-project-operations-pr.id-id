---
title: Catatan pengembang untuk persetujuan
description: Topik ini memberikan informasi pengembang tambahan tentang cara menangani persetujuan.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991670"
---
# <a name="developer-notes-for-approvals"></a>Catatan pengembang untuk persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mencakup logika validasi yang memastikan transisi rekaman yang benar melalui tahapan perjanjian. Transisi rekaman yang benar memastikan: 

  - Semua baris pendukung dibuat dalam tabel terkait, seperti jurnal dan aktual.
  - Pemberi izin ditandai sebagai **pemberi izin proyek** dalam proyek sebelum melanjutkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]