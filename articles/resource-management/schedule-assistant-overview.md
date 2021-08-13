---
title: Sekilas asisten jadwal
description: Topik ini menyediakan informasi tentang cara menangani asisten jadwal untuk memesan sumber daya.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 309cb94ea30c525daccf032c625004c42fb408dada4b337b65d8f36d76219669
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990230"
---
# <a name="schedule-assistant-overview"></a>Sekilas asisten jadwal

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Asisten jadwal digunakan untuk memesan sumber daya berdasarkan persyaratan yang ditentukan oleh manajer proyek. Asisten jadwal bergantung pada parameter yang diberikan dalam persyaratan sumber daya untuk menemukan sumber daya. Asisten jadwal merekomendasikan sumber daya yang sesuai dengan persyaratan yang relevan, seperti periode waktu atau keterampilan yang diperlukan.

Setelah sumber daya yang sesuai diidentifikasi, manajer sumber daya atau proyek dapat memesan sumber daya untuk pekerjaan.

## <a name="prerequisites"></a>Prasyarat

Asisten jadwal adalah bagian dari solusi Universal Resource Scheduling. Solusi ini disertakan dan diinstal dengan Dynamics 365 Project Operations, Dynamics 365 Field Service, dan Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Menyesuaikan persyaratan dengan sumber daya

Persyaratan sumber daya yang dihasilkan didasarkan pada rincian seperti:

-   Karakteristik
-   Peran
-   Unit bisnis
-   Preferensi Sumber Daya
-   Kontur usaha
-   Zona waktu

Asisten jadwal menggunakan rincian ini untuk memfilter sumber daya.

## <a name="launch-the-schedule-assistant"></a>Luncurkan Asisten Jadwal

Ada dua cara di mana asisten jadwal diluncurkan. Jika Anda menggunakan mode hibrida, di kisi anggota tim, Anda dapat memilih anggota tim dengan persyaratan sumber daya yang tidak terpenuhi, lalu memilih **Pesan**. Jika Anda menggunakan mode pusat, manajer sumber daya mencari dan memilih sumber daya.

## <a name="schedule-assistant-filters"></a>Filter Asisten Jadwal

Setelah menjalankan asisten jadwal, rincian dari persyaratan sumber daya ditampilkan sebagai nilai terfilter di panel kiri. Manajer sumber daya atau manajer proyek dapat menyempurnakan hasil dengan menyesuaikan filter untuk memenuhi kebutuhan penjadwalan.

Panel filter menampilkan pilihan yang terkait dengan pekerjaan, termasuk:

-   Awal dan akhir kerja
-   Karakteristik
-   Peran
-   Unit organisasi
-   Perusahaan Pencari Sumber Daya
-   Jenis Sumber Daya
-   Sumber Daya Pilihan


[!INCLUDE[footer-include](../includes/footer-banner.md)]