---
title: Mengimpor dan mengelola transaksi kartu kredit
description: Topik ini menjelaskan cara mengimpor dan mengelola transaksi kartu kredit terkait pengeluaran. Transaksi ini dapat diatur sehingga mereka secara otomatis diimpor pada jadwal berulang, atau mereka dapat secara manual diimpor sebagaimana diperlukan.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995855"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Mengimpor dan mengelola transaksi kartu kredit

Transaksi kartu kredit terkait dengan pengeluaran dapat diatur sehingga mereka secara otomatis diimpor pada jadwal yang berulang. Atau, transaksi dapat diimpor secara manual sebagaimana diperlukan. Transaksi kartu kredit diimpor melalui entitas data transaksi kartu kredit.

Untuk informasi lebih lanjut tentang entitas data, lihat [entitas data](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]