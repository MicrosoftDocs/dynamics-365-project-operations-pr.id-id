---
title: Mengonfigurasi integrasi kartu kredit
description: Laporan topik menjelaskan cara bekerja dengan transaksi kartu kredit yang terkait dengan pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866687"
---
# <a name="set-up-credit-card-integration"></a>Mengonfigurasi integrasi kartu kredit

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Transaksi kartu kredit terkait dengan pengeluaran dapat diatur sehingga mereka secara otomatis diimpor pada jadwal yang berulang. Atau, transaksi dapat diimpor secara manual sebagaimana diperlukan. Transaksi kartu kredit diimpor melalui entitas data transaksi kartu kredit.

## <a name="import-credit-card-transactions"></a>Mengimpor transaksi kartu kredit

Untuk mengimpor transaksi kartu kredit, ikuti langkah-langkah berikut:

1. Pada halaman **transaksi kartu kredit**, pilih **impor transaksi**. Jika Anda membuka manajemen data untuk pertama kalinya, sistem harus memperbarui daftar entitas data agar dapat melanjutkan.
2. Di bidang **Nama**, masukkan deskripsi unik untuk pekerjaan impor.
3. Di bidang **format data sumber**, pilih format file yang berisi transaksi kartu kredit yang akan diimpor.
4. Pilih **Unggah**, lalu Cari dan pilih file yang akan diimpor.
5. Setelah file diunggah, validasi pemetaan file transaksi kartu kredit dan kolom entitas data transaksi kartu kredit dengan memilih tautan **Lihat peta** pada ubin. Jika terjadi kesalahan pemetaan, atau jika Anda harus mengubah pemetaan, buat perubahan pemetaan dari tab **visualisasi pemetaan** atau tab **rincian pemetaan**.
6. Untuk mengotomatisasi transaksi kartu kredit, pilih **buat pekerjaan data yang berulang**. Selanjutnya Anda dapat mengatur pengulangan yang menentukan seberapa sering transaksi kartu kredit harus diimpor. Setelah selesai, pilih **OK**.
7. Untuk mengimpor file yang dipilih sekarang, pilih **impor**.
8. Jika kesalahan terjadi selama impor, Anda dapat melihat log eksekusi atau data penahapan untuk melihat kesalahan yang harus Anda perbaiki untuk membantu memastikan keberhasilan impor.

> [!NOTE]
> Jika Anda ingin mengimpor lebih dari satu format file, Anda harus membuat pekerjaan impor terpisah untuk setiap jenis format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tetapkan ulang transaksi kartu kredit untuk karyawan yang dihentikan

Setelah rekaman karyawan dihentikan, akun Active Directory Domain Services (AD DS) karyawan dinonaktifkan. Namun, mungkin ada transaksi kartu kredit aktif yang harus tetap dikeluarkan dan diganti. Pada halaman **transaksi kartu kredit**, Anda dapat melakukan penetapan ulang karyawan untuk setiap transaksi kartu kredit jika karyawan telah diberhentikan.

Pilih satu atau beberapa transaksi kartu kredit, lalu pilih **tetapkan ulang transaksi**. Selanjutnya Anda dapat memilih karyawan lain untuk ditetapkan transaksi kartu kredit. Setelah transaksi kartu kredit telah dipindahkan, mereka dapat dipilih untuk laporan pengeluaran dan dibayar melalui proses biasa untuk penggantian laporan pengeluaran.

## <a name="delete-credit-card-transactions"></a>Menghapus transaksi kartu kredit 

Terkadang, setelah transaksi kartu kredit diimpor, transaksi tertentu mungkin harus dihapus. Hal ini dapat dikarenakan transaksi merupakan duplikat atau karena data mungkin tidak akurat. Admin dapat menggunakan fitur **"Hapus transaksi kartu kredit"** untuk memilih dan menghapus transaksi kartu kredit yang **tidak dilampirkan** ke laporan pengeluaran. 

1. Buka **tugas Periodik** > **hapus transaksi kartu kredit**.
2. Pilih **Filter** dan berikan informasi untuk mengidentifikasi rekaman yang akan disertakan.
3. Pilih **OK** untuk menghapus rekaman. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
