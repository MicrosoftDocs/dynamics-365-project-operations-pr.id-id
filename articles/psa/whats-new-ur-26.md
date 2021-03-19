---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 26, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280402"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation Pembaruan Rilis 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 26, V3. Versi ini memiliki nomor pembuatan V3.10.44.59 dan umumnya tersedia melalui pembaruan mandiri pada Desember 2020.

## <a name="update-release-26"></a>Pembaruan rilis 26

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- Pengguna dapat mengubah tugas di entri waktu yang telah disetujui/dikirim.
- Terjadi kesalahan "Referensi Objek Tidak Diatur" saat menyimpan entri waktu.
- Impor entri waktu dari tugas sumber daya menyebabkan entri waktu dengan nilai DateTime salah.
- Apabila aplikasi Project Service Automation dan Field Service diinstal, tombol **Baru** akan ditampilkan dua kali di bilah perintah untuk entri waktu di aplikasi Field Service.
- Pembaruan sel **Bolehkan Unit** dan **Grup unit** sekarang berfungsi pada kisi **Estimasi Pengeluaran**.
- Formulir **Perbarui Edit Entri Waktu** mencakup **Garis waktu**.
- Persetujuan waktu untuk entri waktu nonproyek memblokir sistem saat mencari peran pemberi izin proyek.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- Penambahan validasi di plug-in **PostProjectCreate** untuk memeriksa persyaratan utama sebelum membuatnya.
- **Anggota Tim Proyek** dengan cepat membuat formulir menghilangkan pengecualian referensi null jika bidang dihapus dari formulir.
- Membuat persyaratan untuk 12 jam lebih dari 1 tahun akan gagal.
- Peningkatan pesan kesalahan pengecualian referensi null selama pembuatan persyaratan sumber daya.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Peningkatan validasi ke alamat pengecualian referensi null yang dibuat di plug-in **PreProjectUpdate**.
- Proyek yang dipublikasikan melalui add-in desktop Microsoft Project akan menghapus tugas yang belum ditetapkan.
- Penambahan validasi baru apabila referensi proyek tugas tidak valid karena pengecualian referensi null di plug-in **PreValidateProjectTaskUpdate**.
- Kisi Anggota Tim tidak menampilkan tugas yang berbeda pada record anggota tim.
- Penambahan validasi baru dan pesan kesalahan karena pengecualian referensi null di plug-in **PreProjectTaskDelete**.

**Sales**

Masalah berikut telah diperbaiki:

- Saat memilih baris berbasis proyek dalam kuotasi atau kontrak, tombol **Saran** hanya akan terlihat saat memilih baris berbasis produk yang terkait dengan produk yang ada.
- Pisahkan hak istimewa **Buat_Produk** dari hak istimewa **Buat_Kontrak Proyek**.
- Menghapus baris faktur dapat menyebabkan kegagalan referensi pada **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]