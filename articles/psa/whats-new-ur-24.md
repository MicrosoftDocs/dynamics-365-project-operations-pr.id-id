---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 24, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 51d08dd147b7804cb5c9255159aeab2ecd94f4597d6e99c5fa92efe1246c44d0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998060"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation Pembaruan Rilis 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 24. Versi ini memiliki nomor pembuatan V 3.10.42.43 dan umumnya tersedia melalui pembaruan mandiri pada Oktober 2020.

## <a name="update-release-24"></a>Pembaruan rilis 24

### <a name="bug-fixes"></a>Perbaikan bug

**Sales**

Masalah berikut telah diperbaiki:

- Masalah saat menentukan daftar harga produk default.
- Kinerja kuotasi menang lambat karena daftar harga tersemat dan salinan rekaman harga peran.
- **kontrak proyek/pusat penjualan** > **Item baris produk/kuantitas baris pesanan** secara otomatis dibulatkan ke bilangan cacah terdekat.
- Tingkatkan hak istimewa sistem saat membaca daftar harga.
- Salin bidang alamat pelanggan **address1_freighttermscode** dan **address1_shippingmethodcode** ke kuotasi/pesanan. 


**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

- **Kisi entri waktu** tidak mendukung perilaku waktu **tanggal saja**.
- **Entri waktu** tidak disegarkan secara otomatis. Refresh manual diperlukan.
- Tidak dapat mengimpor entri waktu dari tugas bila ada waktu istirahat (0 jam) dalam tugas sumber daya.
- Saat membuat entri waktu, atur awal ke sama dengan **msdyn_date**.
- Aktifkan ulang Edit massal untuk entri waktu.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

- Mencoba memperbarui status pemesanan harian tanpa persyaratan akan menghasilkan pengecualian null-ref.
- Kesalahan saat memuat **tampilan rekonsiliasi**.


**Manajemen proyek**

Masalah berikut telah diperbaiki:

- Dalam **jadwal proyek**, saat mengubah dari **manual** menjadi **Otomatis**, Simpan Otomatis tidak selesai.
- Biaya pengeluaran tidak boleh dihitung ke arah varians pada **kisi pelacakan proyek**.
- Perilaku yang tidak konsisten untuk kolom **tag estimasi** selama memuat versus mengubah jenis **fase waktu**.
- Biaya aktual pada proyek mungkin tidak mencerminkan total dari **aktual**.
- **Estimasi tanggal selesai** pada tab **ringkasan** tidak sesuai dengan **jadwal WBS**.
- **Pembaruan jam aktual** pada outdentasi tidak berfungsi dengan benar.
- Manajer proyek di luar **BU** akar tidak dapat membuat proyek.
- Perubahan pada tugas atau kategori pada **Estimasi pengeluaran** tidak ada.
- **Salinan kontrak** menyalin jadwal faktur dan status Jalankan.
- Tombol **refresh aktual** salah menghitung tugas ringkasan.
- Add-In Microsoft Project: Memperbaiki kesalahan referensi null jika salah satu anggota tim memiliki unit sumber daya kosong.



[!INCLUDE[footer-include](../includes/footer-banner.md)]