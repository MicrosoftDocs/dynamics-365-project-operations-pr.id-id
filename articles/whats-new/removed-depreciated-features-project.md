---
title: Fitur yang dihapus atau tidak digunakan lagi di Dynamics 365 Project Operations
description: Artikel ini menjelaskan fitur yang telah dihapuskan, atau yang direncanakan untuk dihilangkan dari Dynamics 365 Project Operations.
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

Artikel ini menjelaskan fitur yang telah dihapuskan, atau yang direncanakan untuk dihilangkan dari Dynamics 365 Project Operations.

- Fitur *yang dihapuskan* tidak akan lagi tersedia di dalam produk.
- Fitur yang *tidak digunakan lagi* tidak dalam pengembangan aktif dan akan dihapus pada pembaruan mendatang.

Daftar ini ditujukan untuk membantu Anda mempertimbangkan penghapusan dan penghentian ini untuk perencanaan Anda.

> [!NOTE]
> Informasi rinci tentang objek dalam aplikasi keuangan dan operasi dapat ditemukan dalam [**laporan referensi Teknis**](/dynamics/s-e/global/axtechrefrep_61). Anda dapat membandingkan versi laporan ini untuk mempelajari tentang objek yang telah berubah atau telah dihilangkan di setiap versi aplikasi keuangan dan operasi.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Fitur yang dihapus atau tidak digunakan lagi di rilis Project Operations Maret 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parameter manajemen dan akuntansi proyek "Selalu buat transaksi penyesuaian"

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Transaksi penyesuaian diperlukan untuk tujuan audit. Setelah deprekasi, parameter ini akan disembunyikan. Sistem akan selalu membuat transaksi penyesuaian, sama seperti saat ini saat parameter diatur ke **Ya**. |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Project Operations untuk skenario dengan stok/produksi |
| **Status** | tidak digunakan lagi: Pada 1 Maret 2023, kami akan menyembunyikan parameter ini dan mengubah perilaku sistem sehingga transaksi penyesuaian selalu dibuat. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>parameter Manajemen proyek dan akuntansi "Gunakan tanggal penyesuaian sebagai tanggal proyek baru"

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Parameter ini awalnya digunakan untuk memungkinkan penyesuaian ketika periode fiskal ditutup. Namun, transaksi tidak lagi diperlukan karena tanggal akuntansi transaksi dapat diubah ke tanggal pertama periode terbuka, jika dikonfigurasi. Tanggal proyek tidak boleh diubah, karena menunjukkan tanggal saat transaksi terjadi. |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Project Operations untuk skenario dengan stok/produksi |
| **Status** | tidak digunakan lagi: Pada 1 Maret 2023, kami akan menyembunyikan parameter ini dan mengubah perilaku sistem sehingga tanggal proyek tidak pernah diubah pada penyesuaian. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Alur kerja permintaan sumber daya di Project Operations untuk skenario berbasis produksi/stok

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | tidak digunakan lagi karena keterbatasan penggunaan dan volume transaksi yang rendah. |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Project Operations untuk skenario dengan stok/produksi |
| **Status** | alur kerja: Pada 1 Maret 2023, kami akan menonaktifkan pilihan untuk meminta sumber daya untuk proyek dengan menggunakan alur kerja. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Halaman proposal faktur proyek tanpa tampilan Header dan Baris

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | Tidak digunakan lagi karena perbaikan halaman yang diperkenalkan bersama dengan tombol fitur **Gunakan formulir jurnal faktur dan proposal faktur Proyek dengan tampilan Header dan Baris**. |
| **Digantikan oleh fitur lain?** | Ya |
| **Area produk yang terpengaruh** | Aplikasi |
| **Opsi penyebaran** | Project Operations untuk skenario produksi/persediaan; Project Operations untuk skenario sumber daya/non-stok |
| **Status** | tidak digunakan lagi: Pada 1 Maret 2023, kami akan menonaktifkan halaman (lama) sebelumnya mengaktifkan tombol fitur **Gunakan formulir jurnal faktur dan proposal faktur Proyek dengan tampilan Header dan Baris** secara default. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Fitur yang dihapus atau tidak digunakan lagi di rilis Project Operations Desember 2021

### <a name="collaboration-workspaces"></a>Ruang kerja kolaborasi

[Membuat atau menautkan ke ruang kerja kolaborasi (Proyek)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Alasan penghentian/penghapusan** | tidak digunakan lagi karena penggunaan yang rendah. Pelanggan yang menggunakan Project Operations untuk skenario sumber daya/non-stok dapat memanfaatkan [Kolaborasi dengan Office Groups](../project-management/collaboration-groups.md). |
| **Digantikan oleh fitur lain?** | No |
| **Area produk yang terpengaruh** | Aplikasi  |
| **Opsi penyebaran** | Project Operations untuk skenario dengan stok/produksi |
| **Status** | dukungan: Hingga 1 Desember 2022, kami berencana tidak lagi mendukung ruang kerja Kolaborasi. |
