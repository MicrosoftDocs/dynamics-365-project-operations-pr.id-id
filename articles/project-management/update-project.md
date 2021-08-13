---
title: Perbarui proyek
description: Topik ini menyediakan informasi tentang memperbarui proyek di Project operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: b0ec03a2c4dd7bc833b22b7a93fed810b4998a2788f4ff40234e3dd163bd9eb6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000895"
---
# <a name="update-a-project"></a>Perbarui proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Di bawah ini adalah ringkasan bidang yang dapat diperbarui pada proyek setelah dibuat dan implikasi pembaruan yang berlaku.

## <a name="project-detail-fields"></a>Bidang rincian proyek

- **Nama**: Judul proyek.
- **Deskripsi**: Ikhtisar proyek.
- **Pelanggan**: perusahaan yang menerima hasil proyek.
- **Template kalender**: jam kerja proyek. Saat bidang diubah, seluruh jadwal dihitung ulang.
- **Mata uang**: mata uang proyek. Default bidang ini adalah berdasarkan mata uang yang ditentukan di unit kontrak. Saat unit kontrak diperbarui, bidang juga diperbarui.
- **Unit kontrak**: unit organisasi yang mewakili grup perusahaan atau divisi yang terutama bertanggung jawab untuk memenangkan penjualan dan mengelola pengiriman pekerjaan dan layanan kepada pelanggan. 
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