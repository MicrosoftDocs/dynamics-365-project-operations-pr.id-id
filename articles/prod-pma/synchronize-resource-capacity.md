---
title: Mensinkronkan kapasitas sumber daya
description: Topik ini menyediakan informasi tentang cara mensinkronisasi kapasitas sumber daya di seluruh kalender dan proyek.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997515"
---
# <a name="synchronize-resource-capacity"></a>Mensinkronkan kapasitas sumber daya

[!include [banner](../includes/banner.md)]

Proses untuk sinkronisasi sumber daya membantu menjamin bahwa informasi untuk kalender dan kalender dasar menetes ke dalam penjadwalan sumber daya proyek. Jika kalender diubah, proses akan melakukan pembaruan yang diperlukan terhadap penjadwalan sumber daya proyek. Proses juga membantu meningkatkan kinerja, karena informasi sumber daya kalender disinkronisasikan terlebih dahulu. Oleh karena itu, pembaruan untuk informasi penjadwalan sumber daya terjadi lebih cepat. Sebaiknya jadwalkan proses sebagai kumpulan, bukan satu per satu. Jika tidak, ada risiko bahwa seseorang akan melupakan tanggal inklusif saat informasi terakhir disinkronisasi. Jika tanggal inklusif tidak digunakan, kesenjangan dapat terjadi selama sinkronisasi tanggal.

![Sinkronisasi kalender](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sinkronisasikan akumulasi kapasitas sumber daya

Proses sinkronisasi dirancang untuk mensinkronisasi semua informasi kalender sumber daya. Informasi ini mencakup informasi kalender dasar tentang perubahan pada tabel kapasitas kalender sumber daya proyek. Jika sumber daya baru ditambahkan dalam proyek, sinkronisasi akan membantu menjamin bahwa informasi kalender yang diperbarui tersedia. Sinkronisasi ini dapat dilakukan kapan pun.

Sebaiknya Anda menggunakan kumpulan. Pilihan tersedia selama sinkronisasi Pemesanan kapasitas.

1. Pilih **manajemen proyek dan akuntansi** &gt; **Periodik** &gt; **Sinkronisasi kapasitas** &gt; **Sinkronisasi akumulasi kapasitas sumber daya**.
2. Atur pilihan dalam tabel berikut.

    | Opsi      | Deskripsi |
    |-------------|-------------|
    | Kode periode | Atau pilih kode interval tanggal buku besar untuk mengatur tanggal mulai dan berakhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya. |
    | Tanggal mulai  | Masukkan tanggal mulai untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya. |
    | Tanggal berakhir    | Masukkan tanggal akhir untuk proses sinkronisasi untuk akumulasi kapasitas sumber daya. |

[![Proses Sinkronisasi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]