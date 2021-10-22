---
title: Mengkonfigurasi retensi vendor
description: Topik ini menjelaskan cara mengkonfigurasi retensi vendor.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594598"
---
# <a name="set-up-vendor-retention"></a>Mengkonfigurasi retensi vendor

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini memberikan informasi tentang cara mengkonfigurasi retensi vendor.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Mengkonfigurasikan akun retensi vendor dalam buku besar umum

1. Dalam Dynamics 365 Finance, buka **Buku besar Umum** > **konfigurasi Posting** > **Akun untuk transaksi otomatis**.
2. Tambah baris baru.
3. Pada bidang **Jenis posting**, pilih **Retensi Vendor**.
4. Pilih akun utama untuk posting retensi vendor.

## <a name="create-vendor-retention-terms"></a>Membuat persyaratan retensi vendor

Gunakan halaman **persyaratan retensi Vendor** untuk mengkonfigurasikan dan mempertahankan persyaratan retensi untuk pembayaran vendor. Masukkan persentase pembayaran vendor untuk dipertahankan dan persentase jumlah dipertahankan sebelumnya untuk rilis. Jumlah akan disimpan secara otomatis pada faktur vendor hingga kontrak mencapai status penyelesaian yang ditentukan. Setelah persyaratan retensi ditetapkan untuk vendor, Anda dapat menerapkannya ke proyek tempat vendor bekerja.

1. Di Finance, buka **Manajemen proyek dan akuntansi** > **Konfigurasi** > **Retensi** > **Persyaratan retensi pembayaran vendor**.
2. Pilih **baru** untuk menambahkan persyaratan retensi vendor baru. Nilai pada bidang **ID Aturan** untuk istilah baru akan secara otomatis dimasukkan. 
3. Di bidang **Deskripsi**, masukkan nama deskriptif untuk istilah baru.
4. Pada tab  **Persyaratan**  pilih  **Tambah baris**  untuk memasukkan masa berlaku retensi vendor.
5. Dalam Bidang  **Persentase unit yang dikirim**  masukkan persentase penyelesaian untuk aturan. Jumlah disimpan secara otomatis pada faktur vendor hingga tahapan penyelesaian proyek sama dengan persentase yang Anda masukkan. Misalnya, jika Anda memasukkan 50,00, jumlah ditahan hingga proyek 50 persen selesai.
6. Dalam Bidang  **Persentase untuk dipertahankan**  masukkan persentase jumlah faktur vendor untuk dipertahankan. Contohnya, jika Anda memasukkan 10,00 di bidang ini, 10 persen dari jumlah pada faktur vendor dipertahankan hingga proyek mencapai persentase penyelesaian yang Anda pilih dalam Bidang  **Persentase unit terkirim**.
7. Di bidang  **Persentase untuk dilepas**  masukkan persentase dari jumlah yang dipertahankan sebelumnya untuk dirilis pada tingkat penyelesaian proyek yang dipilih.

> [!NOTE]
> Jika Anda memiliki lebih dari satu tahap untuk berbagai tingkat penyelesaian proyek, masukkan baris masa berlaku retensi vendor terpisah untuk setiap aturan retensi. Setiap baris dapat menentukan persentase yang berbeda untuk dipertahankan dan persentase yang berbeda untuk dirilis untuk setiap tingkat penyelesaian proyek yang ditetapkan.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Mengkonfigurasi perjanjian vendor untuk proyek

Konfigurasikan persyaratan retensi vendor yang berlaku untuk proyek. Persyaratan retensi vendor juga ditampilkan pada pesanan pembelian yang Anda buat untuk vendor.

1. Di Finance, buka **Manajemen proyek dan akuntansi** > **Proyek** > **Semua Proyek**. 
2. Pilih proyek, dan di Panel Tindakan, pilih **Grup proyek** > **perjanjian Vendor**.
3. Pada halaman **perjanjian Vendor**, tambahkan baris baru.
4. Di bidang **kode akun**, pilih salah satu pilihan berikut:
   - **Tabel**: persyaratan retensi vendor berlaku untuk satu vendor.
   - **Grup**: persyaratan retensi vendor berlaku untuk semua vendor dalam grup vendor.
   - **Semua**: persyaratan retensi vendor berlaku untuk semua vendor.
5. Di bidang **vendor/grup vendor**, pilih vendor atau grup vendor yang menerapkan persyaratan retensi vendor. Jika Anda memilih  **semua**  di langkah sebelumnya, bidang ini tidak tersedia.
6. Pada bidang **persyaratan retensi Vendor**, pilih ID aturan untuk persyaratan retensi yang akan diterapkan ke vendor ini.

