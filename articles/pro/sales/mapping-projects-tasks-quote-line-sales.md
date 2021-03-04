---
title: Memetakan proyek dan tugas ke baris kuotasi berbasis proyek
description: Topik ini menyediakan informasi tentang cara memetakan proyek dan tugas ke baris tugas berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130717"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Memetakan proyek dan tugas ke baris kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Pada baris kuotasi berbasis proyek, Anda dapat memetakan tugas spesifik proyek yang sudah terkait dengan baris kuotasi.

Bila Anda memetakan tugas ke baris kuotasi, item berikut yang ditentukan pada baris kuotasi hanya akan berlaku untuk tugas tersebut:

- Metode Penagihan
- Opsi ketertagihan
- Batas Jangan terlampaui
- Pelanggan

Misalnya, Anda mungkin memiliki proyek dengan satu fase adalah harga tetap dan semua fase lainnya adalah waktu dan bahan. Dalam kasus ini, Anda dapat mengaitkan tahap pertama, dan semua tugas anak, ke baris kuotasi untuk fase tersebut dengan metode penagihan harga tetap. Anda kemudian dapat mengaitkan Semua tahapan lain ke baris kuotasi berbasis waktu dan bahan.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Kaitkan tugas ke Baris Kuotasi berbasis Proyek

Anda dapat mengaitkan tugas dengan baris kuotasi dari lokasi berikut:

- Halaman **proyek** > tab **Penagihan tugas** (optimal)
- Halaman **baris kuotasi** > tab **tugas yang ditagih** 

### <a name="from-the-project-page"></a>Dari halaman proyek

Halaman **proyek** memberikan pengalaman optimal untuk mengaitkan tugas ke baris kuotasi. Anda dapat menggunakan Halaman ini untuk memilih beberapa tugas dan mengaitkan semuanya, serta tugas anak mereka, ke baris kuotasi yang dipilih.

1. Pada tab **Umum** baris kuotasi berbasis proyek, Verifikasikan bidang **proyek** diisi.
2. Di bidang **tugas yang disertakan**, pilih **tugas yang dipilih saja**.
3. Simpan Baris kuotasi berbasis proyek. Saat formulir disegarkan, tab **tugas yang bisa ditagih** akan ditampilkan.
4. Pada tab **Umum**, pilih tautan untuk proyek dari bidang **proyek**.
5. Pada halaman **proyek**, pilih tab **Penagihan tugas**.
6. Di kisi kedua, yang berlaku untuk penyiapan penagihan khusus tugas, pilih satu atau beberapa tugas, lalu pilih **Kaitkan baris kuotasi**.
7. Di halaman dialog yang muncul, pilih baris kuotasi yang menampilkan baris kuotasi berbasis proyek pada kuotasi.
8. Di bidang **jenis penagihan**, tentukan Apakah tugas ini dibebankan atau tidak dikenakan biaya.
9. Pilih kotak centang untuk menunjukkan apakah Asosiasi harus mencakup tugas anak dari tugas yang dipilih. Mencentang kotak akan mengaitkan tugas anak dari tugas yang dipilih ke baris kuotasi.
10. Pilih **OK** untuk menutup dialog.

### <a name="from-the-quote-line-page"></a>Dari halaman baris kuotasi

Anda dapat mengaitkan tugas proyek ke baris kuotasi dari tab **tugas yang dapat ditagih** pada halaman **baris kuotasi**.

>[!NOTE]
>Tempat optimal untuk mengaitkan tugas proyek ke baris kuotasi adalah tab **Penagihan tugas** pada halaman **proyek**. Jika Anda mengaitkan tugas dari tab **tugas dapat ditagih** pada halaman **baris kuotasi**, Anda harus mengkaitkan setiap proyek secara manual.

1. Pada tab **Umum** baris kuotasi berbasis proyek, Verifikasikan bahwa ada proyek yang dipilih di bidang **proyek**.
2. Di bidang **tugas yang disertakan**, pilih **tugas yang dipilih saja**.
3. Simpan Baris kuotasi berbasis proyek. Saat formulir disegarkan, tab **tugas yang bisa ditagih** akan ditampilkan.
4. Pada tab **tugas dapat ditagih**, pilih **Tambah tugas baris kuotasi**.
5. Pada halaman **tugas baris kuotasi**, di bidang **tugas**, pilih tugas dan di bidang **jenis penagihan**, pilih **Simpan**. 
6. Tutup halaman. Tugas yang dipilih sekarang terkait dengan baris kuotasi.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Hapus kaitan tugas dari Baris Kuotasi berbasis Proyek

### <a name="from-the-project-page"></a>Dari halaman proyek

Metode ini memberikan pengalaman paling optimal untuk menghapus kaitan tugas dari baris kuotasi. Anda dapat menggunakan beberapa tugas dan menghapus kaitan semuanya, serta tugas anak mereka, dari baris kuotasi yang dipilih.

1. Pada tab **Umum** baris kuotasi berbasis proyek, di bidang **proyek**, pilih tautan proyek.
2. Pada halaman **proyek**, pilih tab **Penagihan tugas**.
3. Di kisi kedua, yang berlaku untuk penyiapan penagihan khusus tugas, pilih satu atau beberapa tugas, lalu pilih **Hapus kaitan baris kuotasi**.
4. Di halaman dialog yang muncul, pilih baris kuotasi.
5. Pilih kotak centang untuk menunjukkan apakah Asosiasi juga harus dihapus dari tugas anak dari tugas yang dipilih. Mencentang kotak juga akan menghapus kaitan tugas anak dari tugas yang dipilih ke baris kuotasi.
6. Pilih **OK**. Pesan peringatan akan menginformasikan bahwa jika Anda menghapus Asosiasi ini, setiap aktual yang sebelumnya dicatat pada tugas tersebut dapat dibalik. 
7. Pilih **OK** untuk melanjutkan dan menghapus keterkaitan antara tugas dan baris kuotasi berbasis proyek.

### <a name="from-the-quote-line-page"></a>Dari halaman baris kuotasi

Anda juga dapat menghapus kaitan tugas proyek ke baris kuotasi dari tab **tugas yang dapat ditagih** pada halaman **baris kuotasi**.

1. Pada tab **tugas dapat ditagih**, pilih **Hapus tugas baris kuotasi**.
2. Pilih **OK**. Pesan peringatan akan menginformasikan bahwa jika Anda menghapus Asosiasi ini, setiap aktual yang sebelumnya dicatat pada tugas tersebut dapat dibalik. 
3. Pilih **OK** untuk melanjutkan dan menghapus keterkaitan antara tugas dan baris kuotasi berbasis proyek.

>[!NOTE]
> Prosedur ini tidak menghapus tugas dari proyek. Ini hanya akan menghapus asosiasi tugas dari baris kuotasi berbasis proyek.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]