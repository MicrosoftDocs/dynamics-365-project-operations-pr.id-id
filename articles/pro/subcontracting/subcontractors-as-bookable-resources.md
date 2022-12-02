---
title: Konfigurasi subkontraktor sebagai sumber daya yang dapat dipesan
description: Atikel ini menjelaskan cara menyiapkan dan memelihara sumber daya subkontraktor yang dibuat dari pengguna dan kontak dalam sistem, sehingga mereka dapat dikaitkan dengan subkontraktor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522705"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Konfigurasi subkontraktor sebagai sumber daya yang dapat dipesan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Ikuti langkah-langkah berikut untuk mengkonfigurasi subkontraktor sebagai sumber daya yang dapat dipesan di Microsoft Dynamics 365 Project Operations.

1. Buka **Proyek** \> **Sumber daya**, lalu pilih **Baru**.
2. Pada halaman **Sumber Daya Yang Dapat Dipesan Baru**, di bidang **Jenis Sumber Daya**, pilih salah satu dari pilihan berikut:

    - **Pengguna** – Pilih jenis sumber daya ini jika subkontraktor harus mengakses Project Operations untuk memasukkan waktu atau pengeluaran. Jika Anda memilih **Pengguna**, subkontraktor memerlukan lisensi yang valid untuk mengakses sistem.
    - **Kontak** atau **Akun** – Pilih salah satu jenis sumber daya ini jika subkontraktor tidak memerlukan akses ke Project Operations, namun harus tersedia untuk penugasan tugas atau pemesanan pada proyek. Tidak satu pun dari jenis sumber daya ini yang menyediakan akses ke sistem. Pilih **Akun** untuk menyatakan perusahaan vendor sebagai sumber daya yang dapat dipesan. Pilih **Kontak** untuk menyatakan karyawan individual vendor.

3. Tergantung pada jenis sumber daya yang Anda pilih, Anda akan diminta memilih pengguna, akun, atau rekaman kontak yang terkait.
4. Di bidang **Jenis Pekerja**, pilih "Pekerja kontrak" untuk mengkonfigurasi subkontraktor sebagai sumber daya yang dapat dipesan.

    > [!NOTE]
    > Jika Anda membiarkan bidang **Jenis Pekerja** kosong, sumber daya yang dapat dipesan akan dipertimbangkan sebagai karyawan.

5. Jika Anda memilih **Pekerja Kontrak** sebagai jenis pekerja, pilih vendor yang sumber dayanya digunakan.
6. Pilih zona waktu sumber daya, lalu pilih **Simpan**. Untuk menetapkan template jam kerja ke sumber daya yang dapat dipesan, Anda dapat memilih **Atur kalender** pada halaman daftar **Sumber Daya yang Dapat Dipesan**.

Agar terkait dengan baris baris subkontrak, sumber daya yang dapat dipesan harus memenuhi syarat:

- Sumber daya yang dapat dipesan harus merupakan pekerja kontrak.
- Sumber daya yang dapat dipesan dari jenis sumber daya **Kontak** harus terkait dengan akun vendor sebagai kontak. Sumber daya yang dapat dipesan dari jenis sumber daya **Pengguna** tidak harus terkait dengan akun vendor sebagai kontak.
- Nilai bidang **Vendor** untuk sumber daya yang dapat dipesan harus sesuai dengan nilai bidang **Vendor** untuk subkontrak.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Memperbarui jenis pemetaan pekerja dan vendor untuk sumber daya yang dapat dipesan

Bidang **Jenis pekerja** untuk sumber daya yang dapat dipesan menentukan apakah sumber daya yang dapat dipesan adalah pekerja kontrak atau karyawan. Bidang **Vendor** menentukan akun vendor yang terkait dengan sumber daya yang dapat dipesan. Dengan menghubungkan sumber daya yang dapat dipesan dengan vendor sebagai kontak, Anda menunjukkan bahwa kontak adalah karyawan perusahaan vendor.

Jika bidang **Jenis Pekerja** dan **Vendor** untuk sumber daya yang dapat dipesan diubah, perubahan akan mempengaruhi validasi mendatang pada rekaman baru yang dibuat sumber daya yang dapat dipesan, seperti entri waktu. Namun, perubahan tidak membatalkan rekaman yang ada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
