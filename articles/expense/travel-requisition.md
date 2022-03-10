---
title: Permintaan perjalanan
description: Topik ini menyediakan informasi tentang permintaan perjalanan.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f00b5ca2142c4ba5cb523773f1f6dd8f0a055f6f6d474bc2b8e5f775ca0fc739
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994550"
---
# <a name="travel-requisitions"></a>Permintaan perjalanan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Permintaan perjalanan mencantumkan biaya yang akan dikeluarkan untuk tujuan perjalanan. Permintaan perjalanan diajukan untuk ditinjau dan dapat digunakan untuk mengotorisasi pengeluaran.

Anda mungkin diminta untuk mengajukan permintaan perjalanan sebelum Anda dikenakan biaya yang dibebankan kepada organisasi. Persyaratan ini berlaku, terlepas dari Apakah Anda membebankan biaya pada kartu kredit perusahaan, membelanjakan uang tunai yang Anda terima dari uang muka, atau pengeluaran biaya mandiri yang akan diganti oleh organisasi.

Permintaan dan kebijakan perjalanan dapat digunakan untuk membantu mengelola pengeluaran organisasi. Misalnya, jika organisasi Anda mengerjakan proyek harga tetap yang mensyaratkan perjalanan, pengeluaran perjalanan dari anggota tim proyek harus sesuai dengan anggaran proyek. Dengan mewajibkan pengeluaran perjalanan disetujui sebelum dikeluarkan, organisasi dapat membantu memastikan bahwa proyek tetap dalam anggaran.

## <a name="configuration"></a>Konfigurasi 

Permintaan perjalanan dapat dikonfigurasi sebagai "wajib" dengan mengaktifkan parameter "pra-otorisasi perjalanan wajib" dalam parameter manajemen pengeluaran. 

## <a name="create-and-submit-a-travel-requisition"></a>Membuat dan mengajukan permintaan perjalanan

1. Buka **Pengeluaran saya: permintaan perjalanan**, lalu pilih **permintaan perjalanan baru**.
2. Masukkan tujuan dan destinasi untuk permintaan.
3. Di bidang  **Deskripsi perjalanan**, masukkan informasi tambahan. 
4. Untuk setiap pengeluaran yang diharapkan, seperti penerbangan, makan, atau Penyewaan Mobil, buat item baris pengeluaran. Sertakan estimasi tanggal, jumlah estimasi, dan mata uang untuk setiap pengeluaran. 
5. Setelah selesai menambahkan pengeluaran yang diharapkan, pilih **Simpan**.
6. Bila Anda siap mengirimkan permintaan perjalanan, pilih **alur kerja** > **Ajukan**.

Anda dapat melihat permintaan perjalanan yang disetujui dalam **pengeluaran saya: permintaan perjalanan**. 

## <a name="view-available-travel-requisitions"></a>Lihat permintaan perjalanan yang tersedia

Anda dapat melihat semua perjalanan permintaan dalam **pengeluaran saya: permintaan perjalanan**.

## <a name="approve-travel-requisitions"></a>Setujui Permintaan perjalanan

Pilih permintaan perjalanan yang ingin Anda setujui, lalu pilih **alur kerja** > **setujui**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Ajukan Laporan pengeluaran menggunakan permintaan perjalanan yang disetujui

1. Buat laporan pengeluaran baru dan di header laporan pengeluaran, dan dari daftar permintaan perjalanan yang disetujui, pilih **Petakan ke permintaan perjalanan**.
2. Bidang **jumlah permintaan perjalanan** diperbarui secara otomatis di header laporan pengeluaran.
3. Tambahkan setiap pengeluaran yang timbul untuk perjalanan. Jika **bidang pra-otorisasi** diaktifkan, jumlah yang direkonsiliasi dan jumlah yang diotorisasi untuk kategori pengeluaran spesifik akan diperbarui.

> [!NOTE]
> Bila Anda memetakan laporan pengeluaran untuk permintaan perjalanan yang disetujui, jumlah transaksi tidak dapat melebihi jumlah yang diizinkan. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]