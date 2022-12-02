---
title: Mengaktifkan dan merevisi kuotasi proyek
description: Artikel ini memberikan informasi tentang mengaktifkan dan merevisi kuotasi di Microsoft Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Mengaktifkan dan merevisi kuotasi proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kemampuan aktivasi dan revisi membantu Anda melacak versi kuotasi berbasis proyek selama fase perkiraan dan negosiasi. Bila draf kuotasi diaktifkan, maka kuotasi menjadi hanya baca.

Kemampuan aktivasi dan revisi memungkinkan Anda melakukan tugas berikut:

- Menang atau kalahnya kuotasi hanya setelah aktivasi.
- Alihkan kuotasi untuk membuat perubahan pada kuotasi yang ada atau buat versi baru.

> [!NOTE]
> Setelah fitur untuk aktivasi dan revisi kuotasi diaktifkan, fitur tersebut tidak dapat dinonaktifkan.

Untuk mengaktifkan dan merevisi kuotasi berbasis proyek, ikuti langkah-langkah berikut.

1. Buka **Pengaturan** \> **Parameter**.
1. Buka rekaman **parameter**.
1. Pada Panel Tindakan, pada tab **Kontrol Fitur**, pilih **Aktifkan aktivasi dan revisi kuotasi**.
1. Pilih **OK** di kotak dialog konfirmasi.
1. Setelah beberapa saat, refresh browser Anda. Kemampuan aktivasi dan revisi sekarang harus tersedia. Anda akan mengetahui bahwa kemampuan ini telah diaktifkan jika tombol **Aktifkan aktivasi dan revisi untuk kuotasi** tidak muncul lagi di Panel Tindakan.

## <a name="activating-a-quote"></a>Mengaktifkan Kuotasi

Setelah fitur untuk aktivasi dan revisi kuotasi diaktifkan, tombol **Tutup kuotasi sebagai menang** dan **Tutup sebagai kuotasi sebagai kalah** di Panel Tindakan tidak tersedia untuk draf kuotasi proyek. Tersedia hanya setelah kuotasi diaktifkan.

Aktivasi menunjukkan tahapan dalam proses kuotasi bila Anda ingin mencegah perubahan lainnya pada kuotasi. Pada tahap ini, kuotasi dikirim untuk tinjauan internal atau ke pelanggan.

Tombol **Tutup kuotasi sebagai menang** dan **Tutup kuotasi sebagai kalah** pada Panel Tindakan tersedia untuk kuotasi yang diaktifkan. Tergantung pada hasil tinjauan internal atau pelanggan, Anda dapat menggunakan salah satu tombol ini untuk menutup kuotasi yang diaktifkan. Anda dapat melakukan negosiasi dan perubahan pada kuotasi yang diaktifkan dengan memilih **Revisikuotasi**.

## <a name="revising-a-quote"></a>Merevisi kuotasi

Jika Anda harus melakukan perubahan pada kuotasi yang diaktifkan, pilih **Revisi kuotasi**. Kuotasi ditutup dan kode alasan **direvisi** digunakan. Kuotasi baru kemudian dibuat yang memiliki ID yang sama dan jumlah revisi yang ditambahkan. Semua rincian dari kuotasi asli disalin ke kuotasi baru. Kuotasi baru berada dalam status draf dan dapat diedit jika diperlukan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
