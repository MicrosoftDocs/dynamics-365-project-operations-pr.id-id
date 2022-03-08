---
title: Memetakan proyek dan tugas ke baris kontrak berbasis proyek - lite
description: Topik ini menyediakan informasi tentang menambahkan dan menghapus proyek dan tugas ke baris kontrak.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ce99e6f770c5eb39e5f2740a861721cf3d210ac9743bbd9d2a1e1a7236f368c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989735"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Memetakan proyek dan tugas ke baris kontrak berbasis proyek 

_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_

Pada baris kontrak berbasis proyek, Anda dapat memetakan tugas tertentu dalam proyek ke baris kontrak.

Bila Anda memetakan tugas tertentu ke baris kontrak, metode penagihan, pilihan penagihan, batas yang tidak boleh terlampaui, dan pelanggan yang ditentukan pada baris kontrak hanya akan berlaku untuk tugas khusus tersebut.

Jika Anda memiliki skenario di mana satu fase proyek, misalnya fase prototipe, adalah harga tetap dan semua fase lainnya adalah waktu dan material, Anda akan dapat mengaitkan fase prototipe dan semua tugas anak terkait ke baris kontrak untuk fase tersebut dengan metode penagihan harga tetap.

Semua tahapan lain dalam struktur rincian kerja proyek Anda (WBS) dapat dikaitkan dengan waktu dan baris kontrak berbasis material.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Kaitkan tugas ke Baris Kontrak berbasis Proyek

Tugas dapat dikaitkan ke baris kontrak dari tab **kena biaya** di halaman **baris kontrak** atau dari tab **tagihan tugas** pada halaman **proyek**.

### <a name="from-the-contract-line-page"></a>Dari halaman baris kontrak

Selesaikan langkah-langkah berikut untuk mengaitkan tugas proyek ke baris kontrak dari tab **tugas kena biaya** pada halaman **baris kontrak**.

1. Pada tab **Umum** baris kontrak berbasis proyek, Verifikasikan bahwa bidang **proyek** diisi.
2. Di bidang **tugas yang disertakan**, pilih **tugas yang dipilih saja**.
3. Simpan perubahan. Formulir akan disegarkan dan tab **tugas kena biaya** akan terlihat.
4. Pilih tab **tugas kena biaya**, dan di subkisi, pilih **Tambah tugas baris kontrak**.
5. Pada halaman **tugas baris kontrak**, di drop-down **tugas**, pilih tugas. 
6. Masukkan informasi di bidang **jenis penagihan**, lalu pilih **Simpan dan tutup**. Tugas yang dipilih dikaitkan ke baris kontrak.

> [!NOTE]
> Ini bukan pengalaman yang paling optimal untuk mengaitkan tugas proyek ke baris kontrak. Setiap proyek harus dikaitkan secara manual dalam pengalaman ini. Cara yang dipilih adalah dari tab **tagihan tugas** pada halaman **proyek**.

### <a name="from-the-project-page"></a>Dari halaman proyek

Ini adalah metode optimal untuk mengaitkan tugas ke baris kontrak. Anda dapat memilih beberapa tugas dan mengaitkan semua tugas dan tugas anak ke baris kontrak yang dipilih. Selesaikan langkah-langkah berikut untuk mengaitkan tugas ke baris kontrak dari halaman **proyek**.

1. Pada tab **Umum** baris kontrak berbasis proyek, Verifikasikan bahwa bidang **proyek** diisi.
2. Di bidang **tugas yang disertakan**, pilih **tugas yang dipilih saja**.
3. Simpan Baris kontrak berbasis proyek. Formulir akan disegarkan dan tab **tugas kena biaya** akan terlihat. Hanya untuk tujuan verifikasi.
4. Pada tab **Umum** baris kontrak berbasis proyek, di bidang **proyek**, pilih tautan proyek.
5. Pada halaman **proyek**, pilih tab **Pengaturan penagihan tugas**.
6. Ada dua kisi. Satu kisi adalah untuk baris kontrak yang berlaku untuk seluruh proyek. Kisi kedua berlaku untuk penyiapan penagihan khusus tugas. Di kisi kedua, pilih satu atau beberapa tugas, lalu pilih **kaitkan baris kontrak**.
7. Di halaman dialog yang terbuka, pilih baris kontrak dari drop-down.
8. Gunakan drop-down **jenis penagihan** untuk menandai tugas sebagai kena biaya atau tidak dikenakan biaya.
9. Pilih kotak centang untuk menunjukkan apakah asosiasi juga harus menyertakan tugas anak dari tugas yang dipilih. Mencentang kotak juga akan mengaitkan tugas anak dari tugas yang dipilih ke baris kontrak.
10. Pilih **OK** untuk menutup dialog.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Hapus kaitan tugas dari Baris Kontrak berbasis Proyek

### <a name="from-the-contract-line-page"></a>Dari halaman baris kontrak

Selesaikan langkah-langkah berikut untuk menghapus kaitan tugas proyek dari baris kontrak di tab **tugas kena biaya** pada halaman **baris kontrak**.

1. Pada tab **tugas kena biaya**, pilih **Hapus tugas baris kontrak**.
2. Pesan peringatan menunjukkan bahwa menghapus Asosiasi ini dapat mengakibatkan pembalikan setiap aktual yang direkam sebelumnya pada tugas. Pilih **OK** pada dialog untuk menghapus kaitan antara tugas dan baris kontrak berbasis proyek. 

> [!NOTE]
> Ini tidak akan menghapus tugas dari proyek. Namun, ini menghapus Asosiasi tugas dari baris kontrak berbasis proyek.

### <a name="from-the-project-page"></a>Dari halaman proyek

Ini adalah pengalaman yang lebih optimal untuk menghapus kaitan tugas dari baris kontrak. Anda dapat memilih beberapa tugas dan menghapus kaitan semua tugas dan tugas anak dari baris kontrak yang dipilih. Selesaikan langkah-langkah berikut untuk menghapus kaitan tugas dari baris kontrak.

1. Dari tab **Umum** baris kontrak berbasis proyek, di bidang **proyek**, klik tautan untuk proyek.
2. Pada halaman **proyek**, pilih tab **Pengaturan penagihan tugas**.
3. Ada dua kisi pada halaman. Satu kisi adalah untuk baris kontrak yang berlaku untuk seluruh proyek dan yang kedua berlaku untuk penyiapan penagihan khusus tugas. Di kisi kedua, pilih satu atau beberapa tugas, lalu pilih **Hapus kaitan baris kontrak**.
4. Di halaman dialog yang terbuka, pilih baris kontrak dari drop-down.
5. Pilih kotak centang untuk menunjukkan apakah asosiasi juga dihapus dari tugas anak dari tugas yang dipilih. Mencentang kotak juga akan menghapus kaitan tugas anak dari tugas yang dipilih dari baris kontrak.
6. Pilih **OK**. Pesan peringatan menunjukkan bahwa menghapus Asosiasi ini dapat mengakibatkan pembalikan setiap aktual yang direkam sebelumnya pada tugas. Pilih **OK** pada dialog peringatan untuk menghapus kaitan antara tugas dan baris kontrak berbasis proyek.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
