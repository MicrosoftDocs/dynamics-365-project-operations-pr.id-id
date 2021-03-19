---
title: Catatan pengembang untuk persetujuan
description: Topik ini memberikan informasi pengembang tambahan tentang cara menangani persetujuan.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290273"
---
# <a name="developer-notes-for-approvals"></a>Catatan pengembang untuk persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mencakup logika validasi yang memastikan transisi rekaman yang benar melalui tahapan perjanjian. Transisi rekaman yang benar memastikan: 

  - Semua baris pendukung dibuat dalam tabel terkait, seperti jurnal dan aktual.
  - Pemberi izin ditandai sebagai **pemberi izin proyek** dalam proyek sebelum melanjutkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]