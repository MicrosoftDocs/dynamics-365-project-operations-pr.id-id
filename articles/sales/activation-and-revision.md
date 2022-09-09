---
title: Mengaktifkan dan merevisi kutipan proyek
description: Artikel ini menyediakan informasi tentang mengaktifkan dan merevisi kutipan di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410382"
---
# <a name="activate-and-revise-a-project-quote"></a>Mengaktifkan dan merevisi kutipan proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kemampuan aktivasi dan revisi membantu Anda melacak penerapan versi untuk kutipan berbasis proyek selama fase estimasi dan negosiasi. Ketika draf kutipan diaktifkan, itu menjadi hanya-baca.

Kemampuan aktivasi dan revisi memungkinkan Anda melakukan tugas-tugas berikut:

- Menang atau kalahkan kutipan hanya setelah aktivasi.
- Merevisi kutipan untuk membuat perubahan pada kutipan yang ada atau membuat versi baru.

> [!NOTE]
> Setelah fitur untuk aktivasi dan revisi kutipan diaktifkan, itu tidak dapat dinonaktifkan.

Untuk mengaktifkan kemampuan mengaktifkan dan merevisi kutipan berbasis proyek, ikuti langkah-langkah berikut.

1. Buka **Parameter Pengaturan** \> **·**.
1. Buka **catatan Parameter**.
1. Pada Panel Tindakan, pada tab **Kontrol** Fitur, pilih **Aktifkan aktivasi dan revisi tanda kutip**.
1. Pilih **OK** di kotak dialog konfirmasi.
1. Setelah beberapa saat, segarkan browser Anda. Kemampuan aktivasi dan revisi sekarang harus tersedia. Anda akan tahu bahwa kemampuan ini telah diaktifkan jika **tombol Aktifkan aktivasi dan revisi untuk tanda kutip** tidak lagi muncul di Panel Tindakan.

## <a name="activating-a-quote"></a>Mengaktifkan kutipan

Setelah fitur untuk aktivasi dan revisi kutipan diaktifkan, **tombol Tutup kutipan sebagai won** dan **Close quote as lost** pada Panel Tindakan tidak tersedia untuk draf kutipan proyek. Mereka hanya tersedia setelah kutipan diaktifkan.

Aktivasi mewakili tahap dalam proses kutipan ketika Anda ingin mencegah lebih banyak perubahan pada kutipan. Pada tahap ini, penawaran dikirim untuk tinjauan internal atau kepada pelanggan.

Tombol **Tutup kutipan sebagai kutipan menang** dan **Tutup sebagai hilang** pada Panel Tindakan tersedia untuk kutipan yang diaktifkan. Bergantung pada hasil tinjauan internal atau pelanggan, Anda dapat menggunakan salah satu tombol ini untuk menutup penawaran yang diaktifkan. Anda dapat melakukan negosiasi dan perubahan pada kutipan yang diaktifkan dengan **memilih Revisi kutipan**.

## <a name="revising-a-quote"></a>Merevisi kutipan

Jika Anda harus membuat perubahan pada kutipan yang diaktifkan, pilih **Revisi kutipan**. Kutipan ditutup, dan kode alasan yang direvisi **digunakan**. Kutipan baru kemudian dibuat yang memiliki ID yang sama dan nomor revisi yang bertambah. Semua detail dari kutipan asli disalin ke kutipan baru. Kutipan baru dalam status draf dan dapat diedit sesuai kebutuhan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
