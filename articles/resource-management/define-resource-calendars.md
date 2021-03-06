---
title: Menentukan kalender sumber daya
description: Topik ini menyediakan informasi tentang cara menentukan kalender jam kerja untuk sumber daya dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961884"
---
# <a name="define-resource-calendars"></a>Menentukan kalender sumber daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Setiap sumber daya dapat dipesan yang mengerjakan proyek harus memiliki kalender jam kerja untuk menentukan ketersediaan mereka. Jam kerja untuk sumber daya dapat didefinisikan dengan dua cara: 

   - Menentukan aturan kalender individual untuk sumber daya
   - Menerapkan template kalender yang ada untuk sumber daya

## <a name="define-a-resources-working-hours"></a>Menentukan jam kerja sumber daya

1. Pada menu **sumber daya**, pilih **sumber daya**.
2. Dari tampilan kisi, pilih **sumber daya dapat dipesan** yang berlaku.
3. Pada halaman **rincian sumber daya**, pilih tab **jam kerja**. Secara default, kalender sumber daya yang dapat dipesan akan default ke jam kerja template jam kerja default yang ditentukan untuk organisasi.
4. Untuk memperbarui jam kerja, klik kanan pada tanggal mulai aturan kalender yang diusulkan yang akan ditentukan. Gunakan menu aturan kalender untuk menentukan aturan kalender untuk hari tertentu, sisa rangkaian, atau seluruh kalender.
5. Setelah pilihan dipilih, Anda kemudian dapat menentukan:

    - Hari kerja dalam sepekan di mana jam kerja akan berlaku.
    - Waktu kerja dalam setiap hari.
    - Zona waktu lokal untuk aturan kalender.
    - Jika berlaku, waktu non-kerja juga dapat ditentukan untuk aturan.

## <a name="applying-a-calendar-template-to-a-resource"></a>Menerapkan template kalender ke sumber daya

1. Pada menu **sumber daya**, pilih **sumber daya**.
2. Dari tampilan kisi, pilih hingga 25 **sumber daya dapat dipesan** untuk diperbarui.
3. Pilih **Atur kalender** dan dialog akan meminta Anda daftar template jam kerja yang tersedia.
4. Pilih template yang ingin Anda gunakan, kemudian pilih **Terapkan**.
