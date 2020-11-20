---
title: Membuat faktur proforma manual - lite
description: Topik ini memberikan informasi tentang membuat faktur proforma manual di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176390"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Membuat faktur proforma manual - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Dynamics 365 Project Operations, faktur proforma dapat dibuat secara manual sesuai kebutuhan. Anda dapat secara manual membuat faktur proforma dari halaman daftar **kontrak proyek** atau dari halaman rincian **kontrak proyek**.

##  <a name="project-contracts-list-page"></a>Daftar Harga Kontrak Proyek

Dari halaman daftar **kontrak proyek**, pilih satu atau beberapa kontrak proyek, dan buat faktur untuk semua rekaman yang dipilih.

Sistem akan memeriksa untuk melihat yang mana dari kontrak proyek yang dipilih memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini. Dari kontrak tersebut, sistem membuat faktur proforma draft. Jika kontrak proyek memiliki beberapa pelanggan, mungkin ada satu faktur dibuat per pelanggan, dan beberapa faktur per kontrak proyek.

Semua faktur proyek yang dibuat tersedia pada halaman **faktur** di Bagian **tagihan** area **penjualan**.

## <a name="project-contract-details-page"></a>Halaman Detail Kontrak Proyek

Faktur proforma juga dapat dibuat dari halaman rincian **kontrak proyek**, yang membuat faktur untuk kontrak proyek tertentu. Sistem akan memverifikasi bahwa kontrak proyek memiliki backlog **siap untuk faktur** dengan tanggal sebelum tanggal hari ini. Dari kontrak ini, sistem membuat rancangan faktur proforma berdasarkan jumlah pelanggan pada setiap baris kontrak.

Bila ada faktur proforma tunggal yang dibuat, halaman **faktur** akan terbuka. Jika ada beberapa faktur yang dibuat untuk kontrak proyek tersebut, maka halaman daftar **faktur** akan terbuka untuk menampilkan semua faktur yang dibuat.
