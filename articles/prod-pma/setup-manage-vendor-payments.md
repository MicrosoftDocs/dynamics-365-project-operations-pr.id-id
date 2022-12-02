---
title: Mengonfigurasi dan menggunakan pembayaran vendor "bayar jika dibayar"
description: Artikel ini menjelaskan cara membuat persyaratan bayar-saat berbayar (PWP) sehingga anda dapat merilis sebagian pembayaran vendor, berdasarkan pembayaran pelanggan.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 10e8e57695caece6c4b6ba4c2ddb52395dad1218
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920754"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Mengonfigurasi dan menggunakan pembayaran vendor "bayar jika dibayar"

[!include [banner](../includes/banner.md)]

Bila Anda menyetujui vendor untuk bekerja sebagai subkontraktor, Anda mungkin ingin menahan pembayaran ke Penjual hingga pelanggan membayar Anda untuk proyek tersebut. Untuk mendukung skenario ini, Anda dapat mengkonfigurasi persyaratan bayar-saat dibayar (PWP) saat mengkonfigurasi pesanan pembelian (PO) dengan vendor.

Misalnya, bila pelanggan membayar sejumlah faktur proyek, Anda dapat memberikan sebagian atau semua jumlah faktur vendor. Cukup Konfigurasikan persyaratan PWP yang menentukan bahwa vendor akan dibayar setelah Anda menerima persentase pembayaran yang terkait dari pelanggan. Jika Anda menerima pembayaran parsial dari pelanggan, Anda dapat secara manual menerbitkan beberapa faktur terkait vendor untuk pembayaran.

Contoh berikut menguraikan proses saat persyaratan PWP digunakan.

## <a name="example"></a>Contoh

Organisasi Anda setuju untuk menyediakan untuk pelanggan 100 komputer yang telah diinstal perangkat lunak, dengan harga 150,00 dolar AS (USD) per komputer. Anda kemudian menyewa vendor untuk menyediakan komputer yang memiliki perangkat lunak diinstal. Berdasarkan perjanjian, pelanggan harus menyetujui kualitas komputer sebelum membayar organisasi Anda. Kebijakan organisasi Anda adalah menahan pembayaran ke vendor hingga pelanggan membayar Anda. Oleh karena itu, Anda mengkonfigurasi proyek sehingga memiliki persentase PWP 100 persen.

Vendor mengirimi Anda 100 komputer yang memiliki perangkat lunak terinstal, bersama dengan faktur untuk 10.000,00 USD. Karena persyaratan PWP diatur untuk proyek Anda, Anda tidak membayar vendor setelah menerima komputer. Namun, Anda mengirim komputer ke pelanggan, bersama dengan faktur senilai 15.000,00. Pelanggan memeriksa komputer dan menyetujui jumlah penuh faktur proyek.

Setelah Anda menerima pembayaran penuh dari pelanggan, Anda membayar vendor 10.000,00, jumlah penuh faktur vendor.

## <a name="set-up-pwp-terms-for-a-project"></a>Konfigurasikan persyaratan PWP untuk proyek

Saat Anda menyiapkan persyaratan PWP untuk suatu proyek, Anda harus menentukan, sebagai persentase, jumlah minimum yang harus dibayar pelanggan untuk proyek sebelum Anda akan membayar vendor. Jumlah ambang batas secara otomatis dihitung pada faktur pelanggan untuk proyek. Ikuti langkah-langkah berikut untuk menyiapkan persentase ambang batas untuk persyaratan PWP.

1. Buka **manajemen proyek dan akuntansi** \> **proyek** \> **Semua proyek**.
2. Cari dan buka proyek yang ingin Anda konfigurasikan persyaratan PWP-nya.
3. Pada fasttab **perjanjian vendor**, pilih **Tambah baris**.
3. Di bidang **kode akun**, pilih salah satu pilihan berikut:

    - **Tabel** – persyaratan PWP berlaku untuk satu vendor.
    - **Grup**– persyaratan PWP berlaku untuk semua vendor dalam grup vendor.
    - **Semua** – persyaratan PWP berlaku untuk semua vendor.

4. Jika Anda memilih **tabel** atau **grup** dalam langkah sebelumnya, di bidang **grup vendor/vendor**, pilih vendor atau grup Penjual yang menerapkan persyaratan PWP. Jika Anda memilih **semua** di langkah sebelumnya, bidang **grup vendor/vendor** tidak dapat diedit.
5. Jika persyaratan retensi vendor diatur untuk vendor dalam proyek, di bidang **persyaratan retensi vendor**, pilih id aturan untuk persyaratan retensi.
6. Di bidang **persentase ambang PWP**, masukkan persentase ambang batas untuk proyek. Persentase yang Anda masukkan untuk proyek menentukan jumlah minimum yang harus dibayar pelanggan sebelum Anda akan membayar vendor.

## <a name="create-a-po-that-has-pwp-terms"></a>Membuat PO yang memiliki persyaratan PWP

Bila Anda memposting faktur dari vendor, jika vendor tunduk pada persyaratan PWP, persyaratan tersebut akan ditampilkan pada baris PO. Untuk membuat PO yang memiliki persyaratan PWP, ikuti langkah berikut.

1. Buka **pengadaan dan pembekalan** \> **pesanan pembelian** \> **semua pesanan pembelian**.
2. Pada panel tindakan, pilih **Baru**. Kemudian, di kotak dialog **buat pesanan pembelian**, masukkan informasi yang diperlukan, dan pilih **OK**.

    Atau, buka PO yang ada pada halaman daftar **semua pesanan pembelian**.

4. Pada halaman **pesanan pembelian**, di fasttab **baris pesanan pembelian**, Tinjau rincian baris PO untuk vendor. Pilihan **bayar saat berbayar** dipilih secara otomatis, dan nilai di bidang **persentase ambang PWP** secara otomatis disalin dari bidang **persentase ambang PWP** di halaman **proyek**.
6. Jika Anda tidak ingin menerapkan persyaratan PWP ke vendor untuk baris PO, kosongkan pilihan **bayar saat berbayar**. Dalam kasus ini, bidang **persentase ambang PWP** untuk baris PO akan diatur ulang ke 0 (nol).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Memperbarui pembayaran pelanggan dan membayar vendor

Bila vendor menyelesaikan tugasnya dalam proyek dan mengirimkan faktur, Anda harus meninjau status proyek dan faktur pelanggan untuk menentukan apakah persyaratan PWP telah dipenuhi untuk proyek. Jika persyaratan PWP untuk vendor terpenuhi, Anda dapat menentukan baris pada faktur vendor untuk membayar, berdasarkan pembayaran pelanggan untuk proyek. Jika Anda memutuskan untuk membayar vendor meskipun persyaratan PWP tidak terpenuhi, Anda dapat menimpa persyaratan PWP pada halaman **faktur vendor dengan bayar saat dibayar**.

1. Buka **manajemen proyek dan akuntansi** \> **pertanyaan dan laporan** \> **permintaan retensi** \> **Faktur dengan pembayaran saat dibayar**.
2. Pada halaman **faktur vendor dengan bayar saat dibayar**, di bidang pencarian, masukkan nilai untuk menemukan faktur vendor yang ingin Anda tinjau, lalu pilih **Cari**.
3. Pada fasttab **baris faktur vendor**, pilih baris yang akan diubah.
4. Jika **syarat bayar saat dibayar** terpenuhi untuk baris faktur, pilih **Lakukan pembayaran vendor**. Opsi **bayar saat dibayar** dikosongkan, dan nilai bidang **siap untuk pembayaran** diubah ke **ya**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]