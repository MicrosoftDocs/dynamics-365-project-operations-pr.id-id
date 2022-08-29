---
title: Faktur vendor - Konsep dan pembuatan
description: Artikel ini menjelaskan konsep faktur vendor, skenario untuk digunakan, dan cara membuat faktur vendor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261938"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Faktur vendor - Konsep dan pembuatan

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat digunakan untuk mencatat biaya dari pengiriman layanan dan/atau materi pada proyek oleh vendor.

Ketika layanan dan/atau materi disubkontrakkan ke vendor, subkontrak mewakili perjanjian kontraktual dengan vendor tersebut. Saat vendor memberikan layanan, atau materi diterima dan digunakan pada tugas proyek, biaya dicatat pada proyek. Secara berkala, vendor mengirimkan faktur yang diverifikasi dan dicocokkan dengan biaya yang dicatat pada proyek. Setelah proses verifikasi selesai, faktur vendor dikonfirmasi dan dirilis untuk pembayaran.

## <a name="scenarios-for-use"></a>Skenario untuk digunakan

Faktur vendor dalam Operasi Proyek dapat digunakan untuk mendukung dua skenario berbeda.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak penuh

Pengalaman faktur vendor menyediakan cara untuk memverifikasi dan mencocokkan entri waktu, penggunaan material, dan entri pengeluaran yang mereferensikan komponen yang disubkontrakkan dengan baris faktur vendor. Proses ini dapat digunakan untuk memverifikasi keakuratan baris faktur vendor. Setelah proses verifikasi selesai dan faktur vendor dikonfirmasi, aplikasi akan membalikkan aktual yang dicatat oleh waktu, pengeluaran, dan log penggunaan material yang disetujui, dan membuat aktual biaya baru dengan menggunakan baris faktur vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak penuh tetapi ingin memiliki tampilan terpadu tentang biaya pada proyek di Project Operations

Jika Anda melacak proses subkontrak dalam sistem pihak ketiga, Anda dapat mencatat biaya dari sistem pihak ketiga tersebut ke Operasi Proyek dengan membuat faktur vendor yang tidak mereferensikan subkontrak. Dengan cara ini, manajer proyek Anda dapat memiliki pandangan tunggal dan terpadu tentang semua biaya pada proyek tertentu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Pembuatan faktur vendor dalam Operasi Proyek

Faktur vendor dapat dibuat dengan dua cara:

- Dari halaman daftar faktur vendor atau halaman detail untuk satu faktur vendor
- Dari halaman daftar subkontrak atau halaman detail untuk satu subkontrak

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Pembuatan dari halaman daftar faktur vendor atau halaman detail

1. **Buka Faktur Vendor Pembelian** \> **·**.
2. Pada halaman daftar faktur vendor atau halaman detail untuk satu faktur vendor, pilih **Baru** untuk membuat faktur vendor baru.

Faktur vendor yang dibuat dengan cara ini juga dapat mereferensikan subkontrak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Pembuatan dari halaman daftar subkontrak atau halaman detail

1. Pergi ke **Pembelian** \> **Subkontrak.**
2. Pilih satu atau beberapa subkontrak.
3. Pada halaman daftar subkontrak atau halaman detail untuk satu subkontrak, pilih **Buat faktur** vendor untuk membuat faktur vendor baru.

Faktur vendor baru dalam **status Draf** dibuat untuk setiap subkontrak yang Anda pilih.

Faktur vendor yang Anda buat dengan cara ini selalu mereferensikan subkontrak pada header faktur vendor. Setiap baris pada subkontrak yang memiliki waktu dan metode penagihan material akan menyebabkan baris dibuat pada faktur vendor. Setiap baris pada subkontrak yang memiliki metode penagihan harga tetap akan menyebabkan baris dibuat pada faktur vendor untuk setiap tonggak baris subkontrak yang memiliki status **Siap untuk faktur**.

Bidang berikut dan catatan terkait akan disalin dari subkontrak ke header faktur vendor:

- Penjual.
- Daftar harga terkait akan disalin ke faktur vendor sebagai daftar harga.
- Mata Uang.
- Unit kontrak.
- Ketentuan pembayaran.

Untuk baris subkontrak Waktu dan material, bidang berikut dan catatan terkait akan disalin dari baris subkontrak ke baris faktur vendor:

- Mensubkontrakkan dan mensubkontrakkan referensi baris
- Kelas Transaksi
- Peran
- Kategori Transaksi
- Bidang produk
- Project
- Tugas
- Sumber daya yang dapat dipesan

Untuk baris subkontrak harga tetap, bidang berikut akan disalin dari baris subkontrak dan tonggak baris subkontrak ke baris faktur vendor:

- Subkontrak dan subkontrak referensi baris.
- Kelas transaksi. Secara default, nilainya adalah **Milestone**.
- Nama dan jumlah milestone akan disalin dari milestone baris subkontrak terkait.
- Pengguna akan dapat memilih proyek dan tugas pada baris faktur vendor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
