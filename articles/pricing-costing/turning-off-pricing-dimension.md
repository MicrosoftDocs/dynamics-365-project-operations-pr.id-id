---
title: Menonaktifkan dimensi harga
description: Topik ini menyediakan informasi tentang cara menonaktifkan dimensi harga.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1a7c91ef70b1dd3697f6a8b5044c6ad4a14c4e74
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078580"
---
# <a name="turning-off-a-pricing-dimension"></a>Menonaktifkan dimensi harga

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda mungkin harus meninjau dan memperbarui strategi harga setiap beberapa tahun. Pembaruan apa pun yang Anda buat mungkin mengharuskan Anda menonaktifkan dimensi harga yang ada dan membuat yang baru. Misalnya, Anda mungkin sebelumnya menetapkan harga berdasarkan **peran** , tapi sekarang Anda telah memutuskan harga dengan **pengalaman kerja**. Ini mungkin mengharuskan Anda menonaktifkan **peran** sebagai dimensi harga dan membuat **pengalaman kerja** sebagai dimensi harga baru. 

Menonaktifkan dimensi harga, tidak peduli apakah itu bawaan atau kustom, dapat dilakukan dengan mengatur bidang **berlaku untuk biaya** dan **berlaku untuk penjualan** pada dimensi harga ke **tidak**.

Namun, bila Anda melakukannya, Anda mungkin menerima pesan kesalahan, **dimensi harga tidak dapat diperbarui atau dihapus jika ada rekaman harga terkait.**

Pesan kesalahan ini menunjukkan bahwa ada rekaman harga yang diatur sebelumnya untuk dimensi yang dinonaktifkan. Semua rekaman **harga peran** dan **markup harga peran** yang merujuk ke dimensi harus dihapus sebelum penerapan dimensi dapat diatur ke **tidak**. Aturan ini berlaku untuk dimensi harga Bawaan dan dimensi harga kustom apa pun yang mungkin telah Anda buat. Alasan untuk validasi ini adalah karena setiap rekaman **harga peran** harus memiliki kombinasi dimensi yang unik. Misalnya, pada daftar harga yang disebut **Tarif Biaya AS 2018** , Anda memiliki baris **harga peran** berikut. 

| Jabatan standar         | Unit Organisasi    |Unit   |Harga  |Mata Uang  |
| -----------------------|-------------|-------|-------|----------|
| Insinyur sistem|Contoso AS|Hour| 100|USD|
| Insinyur sistem senior|Contoso AS|Hour| 150| USD|


Bila Anda menonaktifkan **jabatan standar** sebagai dimensi harga, dan mesin harga mencari harga, ia hanya akan menggunakan nilai **unit organisasi** dari konteks input. Jika **unit organisasi** konteks input adalah "Aswono US", hasilnya akan non-deterministik karena kedua baris akan cocok. Untuk menghindari skenario ini, saat Anda membuat rekaman **harga peran** , sistem memvalidasi bahwa kombinasi dimensi itu adalah unik. Jika dimensi dinonaktifkan setelah rekaman **harga peran** dibuat, kendala ini dapat dilanggar. Oleh karena itu, diperlukan bahwa sebelum Anda menonaktifkan dimensi, Anda menghapus semua baris **harga peran** dan **markup harga peran** yang diisi nilai dimensi tersebut.
