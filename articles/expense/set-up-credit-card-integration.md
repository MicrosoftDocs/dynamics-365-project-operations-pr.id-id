---
title: Mengonfigurasi integrasi kartu kredit
description: Topik ini menjelaskan cara mengimpor dan mengelola transaksi kartu kredit terkait pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120862"
---
# <a name="set-up-credit-card-integration"></a>Mengonfigurasi integrasi kartu kredit

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Transaksi kartu kredit terkait dengan pengeluaran dapat diatur sehingga mereka secara otomatis diimpor pada jadwal yang berulang. Atau, transaksi dapat diimpor secara manual sebagaimana diperlukan. Transaksi kartu kredit diimpor melalui entitas data transaksi kartu kredit.

## <a name="import-credit-card-transactions"></a>Mengimpor transaksi kartu kredit

1. Pada halaman **transaksi kartu kredit**, pilih **impor transaksi**. Jika Anda membuka manajemen data untuk pertama kalinya, sistem harus memperbarui daftar entitas data agar dapat melanjutkan.
2. Di bidang **Nama**, masukkan deskripsi unik untuk pekerjaan impor.
3. Di bidang **format data sumber**, pilih format file yang berisi transaksi kartu kredit yang akan diimpor.
4. Pilih **Unggah**, lalu Cari dan pilih file yang akan diimpor.
5. Setelah file diunggah, validasi pemetaan file transaksi kartu kredit dan kolom entitas data transaksi kartu kredit dengan memilih tautan **Lihat peta** pada ubin. Jika terjadi kesalahan pemetaan, atau jika Anda harus mengubah pemetaan, buat perubahan pemetaan dari tab **visualisasi pemetaan** atau tab **rincian pemetaan**.
6. Untuk mengotomatisasi transaksi kartu kredit, pilih **buat pekerjaan data yang berulang**. Selanjutnya Anda dapat mengatur pengulangan yang menentukan seberapa sering transaksi kartu kredit harus diimpor. Setelah selesai, pilih **OK**.
7. Untuk mengimpor file yang dipilih sekarang, pilih **impor**.
8. Jika kesalahan terjadi selama impor, Anda dapat melihat log eksekusi atau data penahapan untuk melihat kesalahan yang harus Anda Perbaiki untuk membantu menjamin impor yang berhasil.

> [!NOTE]
> Jika Anda harus mengimpor lebih dari satu format file, Anda harus membuat tugas impor terpisah untuk setiap jenis format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tetapkan ulang transaksi kartu kredit untuk karyawan yang dihentikan

Setelah rekaman karyawan dihentikan, akun Active Directory Domain Services (AD DS) karyawan dinonaktifkan. Namun, mungkin ada transaksi kartu kredit aktif yang harus tetap dikeluarkan dan diganti. Dari halaman **transaksi kartu kredit**, Anda dapat menetapkan ulang karyawan untuk setiap transaksi kartu kredit dengan karyawan yang terkait telah dihentikan.

Pilih satu atau beberapa transaksi kartu kredit, lalu pilih **tetapkan ulang transaksi**. Selanjutnya Anda dapat memilih karyawan lain untuk ditetapkan transaksi kartu kredit. Setelah transaksi kartu kredit telah dipindahkan, mereka dapat dipilih untuk laporan pengeluaran dan dibayar melalui proses biasa untuk penggantian laporan pengeluaran.
