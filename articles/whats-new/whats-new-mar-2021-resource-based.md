---
title: Yang baru di bulan Maret 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Maret 2021 Operasi Proyek untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932944"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Maret 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi berikut Dynamics 365 Project Operations:

- Lingkungan Project Operations untuk Dataverse versi 4.8.0.91 
- Manajemen proyek dan akuntansi pada lingkungan Dynamics 365 Finance versi 10.0.16 

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse


| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan harga | 2133873 | Memperbaiki tampilan simbol mata uang **Harga Penjualan Unit** di kisi **Estimasi Pengeluaran**. |
| Penagihan dan harga | 2174616 | Bila kuotasi dimenangkan, daftar harga kustom kontrak direferensikan pada rincian baris kontrak yang disalin dari kuotasi. |
| Manajemen peluang | 2167475 | Memperbaiki Jumlah pajak dalam faktur koreksi yang berasal dari entri aktual yang belum ditagih. |
| Manajemen peluang | 2176285 | Jumlah pajak tidak boleh disalin dari rincian kontrak penjualan/baris kuotasi ke detail kontrak biaya/baris kuotasi. |
| Manajemen peluang | 2188079 | Aturan penagihan terpisah tidak boleh dibuat untuk kontrak yang tidak berbasis kerja. |
| Perencanaan dan Pelacakan | 2125274 | Atribut **Peta Tulis Ganda Proyek** untuk **Pemetaan Tanggal Mulai Proyek** diperbarui dari **msdyn\_taskearlieststart** ke **msdyn\_actualstart**. |
| Perencanaan dan Pelacakan | 2138853 | Fungsi salinan proyek diperbarui untuk memastikan baris estimasi yang mereferensi tugas disalin ke proyek tujuan. |
| Perencanaan dan Pelacakan | 2154306 | Memperbaiki masalah penghapusan estimasi pengeluaran dalam Project Operations untuk skenario berbasis sumber daya. |
| Perencanaan dan Pelacakan | 2173259 | Fungsi salinan proyek yang diperbarui untuk memastikan tidak menampilkan pesan kesalahan **WBS Penyalinan** dalam skenario tertentu. |
| Waktu dan Pengeluaran | 2148910 | Memperbaiki masalah tampilan halaman **Edit Entri** di kisi **Entri Waktu**. |
| Waktu dan Pengeluaran | 2159798 | Mengetatkan Kontrol untuk memastikan entri pengeluaran yang disetujui tidak dapat diedit. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

Untuk informasi lebih lanjut, lihat [Yang baru di bulan Januari 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan peraturan untuk aplikasi Keuangan dan Operasi, lihat [Pembaruan peraturan](/dynamics365/finance/localizations/regulatory-updates). Cara lain untuk mempelajari tentang pembaruan peraturan adalah masuk ke LCS dan melihat pembaruan peraturan yang direncanakan menggunakan alat pencarian masalah. Pencarian Masalah memungkinkan Anda mencari berdasarkan negara, jenis fitur, dan rilis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]