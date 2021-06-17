---
title: Catatan pengembang untuk persetujuan
description: Topik ini memberikan informasi pengembang tambahan tentang cara menangani persetujuan.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996795"
---
# <a name="developer-notes-for-approvals"></a>Catatan pengembang untuk persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mencakup logika validasi yang memastikan transisi rekaman yang benar melalui tahapan perjanjian. Transisi rekaman yang benar memastikan: 

  - Semua baris pendukung dibuat dalam tabel terkait, seperti jurnal dan aktual.
  - Pemberi izin ditandai sebagai **pemberi izin proyek** dalam proyek sebelum melanjutkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]