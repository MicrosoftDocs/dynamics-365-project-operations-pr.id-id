---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 17, V3
description: Artikel ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 17, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915694"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation Pembaruan Rilis 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.  Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Artikel ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 17. Versi ini memiliki nomor pembuatan V3.10.6.34 dan umumnya tersedia melalui pembaruan mandiri pada Maret 2020.


## <a name="update-release-17"></a>Pembaruan rilis 17

### <a name="bug-fixes"></a>Perbaikan bug

**Umum**

- Diperbaiki: Memperbarui Project Service Automation untuk menegakkan lisensi Team Member (Pusat sumber daya proyek akan mencakup metadata paket Team Member 3.x)
 
**Waktu dan Pengeluaran**

- Diperbaiki tidak dapat mengubah perkiraan pengeluaran dari harga non-nol menjadi nol (0). Perubahan diabaikan.

**Manajemen proyek**

- Diperbaiki: Pemeriksaan nilai null telah ditambahkan pada nama posisi anggota tim.
- Diperbaiki bidang **msdyn_userresourceid** pada entitas **msdyn_resourceassignment** telah ditolak.
- Diperbaiki Peningkatan dari 2. x ke 3. x sekarang menangani kontur usaha kosong pada penugasan tugas.

**Sales**

- Diperbaiki: **faktur. PreValidateInvoiceUpdate** sekarang menangani skenario menetapkan kembali pemilik rekaman dengan benar.
- Diperbaiki: saat kelas transaksi adalah **waktu**, **unitgroup** tidak dapat diedit untuk semua entitas termasuk **quotelinedetails**, **JournalLine**, **InvoiceLineDetail**, dan **ContractLineDetails**. Namun, **unit** hanya tidak bisa diedit untuk **journalline** dan **invoicelinedetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
