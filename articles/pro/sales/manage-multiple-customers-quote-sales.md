---
title: Mengelola beberapa pelanggan pada kuotasi proyek - lite
description: Artikel ini menyediakan informasi tentang menangani kuotasi dengan beberapa pelanggan yang akan mendanai proyek. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 337619e8d8081cdebd73f9336fa9fa99885a0ab2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921076"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Mengelola beberapa pelanggan pada kuotasi proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Kuotasi proyek mendukung skenario di mana proposal melibatkan beberapa pelanggan yang akan mendanai transaksi. Tab **ringkasan** kuotasi memiliki bidang **calon pelanggan** yang mengidentifikasi pelanggan utama dari transaksi. Pelanggan lain untuk transaksi dapat diatur pada tab **pelanggan** dalam kuotasi proyek.

Semua pelanggan kuotasi pada tab **pelanggan** kuotasi proyek memiliki default sebagai pelanggan baris kuotasi pada baris kuotasi berbasis proyek **baru** yang dibuat untuk kuotasi. Setiap baris kuotasi berbasis proyek yang ada tidak akan mewarisi rekaman pelanggan kuotasi baru yang dibuat setelah mereka.

Baris kuotasi berbasis produk secara otomatis terkait dengan pelanggan utama yang juga pelanggan di bidang **calon pelanggan** di tab **ringkasan** kuotasi.

Pelanggan kuotasi dan pelanggan baris kuotasi dapat ditambahkan, diperbarui, atau dihapus kapan pun sebelum kuotasi dimenangkan.

## <a name="concept-of-a-primary-customer"></a>Konsep pelanggan utama

Pelanggan yang ada pada tab ringkasan proyek kuotasi sebagai calon pelanggan adalah pelanggan utama kuotasi. Jika Anda mencoba menghapus pelanggan utama dari daftar pelanggan pada kuotasi, Anda akan melihat kesalahan bahwa rekaman pelanggan utama pada kuotasi tidak dapat dihapus.

Pelanggan utama tidak boleh diperbarui dari daftar pelanggan pada kuotasi. Namun, Anda dapat mempengaruhi pelanggan utama dengan mengubah calon pelanggan di tab **ringkasan** kuotasi. Bila bidang ini diperbarui pada **ringkasan kuotasi**, calon pelanggan yang baru dipilih akan ditambahkan sebagai pelanggan kuotasi baru dengan rangkaian bendera **utama**. Calon pelanggan lama akan tetap menjadi pelanggan pada kuotasi.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Membuat, memperbarui, atau menghapus rekaman pelanggan kuotasi

Pelanggan kuotasi dapat dibuat, diperbarui, atau dihapus dari tab **pelanggan kuotasi** pada halaman **kuotasi**. Bidang yang tercantum dalam tabel berikut ada pada rekaman pelanggan kuotasi dari kuotasi proyek.

| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Akun | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Daftar semua akun aktif. Bidang ini dikunci setelah rekaman dibuat. Jika Anda ingin memperbaruinya, Hapus rekaman, dan buat ulang. Jika Anda telah merekam aktual apa pun, atau jika rekaman pelanggan kuotasi adalah pelanggan utama, Anda tidak akan dibolehkan menghapus rekaman. | Pelanggan kuotasi disalin sebagai pelanggan kuotasi saat baris kuotasi dibuat. Pelanggan kuotasi juga disalin ke pelanggan kontrak proyek saat kuotasi dimenangkan. |
| Persentase pembagian Penagihan | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Menunjukkan persentase setiap transaksi penjualan yang tidak ditagih yang akan dikaitkan dengan pelanggan kuotasi ini. | Disalin ke baris kuotasi baru dan ke pelanggan kontrak proyek. |
| Tagih ke Nama Kontak | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Ini adalah Bidang teks dan harus digunakan untuk mengidentifikasi kontak orang faktur untuk pelanggan ini. Ini akan default dari rekaman akun terkait | Disalin ke pelanggan kontrak proyek ketika kuotasi dimenangkan dan pada bidang tagih ke nama kontrak pada faktur yang dihasilkan untuk pelanggan ini. |
| Tagih ke Nama | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Bidang teks ini harus digunakan untuk mengidentifikasi orang kontak faktur untuk pelanggan ini. | Disalin ke pelanggan kontrak proyek ketika kuotasi dimenangkan dan pada bidang **tagih ke nama kontrak** pada faktur yang dihasilkan untuk pelanggan ini. |
| Ketentuan Pembayaran | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Ini adalah rangkaian pilihan dengan nilai default dari rekaman akun terkait. | Disalin ke pelanggan kontrak proyek ketika kuotasi dimenangkan dan pada bidang **tagih ke nama kontrak** pada faktur yang dihasilkan untuk pelanggan ini. |
| Adalah Pembulatan | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Menunjukkan jika pelanggan ini adalah pelanggan pembulatan default untuk transaksi ini. | Disalin ke pelanggan kontrak proyek saat kuotasi dimenangkan. |
| Batas Jangan terlampaui | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Menunjukkan jika ada batas negosiasi atau batas yang dirundingkan ke jumlah keseluruhan yang akan ditagih ke pelanggan untuk keterlibatan ini | Disalin ke pelanggan kontrak proyek saat kuotasi dimenangkan. |

## <a name="editing-billing-split-percentages"></a>Mengedit persentase pembagian penagihan

Anda dapat mengedit persentase pembagian penagihan dengan menggunakan pengalaman Edit kisi sebaris. Bila persentase pembagian penagihan tidak Total 100%, kesalahan akan terjadi. Setelah memperbarui persentase pembagian penagihan, segarkan halaman untuk menghilangkan kesalahan.

Anda juga dapat mencoba memilih **distribusikan secara merata** pada subkisi pelanggan kuotasi. Tindakan ini mengalokasikan pembagian penagihan ke semua pelanggan kuotasi. Jika ada faktor pembulatan, itu akan ditambahkan ke pelanggan pembulatan. Salah satu pelanggan kuotasi selalu ditandai sebagai pelanggan pembulatan. Ini berarti bahwa rekaman pelanggan kuotasi memiliki bendara **pembulatan** diatur ke **ya**. Biasanya ini adalah pelanggan utama kuotasi, namun dapat diubah.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
