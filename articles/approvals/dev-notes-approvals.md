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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483952"
---
# <a name="developer-notes-for-approvals"></a>Catatan pengembang untuk persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mencakup logika validasi yang memastikan transisi rekaman yang benar melalui tahapan perjanjian. Transisi rekaman yang benar memastikan: 

  - Semua baris pendukung dibuat dalam tabel terkait, seperti jurnal dan aktual.
  - Pemberi izin ditandai sebagai **pemberi izin proyek** dalam proyek sebelum melanjutkan.
