---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643267"
---
<a name="project-service-automation-update-release-26-v3"></a>Project Service Automation Pembaruan Rilis 26, V3
================================================

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 26, V3. Versi ini memiliki nomor pembuatan V3.10.44.59 dan umumnya tersedia melalui pembaruan mandiri pada Desember 2020.

<a name="update-release-26"></a>Pembaruan rilis 26
-----------------

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

Masalah berikut telah diperbaiki:

-   Pengguna dapat mengubah tugas di entri waktu yang telah disetujui/dikirim.

-   Terjadi kesalahan "Referensi Objek Tidak Diatur" saat menyimpan entri waktu.

-   Impor entri waktu dari tugas sumber daya menyebabkan entri waktu dengan nilai DateTime salah.

-   Apabila aplikasi Project Service Automation dan Field Service diinstal, tombol **Baru** akan ditampilkan dua kali di bilah perintah untuk entri waktu di aplikasi Field Service.

-   Pembaruan sel **Bolehkan Unit** dan **Grup unit** sekarang berfungsi pada kisi **Estimasi Pengeluaran**.

-   Formulir **Perbarui Edit Entri Waktu** mencakup **Garis waktu**.

-   Persetujuan waktu untuk entri waktu nonproyek memblokir sistem saat mencari peran pemberi izin proyek.

**Manajemen sumber daya**

Masalah berikut telah diperbaiki:

-   Penambahan validasi di plug-in **PostProjectCreate** untuk memeriksa persyaratan utama sebelum membuatnya.

-   **Anggota Tim Proyek** dengan cepat membuat formulir menghilangkan pengecualian referensi null jika bidang dihapus dari formulir.

-   Membuat persyaratan untuk 12 jam lebih dari 1 tahun akan gagal.

-   Peningkatan pesan kesalahan pengecualian referensi null selama pembuatan persyaratan sumber daya.

**Manajemen proyek**

Masalah berikut telah diperbaiki:

-   Peningkatan validasi ke alamat pengecualian referensi null yang dibuat di plug-in **PreProjectUpdate**.

-   Proyek yang dipublikasikan melalui add-in desktop Microsoft Project akan menghapus tugas yang belum ditetapkan.

-   Penambahan validasi baru apabila referensi proyek tugas tidak valid karena pengecualian referensi null di plug-in **PreValidateProjectTaskUpdate**.

-   Kisi Anggota Tim tidak menampilkan tugas yang berbeda pada record anggota tim.

-   Penambahan validasi baru dan pesan kesalahan karena pengecualian referensi null di plug-in **PreProjectTaskDelete**.

**Sales**

Masalah berikut telah diperbaiki:

-   Saat memilih baris berbasis proyek dalam kuotasi atau kontrak, tombol **Saran** hanya akan terlihat saat memilih baris berbasis produk yang terkait dengan produk yang ada.

-   Pisahkan hak istimewa **Buat_Produk** dari hak istimewa **Buat_Kontrak Proyek**.

-   Menghapus baris faktur dapat menyebabkan kegagalan referensi pada **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
