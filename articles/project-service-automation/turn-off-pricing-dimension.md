---
title: Menonaktifkan dimensi harga
description: Topik ini menunjukkan cara mengkonfigurasi dimensi harga dalam solusi Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752474"
---
# <a name="turn-off-a-pricing-dimension"></a>Menonaktifkan dimensi harga

Anda mungkin harus meninjau dan memperbarui strategi harga setiap beberapa tahun. Pembaruan apa pun yang Anda buat mungkin mengharuskan Anda menonaktifkan dimensi harga yang ada dan membuat yang baru. Misalnya, Anda mungkin sebelumnya menetapkan harga berdasarkan **peran**, tapi sekarang Anda telah memutuskan harga dengan **pengalaman kerja**. Ini mungkin mengharuskan Anda menonaktifkan **peran** sebagai dimensi harga dan membuat **pengalaman kerja** sebagai dimensi harga baru. 

Menonaktifkan dimensi harga, tidak peduli apakah itu bawaan atau kustom, dapat dilakukan dengan mengatur bidang **berlaku untuk biaya** dan **berlaku untuk penjualan** pada dimensi harga ke **tidak**.

Namun, bila Anda melakukannya, Anda mungkin menerima pesan kesalahan berikut.

![Kesalahan proses bisnis cenderung terjadi saat mematikan dimensi harga](media/Business-Process-Error.png)


Pesan kesalahan ini menunjukkan bahwa ada rekaman harga yang diatur sebelumnya untuk dimensi yang dinonaktifkan. Semua rekaman **harga peran** dan **markup harga peran** yang merujuk ke dimensi harus dihapus sebelum penerapan dimensi dapat diatur ke **tidak**. Aturan ini berlaku untuk dimensi harga Bawaan dan dimensi harga kustom apa pun yang mungkin telah Anda buat. Alasan untuk validasi ini adalah karena Project Service memiliki batasan bahwa setiap rekaman **harga peran** harus memiliki kombinasi dimensi yang unik. Misalnya, pada daftar harga yang disebut **Tarif Biaya AS 2018**, Anda memiliki baris **harga peran** berikut. 

| Jabatan standar         | Unit Organisasi    |Unit   |Harga  |Mata Uang  |
| -----------------------|-------------|-------|-------|----------|
| Insinyur sistem|Contoso AS|Hour| 100|USD|
| Insinyur sistem senior|Contoso AS|Hour| 150| USD|


Bila Anda menonaktifkan **jabatan standar** sebagai dimensi harga, dan mesin harga Project Service mencari harga, ia hanya akan menggunakan nilai **unit organisasi** dari konteks input. Jika **unit organisasi** konteks input adalah "Aswono US", hasilnya akan non-deterministik karena kedua baris akan cocok. Untuk menghindari skenario ini, saat Anda membuat rekaman **harga peran**, Project Service memvalidasi bahwa kombinasi dimensi itu adalah unik. Jika dimensi dinonaktifkan setelah rekaman **harga peran** dibuat, kendala ini dapat dilanggar. Oleh karena itu, diperlukan bahwa sebelum Anda menonaktifkan dimensi, Anda menghapus semua baris **harga peran** dan **markup harga peran** yang diisi nilai dimensi tersebut.

