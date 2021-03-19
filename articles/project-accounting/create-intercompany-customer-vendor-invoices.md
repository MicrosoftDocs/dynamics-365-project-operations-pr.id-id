---
title: Membuat faktur vendor dan pelanggan antarperusahaan
description: Topik ini memberikan informasi tentang cara membuat faktur pelanggan dan vendor antarperusahaan.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287467"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Membuat faktur vendor dan pelanggan antarperusahaan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Akuntan proyek dalam entitas hukum pemberi pinjaman membuat faktur pelanggan antarperusahaan untuk biaya proyek yang ditransfer ke entitas peminjam. Setelah faktur pelanggan antarperusahaan disetujui dan diposting, entitas hukum pemberi pinjaman mengirimkan faktur antarperusahaan ke entitas hukum peminjam.

Akuntan proyek untuk entitas hukum pemberi pinjaman dapat mengonfigurasi proses batch untuk menghasilkan faktur antarperusahaan secara berulang. Akuntan proyek menentukan kriteria, seperti proyek spesifik, untuk membuat faktur antarperusahaan dalam sebuah batch.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Membuat faktur pelanggan antarperusahaan secara manual untuk transaksi proyek 

Gunakan prosedur ini untuk membuat faktur pelanggan antarperusahaan secara manual untuk transaksi proyek. Cari jumlah jam yang diposting oleh pekerja pada proyek di entitas hukum peminjam dan untuk biaya yang ditimbulkan oleh entitas hukum Anda atas nama entitas hukum peminjam. Anda dapat mencari berdasarkan nama entitas hukum, nomor kontrak proyek, nomor proyek, rentang tanggal, atau kombinasi beberapa pilihan ini. Di hasil pencarian, pilih transaksi untuk ditambahkan ke faktur antarperusahaan.

1. Di Dynamics 365 Finance, buka **Manajemen dan akuntansi proyek** > **Faktur proyek** > **Faktur pelanggan antarperusahaan**. Pada halaman daftar **Faktur pelanggan antarperusahaan**, di Panel Tindakan, pilih **Baru**.
2. Pada halaman **Buat faktur antarperusahaan**, di bidang **Entitas hukum**, pilih entitas hukum peminjam.
3. Opsional: Masukkan kontrak proyek dan nomor proyek tertentu.
4. Persempit pencarian dengan memilih rentang tanggal. Masukkan tanggal tertentu di bidang **Tanggal mulai** dan **Tanggal akhir**. Hanya transaksi antarperusahaan yang diposting dalam rentang tanggal ini yang akan ditampilkan di hasil pencarian.
5. Atur **Parameter baris jurnal lanjutan proyek** ke **Ya** dan pilih **Cari**.
6. Di hasil pencarian, pilih transaksi yang akan disertakan dalam proposal faktur antarperusahaan, lalu pilih **OK**.
7. Pada halaman **Faktur pelanggan antarperusahaan**, transaksi proyek antarperusahaan yang Anda pilih dari hasil pencarian akan ditampilkan. Untuk mengubah transaksi sebelum Anda mengirim faktur ke entitas hukum peminjam, lakukan langkah-langkah berikut:
  
    1. Buka halaman **Buat proposal faktur**. Pilih transaksi antarperusahaan tambahan untuk faktur saat ini, lalu pilih **Tambah baris**.
    2. Untuk menghilangkan baris, pilih komponen, lalu pilih **Hilangkan**.
    3. Lihat komentar, alasan, dimensi keuangan, dan informasi lainnya tentang baris yang dipilih pada FastTab **Baris faktur**.
    
8. Untuk memposting faktur pelanggan antarperusahaan, pada Panel Tindakan, pilih **Posting**.

> [!NOTE]
> Jika organisasi Anda mewajibkan faktur antarperusahaan ditinjau sebelum diposting, administrator sistem dapat mengonfigurasikan alur kerja untuk faktur antarperusahaan. Jika alur kerja tidak dikonfigurasi untuk faktur antarperusahaan, Anda dapat mengirim faktur antarperusahaan.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Membuat pekerjaan batch untuk faktur antarperusahaan

Anda dapat membuat beberapa faktur antarperusahaan secara bersamaan untuk semua entitas hukum peminjam. Dengan menggunakan fungsi pencarian, Anda dapat misalnya, mencari semua transaksi yang diposting oleh pekerja peminjam dan terkait dengan proyek yang dikelola oleh entitas hukum lainnya. Kemudian, untuk setiap entitas hukum peminjam, Anda dapat membuat faktur antarperusahaan untuk transaksi yang tercantum di hasil pencarian.

1. Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Faktur proyek** > **Buat faktur pelanggan antarperusahaan**.
2. Pada halaman **Buat faktur pelanggan antarperusahaan**, di bidang **Perusahaan**, pilih entitas hukum yang akan dibuatkan fakturnya. Jika Anda tidak memilih perusahaan, semua transaksi yang memenuhi kriteria pencarian akan ditampilkan untuk semua entitas hukum peminjam.
3. Di **Buat satu faktur per**, pilih apakah akan membuat faktur untuk transaksi antarperusahaan berdasarkan proyek atau berdasarkan entitas hukum peminjam.
4. Opsional: Untuk memilih proyek dan kontrak proyek tertentu untuk membuat faktur antarperusahaan, klik **Pilih**. Pada halaman **Pertanyaan**, di bidang **Kriteria**, pilih kontrak proyek, nomor proyek, atau keduanya, lalu pilih **OK**.
5. Pada tab **Batch**, konfigurasikan proses batch untuk membuat faktur antarperusahaan secara berulang. Untuk informasi lebih lanjut, lihat [Mengirimkan pekerjaan pemrosesan batch dari formulir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Untuk memposting faktur antarperusahaan, pada Panel Tindakan, pilih **Posting**.

> [!NOTE]
> Jika organisasi Anda mewajibkan faktur antarperusahaan ditinjau sebelum diposting, administrator sistem dapat mengonfigurasikan alur kerja untuk faktur antarperusahaan. Jika alur kerja tidak dikonfigurasi untuk faktur antarperusahaan, Anda dapat mengirim faktur antarperusahaan.

## <a name="post-the-intercompany-vendor-invoice"></a>Memposting faktur vendor antarperusahaan

Akuntan proyek di entitas hukum peminjam dapat meninjau faktur vendor antarperusahaan yang tertunda saat faktur pelanggan antarperusahaan terkait diposting. Di Keuangan, di entitas hukum peminjam, buka **Utang dagang** > **Faktur** > **Faktur tertunda vendor**. Nomor faktur tertunda faktur akan cocok dengan nomor faktur pelanggan antarperusahaan. Verifikasikan bahwa faktur sudah benar, lalu posting faktur. Memposting faktur vendor antarperusahaan akan menghasilkan subbuku besar proyek dan transaksi buku besar yang menunjukkan biaya transaksi di entitas hukum peminjam.


[!INCLUDE[footer-include](../includes/footer-banner.md)]