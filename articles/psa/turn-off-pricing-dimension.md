---
title: Menonaktifkan dimensi harga
description: Topik ini menunjukkan cara mengkonfigurasi dimensi harga dalam solusi Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014300"
---
# <a name="turn-off-a-pricing-dimension"></a>Menonaktifkan dimensi harga

[!include [banner](../includes/psa-now-project-operations.md)]

Anda mungkin harus meninjau dan memperbarui strategi harga setiap beberapa tahun. Pembaruan apa pun yang Anda buat mungkin mengharuskan Anda menonaktifkan dimensi harga yang ada dan membuat yang baru. Misalnya, Anda mungkin sebelumnya menetapkan harga berdasarkan **peran**, tapi sekarang Anda telah memutuskan harga dengan **pengalaman kerja**. Ini mungkin mengharuskan Anda menonaktifkan **peran** sebagai dimensi harga dan membuat **pengalaman kerja** sebagai dimensi harga baru. 

Menonaktifkan dimensi harga, tidak peduli apakah itu bawaan atau kustom, dapat dilakukan dengan mengatur bidang **berlaku untuk biaya** dan **berlaku untuk penjualan** pada dimensi harga ke **tidak**.

Namun, bila Anda melakukannya, Anda mungkin menerima pesan kesalahan berikut.

![Kesalahan proses bisnis cenderung terjadi saat mematikan dimensi harga](media/Business-Process-Error.png)


Pesan kesalahan ini menunjukkan bahwa ada rekaman harga yang diatur sebelumnya untuk dimensi yang dinonaktifkan. Semua rekaman **harga peran** dan **markup harga peran** yang merujuk ke dimensi harus dihapus sebelum penerapan dimensi dapat diatur ke **tidak**. Aturan ini berlaku untuk dimensi harga Bawaan dan dimensi harga kustom apa pun yang mungkin telah Anda buat. Alasan untuk validasi ini adalah karena Project Service memiliki batasan bahwa setiap rekaman **harga peran** harus memiliki kombinasi dimensi yang unik. Misalnya, pada daftar harga yang disebut **Tarif Biaya AS 2018**, Anda memiliki baris **harga peran** berikut. 

| Jabatan standar         | Unit Organisasi    |Unit   |Harga  |Mata uang  |
| -----------------------|-------------|-------|-------|----------|
| Insinyur sistem|Contoso AS|Jam| 100|USD|
| Insinyur sistem senior|Contoso AS|Jam| 150| USD|


Bila Anda menonaktifkan **jabatan standar** sebagai dimensi harga, dan mesin harga Project Service mencari harga, ia hanya akan menggunakan nilai **unit organisasi** dari konteks input. Jika **unit organisasi** konteks input adalah "Contoso US", hasilnya akan non-deterministik karena kedua baris akan cocok. Untuk menghindari skenario ini, saat Anda membuat rekaman **harga peran**, Project Service memvalidasi bahwa kombinasi dimensi itu adalah unik. Jika dimensi dinonaktifkan setelah rekaman **harga peran** dibuat, kendala ini dapat dilanggar. Oleh karena itu, diperlukan bahwa sebelum Anda menonaktifkan dimensi, Anda menghapus semua baris **harga peran** dan **markup harga peran** yang diisi nilai dimensi tersebut.



[!INCLUDE[footer-include](../includes/footer-banner.md)]