---
title: Mengelola beberapa pelanggan pada baris kontrak berbasis proyek - lite
description: Artikel ini menyediakan informasi tentang mengelola beberapa pelanggan pada jalur kontrak berbasis proyek.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7648c7ef7ec6ffb68932552a0c25b79f1f93733
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922134"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Mengelola beberapa pelanggan pada baris kontrak berbasis proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Baris kontrak berbasis proyek dapat mencakup daftar pelanggan yang bertanggung jawab atas pembayaran. Daftar pelanggan pada baris kontrak berbasis proyek ini dapat sama dengan daftar pelanggan pada kontrak, namun tidak wajib. Bila kuotasi proyek dimenangkan, dan kontrak proyek dibuat, daftar pelanggan pada baris kuotasi akan disalin ke baris kontrak yang sesuai. Pelanggan pada kuotasi akan disalin ke kontrak.

Bila kontrak proyek ditagih, daftar pelanggan pada baris kontrak berbasis proyek akan diprioritaskan berdasarkan daftar pelanggan pada kontrak. Daftar pelanggan pada kontrak proyek hanya digunakan untuk baris kontrak baru default.

Semua pelanggan kontrak pada tab **pelanggan** pada kontrak proyek di-default sebagai pelanggan baris kontrak pada baris kontrak baru yang dibuat untuk kontrak proyek. Baris kontrak yang ada tidak akan mewarisi rekaman pelanggan kontrak baru yang dibuat setelah mereka.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Membuat, memperbarui, atau menghapus rekaman pelanggan baris kontrak

Anda dapat membuat, memperbarui, atau menghapus pelanggan baris kontrak dari tab pelanggan baris kontrak pada halaman baris kontrak berbasis proyek. Bila pelanggan baru ditambahkan pada baris kontrak berbasis proyek, mereka juga ditambahkan pada kontrak keseluruhan sebagai pelanggan kontrak dengan pemecahan penagihan default nol persen. Persentase pemecahan penagihan pada kontrak keseluruhan disalin ke baris kontrak baru dan ke kontrak proyek akhirnya. Namun, saat menagih dengan faktur dari kontrak, persentase pemecahan penagihan pada tingkat baris kontraklah yang digunakan dan bukan persentase pemecahan penagihan pada tingkat kontrak keseluruhan.

Di bawah ini adalah bidang pada rekaman pelanggan baris **kontrak** dari baris kontrak berbasis proyek yang perlu diingat saat Anda bekerja dengannya:

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| **Akun** | Kisi yang dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Semua Akun Aktif. Bidang ini dikunci setelah rekaman dibuat. Untuk memperbarui bidang, Hapus rekaman, dan buat rekaman baru. Jika Anda telah merekam aktual, Anda tidak dapat menghapus rekaman. Namun, Anda dapat menandai persentase penagihan terpisah sebagai nol untuk akun tersebut. Bila rekaman ditandai sebagai nol, aktual biaya dan pendapatan pada masa mendatang yang dikaitkan atau dipecah untuk pelanggan ini terpengaruh. | Bila Anda memilih akun dari daftar induk akun untuk ditambahkan dan menyimpannya, pelanggan baris kontrak juga akan ditambahkan sebagai pelanggan kontrak. Pelanggan baris kontrak digunakan saat faktur dibuat. |
| **Persentase Split Penagihan** | Kisi yang dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Bidang ini mewakili persentase setiap transaksi penjualan yang tidak ditagih yang akan dikaitkan ke pelanggan baris kontrak ini. | Pelanggan baris kontrak dan persentase pemecahan penagihan digunakan saat aktual dibuat setelah disetujui dan setelah faktur dibuat. |
| **Batas Jangan terlampaui** | Kisi yang dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Menunjukkan jika ada batas atau pagu negosiasi untuk jumlah keseluruhan yang akan ditagih ke pelanggan ini untuk baris kontrak. | Batas yang tidak boleh terlewati untuk pelanggan baris kontrak digunakan saat aktual dibuat dan faktur dihasilkan. |
| **Adalah Pembulatan** | Kisi yang dapat diedit pada tab **pelanggan kontrak** dan formulir **buat cepat** dan **utama** untuk pelanggan baris kontrak. | Bidang ini menunjukkan jika pelanggan ini adalah pelanggan pembulatan default untuk baris kontrak berbasis proyek ini. | Bila Anda membuat aktual berdasarkan persentase pemecahan penagihan, mungkin ada beberapa perbedaan pembulatan. Pelanggan ini dikaitkan dengan perbedaan pembulatan dalam kasus ini. |

## <a name="edit-billing-split-percentages"></a>Mengedit persentase pembagian penagihan

Persentase pemecahan penagihan dapat diedit di kisi. Bila persentase pemecahan penagihan tidak berjumlah Total 100 persen, kesalahan akan terjadi. Setelah Anda mengedit persentase pemecahan penagihan, segarkan halaman untuk menghilangkan kesalahan.

Anda juga dapat memilih **distribusikan secara merata** pada subkisi pelanggan baris kontrak. Tindakan ini secara merata mengalokasikan pembagian tagihan ke semua pelanggan baris kontrak. Jika ada faktor pembulatan, maka akan ditambahkan ke pelanggan pembulatan. Pelanggan baris kontrak selalu ditandai sebagai pelanggan **pembulatan** dengan bendera **Pembulatan** diatur ke **ya**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]