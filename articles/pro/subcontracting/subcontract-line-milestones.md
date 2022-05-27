---
title: Tahap Baris Subkontrak
description: Topik ini menjelaskan cara membuat dan mengelola jadwal faktur berbasis tahapan untuk subkontrak dengan vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d1c30f48e0d43aa55e2c1650637f7f102fb200de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579126"
---
# <a name="subcontract-line-milestones"></a>Tahap Baris Subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Dalam Dynamics 365 Project Operations, baris subkontrak dengan metode penagihan harga tetap dapat menentukan jadwal faktur berbasis tahapan dengan vendor.

Tahapan untuk faktur vendor dapat dibuat secara otomatis menggunakan frekuensi yang ditentukan, atau Anda dapat membuatnya secara manual.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Secara otomatis membuat jadwal faktur berbasis tahapan untuk baris subkontrak

Selesaikan langkah-langkah berikut untuk secara otomatis membuat jadwal faktur berbasis tahap untuk rangkaian tetap tahap terdistribusi yang sama.

1. Buka **Pengaturan** > **Frekuensi Faktur** dan atur frekuensi faktur untuk baris subkontrak.
2. Buka halaman **Subkontrak**, buka subkontrak yang ingin Anda kerjakan, lalu buka baris subkontrak harga tetap yang akan Anda buat jadwal tahapannya.
3. Pada tab **Tahapan Baris Subkontrak**, pilih **Buat Tahapan Periodik**.
4. Di kotak dialog, masukkan atau pilih rentang tanggal, jumlah tahapan, dan frekuensi faktur. Anda dapat memilih tanggal mulai, atau Anda dapat memilih jumlah tahapan dan frekuensi faktur atau tanggal mulai, atau Anda dapat memilih tanggal berakhir dan frekuensi faktur. Anda tidak dapat memilih tanggal berakhir dan jumlah tahapan.
Dengan menggunakan informasi ini, sistem akan menghasilkan tahapan dan rekaman yang ditampilkan dalam kisi **Tahapan**.

   - **Nama Tahapan** - Nama tahapan diatur ke tanggal tahapan berdasarkan frekuensi faktur.
   - **Tanggal Tahapan** - Tanggal berdasarkan frekuensi faktur.
   - **Jumlah Tahapan** - Dihitung dengan membagi jumlah subtotal pada baris subkontrak dengan jumlah tahapan.

Jika baris subkontrak memiliki nilai dalam bidang **Perkiraan Jumlah Pajak**, nilai ini ditambahkan ke setiap tahapan secara merata saat menghasilkan tahapan periodik.

Total jumlah pada tahap baris subkontrak harus sama dengan nilai baris subkontrak. Jika tidak sama, kesalahan terjadi. Anda dapat memperbaiki kesalahan dan memverifikasi bahwa total tahapan sama dengan nilai baris subkontrak dengan membuat, mengedit, atau menghapus tahapan dan jumlah pajak. Setelah perubahan dibuat, simpan dan refresh halaman untuk memastikan tidak ada kesalahan lagi.

## <a name="manually-create-subcontract-line-milestones"></a>Buat Tahapan Baris Subkontrak secara manual

Tahapan harga tetap pada baris subkontrak dapat dihasilkan secara manual bila tidak terpecah secara periodik. Untuk membuat tahap baris subkontrak secara manual, selesaikan langkah-langkah berikut.

1. Di panel navigasi, pilih **Subkontrak**, dan buka Subkontrak yang ingin Anda kerjakan.
2. Buka baris subkontrak harga tetap yang ingin Anda buat tahapannya.
3. Pada tab **Tahapan baris Subkontrak**, pada subkisi, pilih **+ Tahapan Baris Subkontrak Baru**.
4. Pada halaman **Tahapan Baris Subkontrak Baru**, masukkan informasi yang diperlukan berdasarkan tabel berikut.

    | Bidang | KETERANGAN |Dampak Fungsional|
    | --- | --- |----------------------|
    | Nama Tahap | Nama tonggak. |Ini akan ditampilkan sebagai kolom pertama di semua pencarian berdasarkan tahapan baris subkontrak. Baris faktur vendor yang dibuat berdasarkan tahapan ini juga akan menggunakan nama tahapan baris subkontrak sebagai nama default baris faktur vendor.|
    | KETERANGAN | Deskripsi tahapan. |Baris faktur vendor yang dibuat berdasarkan tahapan ini juga akan menggunakan deskripsi tahapan baris subkontrak sebagai deskripsi default baris faktur vendor.|
    | Tanggal Tahap | Tanggal saat proses pembuatan faktur otomatis harus mencari status tahapan ini untuk dipertimbangkan untuk faktur.| Nilai ini akan digunakan sebagai tanggal default baris faktur vendor saat pembuatan faktur untuk baris subkontrak ini. |
    | Jumlah | Jumlah atau nilai tonggak pencapaian yang akan ditagih kepada pelanggan. |Nilai ini digunakan sebagai jumlah default di baris faktur vendor saat pembuatan faktur untuk baris subkontrak ini. |
    | Pajak | Jumlah pajak yang berlaku pada tonggak.| Nilai ini digunakan sebagai jumlah pajak default di baris faktur vendor saat pembuatan faktur untuk baris subkontrak ini. |
    | Jumlah setelah Pajak | Bidang hanya baca ini dihitung sebagai Jumlah + Pajak.|Nilai ini digunakan sebagai default di baris faktur vendor saat pembuatan faktur untuk baris subkontrak ini. |
    | Status Faktur | Saat tahapan dibuat, status ini selalu diatur ke  **Tidak siap untuk faktur**.|  Bila status **Siap untuk Faktur**, pembuatan faktur vendor mencakup tahapan ini pada faktur vendor. |

5. Pilih **Simpan dan Tutup**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
