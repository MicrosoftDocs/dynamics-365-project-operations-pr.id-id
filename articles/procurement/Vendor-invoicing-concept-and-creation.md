---
title: Buat faktur vendor
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
# <a name="create-vendor-invoices"></a>Buat faktur vendor

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menggunakan fungsi yang dijelaskan di artikel ini, Anda harus mengaktifkan fitur **Aktifkan pemrosesan aktual subkontrak dengan Project Operations untuk skenario berbasis sumber daya** di ruang kerja **manajemen Fitur**.

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat digunakan untuk merekam biaya dari pelaksanaan layanan dan/atau bahan pada proyek yang diselesaikan oleh vendor.

Bila layanan dan/atau materi disubkontrakkan ke vendor, subkontrak menunjukkan perjanjian kontraktual dengan vendor tersebut. Saat vendor memberikan layanan atau sebagai bahan diterima dan digunakan pada tugas proyek, biaya dicatat pada proyek. Vendor kemudian secara periodik mengirimkan faktur. Faktur-faktur tersebut diverifikasi dan sesuai dengan biaya yang dicatat pada proyek. Setelah proses verifikasi selesai, faktur vendor dikonfirmasi dan dirilis untuk pembayaran.

## <a name="scenarios-for-use"></a>Skenario untuk penggunaan

Faktur vendor dalam Project Operations dapat digunakan untuk mendukung dua skenario yang berbeda:

- Pelanggan menggunakan pengalaman subkontrak lengkap.
- Pelanggan tidak menggunakan pengalaman subkontrak lengkap tetapi ingin memiliki tampilan terpadu biaya pada proyek di Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak lengkap

Pengalaman faktur vendor memberikan cara memverifikasi entri waktu, penggunaan bahan, dan pengeluaran yang mereferensikan komponen, dan mencocokkannya dengan baris faktur vendor. Proses ini dapat digunakan untuk memverifikasi keakuratan baris faktur vendor. Setelah proses verifikasi selesai dan faktur vendor dikonfirmasi, sistem membalikkan aktual yang direkam menurut log waktu, pengeluaran, dan penggunaan bahan yang disetujui, kemudian membuat aktual biaya baru menggunakan baris faktur vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak lengkap tetapi ingin memiliki tampilan terpadu biaya pada proyek di Project Operations

Jika Anda melacak proses subkontrak dalam sistem pihak ketiga, Anda dapat merekam biaya dari sistem pihak ketiga tersebut ke Project Operations dengan membuat faktur vendor yang tidak mereferensikan subkontrak. Dengan cara ini, manajer proyek Anda dapat memiliki satu tampilan terpadu dari semua biaya pada proyek tertentu.

## <a name="create-vendor-invoices-in-project-operations"></a>Buat faktur vendor di Project Operations

Faktur vendor dibuat di Dynamics 365 Finance, menggunakan modul **utang dagang**. Anda tidak dapat membuat faktur vendor secara langsung di Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Mengkonfigurasi verifikasi faktur vendor

Jika faktur vendor ditujukan untuk subkontrak di Dataverse, Anda harus mengaktifkan parameter **verifikasi Manual oleh PM diperlukan**. Pengaturan pilihan menentukan apakah faktur vendor harus secara otomatis dikonfirmasi di Dataverse, atau apakah memerlukan konfirmasi manual. Header dari setiap faktur vendor proyek mencakup pilihan nama yang sama. Secara default, pilihan di header semua faktur vendor proyek diatur ke nilai yang Anda tetapkan di sini. Namun, Anda dapat memperbarui nilai sebagaimana diperlukan di header faktur vendor individual.

Jika pilihan diatur ke **Ya**, faktur vendor yang dibuat di Finance dan disinkronisasikan ke Dataverse memiliki status **Draf**. Selanjutnya faktur harus divalidasi dan diperiksa oleh manajer proyek, dan dikonfirmasikan, sebelum diproses dan diposting ke akun proyek dan buku kas yang spesifik di Finance.

Jika pilihan diatur ke **Tidak**, faktur vendor akan secara otomatis dikonfirmasi. Tidak diperlukan tindakan lebih lanjut.

Ikuti langkah-langkah ini untuk mengatur verifikasi faktur vendor.

1. Di Finance, buka **manajemen proyek dan akuntansi** \> **konfigurasi** \> **parameter manajemen proyek dan akuntansi**.
1. Pada tab **Finance**, atur opsi **Diperlukan verifikasi Manual oleh PM** ke **Ya** jika kebijakan perusahaan memerlukan verifikasi faktur vendor subkontraktor. Jika verifikasi oleh manajer proyek tidak diperlukan di Dataverse, biarkan rangkaian pilihan di **Tidak**. Secara default, pengaturan akan digunakan pada halaman **faktur vendor Tertunda**.

> [!NOTE]
> Faktur vendor yang dibuat untuk subkontrak di Dataverse dapat diproses dengan benar hanya jika opsi **Diperlukan verifikasi Manual oleh PM** diatur ke **Ya**. Aktual waktu, bahan, dan biaya pengeluaran yang dibuat subkontraktor dapat secara manual diimbangi dengan baris faktur vendor oleh manajer proyek hanya jika pilihan ini diatur ke **Ya**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Mengkonfigurasi akun integrasi pengadaan untuk faktur vendor

Ketika faktur vendor diposting di Finance untuk Project Operations – Lingkungan terintegrasi (non-stok), data keuangan dikirim ke akun integrasi pengadaan. Sistem menghasilkan aktual di Dataverse untuk faktur yang diposting. Aktual ini diposting di Finance dengan menggunakan jurnal integrasi Proyek. Mem-posting jurnal integrasi Proyek akan memposting biaya aktual dan membalik akun integrasi Pengadaan.

Untuk mengkonfigurasi akun integrasi pengadaan untuk faktur vendor, ikuti langkah-langkah berikut ini.

1. Di Finance, buka **manajemen proyek dan akuntansi** \> **konfigurasi** \> **parameter manajemen proyek dan akuntansi**.
1. Pada tab **Project Operations pada Dynamics 365 Customer Engagement**, pilih **Bahan** \> **akun integrasi Pengadaan**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Membuat dan memposting faktur vendor subkontrak

Ketika petugas utang dagang menerima faktur dari subkontraktor, faktur baru dibuat di finance.

1. Di Finance, buka **utang dagang** \> **Faktur** \> **faktur vendor yang tertunda**.
1. Pada **Panel Tindakan**, pilih **Baru** untuk membuat faktur vendor.
1. Pada header faktur, di bidang **akun Faktur**, pilih **Subkontraktor**.
1. Pilih tanggal faktur.
1. Pada tab **Header**, atur pilihan **Diperlukan Verifikasi Manual oleh PM** ke **Ya**. Pengaturan default pilihan ini berasal dari halaman **parameter manajemen proyek dan akuntansi**. Namun, ini dapat diubah pada tingkat faktur vendor.
1. Di FastTab **baris faktur**, pilih **Tambah baris** untuk membuat baris faktur vendor.
1. Pilih kategori pembelian yang dibuat untuk baris subkontrak, lalu masukkan harga unit, satuan pengukuran, dan kuantitas.
1. Di bagian baris faktur vendor, pada tab **Proyek**, pilih proyek yang dibagikan faktur subkontraknya oleh subkontraktor.
1. Pilih kategori proyek. Item dapat dari jenis **Item**, **Pengeluaran**, **Bahan**, atau **Jam**.
1. Pilih peran hanya jika kategori proyek yang dipilih adalah dari jenis **Jam**.
1. Pilih **Posting** untuk memposting faktur vendor.

Atau, Anda dapat membuat faktur vendor dengan membuka **utang dagang** \> **Faktur** \> **Buka faktur vendor** dan memilih **Baru**.

Ketika faktur vendor diposting, faktur menjadi tersedia di Dataverse untuk verifikasi dan pemrosesan manajer proyek.

## <a name="vendor-invoice-processing-in-dataverse"></a>Pemrosesan faktur Vendor di Dataverse

Di faktur vendor yang dibuat dalam Dataverse, beberapa nilai bidang berasal dari faktur vendor yang dicatat di Finance. Nilai lain adalah nilai default yang berasal dari subkontrak.

Bidang berikut dan rekaman terkait akan disalin dari subkontrak ke header faktur vendor:

- Mata uang
- Unit Kontrak
- Syarat Pembayaran

Di baris faktur vendor, Project Operations menggunakan nilai bidang berikut untuk memasukkan referensi baris subkontrak dan subkontrak default:

- Kelas Transaksi
- Peran
- Kategori Transaksi
- Bidang Produk
- Project
- Tugas

> [!NOTE]
> Baris subkontrak harga tetap tidak didukung di Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
