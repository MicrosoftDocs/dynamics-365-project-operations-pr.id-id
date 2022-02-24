---
title: Unit dan grup unit
description: Topik ini memberikan informasi tentang cara membuat unit dan grup unit di Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131032"
---
# <a name="units-and-unit-groups"></a>Unit dan grup unit

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Unit adalah kuantitas atau pengukuran tempat Anda menjual produk atau layanan. Misalnya, jika Anda menjual perlengkapan berkebun, Anda mungkin menjual benih dalam satuan paket, kotak, dan palet. Grup unit adalah kumpulan unit berbeda ini.

Untuk menyelesaikan langkah-langkah dalam topik ini, pastikan Anda telah ditetapkan ke peran Administrator sistem, atau manajer Sales Professional, atau memiliki izin yang setara.

## <a name="create-a-unit-group"></a>Membuat grup unit

1. Di peta situs, pilih **Unit**.
2. Pilih **baru**, dan di kotak dialog **Buat grup unit**, masukkan nama unit.
3. Di bidang **unit primer**, Masukkan satuan pengukuran umum terendah yang dari sana produk akan dijual. Misalnya, Anda dapat memasukkan "buah" atau "ounce".
4. Pilih **OK**.

## <a name="add-units-to-a-unit-group"></a>Tambahkan unit ke grup unit

1. Buka grup unit, dan di tab **terkait**, pilih **unit**. Anda akan melihat bahwa unit utama telah ditambahkan.
2. Pilih **Tambah unit baru**, dan di halaman **Buat cepat: unit**, di bidang **nama**, masukkan nama unit.
3. Di bidang **kuantitas**, masukkan kuantitas unit. Sebagai contoh, jika sebuah kotak berisi 2 buah, ketik "2". 
4. Di bidang **satuan dasar**, pilih satuan dasar untuk menetapkan satuan pengukuran terendah untuk unit. Misalnya, Anda dapat memilih "Buah".
5. Pilih **Simpan**:
