---
title: Kelola Prospek (Pro)
description: Topik ini menyediakan informasi tentang mengeluarkan prospek berbasis proyek (Pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896330"
---
# <a name="manage-leads-pro"></a>Kelola Prospek (Pro)

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Prospek berbasis proyek dapat dikelola dan terkualifikasi dalam Project Operations. Proses manajemen prospek mencakup pembuatan prospek berbasis pekerjaan dan mengkualifikasi prospek tersebut. 

## <a name="list-of-project-sales-leads"></a>Daftar Prospek Penjualan proyek

Di Bagian **penjualan**, di panel navigasi kiri, buka halaman daftar **prospek** untuk melihat daftar semua rekaman prospek di sistem. Daftar prospek yang ditampilkan adalah berbasis pekerjaan dan jenis prospek lain yang dapat dibuat jika Anda juga memiliki aplikasi Dynamics 365 Sales atau Dynamics 365 Field Service.

Anda dapat membuat tampilan terfilter untuk melihat hanya prospek berbasis proyek dengan membuat filter pada nilai **jenis**. Misalnya, Anda dapat memilih untuk hanya menampilkan prospek berbasis pekerjaan.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Membuat prospek baru untuk transaksi berbasis proyek

Bila prospek berbasis proyek memenuhi syarat, peluang dan akun dibuat. Peluang berbasis proyek adalah titik awal untuk aktivitas upaya penjualan dalam fase peluang. Peluang berbasis proyek memiliki kemampuan unik yang diperlukan untuk menjual pekerjaan proyek. Kemampuan ini mencakup:

- Metode penagihan harga tetap serta waktu dan material
- daftar harga efektif Beberapa tanggal untuk sumber daya manusia, pengeluaran, dan material yang ditanggung pada proyek.

Untuk prospek yang memenuhi syarat untuk secara otomatis membuat peluang, Atur atribut **jenis** ke **berbasis pekerjaan** saat Anda membuat prospek. Jika Anda memilih jenis yang berbeda, prospek tidak akan membuat peluang berbasis proyek saat memenuhi syarat. Jika peluang berbasis proyek tidak dibuat, kemampuan khusus proyek tidak akan tersedia di proses penjualan hilir.

Tabel berikut mencakup informasi bidang penting untuk prospek, dan implikasi hilir dari bidang tersebut.

| **Bidang** | **Lokasi** | **Relevansi, tujuan, dan panduan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Topik | Tab Umum | Bidang teks ini dan harus berisi deskripsi singkat tentang penawaran. | Topik prospek akan default sebagai topik peluang, dan nama kuotasi dan kontrak proyek. |
| Tipe | Tab Umum | Bidang rangkaian pilihan ini memiliki pilihan berikut:</br>- berbasis Pekerjaan (tersedia hanya bila Project Operations diinstal)</br>- berbasis item (tersedia hanya bila Project Operations dan Sales diinstal)</br>- Berbasis pemeliharaan layanan (tersedia saat Field Service diinstal) | Bila nilai bidang ini diatur ke **berbasis pekerjaan** di prospek, prospek akan dikualifikasi untuk membuat peluang berbasis proyek. Peluang berbasis proyek diperlukan untuk mengaktifkan semua ekstensi dan fungsi khusus proyek di proses penjualan hilir untuk transaksi ini. |
| Nama depan | Tab Umum | Nama depan kontak prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Nama depan kontak adalah nilai yang ditetapkan di sini. |
| Nama belakang | Tab Umum | Nama belakang kontak prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Nama belakang kontak adalah nilai yang ditetapkan di sini. |
| Perusahaan | Tab Umum | Nama perusahaan pelanggan prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Nama akun yang dibuat adalah nilai yang ditetapkan di sini. |
| Mata uang | Tab rincian | Mata uang pelanggan prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Mata uang akun yang dibuat adalah nilai yang ditetapkan di sini. |

## <a name="qualify-a-new-project-based-lead"></a>Kualifikasi prospek berbasis proyek baru

Prospek yang memiliki nilai **jenis** yang ditetapkan ke **berbasis pekerjaan** disebut prospek berbasis proyek. Bila prospek berbasis proyek memenuhi syarat, berikut ini dibuat:

- Akun yang menggunakan bidang **perusahaan** dari prospek.
- Rekaman kontak yang terkait dengan akun berdasarkan nilai pada bidang **nama depan** dan **nama belakang** pada prospek.
- Peluang berbasis proyek yang bidang **jenis**-nya diatur ke &quot;**berbasis pekerjaan**.

Untuk informasi lebih rinci tentang prospek yang memenuhi syarat, lihat[kualifikasi atau mengkonversi prospek](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Alur proses bisnis untuk transaksi berbasis proyek

Alur proses bisnis berikut didukung untuk transaksi berbasis proyek dalam Project Operations:

- Proses bisnis Prospek ke Peluang
- Proses Penjualan Peluang

Proses bisnis prospek ke peluang mendukung tahapan berikut:

| Nama Tahapan | Entitas yang dipetakan | Fungsi |
| --- | --- | --- |
| Kualifikasi | Prospek | Kualifikasi prospek untuk membuat akun, kontrak, dan peluang. |
| Kembangkan | Peluang | Kembangkan peluang untuk menambahkan informasi lebih lanjut tentang pekerjaan yang terlibat, pemangku kepentingan utama, dan pesaing. |
| Usulkan | Peluang | Kembangkan proposal dan Dapatkan persetujuan dari tim peninjauan internal. |
| Tutup | Peluang | Menangkan peluang untuk menutup penawaran. |
