---
title: Apa yang baru di akses awal 2021 gelombang 2 - penyebaran Project Operations lite
description: Artikel ini menyediakan informasi tentang fitur yang tersedia dalam rilis akses awal 2 gelombang 2 2021 dari penyebaran Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924112"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Apa yang baru di akses awal 2021 gelombang 2 - penyebaran Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi berikut Dynamics 365 Project Operations:

  - Lingkungan Project Operations untuk Dataverse versi 4.23.0.4

Rilis hanya diterapkan bila lingkungan [dipilih ke Akses Awal](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

[Manajemen subkontrak](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - Fitur ini memberikan visibilitas dan kontrol yang lebih baik atas semua aspek pekerjaan pada proyek. Pratinjau manajemen subkontrak mencakup kemampuan berikut:

  - Manajer proyek dapat membuat subkontrak dengan vendor. Secara default, daftar harga yang dilampirkan ke rekaman vendor digunakan untuk subkontrak. Akun vendor memiliki jenis relasi **Vendor** atau **Pemasok**.
  - Manajer proyek dapat memerinci semua pembelian sebagai item baris pada subkontrak. Baris subkontrak dapat untuk waktu, pengeluaran, atau produk. Kelas transaksi baris subkontrak menentukan tujuan baris tersebut.
  - Manajer akun vendor dan manajer proyek dapat mengulang proses subkontrak. Harga dapat disesuaikan dalam daftar harga Pembelian yang dilampirkan ke Subkontrak.
  - Selama proses, jika baris subkontrak adalah untuk waktu, manajer akun vendor dapat mengaitkan kontak vendor dengan setiap baris subkontrak. Keterkaitan ini memberikan informasi kepada manajer proyek yang sedang mengerjakan subkontrak. Bila kontak vendor dikaitkan dengan baris subkontrak, sistem secara otomatis membuat sumber daya yang dapat dipesan dari kontak, jika sumber daya yang dapat dipesan belum ada.
  - Metode penagihan di setiap baris subkontrak dapat bisa Harga Tetap atau Waktu dan Bahan. Untuk baris subkontrak harga tetap, jadwal faktur berbasis pencapaian dikonfigurasikan.
