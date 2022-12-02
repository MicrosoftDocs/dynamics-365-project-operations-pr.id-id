---
title: Mengelola beberapa pelanggan pada baris kuotasi berbasis proyek
description: Artikel ini menyediakan informasi tentang cara mengelola beberapa peal pada baris kuotasi berbasis proyek.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0160a7023ff1d5f806b8c01115a48d0552008d15
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928252"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Mengelola beberapa pelanggan pada baris kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Baris kuotasi berbasis proyek mendukung skenario dengan setiap baris kuotasi memiliki daftar pelanggan yang membayarnya. Daftar pelanggan pada baris kuotasi berbasis proyek bisa sama dengan daftar pelanggan pada kuotasi. Anda juga dapat mengubah daftar pelanggan menjadi berbeda. Untuk membuat kontrak proyek akhir saat kuotasi proyek dimenangkan, daftar pelanggan pada baris kuotasi berbasis proyek disalin ke baris kontrak berbasis proyek yang terkait. Pelanggan pada kuotasi berbasis proyek disalin ke kontrak proyek.

Ketika Anda menagih kontrak proyek akhirnya, daftar pelanggan pada baris kontrak berbasis proyek diutamakan di atas daftar pada kontrak proyek. Daftar pelanggan pada kontrak proyek hanya digunakan untuk default baris kontrak proyek baru.

Semua pelanggan kuotasi pada tab **pelanggan** kuotasi proyek memiliki default sebagai pelanggan baris kuotasi pada baris kuotasi berbasis proyek baru yang dibuat untuk kuotasi proyek. Setiap baris kuotasi berbasis proyek yang ada tidak mewarisi rekaman pelanggan kuotasi baru yang dibuat setelah mereka.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Membuat, memperbarui, atau menghapus rekaman pelanggan baris kuotasi

Anda dapat membuat, memperbarui, atau menghapus pelanggan baris kuotasi pada tab **pelanggan baris kuotasi** pada halaman **baris kuotasi berbasis proyek**. Bila Anda menambahkan pelanggan baru pada baris kuotasi berbasis proyek, pelanggan juga ditambahkan ke kuotasi keseluruhan sebagai pelanggan kuotasi, dengan persentase pembagian penagihan default pada kuotasi keseluruhan sebesar 0%. Persentase pembagian penagihan pada kuotasi keseluruhan disalin ke baris kuotasi baru dan kontrak proyek akhirnya. Namun, bila Anda menagih dari kontrak, persentase pembagian penagihan pada tingkat baris kuotasi digunakan, bukan persentase pembagian penagihan pada tingkat kontrak keseluruhan. 

Tabel berikut menampilkan bidang pada pada rekaman pelanggan baris kuotasi dari baris kuotasi berbasis proyek.

| Bidang | Lokasi | Panduan dan deskripsi | Dampak hilir |
| --- | --- | --- | --- |
| **Akun** | Kisi yang dapat diedit pada tab **pelanggan baris kuotasi**, formulir utama, dan formulir Buat Cepat untuk pelanggan baris kuotasi. | Daftar semua akun aktif. Bidang ini dikunci setelah rekaman dibuat. Jika Anda perlu memperbarui bidang, Hapus dan buat ulang rekaman. Jika Anda merekam aktual apa pun, Anda tidak dapat menghapus rekaman. | Bila Anda memilih akun dari daftar induk akun untuk ditambahkan, pelanggan kuotasi juga ditambahkan sebagai pelanggan kuotasi. Pelanggan baris kuotasi juga disalin ke pelanggan baris kontrak proyek saat kuotasi dimenangkan. |
| **Persentase pembagian Penagihan** | Kisi yang dapat diedit pada tab **pelanggan baris kuotasi**, formulir utama, dan formulir Buat Cepat untuk pelanggan baris kuotasi. | Menunjukkan persentase setiap transaksi penjualan yang tidak ditagih yang akan dikaitkan dengan pelanggan baris kuotasi ini. | Disalin ke Pelanggan Baris Kontrak Proyek. |
| **Batas Jangan terlampaui** | Kisi yang dapat diedit pada tab **pelanggan baris kuotasi**, formulir utama, dan formulir Buat Cepat untuk pelanggan baris kuotasi. | Menunjukkan apakah ada batas negosiasi atau batas yang dirundingkan ke jumlah keseluruhan yang akan ditagih ke pelanggan untuk baris kuotasi ini. | Disalin ke pelanggan baris kontrak proyek saat kuotasi dimenangkan. |
| **Perusahaan Pemilik** | Kisi yang dapat diedit pada tab **pelanggan baris kuotasi**, formulir utama, dan formulir Buat Cepat untuk pelanggan baris kuotasi, | Entitas hukum pengaturan pelanggan ini dalam modul **manajemen proyek dan akuntansi**. Bidang ini hanya baca dan diatur ke perusahaan pemilik kuotasi itu sendiri. Daftar Pelanggan yang akan ditambahkan di bidang **akun** sudah difilter ke daftar dari perusahaan pemilik ini di modul **manajemen proyek dan akuntansi** Project Operations. | Perusahaan pemilik setara dengan konsep entitas hukum. Semua biaya dan pendapatan yang Diperoleh dari proyek ini diperhitungkan dalam buku besar perusahaan pemilik. |
| **Adalah Pembulatan** | Kisi yang dapat diedit pada tab **pelanggan baris kuotasi**, formulir utama, dan formulir Buat Cepat untuk pelanggan baris kuotasi. | Menunjukkan apakah pelanggan ini adalah pelanggan pembulatan default untuk baris kuotasi berbasis proyek ini. | Disalin ke pelanggan kontrak proyek saat kuotasi dimenangkan. |

## <a name="edit-billing-split-percentages"></a>Mengedit persentase pembagian penagihan

Anda dapat mengedit persentase pembagian penagihan secara in-line. Bila persentase pembagian penagihan tidak Total 100%, kesalahan akan terjadi. Setelah mengedit persentase pembagian penagihan, segarkan halaman baris kuotasi untuk menghilangkan kesalahan.

Gunakan tindakan mendistribusikan merata pada subkisi pelanggan baris kuotasi untuk mengalokasikan pembagian penagihan ke semua pelanggan baris kuotasi. Jika ada faktor pembulatan, itu akan ditambahkan ke pelanggan pembulatan. Salah satu pelanggan kuotasi selalu ditandai sebagai pelanggan pembulatan, yang berarti rekaman pelanggan baris kuotasi memiliki peringatan tentang pembulatan yang diatur ke **ya**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]