---
title: Pemenuhan persyaratan sumber daya generik
description: Artikel ini menyediakan informasi tentang cara pemesanan sumber daya bernama untuk persyaratan sumber daya generik.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 149ad8305b1442f5bf501d7415264fd4ad7c088d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918546"
---
# <a name="generic-resource-requirement-fulfillment"></a>Pemenuhan persyaratan sumber daya generik

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda dapat memesan sumber daya bernama untuk menggantikan sumber daya generik yang memiliki persyaratan sumber daya.

1. Pada halaman **proyek**, pilih tab **Tim**.
2. Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu pilih **pesan**. Atau, buka persyaratan sumber daya, lalu pilih **pesan**.
3. Di halaman **asisten jadwal**, pilih sumber daya bernama untuk melakukan pemesanan ke tim proyek, lalu pilih **pesan**.

Bila Pemesanan selesai dan dipenuhi oleh sumber daya bernama, sumber daya generik digantikan dengan sumber daya bernama.

Tugas pada jadwal diperbarui dengan sumber daya bernama juga.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Penuhi sumber daya generik dengan beberapa sumber daya bernama
Memenuhi persyaratan untuk sumber daya generik dengan beberapa sumber daya bernama serupa dengan menetapkan satu sumber daya bernama. Misalnya, ada tugas dengan durasi lima hari dan 120 jam upaya. Tugas ini tidak dapat diselesaikan dengan satu sumber daya yang bekerja selama delapan jam sehari selama lima hari seminggu. 

Persyaratannya adalah untuk 120 jam rekayasa Robotika selama lima hari, yang merupakan 24 jam per hari.

Ini adalah contoh bila beberapa sumber daya bernama diperlukan untuk memenuhi permintaan sumber daya generik. Anda perlu memesan beberapa sumber daya untuk memenuhi persyaratan.

Perbedaan utama dalam skenario ini adalah bahwa sumber daya generik tetap pada tim yang ditetapkan untuk tugas, dan anggota tim sumber daya bernama yang dipesan tidak ditetapkan sebagai bagian dari posisi. Manajer proyek dapat menetapkan pekerjaan yang sesuai dengan sumber daya bernama. Tampilan **rekonsiliasi** dapat membantu manajer proyek dalam memecah Pemesanan di beberapa sumber daya menjadi penetapan tugas. Hal ini tidak dilakukan secara otomatis karena dalam skenario apa pun yang lebih rumit daripada contoh sederhana di atas, seperti di mana Anda memiliki bundel tugas yang membuat persyaratan atau maksud dari bagaimana manajer proyek ingin menugaskan, harus diasumsikan oleh sistem. Karena sistem tidak dapat memahami maksud, mungkin asumsi cenderung akan berbeda dari yang dimaksudkan dan hasil yang tidak tepat atau tidak terduga akan terjadi. Hasil yang dapat diprediksi adalah bahwa sumber daya generik tetap ditugaskan hingga manajer proyek dengan sengaja membuat tugas, dengan bantuan tampilan **rekonsiliasi**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]