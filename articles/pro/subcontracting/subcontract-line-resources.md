---
title: Sumber Daya Baris Subkontrak
description: Artikel ini menjelaskan cara menentukan sumber daya khusus yang disediakan oleh vendor untuk baris subkontrak tertentu untuk waktu.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522376"
---
# <a name="subcontract-line-resources"></a>Sumber Daya Baris Subkontrak

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dalam Dynamics 365 Project Operations, vendor dapat menentukan sumber daya yang akan digunakan untuk menyediakan kapasitas sumber daya yang dibeli pada baris subkontrak untuk waktu.

## <a name="create-subcontract-line-resources"></a>Buat Sumber Daya Baris Subkontrak

Untuk membuat sumber daya baris subkontrak, selesaikan langkah-langkah berikut.

1. Di panel navigasi, pilih **Subkontrak**, dan buka Subkontrak yang ingin Anda kerjakan.
2. Buka baris subkontrak untuk waktu yang akan ditentukan sumber daya vendornya.
3. Pada tab **Sumber daya baris Subkontrak**, pada subkisi, pilih **+ Sumber daya Baris Subkontrak Baru**.
4. Pada halaman **Sumber Daya Baris Subkontrak Baru**, masukkan informasi yang diperlukan, lalu pilih **Simpan dan Tutup**.

Tabel berikut menjelaskan bidang pada sumber daya baris subkontrak.

| Bidang | KETERANGAN | Dampak Fungsional |
| ----- | ----------- | ----------------- |
| Sumber Daya yang Dapat Dipesan | Pilih sumber daya yang dapat dipesan dari jenis **Pekerja kontrak** yang akan digunakan sebagai sumber daya pada baris subkontrak.| Jika Anda belum membuat sumber daya yang dapat dipesan untuk pekerja kontrak, biarkan bidang ini kosong. Sumber daya yang dapat dipesan akan dibuat saat Anda menyimpan rekaman.  |
| Kontak | Anda dapat membuat sumber daya baris subkontrak dari kontak yang ada. Gunakan pencarian untuk melihat daftar kontak aktif dalam sistem. Pilih kontak untuk vendor subkontrak ini. Jika kontak yang Anda pilih bukan kontak yang valid untuk vendor pada subkontrak, rekaman sumber daya baris subkontrak tidak akan disimpan.| Jika tidak ada sumber daya yang dapat dipesan untuk kontak yang dipilih, sistem membuat sumber daya yang dapat dipesan untuk kontak yang dipilih sebelum membuat sumber daya baris subkontrak. |
| Pengguna | Anda dapat membuat sumber daya baris subkontrak dengan memilih pengguna aktif. Gunakan pencarian untuk melihat daftar pengguna aktif dalam sistem.| Jika tidak ada sumber daya yang dapat dipesan untuk pengguna yang dipilih, sistem membuat sumber daya yang dapat dipesan untuk pengguna yang dipilih sebelum membuat sumber daya baris subkontrak. |
| Tanggal Mulai | Tanggal dimulainya penugasan pekerja subkontrak.| Jika sumber daya ini dipesan selama periode yang jatuh sebelum rentang tanggal ini, peringatan akan terjadi. |
| Tanggal Akhir | Tanggal penugasan pekerja subkontrak selesai.| Jika sumber daya ini dipesan selama periode yang jatuh setelah rentang tanggal ini, peringatan akan terjadi. |
| Upaya | Jumlah total jam upaya yang akan dihabiskan pekerja kontrak pada baris subkontrak ini.| Jika sumber daya ini dipesan di luar upaya yang dialokasikan pada subkontrak ini, peringatan akan terjadi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
