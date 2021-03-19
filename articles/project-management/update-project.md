---
title: Perbarui proyek
description: Topik ini menyediakan informasi tentang memperbarui proyek di Project operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286387"
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