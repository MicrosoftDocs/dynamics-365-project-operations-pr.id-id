---
title: Apa yang baru di akses awal 2021 gelombang 2 - penyebaran Project Operations lite
description: Topik ini menyediakan informasi tentang fitur yang tersedia dalam rilis akses Awal gelombang 2 2021 penyebaran Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323915"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Apa yang baru di akses awal 2021 gelombang 2 - penyebaran Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

  - Lingkungan Project Operations untuk Dataverse versi 4.23.0.4

Rilis hanya diterapkan bila lingkungan [dipilih ke Akses Awal](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

[Manajemen subkontrak](../subcontracting/subcontracting_EA_scope.md) - Fitur ini memberikan visibilitas dan kontrol yang lebih baik atas semua aspek pekerjaan pada proyek. Pratinjau manajemen subkontrak mencakup kemampuan berikut:

  - Manajer proyek dapat membuat subkontrak dengan vendor. Secara default, daftar harga yang dilampirkan ke rekaman vendor digunakan untuk subkontrak. Akun vendor memiliki jenis relasi **Vendor** atau **Pemasok**.
  - Manajer proyek dapat memerinci semua pembelian sebagai item baris pada subkontrak. Baris subkontrak dapat untuk waktu, pengeluaran, atau produk. Kelas transaksi baris subkontrak menentukan tujuan baris tersebut.
  - Manajer akun vendor dan manajer proyek dapat mengulang proses subkontrak. Harga dapat disesuaikan dalam daftar harga Pembelian yang dilampirkan ke Subkontrak.
  - Selama proses, jika baris subkontrak adalah untuk waktu, manajer akun vendor dapat mengaitkan kontak vendor dengan setiap baris subkontrak. Keterkaitan ini memberikan informasi kepada manajer proyek yang sedang mengerjakan subkontrak. Bila kontak vendor dikaitkan dengan baris subkontrak, sistem secara otomatis membuat sumber daya yang dapat dipesan dari kontak, jika sumber daya yang dapat dipesan belum ada.
  - Metode penagihan di setiap baris subkontrak dapat bisa Harga Tetap atau Waktu dan Bahan. Untuk baris subkontrak harga tetap, jadwal faktur berbasis pencapaian dikonfigurasikan.
