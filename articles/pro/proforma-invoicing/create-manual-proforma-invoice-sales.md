---
title: Membuat faktur proforma manual - lite
description: Topik ini memberikan informasi tentang membuat faktur proforma manual di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274192"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Membuat faktur proforma manual - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Dynamics 365 Project Operations, faktur proforma dapat dibuat secara manual jika diperlukan. Anda dapat secara manual membuat faktur proforma dari halaman daftar **kontrak proyek** atau dari halaman rincian **kontrak proyek**.

##  <a name="project-contracts-list-page"></a>Daftar Harga Kontrak Proyek

Dari halaman daftar **kontrak proyek**, pilih satu atau beberapa kontrak proyek, dan buat faktur untuk semua rekaman yang dipilih.

Sistem akan memeriksa untuk melihat yang mana dari kontrak proyek yang dipilih memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini. Dari kontrak tersebut, sistem membuat faktur proforma draft. Jika kontrak proyek memiliki beberapa pelanggan, mungkin ada satu faktur dibuat per pelanggan, dan beberapa faktur per kontrak proyek.

Semua faktur proyek yang dibuat tersedia pada halaman **faktur** di Bagian **tagihan** area **penjualan**.

## <a name="project-contract-details-page"></a>Halaman Detail Kontrak Proyek

Faktur proforma juga dapat dibuat dari halaman rincian **Kontrak Proyek**. Sistem akan memverifikasi apakah kontrak proyek memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini. Dari kontrak ini, sistem membuat rancangan faktur proforma berdasarkan jumlah pelanggan pada setiap baris kontrak.

Bila ada faktur proforma tunggal yang dibuat, halaman **faktur** akan terbuka. Jika beberapa faktur dibuat untuk kontrak proyek tersebut, halaman daftar **Faktur** akan terbuka untuk menampilkan semua faktur yang dibuat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]