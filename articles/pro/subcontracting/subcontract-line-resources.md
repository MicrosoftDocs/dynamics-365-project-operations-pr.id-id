---
title: Sumber Daya Baris Subkontrak
description: Topik ini menjelaskan cara menentukan sumber daya khusus yang disediakan oleh vendor untuk baris subkontrak tertentu untuk waktu.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323375"
---
# <a name="subcontract-line-resources"></a>Sumber Daya Baris Subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Dalam Dynamics 365 Project Operations, vendor dapat menentukan sumber daya yang akan digunakan untuk menyediakan kapasitas sumber daya yang dibeli pada baris subkontrak untuk waktu.

## <a name="create-subcontract-line-resources"></a>Buat Sumber Daya Baris Subkontrak

Untuk membuat sumber daya baris subkontrak, selesaikan langkah-langkah berikut.

1. Di panel navigasi, pilih **Subkontrak**, dan buka Subkontrak yang ingin Anda kerjakan.
2. Buka baris subkontrak untuk waktu yang akan ditentukan sumber daya vendornya.
3. Pada tab **Sumber daya baris Subkontrak**, pada subkisi, pilih **+ Sumber daya Baris Subkontrak Baru**.
4. Pada halaman **Tahapan Baris Subkontrak Baru**, masukkan informasi yang diperlukan kemudian pilih **Simpan dan Tutup**.

Tabel berikut menjelaskan bidang pada sumber daya baris subkontrak.

| Bidang |  KETERANGAN |
| ----- | ------------ |
| Sumber Daya yang Dapat Dipesan | Pilih sumber daya yang dapat dipesan dari jenis "Pekerja kontrak" yang akan digunakan sebagai sumber daya pada baris subkontrak. Jika Anda belum membuat sumber daya yang dapat dipesan untuk pekerja kontrak, biarkan bidang ini kosong. Sumber daya yang dapat dipesan akan dibuat saat Anda menyimpan rekaman.  |
| Kontak | Jika bidang **Sumber Daya yang Dapat Dipesan** kosong, Anda dapat membuat sumber daya baris subkontrak dari kontak yang ada. Gunakan pencarian untuk melihat daftar kontak aktif dalam sistem. Pilih kontak untuk vendor subkontrak ini. Kontak yang Anda pilih akan divalidasi saat Anda menyimpan rekaman. Jika kontak yang Anda pilih bukan kontak yang valid, rekaman Anda tidak akan disimpan. Jika tidak ada sumber daya yang dapat dipesan untuk kontak yang dipilih, sistem membuat sumber daya yang dapat dipesan untuk kontak yang dipilih sebelum membuat sumber daya baris subkontrak. |
| Pengguna | Jika bidang **Sumber Daya yang Dapat Dipesan** kosong, Anda dapat membuat sumber daya baris subkontrak dengan memilih pengguna yang aktif. Gunakan pencarian untuk melihat daftar pengguna aktif dalam sistem. Jika tidak ada sumber daya yang dapat dipesan untuk pengguna yang dipilih, sistem membuat sumber daya yang dapat dipesan untuk pengguna yang dipilih sebelum membuat sumber daya baris subkontrak. |
| Tanggal Mulai | Tanggal dimulainya penugasan pekerja subkontrak. Jika sumber daya ini dipesan selama periode yang jatuh sebelum rentang tanggal ini, peringatan akan terjadi. |
| Tanggal Akhir | Tanggal penugasan pekerja subkontrak selesai. Jika sumber daya ini dipesan selama periode yang jatuh setelah rentang tanggal ini, peringatan akan terjadi. |
| Upaya | Jumlah total jam upaya yang akan dihabiskan pekerja subkontrak pada baris subkontrak ini. Jika sumber daya ini dipesan di luar upaya yang dialokasikan pada subkontrak ini, peringatan akan terjadi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
