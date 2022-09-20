---
title: Membuat faktur vendor
description: Artikel ini menjelaskan konsep faktur vendor dan menjelaskan cara membuatnya di Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475468"
---
# <a name="create-vendor-invoices"></a>Membuat faktur vendor

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menggunakan fungsionalitas yang dijelaskan dalam artikel ini, Anda harus mengaktifkan **fitur Aktifkan pemrosesan aktual subkontrak dengan Operasi Proyek untuk skenario** berbasis sumber daya di **ruang kerja Manajemen** fitur.

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat digunakan untuk mencatat biaya dari pengiriman layanan dan/atau materi pada proyek yang diselesaikan oleh vendor.

Ketika layanan dan/atau materi disubkontrakkan ke vendor, subkontrak mewakili perjanjian kontraktual dengan vendor tersebut. Saat vendor memberikan layanan, atau saat materi diterima dan digunakan pada tugas proyek, biaya dicatat pada proyek. Vendor kemudian secara berkala mengirimkan faktur. Faktur tersebut diverifikasi dan dicocokkan dengan biaya yang dicatat pada proyek. Setelah proses verifikasi selesai, faktur vendor dikonfirmasi dan dirilis untuk pembayaran.

## <a name="scenarios-for-use"></a>Skenario untuk digunakan

Faktur vendor dalam Project Operations dapat digunakan untuk mendukung dua skenario berbeda:

- Pelanggan menggunakan pengalaman subkontrak penuh.
- Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin memiliki tampilan terpadu tentang biaya pada proyek di Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman faktur vendor menyediakan cara untuk memverifikasi entri waktu, penggunaan material, dan entri pengeluaran yang mereferensikan komponen yang disubkontrakkan, dan mencocokkannya dengan baris faktur vendor. Proses ini dapat digunakan untuk memverifikasi keakuratan baris faktur vendor. Setelah proses verifikasi selesai dan faktur vendor dikonfirmasi, sistem membalikkan aktual yang dicatat oleh waktu, pengeluaran, dan log penggunaan material yang disetujui, dan kemudian membuat aktual biaya baru dengan menggunakan baris faktur vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin memiliki tampilan terpadu tentang biaya pada proyek di Project Operations

Jika Anda melacak proses subkontrak dalam sistem pihak ketiga, Anda dapat mencatat biaya dari sistem pihak ketiga tersebut ke Operasi Proyek dengan membuat faktur vendor yang tidak mereferensikan subkontrak. Dengan cara ini, manajer proyek Anda dapat memiliki satu tampilan terpadu dari semua biaya pada proyek tertentu.

## <a name="create-vendor-invoices-in-project-operations"></a>Membuat faktur vendor di Project Operations

Faktur vendor dibuat dalam Dynamics 365 Finance, dengan **menggunakan modul Hutang** dagang. Anda tidak dapat membuat faktur vendor secara langsung di Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Menyiapkan verifikasi faktur vendor

Jika faktur vendor ditujukan untuk subkontrak di Dataverse, Anda harus mengaktifkan **verifikasi Manual oleh PM diperlukan** parameter. Pengaturan opsi menentukan apakah faktur vendor harus dikonfirmasi secara otomatis di Dataverse, atau apakah itu memerlukan konfirmasi manual. Header setiap faktur vendor proyek menyertakan opsi dengan nama yang sama. Secara default, opsi pada header semua faktur vendor proyek diatur ke nilai yang Anda tetapkan di sini. Namun, Anda dapat memperbarui nilai seperti yang diperlukan pada header faktur vendor individual.

Jika opsi diatur ke **Ya, faktur vendor yang dibuat di Keuangan dan disinkronkan memiliki** Dataverse status **Draf**. Faktur kemudian harus divalidasi dan diverifikasi oleh manajer proyek, dan dikonfirmasi, sebelum diproses dan diposting ke akun proyek dan buku besar tertentu di Keuangan.

Jika opsi diatur ke **Tidak**, faktur vendor akan dikonfirmasi secara otomatis. Tidak diperlukan tindakan lebih lanjut.

Untuk menyiapkan verifikasi faktur vendor, ikuti langkah-langkah berikut.

1. Di Keuangan, buka **Manajemen proyek dan akuntansi** \> **Setup** \> **Manajemen proyek dan parameter** akuntansi.
1. Pada tab **Keuangan**, atur **opsi Verifikasi manual oleh PM diperlukan** ke **Ya** jika kebijakan perusahaan memerlukan verifikasi faktur vendor subkontraktor. Jika verifikasi oleh manajer proyek tidak diperlukan, Dataverse biarkan rangkaian pilihan ke **Tidak**. Secara default, pengaturan akan digunakan pada **halaman Faktur** vendor tertunda.

> [!NOTE]
> Faktur vendor yang dibuat untuk subkontrak di Dataverse dapat diproses dengan benar hanya jika **opsi Verifikasi manual oleh PM diperlukan** diatur ke **Ya**. Waktu, materi, dan biaya aktual pengeluaran yang dibuat oleh subkontraktor dapat dicocokkan secara manual dengan baris faktur vendor oleh manajer proyek hanya jika opsi ini diatur ke **Ya**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Menyiapkan akun integrasi pengadaan untuk faktur vendor

Ketika faktur vendor diposting di Keuangan untuk Operasi Proyek – Lingkungan terintegrasi (non-stok), keuangan diposting ke akun integrasi Pengadaan. Sistem menghasilkan aktual untuk Dataverse faktur yang diposting. Aktual ini diposting di Keuangan dengan menggunakan jurnal integrasi Proyek. Posting jurnal integrasi Proyek memposting biaya aktual dan membalikkan akun integrasi Pengadaan.

Untuk menyiapkan akun integrasi Pengadaan untuk faktur vendor, ikuti langkah-langkah berikut.

1. Di Keuangan, buka **Manajemen proyek dan akuntansi** \> **Setup** \> **Manajemen proyek dan parameter** akuntansi.
1. Pada operasi **proyek pada tab keterlibatan** pelanggan Dynamics 365, pilih **akun** integrasi Pengadaan Material \>**·**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Membuat dan memposting faktur vendor subkontrak

Ketika petugas hutang Akun menerima faktur dari subkontraktor, faktur baru dibuat di Keuangan.

1. Di Keuangan, buka **Faktur** \> **hutang** \> **dagang Faktur Menunggu faktur vendor**.
1. **Pada Panel** Tindakan, pilih **Baru** untuk membuat faktur vendor.
1. Pada header faktur, di **bidang Akun faktur**, pilih **Subkontraktor**.
1. Pilih tanggal faktur.
1. Pada tab **Header**, atur **opsi Verifikasi manual menurut PM diperlukan** ke **Ya**. Pengaturan default opsi ini berasal dari **halaman Manajemen proyek dan parameter** akuntansi. Namun, itu dapat diubah pada tingkat faktur vendor.
1. **Pada baris** Faktur FastTab, pilih **Tambahkan baris** untuk membuat baris faktur vendor.
1. Pilih kategori pengadaan yang dibuat untuk garis subkontrak, dan masukkan harga satuan, satuan pengukuran, dan kuantitas.
1. Di bagian baris faktur vendor, pada **tab Proyek**, pilih proyek yang digunakan oleh subkontraktor untuk berbagi faktur subkontrak.
1. Pilih kategori proyek. Ini bisa dari semua jenis Barang, Pengeluaran, Bahan, atau **Jam**.**·** **·** **·**
1. Pilih peran hanya jika kategori proyek yang dipilih adalah dari **jenis Jam**.
1. Pilih **Posting** untuk memposting faktur vendor.

Atau, Anda dapat membuat faktur vendor dengan membuka **Faktur** \> **hutang** \> **dagang Buka faktur** vendor dan pilih **Baru.**

Ketika faktur vendor diposting, faktur tersebut akan tersedia Dataverse untuk verifikasi dan pemrosesan manajer proyek.

## <a name="vendor-invoice-processing-in-dataverse"></a>Pemrosesan faktur vendor di Dataverse

Pada vendor invoice yang dibuat di Dataverse, beberapa field value berasal dari vendor invoice yang tercatat di Finance. Nilai lainnya adalah nilai default yang berasal dari subkontrak.

Bidang berikut dan catatan terkait akan disalin dari subkontrak ke header faktur vendor:

- Mata uang
- Unit Kontrak
- Syarat Pembayaran

Pada baris faktur vendor, Operasi Proyek menggunakan nilai bidang berikut untuk memasukkan referensi baris subkontrak dan subkontrak default:

- Kelas Transaksi
- Peran
- Kategori Transaksi
- Bidang produk
- Project
- Tugas

> [!NOTE]
> Jalur subkontrak harga tetap tidak didukung dalam Operasi Proyek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
