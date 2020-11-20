---
title: Membuat jadwal faktur di baris kontrak berbasis proyek
description: Topik ini menyediakan informasi tentang bagaimana membuat jadwal faktur dan tonggak di baris kontrak.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 674f4ccced3d0e3178799f60d9f95a2ec27cd153
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180781"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Membuat jadwal faktur di baris kontrak berbasis proyek 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Anda dapat membuat jadwal faktur untuk baris kontrak berbasis proyek. Faktur hanya diizinkan setelah kontrak dimenangkan dan Anda membuat kontrak proyek. Jadwal faktur memungkinkan draf faktur untuk baris kontrak berbasis proyek dibuat secara otomatis. Namun jika Anda hanya membuat faktur secara manual, Anda dapat melewatkan pembuatan jadwal faktur pada baris kontrak.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Buat jadwal faktur waktu dan material untuk baris kontrak

Bila baris kontrak berbasis proyek memiliki metode penagihan waktu dan material, Anda dapat membuat jadwal faktur berdasarkan tanggal. Untuk secara otomatis membuat jadwal faktur berdasarkan tanggal, selesaikan langkah-langkah berikut.

1. Buka **pengaturan** > **frekuensi faktur** dan atur frekuensi faktur.
2. Buka rekaman kontrak proyek, dan di tab **ringkasan**, di bidang **tanggal pengiriman yang diminta**, pilih tanggal.
3. Buka baris kontrak **waktu dan material** yang Anda perlukan untuk membuat jadwal faktur berdasarkan tanggal. 
4. Pada tab **jadwal faktur**, pilih tanggal mulai penagihan dan frekuensi faktur.
5. Pada subkisi, pilih **buat jadwal faktur**. Jadwal faktur dibuat dengan **tanggal Jalankan faktur**, **tanggal batas transaksi**, dan bidang **status menjalankan** yang diatur sebagai berikut:

    - **Tanggal Jalankan faktur**: Tanggal ini didikte oleh frekuensi faktur.
    - **Tanggal batas transaksi**: hari sebelum tanggal Jalankan faktur.
    - **Status Jalankan**: Otomatis diatur ke **tidak berjalan**. Ketika pekerjaan pembuatan faktur otomatis berjalan untuk faktur tertentu tanggal berjalan, bidang ini diperbarui ke **berhasil menjalankan** atau **gagal menjalankan**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Buat jadwal faktur harga tetap untuk baris kontrak

Bila baris kontrak memiliki metode penagihan tetap, Anda dapat membuat jadwal faktur berbasis tonggak. 

> [!NOTE]
> Tonggak tidak dapat dibuat pada baris kontrak jika tidak ada proyek yang dipetakan ke baris kontrak.

Selesaikan langkah-langkah berikut untuk membuat jadwal faktur berbasis tonggak pencapaian untuk tonggak pencapaian yang didistribusikan secara merata untuk periode kalender.

1. Buka **pengaturan** > **frekuensi faktur** dan atur frekuensi faktur.
2. Buka rekaman kontrak proyek, dan di tab **ringkasan**, di bidang **tanggal pengiriman yang diminta**, pilih tanggal.
3. Buka baris kontrak **harga tetap** yang Anda buat jadwal tonggaknya. Pada tab **Tonggak Penagihan**, pilih tanggal mulai penagihan dan frekuensi faktur. 
4. Pada subkisi, pilih **buat tonggak periode**. Jadwal faktur dibuat dengan bidang **nama tonggak**, **tanggal tonggak**, dan **jumlah tonggak** diatur sebagai berikut:

    - **Nama Tonggak**: Tanggal ini didikte oleh frekuensi faktur.
    - **Tanggal Tonggak**: Tanggal ini didikte oleh frekuensi faktur.
    - **Jumlah tonggak**: Jumlah dihitung dengan membagi jumlah kontrak pada baris kontrak berbasis proyek berdasarkan jumlah tonggak yang didikte oleh frekuensi dan awal penagihan dan tanggal pengiriman yang diminta.

    Jika baris kontrak memiliki nilai di bidang **Estimasi jumlah pajak**, maka bidang ini juga dibagikan ke setiap tonggak dengan setara saat menghasilkan tonggak periodik.

Tonggak penagihan harus sama dengan nilai kontrak baris kontrak. Jika tidak, Anda akan menerima kesalahan pada halaman **baris kontrak**. Anda dapat memperbaiki kesalahan dengan memverifikasi tonggak penagihan merupakan total nilai kontrak baris dengan membuat, mengedit, atau menghapus tonggak. Setelah perubahan dibuat, segarkan halaman untuk menghilangkan kesalahan.

### <a name="manually-create-milestones"></a>Buat tonggak secara manual

Anda dapat membuat tonggak harga tetap secara manual saat tidak dibagi secara berkala. Selesaikan langkah-langkah berikut untuk membuat proyek baru secara manual.

1. Buka baris kontrak harga tetap yang Anda buat tonggak untuknya, dan pada tab **jadwal faktur**, pada subkisi, pilih **+ buat tonggak baris kontrak baru**. 
2. Pada halaman **pembuatan tonggak**, masukkan informasi yang diperlukan berdasarkan tabel berikut.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| Nama Tahap | Buat Cepat | Bidang teks untuk nama tonggak. | Ini dibawa ke tonggak baris kontrak proyek dan ke faktur. |
| Tugas Proyek | Buat Cepat | Jika tonggak terkait dengan tugas proyek, gunakan referensi ini untuk menambahkan logika kustom untuk mengatur status tonggak berdasarkan status tugas. | Aplikasi ini tidak memiliki dampak hilir terkait referensi ini untuk tugas. |
| Tanggal Tahap | Buat Cepat | Atur tanggal untuk proses pembuatan faktur otomatis mencari status tonggak ini untuk dipertimbangkan untuk faktur. | Ini dibawa ke tonggak baris kontrak proyek dan ke faktur. |
| Status Faktur | Buat Cepat | Bila tonggak dibuat, status ini selalu diatur ke **tidak siap untuk faktur** atau **Belum Dimulai**. | Ini dibawa ke tonggak baris kontrak proyek dan ke faktur. |
| Jumlah Baris | Buat Cepat | Jumlah atau nilai tonggak yang akan ditagih kepada pelanggan. | Ini dibawa ke tonggak baris kontrak proyek dan ke faktur. |
| Pajak | Buat Cepat | Jumlah pajak yang berlaku pada tonggak. | Ini dibawa ke tonggak baris kontrak proyek dan ke faktur. |

3. Pilih **Simpan dan Tutup**.
