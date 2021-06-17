---
title: Pembayaran harian
description: Topik ini menyediakan informasi tentang aturan uang saku yang digunakan dalam manajemen pengeluaran.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995265"
---
# <a name="per-diems"></a>Pembayaran harian

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Uang saku adalah jatah uang yang dibayarkan kepada pekerja yang melakukan pekerjaan. Di manajemen pengeluaran, Anda dapat membuat aturan uang saku untuk berbagai situasi perjalanan. Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya. Saat membuat aturan uang saku, Anda dapat menentukan bahwa persentase tingkat uang saku diabaikan jika pekerja menerima makanan, atau layanan gratis. Anda juga dapat menetapkan jumlah jam minimum dan maksimum yang dapat diterapkan dalam tarif uang saku untuk perjalanan pekerja.

## <a name="configuration"></a>Konfigurasi 

1. Untuk menambahkan lokasi uang saku, buka **Konfigurasikan** > **penghitungan dan kode** > **lokasi uang saku**.
2. Untuk setiap lokasi yang ditambahkan di atas, pilih tingkat uang saku, dan mata uang yang berlaku antara tanggal mulai, dan berakhir tertentu untuk hotel, makan, dan biaya lainnya. Tarif uang saku dan mata uang dikonfigurasi dalam **Konfigurasikan** > **penghitungan dan kode** > **uang saku**.
3. Di halaman **lokasi uang saku**, konfigurasikan tingkatan tarif uang saku. Tingkatan tarif uang saku memungkinkan Anda menentukan persentase pembagian penyisihan harian untuk hotel, makan, dan biaya lainnya. 
4. Untuk menentukan pengurangan persentase makanan untuk sarapan, Makan Siang, atau makan malam, Perbarui bidang pada halaman **parameter manajemen pengeluaran** pada tab **uang saku**. 
    
## <a name="submit-expenses-using-per-diem"></a>Ajukan pengeluaran menggunakan uang saku
Untuk mengajukan pengeluaran menggunakan uang saku, gunakan kategori pengeluaran **uang saku** saat membuat laporan pengeluaran. Masukkan **uang saku dari tanggal**, **uang saku hingga tanggal**, dan **lokasi uang saku**. Jumlah tersebut akan dihitung berdasarkan harga uang saku untuk lokasi yang dipilih dan pengurangan makanan akan dihitung berdasarkan tingkatan tarif uang saku.


[!INCLUDE[footer-include](../includes/footer-banner.md)]