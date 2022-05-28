---
title: Mengelola beberapa pelanggan pada baris kontrak berbasis proyek
description: Topik ini menyediakan informasi tentang bekerja dengan baris kontrak dan kontrak yang berisi beberapa pelanggan.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1efa9e5b5ad432e1564fb3d8db0405134a4dc73
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584922"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Mengelola beberapa pelanggan pada baris kontrak berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Baris kontrak berbasis proyek dapat mencakup daftar pelanggan yang bertanggung jawab atas pembayaran. Daftar pelanggan pada baris kontrak berbasis proyek ini dapat sama dengan daftar pelanggan pada kontrak, namun tidak wajib. Bila kuotasi proyek dimenangkan, dan kontrak proyek dibuat, daftar pelanggan pada baris kuotasi akan disalin ke baris kontrak yang sesuai. Pelanggan pada kuotasi akan disalin ke kontrak.

Bila kontrak proyek ditagih, daftar pelanggan pada baris kontrak berbasis proyek akan diprioritaskan berdasarkan daftar pelanggan pada kontrak. Daftar pelanggan pada kontrak proyek hanya digunakan untuk baris kontrak baru default.

Semua pelanggan kontrak pada tab **pelanggan** pada kontrak proyek di-default sebagai pelanggan baris kontrak pada baris kontrak baru yang dibuat untuk kontrak proyek. Baris kontrak yang ada tidak akan mewarisi rekaman pelanggan kontrak baru yang dibuat setelah mereka.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Membuat, memperbarui, atau menghapus rekaman pelanggan baris kontrak

Anda dapat membuat, memperbarui, atau menghapus pelanggan baris kontrak dari tab **pelanggan baris kontrak** pada halaman **baris kontrak berbasis proyek**. Bila pelanggan baru ditambahkan pada baris kontrak berbasis proyek, mereka juga ditambahkan pada kontrak keseluruhan sebagai pelanggan kontrak dengan pemecahan penagihan default nol persen. Persentase pemecahan penagihan pada kontrak keseluruhan disalin ke baris kontrak baru dan ke kontrak proyek akhirnya. Namun, saat menagih dengan faktur dari kontrak, persentase pemecahan penagihan pada tingkat baris kontraklah yang digunakan dan bukan persentase pemecahan penagihan pada tingkat kontrak keseluruhan. 

Di bawah ini adalah bidang pada rekaman pelanggan baris kontrak dari baris kontrak berbasis proyek yang perlu diingat saat Anda bekerja dengannya:

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| Akun | Kisi yang dapat diedit pada tab **pelanggan baris kontrak** dan formulir buat cepat dan utama untuk pelanggan baris kontrak | Semua Akun Aktif. Bidang ini dikunci setelah rekaman dibuat. Untuk memperbarui bidang, Hapus rekaman, dan buat rekaman baru. Jika Anda telah merekam aktual, Anda tidak dapat menghapus rekaman. Namun, Anda dapat menandai persentase penagihan terpisah sebagai nol untuk akun tersebut. Bila rekaman ditandai sebagai nol, aktual biaya dan pendapatan pada masa mendatang yang dikaitkan atau dipecah untuk pelanggan ini terpengaruh. | Bila Anda memilih akun dari daftar induk akun untuk ditambahkan dan menyimpannya, pelanggan baris kontrak juga akan ditambahkan sebagai pelanggan kontrak. Pelanggan baris kontrak digunakan saat faktur dibuat. |
| Persentase pembagian Penagihan | Kisi yang dapat diedit pada tab **pelanggan baris kontrak** dan formulir buat cepat dan utama untuk pelanggan baris kontrak | Bidang ini mewakili persentase setiap transaksi penjualan yang tidak ditagih yang akan dikaitkan ke pelanggan baris kontrak ini. | Pelanggan baris kontrak dan persentase pemecahan penagihan digunakan saat aktual dibuat setelah disetujui dan setelah faktur dibuat. |
| Batas Jangan terlampaui | Kisi yang dapat diedit pada tab **pelanggan baris kontrak** dan formulir buat cepat dan utama untuk pelanggan baris kontrak | Menunjukkan jika ada batas atau pagu negosiasi untuk jumlah keseluruhan yang akan ditagih ke pelanggan ini untuk baris kontrak. | Batas yang tidak boleh terlewati untuk pelanggan baris kontrak digunakan saat aktual dibuat dan faktur dihasilkan. |
| Perusahaan Pemilik | Kisi yang dapat diedit pada tab **pelanggan baris kuotasi** dan formulir buat cepat dan utama untuk pelanggan baris kuotasi | Entitas hukum yang diatur untuk pelanggan ini. Bidang ini hanya baca dan diatur ke perusahaan pemilik kuotasi. Daftar Pelanggan yang akan ditambahkan di bidang **akun** telah difilter ke daftar dari perusahaan pemilik ini. | Konsep perusahaan pemilik setara dengan konsep entitas hukum. Semua biaya dan pendapatan yang Diperoleh dari proyek ini diperhitungkan dalam buku besar perusahaan pemilik. |
| Adalah Pembulatan | Kisi yang dapat diedit pada tab **pelanggan baris kontrak** dan formulir buat cepat dan utama untuk pelanggan baris kontrak | Bidang ini menunjukkan jika pelanggan ini adalah pelanggan pembulatan default untuk baris kontrak berbasis proyek ini. | Bila Anda membuat aktual berdasarkan persentase pemecahan penagihan, mungkin ada beberapa perbedaan pembulatan. Pelanggan ini dikaitkan dengan perbedaan pembulatan dalam kasus ini. |

## <a name="edit-billing-split-percentages"></a>Mengedit persentase pembagian penagihan

Persentase pemecahan penagihan dapat diedit di kisi. Bila persentase pemecahan penagihan tidak berjumlah Total 100 persen, kesalahan akan terjadi. Setelah Anda mengedit persentase pemecahan penagihan, segarkan halaman untuk menghilangkan kesalahan.

Anda juga dapat mencoba memilih **distribusikan secara merata** pada subkisi pelanggan baris kontrak. Tindakan ini secara merata mengalokasikan pembagian tagihan ke semua pelanggan baris kontrak. Jika ada faktor pembulatan, maka akan ditambahkan ke pelanggan pembulatan. Pelanggan baris kontrak selalu ditandai sebagai pelanggan **pembulatan** dengan bendera **Pembulatan** diatur ke **ya**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]