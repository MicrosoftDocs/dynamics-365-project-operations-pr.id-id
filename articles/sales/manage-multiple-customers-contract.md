---
title: Mengelola beberapa pelanggan pada kontrak proyek
description: Artikel ini berisi informasi tentang cara mengelola beberapa pelanggan pada suatu kontrak proyek.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928344"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Mengelola beberapa pelanggan pada kontrak proyek

Artikel ini berisi informasi tentang cara mengelola beberapa pelanggan pada suatu kontrak proyek. Anda dapat menggunakan kontrak proyek saat perjanjian kontrak untuk beberapa pelanggan diperlukan untuk mendanai transaksi. Pada halaman **Kontrak Proyek**, tab **Rangkuman** berisi informasi tentang pelanggan utama untuk transaksi. Pelanggan lain yang berpartisipasi dalam transaksi dapat ditambahkan ke tab **Pelanggan**.

Semua pelanggan kontrak pada tab **Pelanggan** kontrak proyek merupakan default pelanggan baris kontrak pada setiap baris kontrak berbasis proyek baru yang dibuat untuk kontrak proyek. Setiap baris kontrak berbasis proyek yang ada tidak mewarisi record pelanggan kontrak baru yang dibuat kemudian.

Anda dapat menambahkan, memperbarui, atau menghapus kontrak dan pelanggan baris kontrak kapan pun sebelum kontrak dimenangkan. Pelanggan pada kontrak proyek harus diatur sebagai pelanggan di perusahaan pemilik atau entitas hukum pada halaman **Pelanggan**. Entitas hukum diatur dalam modul **Manajemen dan akuntansi proyek** Dynamics 365 Project Operations dan tersedia sebagai perusahaan pada modul **Penjualan** dan **Penyerahan Proyek** di Project Operations.

## <a name="primary-customers"></a>Pelanggan utama

Calon pelanggan pada tab **Rangkuman** kontrak proyek merupakan pelanggan utama untuk kontrak tersebut. Anda tidak dapat memperbarui pelanggan utama dari daftar pelanggan kontrak. Jika Anda mencoba menghapus pelanggan utama dari daftar pelanggan pada kontrak, pesan kesalahan akan muncul bahwa record pelanggan utama pada kontrak tidak dapat dihapus. Atau, ubah pelanggan di bidang **Calon Pelanggan** pada tab **Rangkuman** kontrak proyek. Saat Anda memperbarui bidang ini, pelanggan yang baru dipilih akan ditambahkan sebagai pelanggan kontrak baru dengan tanda **Utama** diatur ke **Ya**. Pelanggan utama sebelumnya masih merupakan pelanggan pada kontrak tersebut, namun mereka tidak lagi menjadi pelanggan utama.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Membuat, memperbarui, atau menghapus rekaman pelanggan kontrak

Anda dapat membuat, memperbarui, atau menghapus pelanggan kontrak dari tab **Pelanggan Kontrak** pada halaman **Kontrak**. Bidang berikut disertakan di record pelanggan kontrak dari suatu kontrak proyek.

| **Bidang** | **Lokasi** | **Deskripsi** | 
| --- | --- | --- | 
| Akun | Kisi yang dapat diedit pada tab **Pelanggan Kontrak** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak. | Daftar semua akun aktif. Bidang ini dikunci setelah rekaman dibuat. Untuk memperbarui record, Anda harus menghapusnya, lalu membuatnya kembali. Jika Anda telah merekam setiap aktual, atau jika rekaman pelanggan kontrak adalah pelanggan utama, Anda tidak dapat menghapus rekaman. Saat baris kontrak dibuat, pelanggan kontrak disalin sebagai pelanggan baris kontrak. |
| Persentase Split Penagihan | Kisi yang dapat diedit pada tab **Pelanggan Kontrak** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak. | Mewakili persentase setiap transaksi penjualan yang belum ditagih yang akan dikaitkan ke pelanggan kontrak. Saat baris kontrak proyek baru dibuat, persen penagihan terpisah disalin ke baris kontrak baru yang dibuat dan ke pelanggan baris kontrak proyek. |
| Tagih ke Nama Kontak | Kisi yang dapat diedit pada tab **Pelanggan Kontrak** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak. | Bidang teks ini harus digunakan untuk mengidentifikasi kontak pengguna faktur untuk pelanggan. Nilai default ditentukan dari record akun terkait. Nama kontak disalin ke **Tagih ke Nama Kontrak** pada faktur yang dibuat untuk pelanggan tersebut. |
| Nama Penagihan | Kisi yang dapat diedit pada tab **Pelanggan Kontrak** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak. | Gunakan bidang ini untuk mengidentifikasi kontak pengguna faktur untuk pelanggan. Nilai default ditentukan dari record akun terkait. Nama disalin pada bidang **Tagih ke Nama Kontrak** pada faktur yang dibuat untuk pelanggan. |
| Ketentuan Pembayaran | Kisi yang dapat diedit pada tab **Pelanggan Kontrak** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak. | Nilai default ditentukan dari record akun terkait. Persyaratan disalin melalui **Tagih ke Nama Kontrak** pada faktur yang dibuat untuk pelanggan tersebut. |
| Perusahaan Pemilik | Kisi yang dapat diedit pada tab **Pelanggan Kontrak Proyek** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak proyek. | Entitas hukum tempat pelanggan mengonfigurasikan modul **Manajemen dan akuntansi proyek**. Bidang ini hanya baca dan diatur ke perusahaan pemilik kontrak proyek.</br>Daftar Pelanggan yang akan ditambahkan di bidang **akun** sudah difilter ke daftar dari perusahaan pemilik ini di modul **manajemen proyek dan akuntansi** Project Operations. Perusahaan pemilik sama dengan entitas hukum di modul **Manajemen dan akuntansi proyek** dari Project Operations. Semua biaya dan pendapatan yang Diperoleh dari proyek ini diperhitungkan dalam buku besar perusahaan pemilik. |
| Adalah Pembulatan | Kisi yang dapat diedit pada tab **Pelanggan Kontrak** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak. | Menunjukkan apakah pelanggan merupakan pelanggan pembulatan default untuk transaksi. Hanya dapat ada satu pelanggan pembulatan pada kontrak proyek. Bila pemecahan biaya dan penjualan yang belum ditagih pada kuantitas dan menyebabkan perbedaan pembulatan, selisih tersebut diterapkan pada aktual yang dipetakan ke pelanggan ini. |
| Batas Jangan terlampaui | Kisi yang dapat diedit pada tab **Pelanggan Kontrak** dan halaman utama serta halaman yang dibuat dengan cepat untuk pelanggan kontrak. | Menunjukkan apakah terdapat batas atau pagu negosiasi untuk jumlah keseluruhan yang akan ditagih ke pelanggan untuk kesepakatan ini. Batas yang tidak boleh dilewati yang diatur pada tingkat pelanggan kontrak akan dievaluasi berdasarkan pada aktual penjualan yang belum ditagih yang merujuk pada pelanggan kontrak ini. |

## <a name="edit-billing-split-percentages"></a>Mengedit persentase pembagian penagihan

Anda dapat mengedit persentase pemecahan penagihan dengan mengedit di kisi. Apabila jumlah persentase pemecahan penagihan tidak sama dengan 100 persen, kesalahan terjadi. Setelah Anda mengedit persentase pemecahan, segarkan halaman **Kontrak Proyek** untuk menghapus kesalahan.

Anda juga dapat memilih **Distribusikan Secara Merata** pada subkisi pelanggan kontrak proyek. Pemecahan penagihan dialokasikan secara merata ke semua pelanggan pada kontrak proyek. Jika terdapat faktor pembulatan, faktor tersebut akan ditambahkan ke pelanggan pembulatan. Salah satu pelanggan kontrak selalu memiliki tanda **Pembulatan** yang diatur ke **Ya**. Pelanggan tersebut adalah pelanggan pembulatan. Biasanya, pelanggan pembulatan juga merupakan pelanggan utama kontrak, namun itu tidak diperlukan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]