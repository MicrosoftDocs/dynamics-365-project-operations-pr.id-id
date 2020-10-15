---
title: Kelola beberapa pelanggan pada kuotasi proyek
description: Topik ini menyediakan informasi tentang menangani kuotasi yang melibatkan beberapa pelanggan yang akan mendanai proyek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908258"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Kelola beberapa pelanggan pada kuotasi proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kuotasi proyek mendukung skenario di mana proposal melibatkan beberapa pelanggan yang akan mendanai transaksi. Tab **ringkasan** kuotasi memiliki bidang **calon pelanggan** yang mengidentifikasi pelanggan utama dari transaksi. Pelanggan lain untuk transaksi dapat diatur pada tab **pelanggan** dalam kuotasi proyek.

Semua pelanggan kuotasi pada tab **pelanggan** kuotasi proyek memiliki default sebagai pelanggan baris kuotasi pada baris kuotasi berbasis proyek **baru** yang dibuat untuk kuotasi. Setiap baris kuotasi berbasis proyek yang ada tidak akan mewarisi rekaman pelanggan kuotasi baru yang dibuat setelah mereka.

Pelanggan kuotasi dan pelanggan baris kuotasi dapat ditambahkan, diperbarui, atau dihapus kapan pun sebelum kuotasi dimenangkan. Pelanggan yang valid dalam kuotasi harus diatur sebagai pelanggan di perusahaan pemilik atau entitas hukum pada halaman **pelanggan**. Entitas hukum dikonfigurasi di modul **manajemen proyek dan akuntansi** dari Dynamics 365 Project Operations dan dibuat tersedia sebagai perusahaan dalam modul **penjualan dan pengiriman proyek** dari Project Operations.

## <a name="concept-of-a-primary-customer"></a>Konsep pelanggan utama

Pelanggan yang terdaftar pada tab **ringkasan** proyek kuotasi sebagai calon pelanggan adalah pelanggan utama kuotasi. Jika Anda mencoba menghapus pelanggan utama dari daftar pelanggan pada kuotasi, Anda akan menerima kesalahan bahwa rekaman pelanggan utama pada kuotasi tidak dapat dihapus.

Pelanggan utama tidak boleh diperbarui dari daftar pelanggan pada kuotasi. Namun, Anda dapat mempengaruhi pelanggan utama dengan mengubah calon pelanggan di tab **ringkasan** kuotasi. Bila bidang ini diperbarui pada **ringkasan kuotasi**, calon pelanggan yang baru dipilih akan ditambahkan sebagai pelanggan kuotasi baru dengan rangkaian bendera **utama**. Calon pelanggan lama akan tetap menjadi pelanggan pada kuotasi.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Membuat, memperbarui, atau menghapus rekaman pelanggan kuotasi

Pelanggan kuotasi dapat dibuat, diperbarui, atau dihapus dari tab **pelanggan kuotasi** pada halaman **kuotasi**. Bidang yang tercantum dalam tabel berikut ada pada rekaman pelanggan kuotasi dari kuotasi proyek.

| **Bidang** | **Lokasi** | **Relevansi, tujuan, dan panduan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Akun | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Daftar semua akun aktif. Bidang ini dikunci setelah rekaman dibuat. Jika Anda ingin memperbaruinya, Hapus rekaman, dan buat ulang. Jika Anda telah merekam setiap aktual, atau jika rekaman pelanggan kuotasi adalah pelanggan utama, Anda akan diizinkan untuk menghapus rekaman. | Pelanggan kuotasi disalin sebagai pelanggan kuotasi saat baris kuotasi dibuat. Pelanggan kuotasi juga disalin ke pelanggan kontrak proyek saat kuotasi dimenangkan. |
| Persentase pembagian Penagihan | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Menunjukkan persentase setiap transaksi penjualan yang tidak ditagih yang akan dikaitkan dengan pelanggan kuotasi ini. | Disalin ke baris kuotasi baru yang dibuat dan ke pelanggan kontrak proyek. |
| Tagih ke Nama Kontak | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Ini adalah Bidang teks dan harus digunakan untuk mengidentifikasi kontak orang faktur untuk pelanggan ini. Ini akan default dari rekaman akun terkait | Disalin ke pelanggan kontrak proyek ketika kuotasi dimenangkan dan pada bidang tagih ke nama kontrak pada faktur yang dihasilkan untuk pelanggan ini. |
| Tagih ke Nama | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Bidang teks ini harus digunakan untuk mengidentifikasi orang kontak faktur untuk pelanggan ini. | Disalin ke pelanggan kontrak proyek ketika kuotasi dimenangkan dan pada bidang **tagih ke nama kontrak** pada faktur yang dihasilkan untuk pelanggan ini. |
| Ketentuan Pembayaran | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Ini adalah rangkaian pilihan dengan nilai default dari rekaman akun terkait. | Disalin ke pelanggan kontrak proyek ketika kuotasi dimenangkan dan pada bidang **tagih ke nama kontrak** pada faktur yang dihasilkan untuk pelanggan ini. |
| Adalah Pembulatan | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Menunjukkan jika pelanggan ini adalah pelanggan pembulatan default untuk transaksi ini. | Disalin ke pelanggan kontrak proyek saat kuotasi dimenangkan. |
| Perusahaan Pemilik | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Entitas hukum yang diatur oleh pelanggan ini dalam modul **manajemen proyek dan akuntansi**. Bidang ini hanya baca dan diatur ke perusahaan pemilik kuotasi itu sendiri. Daftar Pelanggan yang akan ditambahkan di bidang **akun** sudah difilter ke daftar dari perusahaan pemilik ini di modul **manajemen proyek dan akuntansi** Project Operations. | Perusahaan pemilik setara dengan konsep entitas hukum dalam modul **manajemen proyek dan akuntansi** Project Operations. Semua biaya dan pendapatan yang Diperoleh dari proyek ini diperhitungkan dalam buku besar perusahaan pemilik, |
| Batas Jangan terlampaui | Kisi yang dapat diedit pada tab **pelanggan kuotasi** dan formulir **utama** dan **Buat Cepat** untuk pelanggan kuotasi. | Menunjukkan jika ada batas negosiasi atau batas yang dirundingkan ke jumlah keseluruhan yang akan ditagih ke pelanggan untuk keterlibatan ini. | Disalin ke pelanggan kontrak proyek saat kuotasi dimenangkan. |

## <a name="editing-billing-split-percentages"></a>Mengedit persentase pembagian penagihan

Anda dapat mengedit persentase pembagian penagihan dengan menggunakan pengalaman Edit kisi sebaris. Bila persentase pembagian penagihan tidak Total 100%, kesalahan akan terjadi. Setelah memperbarui persentase pembagian penagihan, segarkan halaman untuk menghilangkan kesalahan.

Anda juga dapat mencoba memilih **mendistribusikan** secara merata pada subkisi pelanggan kuotasi. Tindakan ini mengalokasikan pembagian penagihan ke semua pelanggan kuotasi. Jika ada faktor pembulatan, itu akan ditambahkan ke pelanggan pembulatan. Salah satu pelanggan kuotasi selalu ditandai sebagai pelanggan pembulatan. Ini berarti bahwa rekaman pelanggan kuotasi memiliki bendara **pembulatan** diatur ke **ya**. Biasanya ini adalah pelanggan utama kuotasi, namun dapat diubah.