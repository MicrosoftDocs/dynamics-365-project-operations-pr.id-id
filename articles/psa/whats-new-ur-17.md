---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 17, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126802"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation Pembaruan Rilis 17, V3

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.  Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 17. Versi ini memiliki nomor pembuatan V3.10.6.34 dan umumnya tersedia melalui pembaruan mandiri pada Maret 2020.


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


