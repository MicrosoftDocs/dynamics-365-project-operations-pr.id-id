---
title: Mengelola beberapa pelanggan pada kontrak proyek - lite
description: Topik ini menyediakan informasi tentang mengelola beberapa pelanggan pada kontrak proyek.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181321"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Mengelola beberapa pelanggan pada kontrak proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Kontrak proyek di Dynamics 365 Project Operations mendukung skenario di mana perjanjian kontraktual melibatkan beberapa pelanggan yang mendanai transaksi. Tab **ringkasan** pada halaman **kontrak proyek** mencakup bidang **pelanggan**. Bidang ini mengidentifikasi pelanggan utama dari transaksi. Pelanggan lain untuk transaksi dapat diatur pada tab **pelanggan** pada halaman **kontrak proyek**.

Semua pelanggan kontrak yang tercantum pada tab pelanggan pada kontrak proyek di-default sebagai pelanggan baris kontrak berbasis proyek baru yang dibuat untuk kontrak proyek. Baris kontrak berbasis proyek yang ada tidak mewarisi pelanggan kontrak baru saat rekaman baru dibuat.

Baris kontrak berbasis produk secara otomatis terkait dengan pelanggan utama.

Pelanggan kontrak dan pelanggan baris kontrak dapat ditambahkan, diperbarui, atau dihapus kapan pun sebelum kontrak dimenangkan.

## <a name="primary-customer"></a>Primary Customer

Pelanggan yang tercantum pada tab **ringkasan** pada kontrak proyek sebagai calon pelanggan adalah pelanggan utama kontrak. Saat Anda mencoba menghapus pelanggan utama dari daftar pelanggan pada kontrak, Anda akan menerima pesan kesalahan bahwa rekaman pelanggan utama pada kontrak tidak dapat dihapus.

Pelanggan utama tidak dapat diperbarui dari daftar pelanggan kontrak. Namun, Ubah calon pelanggan pada tab **ringkasan** kontrak. Bila bidang ini diperbarui pada halaman **ringkasan kontrak**, pelanggan baru akan ditambahkan sebagai pelanggan kontrak baru dengan rangkaian bendera **utama**. Pelanggan utama sebelumnya akan tetap menjadi pelanggan pada kontrak.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Membuat, memperbarui, atau menghapus rekaman pelanggan kontrak

Pelanggan kontrak dapat dibuat, diperbarui, atau dihapus dari tab **pelanggan** pada halaman **kontrak proyek**. Bidang pada tabel berikut ada pada rekaman pelanggan kontrak dari kontrak proyek dan harus diingat saat Anda bekerja dengan kontrak.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| **Akun** | Kisi dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Daftar semua akun aktif. Bidang ini dikunci setelah rekaman dibuat. Untuk memperbarui akun, Hapus rekaman, dan buat lagi. Jika Anda telah merekam setiap aktual, atau jika rekaman pelanggan kontrak adalah pelanggan utama, Anda tidak dapat menghapus rekaman. | Pelanggan kontrak disalin sebagai pelanggan baris kontrak saat baris kontrak dibuat. |
| **Persentase Split Penagihan** | Kisi dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Mewakili persentase setiap transaksi penjualan yang tidak ditagih yang akan dikaitkan ke pelanggan kontrak ini. | Disalin ke baris kontrak baru dan untuk pelanggan proyek baris kontrak pada baris kontrak proyek baru. |
| **Tagih ke Nama Kontak** | Kisi dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Bidang teks ini harus digunakan untuk mengidentifikasi orang kontak faktur untuk pelanggan ini. Bidang ini di-default dari rekaman akun terkait. | Disalin ke bidang **Ditagih ke nama kontrak** pada faktur yang dibuat untuk pelanggan ini. |
| **Nama Penagihan** | Kisi dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak | Bidang teks ini harus digunakan untuk mengidentifikasi orang kontak faktur untuk pelanggan ini. Bidang ini di-default dari rekaman akun terkait. | Disalin ke bidang **Ditagih ke nama kontrak** pada faktur yang dibuat untuk pelanggan ini. |
| **Ketentuan Pembayaran** | Kisi dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Nilai ini di-default dari rekaman akun terkait. | Disalin ke bidang **Ditagih ke nama kontrak** pada faktur yang dibuat untuk pelanggan ini. |
| **Adalah Pembulatan** | Kisi dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Menunjukkan jika pelanggan ini adalah pelanggan pembulatan default untuk transaksi ini. Hanya dapat ada satu pelanggan pembulatan pada kontrak proyek. | Bila pemecahan biaya dan penjualan yang belum ditagih pada kuantitas menyebabkan perbedaan pembulatan, selisih itu diterapkan pada aktual yang dipetakan untuk pelanggan ini. |
| **Batas Jangan terlampaui** | Kisi dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak | Menunjukkan jika ada batas atau pagu negosiasi untuk jumlah keseluruhan yang akan ditagih ke pelanggan untuk kesepakatan ini. | **Batas yang tidak boleh dilewati** yang diatur pada tingkat pelanggan kontrak akan dievaluasi pada **aktual penjualan yang belum ditagih** yang merujuk pada pelanggan kontrak ini. |

## <a name="edit-billing-split-percentages"></a>Mengedit persentase pembagian penagihan

Persentase pemecahan penagihan dapat diedit dengan pengalaman pengeditan kisi inline. Bila persentase pemecahan penagihan tidak berjumlah Total 100 persen, kesalahan akan terjadi. Setelah Anda mengedit persentase pemecahan penagihan, segarkan halaman untuk menghilangkan kesalahan.

Anda juga dapat memilih **mendistribusikan secara merata** pada subkisi **pelanggan kontrak** untuk mengalokasikan pemecahan tagihan secara merata ke semua pelanggan kontrak. Jika ada faktor pembulatan, maka akan ditambahkan ke pelanggan pembulatan. Salah satu dari pelanggan kontrak selalu ditandai sebagai pelanggan **pembulatan**, yang berarti bahwa rekaman pelanggan kontrak memiliki rangkaian bendera pembulatan yang diatur ke **ya**. Biasanya, ini adalah pelanggan utama kontrak, namun juga dapat diubah.
