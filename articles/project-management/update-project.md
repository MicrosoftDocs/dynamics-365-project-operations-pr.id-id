---
title: Membuat dan memperbarui proyek
description: Artikel ini menyediakan informasi tentang memperbarui proyek Operasi Proyek.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911094"
---
# <a name="create-and-update-a-project"></a>Membuat dan memperbarui proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Berikut adalah ringkasan bidang yang dapat diperbarui pada proyek setelah dibuat. Hal ini juga mencakup segala dampak yang berlaku berdasarkan pembaruan ini.

## <a name="project-detail-fields"></a>Bidang rincian proyek

- **Nama**: Judul proyek.
- **Deskripsi**: Ikhtisar proyek.
- **Pelanggan**: perusahaan yang menerima hasil proyek.
- **Template kalender**: jam kerja proyek. Saat bidang diubah, seluruh jadwal dihitung ulang.
- **Mata uang**: mata uang proyek. Nilai default untuk bidang ini didasarkan pada mata uang yang ditentukan di unit kontrak. Saat unit kontrak diperbarui, bidang juga diperbarui.
- **Unit kontrak**: unit organisasi yang mewakili grup perusahaan atau divisi yang terutama bertanggung jawab untuk memenangkan penjualan dan mengelola pengiriman pekerjaan dan layanan kepada pelanggan.  Bila unit organisasi manajer proyek tidak didefinisikan, bidang ini akan diatur default ke nilai yang ditentukan dalam parameter proyek.
- **Manajer Proyek**: anggota tim proyek yang memiliki wewenang untuk meninjau dan menyetujui entri waktu dan pengeluaran.

## <a name="estimate-fields"></a>Bidang estimasi

- **Estimasi tanggal mulai**: tanggal saat proyek akan dimulai. Saat bidang ini diperbarui, tugas apa pun pada proyek akan bergerak secara proporsional dengan tanggal mulai baru mulai.
- **Tanggal selesai**: tanggal saat proyek dijadwalkan berakhir.
- **Upaya**: perkiraan upaya proyek. Bila tugas ditambahkan ke proyek, bidang ini tidak lagi dapat diedit.
- **Estimasi biaya tenaga kerja**: perkiraan biaya tenaga kerja proyek. Bila biaya tenaga kerja ditambahkan ke proyek, bidang ini tidak lagi dapat diedit.
- **Estimasi Pengeluaran**: perkiraan biaya proyek. Bila pengeluaran ditambahkan ke proyek, bidang ini tidak lagi dapat diedit.

## <a name="project-actual-fields"></a>Bidang aktual proyek
- **Mulai aktual**: tanggal saat proyek dimulai.
- **Selesai aktual**: diperbarui setelah proyek selesai.

## <a name="project-status-fields"></a>Bidang Status Proyek

- **status proyek keseluruhan**: kesehatan proyek keseluruhan yang dilakukan oleh manajer proyek.
- **Komentar** : narasi tentang kesehatan saat ini proyek yang dilakukan oleh manajer proyek.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
