---
title: Jadwal faktur pada baris kuotasi berbasis proyek
description: Topik ini menyediakan informasi tentang pembuatan jadwal faktur dan tonggak untuk baris kuotasi.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0a8e94bf7ff807028cec05380ac8c9bc22094d82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010160"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Jadwal faktur pada baris kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Baris kuotasi berbasis proyek memberikan kemampuan untuk mengekspresikan jadwal faktur. Ini opsional selama fase kuotasi karena aplikasi tidak mendukung faktur proyek saat terikat ke baris kuotasi. Faktur hanya diizinkan setelah kuotasi dimenangkan. Satu-satunya dampak hilir untuk membuat jadwal faktur selama fase kuotasi adalah bahwa jadwal faktur ini disalin ke baris kontrak berbasis proyek. Jika Anda tidak membuat jadwal faktur selama fase kuotasi, Anda akan dapat melakukannya pada baris kontrak berbasis proyek.

Secara keseluruhan, tujuan jadwal faktur adalah untuk memungkinkan pembuatan otomatis rancangan faktur untuk baris kontrak berbasis proyek. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Buat jadwal faktur waktu dan material untuk baris kuotasi berbasis proyek

Bila metode penagihan untuk baris kuotasi berbasis proyek adalah waktu dan material, sistem akan menghasilkan jadwal faktur berdasarkan tanggal. Untuk secara otomatis membuat jadwal faktur berdasarkan tanggal, selesaikan langkah-langkah berikut.

1. Buka **pengaturan** > **frekuensi faktur** dan atur frekuensi faktur.
2. Pada halaman **kuotasi**, buka kuotasi proyek dan pada tab **ringkasan**, atur tanggal pengiriman yang diminta.
3. Buka baris kuotasi waktu dan material yang Anda perlukan untuk membuat jadwal faktur berdasarkan tanggal. 
4. Pada tab **jadwal faktur**, pilih nilai di bidang **awal penagihan** penagihan mulai dan **frekuensi faktur**. 
5. Pada subkisi, pilih **buat jadwal faktur**.
6. Aplikasi menghasilkan jadwal faktur dengan **tanggal Jalankan faktur**, **tanggal batas transaksi**, dan bidang **status menjalankan** yang diatur dengan cara berikut:

    - **Tanggal Jalankan faktur** diatur ke tanggal yang didikte berdasarkan frekuensi faktur.
    - **Tanggal batas transaksi** diatur ke hari sebelum **tanggal Jalankan faktur**.
    - **Status Jalankan** diatur secara otomatis ke **tidak berjalan**. Ketika pekerjaan pembuatan faktur otomatis berjalan untuk faktur tertentu tanggal berjalan, itu akan memperbarui bidang ini baik **menjalankan berhasil** atau **menjalankan gagal**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Buat jadwal faktur harga tetap untuk baris kuotasi berbasis proyek

Bila baris kuotasi berbasis proyek memiliki metode penagihan **tetap**, sistem membuat jadwal faktur berbasis tonggak. Selesaikan langkah-langkah berikut untuk secara otomatis membuat jadwal ini untuk rangkaian tetap dari tonggak yang didistribusikan secara merata untuk periode kalender.

1. Buka **pengaturan** > **frekuensi faktur** dan atur frekuensi faktur.
2. Pada halaman **kuotasi**, buka kuotasi proyek dan pada tab **ringkasan**, atur tanggal pengiriman yang diminta.
3. Buka baris kuotasi harga tetap yang Anda perlukan untuk membuat jadwal tonggaknya. 
4. Pada tab **jadwal faktur**, pilih nilai di bidang **awal penagihan** penagihan mulai dan **frekuensi faktur**. 
5. Pada subkisi, pilih **buat tonggak periode**.
6. Aplikasi ini menghasilkan jadwal faktur dengan nama tonggak, tanggal, dan jumlah.

    - Nama tonggak diatur ke tanggal yang didikte berdasarkan frekuensi faktur.
    - Tanggal tonggak diatur ke tanggal yang didikte berdasarkan frekuensi faktur.
    - Jumlah tonggak dihitung dengan membagi jumlah kuotasi pada baris kuotasi berbasis proyek berdasarkan jumlah tonggak yang didikte oleh frekuensi dan awal penagihan dan tanggal pengiriman yang diminta.
    - Jika baris kuotasi juga memiliki jumlah pajak yang diperkirakan, nilai ini terbagi antara setiap tonggak dengan setara saat menghasilkan tonggak periodik.

### <a name="manually-create-milestones"></a>Buat tonggak secara manual

Tonggak harga tetap juga dapat dihasilkan secara manual saat tidak dibagi secara berkala. Untuk membuat tonggak secara manual:

Buka baris kuotasi harga tetap yang Anda perlukan untuk membuat tonggaknya. Pada tab **jadwal faktur**, pada subkisi, pilih **+ buat tonggak pencapaian baris kuotasi baru** dan masukkan informasi yang diperlukan berdasarkan tabel berikut.

| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Nama Tonggak | Buat cepat | Nama tonggak. | Ini disebarkan ke tonggak baris kontrak proyek dan ke faktur |
| Tugas Proyek | Buat cepat | Jika tonggak terkait dengan tugas proyek, Anda dapat menggunakan referensi ini untuk menambahkan logika kustom untuk mengatur status tonggak berdasarkan status tugas. | Aplikasi ini tidak memiliki dampak hilir terkait referensi ini untuk tugas. |
| Tanggal tonggak | Buat cepat | Atur tanggal untuk proses pembuatan faktur otomatis mencari status tonggak ini untuk dipertimbangkan untuk faktur. | Ini disebarkan ke tonggak baris kontrak proyek dan ke faktur. |
| Status faktur | Buat cepat | Bila tonggak dibuat, status ini selalu diatur ke **tidak siap untuk faktur**. | Ini disebarkan ke tonggak baris kontrak proyek dan ke faktur. |
| Jumlah Baris | Buat cepat | Jumlah atau nilai tonggak yang akan ditagih kepada pelanggan. | Ini disebarkan ke tonggak baris kontrak proyek dan ke faktur. |
| Pajak | Buat cepat | Jumlah pajak yang akan diterapkan ke tonggak. | Ini disebarkan ke tonggak baris kontrak proyek dan ke faktur. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]