---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 25, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143757"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Yang baru atau diubah di Project Service Automation Rilis Pembaruan 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, rilis pembaruan 25 Versi ini memiliki nomor pembuatan V 3.10.43.76 dan umumnya tersedia melalui pembaruan mandiri pada oktober 2020.

## <a name="update-release-25"></a>Pembaruan rilis 25

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Diagram entri waktu yang menampilkan data tambahan berdasarkan interval terlalu besar yang diambil.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- Menambahkan kode Package Deployer untuk melewati impor patch Universal Resource Scheduling jika patch versi lebih tinggi sudah ada.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Mengoreksi pembulatan dan selisih kurs yang mengakibatkan kesalahan biaya yang direncanakan dalam kisi pelacakan proyek.
- Mendukung kemampuan untuk menampilkan dua atau lebih kisi reaksi pada formulir **proyek**.
- Menyediakan validasi untuk menangani kemampuan untuk menetapkan tugas yang melewati tanggal berakhir Kalender, yang menghasilkan penetapan sumber daya yang gagal.
- Memperbaiki penanganan kesalahan untuk mengatasi eksepsi referensi null yang dihasilkan dari yang berikut ini:

    - Plug-in **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** saat tugas proyek dibuat tanpa proyek terkait
    - Plug-in **PreProjectTeamMemberCreate**
    - Plug-in **PostProjectTeamMemberDelete**
    - Plug-in **PreValidateProjectTaskDelete**

**Sales**

Masalah berikut telah diperbaiki:

- Memperbaiki penanganan kesalahan untuk mengatasi pengecualian referensi null yang dihasilkan dari **salinan proyek: perkiraan manajemen HelperResource**.
- **Tidak siap untuk faktur** pada **Akumulasi tagihan waktu dan material** tidak menghapus status penagihan.
- Mengoreksi tombol **harga** yang salah label pada tab **Harga Peran** dan **item Katalog**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]