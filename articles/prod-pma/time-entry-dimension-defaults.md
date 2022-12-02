---
title: Defaultasi dimensi keuangan untuk entri waktu proyek
description: Artikel ini memberikan informasi tentang cara penerapan dimensi keuangan default pada entri waktu.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916568"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Defaultasi dimensi keuangan untuk entri waktu proyek

[!include [banner](../includes/banner.md)]

Bila Anda menggunakan dimensi keuangan untuk entri waktu proyek, nilai dimensi default akan dinilai dalam urutan berikut:

1. Sumber info
2. Project
3. Sumber pendanaan

Contohnya, jika dimensi default ditentukan pada sumber daya, nilai default diterapkan atas nilai default yang ditentukan untuk proyek. Demikian pula, jika jika dimensi default ditentukan pada proyek, nilai default diterapkan atas nilai default yang ditentukan untuk sumber pendanaan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
