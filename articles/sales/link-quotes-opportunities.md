---
title: Membuat kuotasi proyek dari peluang
description: Topik ini menyediakan informasi tentang membuat kuotasi proyek dari peluang.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898536"
---
# <a name="create-project-quotes-from-opportunities"></a>Membuat kuotasi proyek dari peluang

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kuotasi dapat dibuat dari peluang proyek dengan cara berikut:

- Dari tab **kuotasi** pada halaman **peluang proyek**
- Dari alur Proses Penjualan Peluang
- Dengan memperbarui referensi peluang pada kuotasi yang ada

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Dari tab kuotasi pada halaman peluang proyek

Untuk membuat kuotasi proyek dari peluang, selesaikan langkah berikut.

1. Buka halaman **peluang proyek** dan pilih tab **Kuotasi**. 
2. Pada subkisi **kuotasi**, pilih **+** untuk membuat kuotasi proyek baru berdasarkan peluang. Semua baris peluang dan daftar harga proyek terkait akan disalin ke kuotasi baru dari peluang.

## <a name="from-the-opportunity-sales-process-flow"></a>Dari alur Proses Penjualan Peluang

Untuk membuat kuotasi dari alur proses penjualan peluang, selesaikan langkah berikut.

1. Dari alur proses penjualan peluang, buka peluang.
2. Pilih tahap **Kualifikasi**. 
3. Pilih **berikutnya,** lalu pilih **+ buat** untuk membuat kuotasi baru. Sebagian besar informasi pada tab **ringkasan** untuk kuotasi baru ini akan di-default dari peluang. 
4. Masukkan informasi diperlukan yang tidak ada, atau Perbarui nilai default yang diperlukan pada tab **ringkasan**,
5. Pilih **Simpan**. Kuotasi baru dibuat dan terkait dengan peluang. Anda sekarang dapat melihat informasi kuotasi pada tab **kuotasi** pada halaman **peluang**. 

   Proses penjualan peluang bergerak ke tahap berikutnya, **mengusulkan**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Dengan memperbarui referensi peluang pada kuotasi yang ada

Kuotasi yang ada dapat ditautkan ke peluang. Selesaikan langkah-langkah berikut untuk memperbarui informasi peluang pada kuotasi yang ada.

1. Buka halaman **Kuotasi** dan pilih tab **Ringkasan**.
2. Di bidang **peluang**, pilih peluang yang akan ditautkan ke kuotasi. Anda dapat melihat kuotasi di kisi **kuotasi** peluang. 
3. Menggunakan proses penjualan peluang, peluang dapat dipindahkan ke tahap berikutnya, **mengusulkan**. 

   Saat Anda memindahkan peluang ke tahapan ini, Anda dapat memilih kuotasi ini dari daftar kuotasi yang terkait dengan peluang ini. Memilih kuotasi ini menunjukkan bahwa Anda bergerak maju dengan itu.

   Semua tanda lainnya yang terkait dengan peluang akan tetap tersedia dan aktif hingga salah satunya dimenangkan. Anda dapat memindahkan proses penjualan kembali ke tahap sebelumnya yaitu **Kualifikasi**, dan memilih kuotasi lainnya untuk diteruskan.
