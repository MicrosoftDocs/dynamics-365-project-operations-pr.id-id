---
title: Buat jadwal faktur di baris kontrak berbasis proyek - lite
description: Artikel ini menyediakan informasi tentang membuat jadwal dan pencapaian faktur.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 403b993c3f61ca5f0fb1bac45331aa0613d16439
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921122"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Buat jadwal faktur di baris kontrak berbasis proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Andadapat melampirkan jadwal faktur di baris kontrak berbasis proyek. Faktur hanya diizinkan setelah kontrak dimenangkan untuk membuat kontrak proyek. Jadwal faktur memungkinkan faktur draf untuk baris kontrak berbasis proyek dibuat secara otomatis. Jika Anda berencana untuk selalu membuat faktur secara manual, Anda dapat melewatkan pembuatan jadwal faktur pada baris kontrak berbasis proyek atau baris kontrak.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Membuat jadwal faktur material dan waktu untuk baris kontrak berbasis proyek

Bila baris kontrak berbasis proyek memiliki metode penagihan waktu dan material, Anda dapat membuat jadwal faktur berdasarkan tanggal. Untuk secara otomatis membuat jadwal faktur berdasarkan tanggal, selesaikan langkah-langkah berikut.

1. Buka **pengaturan** > **frekuensi faktur** untuk mengkonfigurasi frekuensi faktur.
2. Buka kontrak proyek dan pada tab **ringkasan**, atur tanggal pengiriman yang diminta.
3. Buka baris kontrak waktu dan material yang diinginkan untuk dibuat jadwal faktur berdasarkan tanggalnya. 
4. Pada tab **jadwal faktur**, pilih tanggal mulai penagihan dan frekuensi faktur. 
5. Pada subkisi, pilih **buat jadwal faktur**.

    Sistem menghasilkan jadwal faktur dengan informasi bidang berikut:

    - **Tanggal Jalankan faktur** diatur ke tanggal berdasarkan frekuensi faktur.
    - **Tanggal batas transaksi** diatur ke hari sebelum **tanggal Jalankan faktur**.
    - **Status Jalankan** diatur secara otomatis ke **tidak berjalan**. Ketika pekerjaan pembuatan faktur otomatis berjalan untuk **Tanggal Jalankan faktur** tertentu, bidang ini diperbarui ke **berhasil menjalankan** atau **gagal menjalankan**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Membuat jadwal faktur harga tetap untuk baris kontrak berbasis proyek

Bila baris kontrak berbasis proyek memiliki metode penagihan harga tetap, Anda dapat membuat jadwal faktur berbasis tonggak pencapaian. Selesaikan langkah-langkah berikut untuk secara otomatis menghasilkan jadwal faktur berdasarkan tonggak pencapaian untuk rangkaian tonggak pencapaian tetap yang didistribusikan secara merata untuk periode kalender.

1. Buka **pengaturan** > **frekuensi faktur** untuk mengkonfigurasi frekuensi faktur.
2. Buka kontrak proyek dan pada tab **ringkasan**, atur tanggal pengiriman yang diminta.
3. Buka baris kontrak harga tetap yang Anda butuhkan untuk membuat jadwal tonggak pencapaian. 
4. Pada tab **jadwal faktur (tonggak pencapaian penagihan)**, pilih tanggal mulai penagihan dan frekuensi faktur. 
5. Pada subkisi, pilih **buat tonggak periode**.

    Sistem menghasilkan jadwal faktur dengan informasi tonggak pencapaian berikut.

    - **Nama tonggak pencapaian** diatur ke tanggal yang didikte berdasarkan frekuensi faktur.
    - **Tanggal tonggak pencapaian** diatur ke tanggal yang didikte berdasarkan frekuensi faktur.
    - **Jumlah tonggak pencapaian** dihitung dengan membagi jumlah kontrak pada baris kontrak berbasis proyek berdasarkan jumlah tonggak pencapaian yang didikte berdasarkan frekuensi, mulai penagihan, dan tanggal pengiriman yang diminta.
    - Jika baris kontrak memiliki nilai di bidang **perkiraan jumlah pajak**, bidang ini juga dibagikan ke setiap tonggak pencapaian secara merata saat membuat tonggak periodik.

Tonggak pencapaian penagihan harus sama dengan nilai kontrak baris kontrak berbasis proyek. Jika tidak sama, kesalahan terjadi. Anda dapat memperbaiki kesalahan tersebut dengan memverifikasi bahwa tonggak pencapaian penagihan mentotalkan nilai kontrak baris dengan membuat, mengedit, atau menghapus tonggak pencapaian. Setelah perubahan dibuat, segarkan halaman.

### <a name="manually-create-milestones"></a>Buat tonggak secara manual

Tonggak pencapaian harga tetap dapat dihasilkan secara manual saat mereka tidak terbagi secara berkala. Untuk membuat tonggak pencapaian secara manual, selesaikan langkah berikut.

1. Buka baris kontrak harga tetap yang Anda butuhkan untuk membuat tonggak pencapaiannya. 
2. Pada tab **jadwal faktur**, pada subkisi, pilih **+ buat tonggak pencapaian baris kontrak baru**.
3. Pada formulir **pembuatan tonggak pencapaian**, masukkan informasi yang diperlukan berdasarkan tabel berikut. 

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| Nama Tahap | Buat Cepat | Bidang teks untuk nama tonggak. | Bidang ini disertakan dalam tonggak pencapaian baris kontrak proyek dan faktur. |
| Tugas Proyek | Buat Cepat | Jika tonggak pencapaian terkait dengan tugas proyek, gunakan referensi ini untuk menambahkan logika kustom dan menetapkan status tonggak pencapaian berdasarkan status tugas. | Tidak ada dampak hilir referensi ini terhadap tugas. |
| Tanggal Tahap | Buat Cepat | Tanggal saat proses pembuatan faktur otomatis akan mencari status tonggak ini untuk dipertimbangkan untuk faktur. | Ini disertakan dalam tonggak pencapaian baris kontrak proyek dan faktur. |
| Status Faktur | Buat Cepat | Saat tonggak dibuat, status ini selalu diatur ke **tidak siap untuk faktur** atau **tidak dimulai**. | Ini disertakan dalam tonggak pencapaian baris kontrak proyek dan faktur. |
| Jumlah Baris | Buat Cepat | Jumlah atau nilai tonggak pencapaian yang akan ditagih kepada pelanggan. | Bidang ini disertakan dalam tonggak pencapaian baris kontrak proyek dan faktur, |
| Pajak | Buat Cepat | Jumlah pajak yang berlaku pada tonggak. | Ini disertakan dalam tonggak pencapaian baris kontrak proyek dan faktur. |

4. Pilih **Simpan dan Tutup**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]