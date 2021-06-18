---
title: Gunakan bidang yang ada dalam Project Service sebagai dimensi harga
description: Topik ini menyediakan informasi tentang penggunaan Project Service proyek yang ada sebagai dimensi harga.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008090"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Gunakan bidang yang ada dalam Project Service sebagai dimensi harga

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) memiliki banyak bidang pada entitas **aktual** yang dapat digunakan sebagai dimensi harga untuk harga berbasis sumber daya dalam organisasi proyek. Misalnya, satu bidang umum adalah **sumber daya dapat dipesan**. Perusahaan kecil yang memiliki sumber daya yang dapat ditagih kurang dari 20-30 mungkin menemukan bahwa memiliki tarif tagihan dan biaya yang spesifik untuk setiap sumber daya adalah pendekatan yang lebih sederhana. Namun, karena tenaga kerja yang dapat ditagih tumbuh, tingkat spesifik dapat menjadi tidak realistis untuk dipertahankan karena biaya sumber daya dan tarif tagihan mulai bervariasi seiring sumber daya dipromosikan, mendapatkan lebih banyak pengalaman, atau memperoleh set keahlian yang berbeda. Karena pendekatan ini masih berfungsi untuk perusahaan dengan ukuran tertentu, lihat [gunakan sumber daya yang dapat dipesan sebagai dimensi](bookable-resource-pricing-dimension.md) harga untuk memahami bagaimana bidang Project Service yang ada dapat digunakan sebagai dimensi harga.

Contoh lainnya adalah kategori transaksi. Pelanggan dan pelaksana telah menggunakan kategori transaksi dalam PSA untuk mengklasifikasikan pekerjaan dan menggunakan bidang untuk menetapkan harga dan biaya berdasarkan Kategori pekerjaan. Untuk informasi lebih lanjut, Lihat [menggunakan kategori transaksi sebagai dimensi harga](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]