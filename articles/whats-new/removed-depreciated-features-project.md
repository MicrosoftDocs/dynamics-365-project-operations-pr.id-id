---
title: Fitur yang dihapus atau tidak digunakan lagi di Dynamics 365 Project Operations
description: Artikel ini menjelaskan fitur yang telah dihapus, atau yang direncanakan untuk dihapus dari Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028333"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Fitur yang dihapus atau tidak digunakan lagi di Dynamics 365 Project Operations

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, Penyebaran Lite - menangani faktur proforma, dan Project Operations untuk skenario berbasis stok/produksi_

Artikel ini menjelaskan fitur yang telah dihapus, atau yang direncanakan untuk dihapus dari Dynamics 365 Project Operations.

- Fitur *yang dihapuskan* tidak akan lagi tersedia di dalam produk.
- Fitur yang *tidak digunakan lagi* tidak dalam pengembangan aktif dan akan dihapus pada pembaruan mendatang.

Daftar ini ditujukan untuk membantu Anda mempertimbangkan penghapusan dan penghentian ini untuk perencanaan Anda.

> [!NOTE]
> Informasi terperinci tentang objek dalam aplikasi keuangan dan operasi dapat ditemukan di [**laporan Referensi teknis**](/dynamics/s-e/global/axtechrefrep_61). Anda dapat membandingkan berbagai versi laporan ini untuk mempelajari tentang objek yang telah berubah atau telah dihapus di setiap versi aplikasi keuangan dan operasi.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Fitur yang dihapus atau tidak digunakan lagi dalam rilis Operasi Proyek Maret 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Manajemen proyek dan akuntansi parameter "Selalu buat transaksi penyesuaian"

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Transaksi penyesuaian diperlukan untuk tujuan audit. Setelah penghentian, parameter ini akan disembunyikan. Sistem akan selalu membuat transaksi penyesuaian, seperti yang dilakukan saat ini ketika parameter diatur ke **Ya**. |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Operasi Proyek untuk skenario produksi/stok |
| **Status** | Tidak digunakan lagi: Pada 1 Maret 2023, kami akan menyembunyikan parameter dan mengubah perilaku sistem sehingga transaksi penyesuaian selalu dibuat. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Manajemen proyek dan akuntansi parameter "Gunakan tanggal penyesuaian sebagai tanggal proyek baru"

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Parameter ini awalnya digunakan untuk memungkinkan penyesuaian ketika periode fiskal ditutup. Namun, itu tidak lagi diperlukan, karena tanggal akuntansi transaksi dapat diubah ke tanggal pertama periode terbuka, jika dikonfigurasi. Tanggal proyek tidak boleh diubah, karena mewakili tanggal ketika transaksi terjadi. |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Operasi Proyek untuk skenario produksi/stok |
| **Status** | Tidak digunakan lagi: Pada 1 Maret 2023, kami akan menyembunyikan parameter dan mengubah perilaku sistem sehingga tanggal proyek tidak pernah diubah pada penyesuaian. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Alur kerja permintaan sumber daya dalam Operasi Proyek untuk skenario berbasis stok/produksi

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Tidak digunakan lagi karena penggunaan yang rendah dan keterbatasan volume transaksi. |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Operasi Proyek untuk skenario produksi/stok |
| **Status** | Tidak digunakan lagi: Mulai 1 Maret 2023, kami akan menonaktifkan opsi untuk meminta sumber daya untuk proyek dengan menggunakan alur kerja. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Halaman proposal faktur proyek tanpa tampilan Header dan Garis

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Tidak digunakan lagi karena perbaikan pada halaman yang diperkenalkan bersama dengan **proposal faktur Gunakan Proyek dan formulir jurnal faktur dengan kunci fitur tampilan** Header dan Lines. |
| **Digantikan oleh fitur lain?** | Ya |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Operasi Proyek untuk skenario produksi/stok; Operasi Proyek untuk skenario sumber daya/non-stok |
| **Status** | Tidak digunakan lagi: Pada 1 Maret 2023, kami akan mematikan halaman (warisan) sebelumnya dan mengaktifkan **gunakan proposal faktur Proyek dan formulir jurnal faktur dengan kunci fitur tampilan** Header dan Lines secara default. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Fitur yang dihapus atau tidak digunakan lagi dalam rilis Operasi Proyek Desember 2021

### <a name="collaboration-workspaces"></a>Ruang kerja kolaborasi

[Membuat atau menautkan ke ruang kerja kolaborasi (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Tidak digunakan lagi karena penggunaan yang rendah. Pelanggan yang menggunakan Operasi Proyek untuk skenario sumber daya/non-stok dapat memanfaatkan [Kolaborasi dengan Grup](../project-management/collaboration-groups.md) Office. |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi  |
| **Opsi penyebaran** | Operasi Proyek untuk skenario produksi/stok |
| **Status** | Tidak digunakan lagi: Mulai 1 Desember 2022, kami berencana untuk tidak lagi mendukung ruang kerja Kolaborasi. |
