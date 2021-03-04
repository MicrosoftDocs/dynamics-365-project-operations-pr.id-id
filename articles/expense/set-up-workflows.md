---
title: Mengkonfigurasi alur kerja untuk manajemen pengeluaran
description: Anda dapat mengkonfigurasi proses alur kerja yang digunakan untuk meninjau dan menyetujui dokumen perjalanan dan pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127702"
---
# <a name="set-up-workflows-for-expense-management"></a>Mengkonfigurasi alur kerja untuk manajemen pengeluaran

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda dapat mengkonfigurasi proses alur kerja untuk meninjau dan menyetujui dokumen perjalanan dan pengeluaran. Anda dapat menentukan alur kerja untuk laporan pengeluaran, rekuisisi perjalanan, dan permintaan uang muka.

Alur kerja menunjukkan proses bisnis dan menentukan bagaimana suatu dokumen mengalir melalui sistem. Alur kerja juga menunjukkan siapa yang harus menyelesaikan tugas atau menyetujui dokumen. Ada beberapa manfaat menggunakan sistem alur kerja di organisasi Anda:

- **Proses yang konsisten**: Anda dapat menentukan proses persetujuan untuk dokumen tertentu, seperti rekusisi pembelian dan laporan pengeluaran. Menggunakan sistem alur kerja membantu memastikan bahwa dokumen diproses dan disetujui secara konsisten dan efisien.
- **Visibilitas proses**: Anda dapat melacak metrik status, riwayat, dan performa instans alur kerja tertentu. Ini akan membantu Anda menentukan apakah perubahan harus dibuat untuk alur kerja untuk meningkatkan efisiensi.
- **Daftar kerja tersentralisasi**: pengguna dapat melihat daftar kerja tersentralisasi untuk melihat tugas dan persetujuan alur kerja yang ditetapkan ke mereka. 

## <a name="workflow-types"></a>Jenis alur kerja

Tabel berikut mencantumkan jenis alur kerja yang dapat Anda buat di **manajemen pengeluaran**.


|              <strong>Jenis</strong>              |                   <strong>Gunakan jenis ini untuk</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Persetujuan otomatis laporan pengeluaran</strong> |            Membuat alur kerja persetujuan untuk laporan pengeluaran.             |
|  <strong>Memposting otomatis laporan pengeluaran</strong>   |        Membuat alur kerja posting otomatis untuk laporan pengeluaran.        |
|       <strong>Item baris pengeluaran</strong>        |     Membuat alur kerja persetujuan untuk item baris pada laporan pengeluaran.      |
| <strong>posting otomatis item baris Pengeluaran</strong> | Membuat alur kerja posting otomatis untuk item baris pada laporan pengeluaran. |
|       <strong>Permintaan perjalanan</strong>       |          Buat alur kerja persetujuan untuk rekusisi perjalanan.           |
|      <strong>Permintaan Uang muka</strong>      |         Buat alur kerja persetujuan untuk permintaan uang muka.          |
|        <strong>Pemulihan PPN</strong>        | Buat alur kerja persetujuan untuk pemulihan pajak pertambahan nilai (PPN).  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]