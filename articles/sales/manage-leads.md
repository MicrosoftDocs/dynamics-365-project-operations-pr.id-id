---
title: Mengelola prospek
description: Artikel ini menyediakan informasi tentang mengelola prospek berbasis proyek.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 080f53ee2f800b8433d055525852f5c2e21aab77
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920202"
---
# <a name="manage-leads"></a>Mengelola prospek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Prospek berbasis proyek dapat dikelola dan terkualifikasi dalam Project Operations. Proses manajemen prospek mencakup pembuatan prospek berbasis pekerjaan dan mengkualifikasi prospek tersebut. 

## <a name="project-sales-leads"></a>Prospek Penjualan proyek

Di Bagian **penjualan**, di panel navigasi kiri, buka halaman daftar **prospek** untuk melihat daftar semua rekaman prospek di sistem. Daftar prospek yang ditampilkan adalah berbasis pekerjaan dan jenis prospek lain yang dapat dibuat jika Anda juga memiliki aplikasi Dynamics 365 Sales atau Dynamics 365 Field Service.

Anda dapat membuat tampilan terfilter untuk melihat hanya prospek berbasis proyek dengan membuat filter pada nilai **jenis**. Misalnya, Anda dapat memilih untuk hanya menampilkan prospek berbasis pekerjaan.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Buat prospek baru untuk transaksi berbasis proyek

Bila prospek berbasis proyek memenuhi syarat, peluang dan akun dibuat. Peluang berbasis proyek adalah titik awal untuk aktivitas upaya penjualan dalam fase peluang. Peluang berbasis proyek memiliki kemampuan unik yang diperlukan untuk menjual pekerjaan proyek. Kemampuan ini mencakup:

- Metode penagihan harga tetap serta waktu dan material
- daftar harga efektif Beberapa tanggal untuk sumber daya manusia, pengeluaran, dan material yang ditanggung pada proyek

Untuk prospek yang memenuhi syarat untuk secara otomatis membuat peluang, Atur atribut **jenis** ke **berbasis pekerjaan** saat Anda membuat prospek. Jika Anda memilih jenis yang berbeda, prospek tidak akan membuat peluang berbasis proyek saat memenuhi syarat. Jika peluang berbasis proyek tidak dibuat, kemampuan khusus proyek tidak akan tersedia di proses penjualan hilir.

Tabel berikut mencakup informasi bidang penting untuk prospek, dan implikasi hilir dari bidang tersebut.
 
| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Topik | Tab Umum | Bidang teks ini harus berisi deskripsi singkat tentang penawaran. | Topik prospek akan default sebagai topik peluang, dan nama kuotasi dan kontrak proyek. |
| Tipe | Tab Umum | Bidang rangkaian pilihan ini memiliki pilihan berikut:</br>- berbasis Pekerjaan (tersedia hanya bila Project Operations diinstal)</br>- berbasis item (tersedia hanya bila Project Operations dan Sales diinstal)</br>- Berbasis pemeliharaan layanan (tersedia saat Field Service diinstal) | Bila nilai bidang ini diatur ke **berbasis pekerjaan** di prospek, prospek akan dikualifikasi untuk membuat peluang berbasis proyek. Peluang berbasis proyek diperlukan untuk mengaktifkan semua ekstensi dan fungsi khusus proyek di proses penjualan hilir untuk transaksi ini. |
| Nama depan | Tab Umum | Nama depan kontak prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Nama depan kontak adalah nilai yang ditetapkan di sini. |
| Nama belakang | Tab Umum | Nama belakang kontak prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Nama belakang kontak adalah nilai yang ditetapkan di sini. |
| Perusahaan | Tab Umum | Nama perusahaan pelanggan prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Nama akun yang dibuat adalah nilai yang ditetapkan di sini. |
| Mata uang | Tab rincian | Mata uang pelanggan prospek | Bila prospek memenuhi syarat, akun, kontrak, dan peluang dibuat. Mata uang akun yang dibuat adalah nilai yang ditetapkan di sini. |

## <a name="qualify-a-new-project-based-lead"></a>Kualifikasi prospek berbasis proyek baru

Prospek yang memiliki nilai **jenis** yang ditetapkan ke **berbasis pekerjaan** disebut prospek berbasis proyek. Bila prospek berbasis proyek memenuhi syarat, berikut ini dibuat:

- Akun yang menggunakan bidang **perusahaan** dari prospek.
- Rekaman kontak yang terkait dengan akun berdasarkan nilai pada bidang **nama depan** dan **nama belakang** pada prospek.
- Peluang berbasis proyek dengan bidang **Jenis** diatur ke **Berbasis pekerjaan**.

Untuk informasi lebih rinci tentang prospek yang memenuhi syarat, lihat [kualifikasi atau mengonversi prospek](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Informasi kualifikasi prospek dan entitas hukum 

Ketika Anda menjalankan Project Operations menggunakan mode penyebaran, Project Operations untuk skenario berbasis sumber daya/non-stok, setiap pelanggan dan peluang harus diatur bidang **perusahaan pemilik**-nya. Perusahaan pemilik adalah entitas hukum di organisasi Anda yang memiliki hasil proyek. Setiap pelanggan, atau akun dengan jenis relasi pelanggan, harus memiliki nilai bidang **perusahaan pemilik** yang diatur ke entitas hukum yang berkontrak dan melakukan negosiasi dengan pelanggan ini. Pelanggan hanya dapat berada di satu entitas hukum.

Bila prospek memenuhi syarat, rekaman pelanggan dan peluang yang dibuat akan memiliki bidang **perusahaan pemilik** yang diatur ke rekaman perusahaan sumber daya dapat dipesan pengguna saat ini.

Jika rekaman sumber daya dapat dipesan pengguna saat ini kosong, maka nilai bidang **perusahaan pemilik** pada rekaman pengguna digunakan untuk default pada rekaman pelanggan dan peluang.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]