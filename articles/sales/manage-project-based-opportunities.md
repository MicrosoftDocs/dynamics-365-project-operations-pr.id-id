---
title: Mengelola peluang berbasis proyek
description: Topik ini memberikan informasi tentang cara bekerja dengan peluang yang terkait dengan proyek.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087965"
---
# <a name="manage-project-based-opportunities"></a>Mengelola peluang berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Perusahaan berbasis proyek biasanya memiliki operasi untuk penyebaran penyebaran di beberapa negara dan geografi. Biaya eksekusi dan pelaksanaan proyek dapat bervariasi berdasarkan geografi atau divisi yang mengelola pelaksanaan. Pada gilirannya, hal ini dapat berdampak pada margin transaksi. Pelaksanaan layanan berbasis proyek biasanya melibatkan sejumlah besar waktu sumber daya manusia, pengeluaran besar untuk perjalanan, biaya material, dan biaya lainnya.

Peluang proyek berbasis di Dynamics 365 Project Operations didesain dengan ekstensi pada Dynamics 365 Sales. Topik ini memberikan rincian tentang bidang yang berbeda dan logika bisnis yang tercakup dalam fungsi tambahan yang diperlukan oleh perusahaan berbasis proyek untuk mengelola peluang berbasis proyek.

## <a name="view-all-project-based-opportunities"></a>Lihat semua peluang berbasis proyek

Daftar semua peluang berbasis proyek dapat dilihat dari halaman daftar **peluang**. 

1. Buka **Penjualan** > **Peluang**.
2. Gunakan **penukar tampilan** untuk memilih tampilan terfilter lainnya dari peluang. Anda dapat membuat tampilan sendiri dengan kriteria filter kustom untuk mengkonfigurasi tampilan dan pilihan navigasi.

Peluang proyek dapat dibuat atau dihapus dari halaman daftar ini atau halaman detail.

## <a name="business-process-flow-for-project-based-deals"></a>Alur proses bisnis untuk transaksi berbasis proyek

Alur proses bisnis berikut didukung untuk transaksi berbasis proyek dalam Project Operations:

- Proses bisnis Prospek ke Peluang
- Proses Penjualan Peluang

### <a name="lead-to-opportunity-business-process"></a>Proses bisnis Prospek ke Peluang 
Proses bisnis prospek ke peluang mendukung tahapan berikut:

| Tahap | Entitas yang dipetakan | Fungsi |
| --- | --- | --- |
| Kualifikasi | Prospek | Kualifikasi prospek untuk membuat akun, kontrak, dan peluang. |
| Kembangkan | Peluang | Kembangkan peluang untuk menambahkan informasi lebih lanjut tentang pekerjaan yang terlibat, pemangku kepentingan utama, dan pesaing. |
| Usulkan | Peluang | Kembangkan proposal dan Dapatkan persetujuan dari tim peninjauan internal. |
| Tutup | Peluang | Menangkan peluang untuk menutup penawaran. |

### <a name="opportunity-sales-process"></a>Proses Penjualan Peluang
Proses penjualan peluang dalam Project Operations adalah perpanjangan ke alur bisnis proses penjualan peluang dalam aplikasi Sales. Proses bisnis ini dirancang secara bawaan untuk mendukung tahapan berikut dalam peluang berbasis proyek.

| Tahap | Entitas yang dipetakan | Fungsi |
| --- | --- | --- |
| Kualifikasi | Peluang | Kualifikasi prospek untuk membuat akun, kontrak, dan peluang. |
| Usulkan | Kuotasi | Kembangkan proposal dengan kuotasi proyek dan dapatkan persetujuan dari tim peninjauan internal. |
| Kontrak | Kontrak Proyek | Menangkan kuotasi untuk membuat kontrak dan memulai eksekusi dan pelaksanaan proyek. |
| Tutup | Kontrak Proyek | Selesaikan pekerjaan dengan sukses dan tutup kontrak proyek. |

> [!NOTE]
> Jika perjanjian berbasis proyek Anda dimulai dengan Prospek, proses bisnis prospek ke peluang lebih diutamakan.
>
> Jika perjanjian berbasis proyek Anda dimulai dengan peluang, proses penjualan peluang lebih diutamakan.

Anda dapat mengedit alur proses bisnis produk atau membuat alur proses bisnis Anda sendiri untuk melacak proses penjualan Anda sesuai kebutuhan. Untuk informasi lebih lanjut tentang alur proses bisnis, lihat [Ikhtisar alur proses bisnis](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).
