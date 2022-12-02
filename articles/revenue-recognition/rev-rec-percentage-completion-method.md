---
title: Proyek estimasi pendapatan harga tetap
description: Artikel ini berisi informasi tentang pendapatan harga tetap dalam berbagai proyek.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928390"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Proyek estimasi pendapatan harga tetap 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Saat Anda membuat baris kontrak proyek dengan atribut berikut pada Dynamics 365 Project Operations di Microsoft Dataverse, sistem akan otomatis membuat proyek estimasi pendapatan harga tetap. Informasi dalam proyek ini berdasarkan pada item berikut:

  - Metode penagihan harga tetap.
  - Proyek yang terkait.
  - Setidaknya satu tonggak pencapaian yang ditentukan di tab **Jadwal Faktur** pada halaman **Baris kontrak proyek**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Meninjau proyek estimasi pendapatan harga tetap
Untuk meninjau proyek estimasi pendapatan harga tetap, lakukan langkah-langkah berikut:

1. Di lingkungan Dynamics 365 Finance, buka **Manajemen dan akuntansi proyek** > **Proyek** > **Proyek estimasi pendapatan harga tetap**.
2. Pilih proyek yang ingin Anda lihat dan klik dua kali **ID proyek estimasi** untuk membuka record dan meninjau rincian proyek.
3. Buka tab **Proyek**. Anda akan melihat satu proyek di kisi **Proyek yang dipilih**. Sistem menggunakan ini sebagai proyek default karena merupakan proyek yang terkait dengan baris kontrak proyek. 
4. Untuk mengubah keterkaitan, pilih proyek tambahan dan tambahkan ke kisi **Proyek yang dipilih**. Jika beberapa proyek dipilih dalam kisi ini, persentase penyelesaian dan pendapatan proyek dihitung bersama untuk semua proyek yang dipilih.

  Biaya proyek, profil pendapatan, template biaya, dan kode periode dapat diatur secara manual. Jika tidak diatur secara manual, nilai default selama perhitungan estimasi pertama untuk proyek menggunakan aturan yang dikonfigurasi untuk profil pendapatan dan biaya proyek.



[!INCLUDE[footer-include](../includes/footer-banner.md)]