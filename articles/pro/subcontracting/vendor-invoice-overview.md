---
title: Faktur vendor - Konsep dan pembuatan
description: Artikel ini menjelaskan konsep faktur vendor, skenario penggunaan, dan cara membuat faktur vendor di Microsoft Dynamics 365 Project Operations.
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

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat digunakan untuk merekam biaya dari pelaksanaan layanan dan/atau bahan pada proyek oleh vendor.

Bila layanan dan/atau materi disubkontrakkan ke vendor, subkontrak menunjukkan perjanjian kontraktual dengan vendor tersebut. Saat vendor memberikan layanan atau bahan diterima dan digunakan pada tugas proyek, biaya dicatat pada proyek. Secara periodik, vendor mengirimkan faktur yang terverifikasi dan sesuai dengan biaya yang dicatat pada proyek. Setelah proses verifikasi selesai, faktur vendor dikonfirmasi dan dirilis untuk pembayaran.

## <a name="scenarios-for-use"></a>Skenario untuk penggunaan

Faktur vendor dalam Project Operations dapat digunakan untuk mendukung dua skenario yang berbeda.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Pelanggan menggunakan pengalaman subkontrak lengkap

Pengalaman faktur vendor memberikan cara memverifikasi dan mencocokkan entri waktu, penggunaan bahan, dan pengeluaran yang mereferensikan komponen subkontrak dengan baris faktur vendor. Proses ini dapat digunakan untuk memverifikasi keakuratan baris faktur vendor. Setelah proses verifikasi selesai dan faktur vendor dikonfirmasi, aplikasi akan membalikkan aktual yang direkam menurut log waktu, pengeluaran, dan penggunaan bahan yang disetujui, dan membuat aktual biaya baru menggunakan baris faktur vendor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Pelanggan tidak menggunakan pengalaman subkontrak lengkap tetapi ingin memiliki tampilan terpadu biaya pada proyek di Project Operations

Jika Anda melacak proses subkontrak dalam sistem pihak ketiga, Anda dapat merekam biaya dari sistem pihak ketiga tersebut ke Project Operations dengan membuat faktur vendor yang tidak mereferensikan subkontrak. Dengan cara ini, manajer proyek Anda dapat memiliki satu tampilan terpadu dari semua biaya pada proyek tertentu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Pembuatan faktur vendor di Project Operations

faktur vendor dapat dibuat dalam dua cara:

- Dari halaman daftar faktur vendor atau halaman rincian untuk satu faktur vendor
- Dari halaman daftar subkontrak atau halaman rincian untuk satu subkontrak

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Pembuatan dari halaman daftar faktur vendor atau halaman rincian

1. Buka **pembelian** \> **faktur Vendor**.
2. Pada halaman daftar faktur vendor atau halaman rincian untuk satu faktur vendor, pilih **Baru** untuk membuat faktur vendor baru.

Faktur vendor yang dibuat dengan cara ini juga dapat mereferensikan subkontrak.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Pembuatan dari halaman daftar subkontrak atau halaman rincian

1. Buka **Pembelian** \> **Subkontrak.**
2. Pilih satu atau beberapa subkontrak.
3. Pada halaman daftar subkontrak atau halaman rincian untuk satu subkontrak, pilih **Buat faktur vendor** untuk membuat faktur vendor baru.

Faktur vendor baru dalam status **Draf** dibuat untuk setiap subkontrak yang Anda pilih.

Faktur vendor yang Anda buat dengan cara ini selalu mereferensikan subkontrak pada header faktur vendor. Setiap baris pada subkontrak yang memiliki metode penagihan Waktu dan bahan akan menyebabkan baris dibuat pada faktur vendor. Setiap baris pada subkontrak yang memiliki metode penagihan harga tetap akan menyebabkan baris dibuat pada faktur vendor untuk setiap tahapan baris subkontrak yang memiliki status **Siap untuk faktur**.

Bidang berikut dan rekaman terkait akan disalin dari subkontrak ke header faktur vendor:

- Vendor.
- Daftar harga terkait akan disalin ke faktur vendor sebagai daftar harga.
- Mata Uang.
- Unit Kontrak.
- Persyaratan Pembayaran.

Untuk baris subkontrak Waktu dan bahan, bidang berikut, dan rekaman terkait akan disalin dari baris subkontrak ke baris faktur vendor:

- Referensi baris subkontrak dan subkontrak
- Kelas Transaksi
- Peran
- Kategori Transaksi
- Bidang Produk
- Project
- Tugas
- Sumber daya yang dapat dipesan

Untuk baris subkontrak harga tetap, bidang berikut akan disalin dari baris subkontrak dan tahapan baris subkontrak ke baris faktur vendor:

- Referensi baris subkontrak dan subkontrak.
- Kelas Transaksi. Secara default, nilai akan menjadi **Tahapan**.
- Nama dan jumlah tahapan akan disalin dari tahapan baris subkontrak terkait.
- Pengguna akan dapat memilih proyek dan tugas di baris faktur vendor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
