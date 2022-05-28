---
title: Faktur vendor - Konsep dan pembuatan
description: Ini topik menjelaskan konsep faktur vendor, skenario untuk digunakan, dan cara membuat faktur vendor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580552"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Faktur vendor - Konsep dan pembuatan

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat digunakan untuk mencatat biaya dari pengiriman layanan dan/atau materi pada proyek oleh vendor.

Ketika layanan dan/atau materi disubkontrakkan ke vendor, subkontrak mewakili perjanjian kontraktual dengan vendor tersebut. Sebagai vendor memberikan layanan, atau bahan yang diterima dan digunakan pada tugas-tugas proyek, biaya dicatat pada proyek. Secara berkala, vendor mengirimkan faktur yang diverifikasi dan dicocokkan dengan biaya yang dicatat pada proyek. Setelah proses verifikasi selesai, faktur vendor dikonfirmasi dan dirilis untuk pembayaran.

## <a name="scenarios-for-use"></a>Skenario untuk digunakan

Faktur vendor dalam Operasi Proyek dapat digunakan untuk mendukung dua skenario berbeda.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman faktur vendor menyediakan cara untuk memverifikasi dan mencocokkan entri waktu, penggunaan material, dan entri pengeluaran yang merujuk komponen subkontrak dengan baris faktur vendor. Proses ini dapat digunakan untuk memverifikasi keakuratan baris faktur vendor. Setelah proses verifikasi selesai dan faktur vendor dikonfirmasi, aplikasi akan membalikkan aktual yang dicatat oleh catatan waktu, biaya, dan penggunaan material yang disetujui, dan membuat aktual biaya baru dengan menggunakan jalur faktur vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin memiliki pandangan terpadu tentang biaya pada proyek-proyek dalam Operasi Proyek

Jika Anda melacak proses subkontrak dalam sistem pihak ketiga, Anda dapat mencatat biaya dari sistem pihak ketiga tersebut ke Operasi Proyek dengan membuat faktur vendor yang tidak merujuk subkontrak. Dengan cara ini, manajer proyek Anda dapat memiliki pandangan tunggal dan terpadu tentang semua biaya pada proyek tertentu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Pembuatan faktur vendor dalam Operasi Proyek

Faktur vendor dapat dibuat dengan dua cara:

- Dari halaman daftar faktur vendor atau halaman detail untuk faktur vendor tunggal
- Dari halaman daftar subkontrak atau halaman detail untuk satu subkontrak

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Pembuatan dari halaman daftar faktur vendor atau halaman detail

1. Buka **Faktur Penjual Pembelian** \> **·**.
2. Pada halaman daftar faktur vendor atau halaman detail untuk faktur vendor tunggal, pilih **Baru** untuk membuat faktur vendor baru.

Faktur vendor yang dibuat dengan cara ini juga dapat merujuk subkontrak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Pembuatan dari halaman daftar subkontrak atau halaman detail

1. Pergi ke **Pembelian** \> **Subkontrak.**
2. Pilih satu atau beberapa subkontrak.
3. Pada halaman daftar subkontrak atau halaman detail untuk satu subkontrak, pilih **Buat faktur** vendor untuk membuat faktur vendor baru.

Faktur vendor baru dalam **status Draf** dibuat untuk setiap subkontrak yang Anda pilih.

Faktur vendor yang Anda buat dengan cara ini selalu mereferensikan subkontrak pada header faktur vendor. Setiap baris pada subkontrak yang memiliki metode penagihan Waktu dan material akan menyebabkan garis dibuat pada faktur vendor. Setiap baris pada subkontrak yang memiliki metode penagihan harga Tetap akan menyebabkan garis dibuat pada faktur vendor untuk setiap tonggak jalur subkontrak yang memiliki status **Siap untuk faktur**.

Bidang berikut dan catatan terkait akan disalin dari subkontrak ke header faktur vendor:

- Penjual.
- Daftar harga terkait akan disalin ke faktur vendor sebagai daftar harga.
- Mata Uang.
- Unit kontraktor.
- Persyaratan pembayaran.

Untuk waktu dan jalur subkontrak material, bidang berikut dan catatan terkait akan disalin dari jalur subkontrak ke baris faktur vendor:

- Referensi subkontrak dan subkontrak jalur
- Kelas Transaksi
- Peran
- Kategori Transaksi
- Bidang produk
- Project
- Tugas
- Sumber daya yang dapat dipesan

Untuk jalur subkontrak harga tetap, bidang berikut akan disalin dari jalur subkontrak dan tonggak jalur subkontrak ke jalur faktur vendor:

- Referensi subkontrak dan subkontrak.
- Kelas transaksi. Secara default, nilainya akan menjadi **Milestone**.
- Nama dan jumlah tonggak akan disalin dari tonggak jalur subkontrak terkait.
- Pengguna akan dapat memilih proyek dan tugas pada baris faktur vendor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
