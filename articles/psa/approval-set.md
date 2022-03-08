---
title: Rangkaian persetujuan
description: Pembaruan topik memberikan informasi tentang kumpulan persetujuan, permintaan, dan subset operasi tersebut.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116875"
---
# <a name="approval-sets"></a>Rangkaian persetujuan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rangkaian persetujuan mengelompokkan permintaan persetujuan grup ke dalam subset operasi yang lebih kecil. Pengelompokan ini memungkinkan persetujuan diproses secara berurutan menurut Proyek dan memungkinkan untuk mencoba ulang dan mengurutkan. Mengelompokkan akan meningkatkan keandalan dan keterlacakan pemrosesan persetujuan untuk volume persetujuan yang besar.

Rangkaian persetujuan menunjukkan status pemrosesan keseluruhan rekaman terkait. Bila rekaman persetujuan diproses menggunakan rangkaian persetujuan, rekaman akan berpindah dari **Diajukan** ke **Disetujui**, dan tidak ditautkan dari rangkaian persetujuan. Jika rekaman gagal saat diajukan untuk persetujuan, rekaman tetap dalam status **Diajukan** dan rangkaian persetujuan ditandai sebagai gagal. Rangkaian persetujuan akan mencatat pesan kesalahan kegagalan.

## <a name="processing-approvals-and-approval-sets"></a>Memproses persetujuan dan rangkaian persetujuan
Persetujuan yang diantrekan untuk pemrosesan dapat dilihat di tampilan **Pemrosesan Persetujuan**. Sistem mencoba memproses semua entri beberapa kali secara asinkron, termasuk mencoba ulang persetujuan jika upaya sebelumnya gagal.

Bidang **Usia Rangkaian Persetujuan** mencatat jumlah upaya yang tersisa untuk memproses rangkaian sebelum ditandai sebagai gagal.

## <a name="failed-approvals-and-approval-sets"></a>Persetujuan dan rangkaian persetujuan yang gagal
Tampilan **Persetujuan Gagal** mencantumkan semua persetujuan yang memerlukan intervensi pengguna. Buka log rangkaian persetujuan yang terkait untuk mengidentifikasi penyebab kegagalan.
Memilih **Coba lagi** menambahkan ke jumlah usia rangkaian persetujuan, memindahkan rangkaian persetujuan kembali ke status **Pemrosesan**, dan mencoba memproses rekaman yang tersisa.

## <a name="configure-approval-sets"></a>Konfigurasikan Rangkaian Persetujuan

###  <a name="enable-the-approval-sets-feature"></a>Aktifkan fitur Rangkaian Persetujuan
Sebelum Anda mengaktifkan fitur rangkaian Persetujuan, pastikan tidak ada persetujuan yang saat ini diproses.

- Buka halaman **parameter Proyek**, lalu pilih **Kontrol Fitur** > **Aktifkan Persetujuan Modern**.

### <a name="turn-off-the-approval-sets-feature"></a>Nonaktifkan fitur Rangkaian Persetujuan
Sebelum Anda menonaktifkan fitur rangkaian Persetujuan, pastikan tidak ada persetujuan yang saat ini diproses.

- Buka halaman **parameter Proyek**, lalu pilih **Kontrol Fitur** > **Nonaktifkan Persetujuan Modern**.

### <a name="configuring-the-asynchronous-threshold"></a>Mengkonfigurasi ambang batas asinkron 
Bila rangkaian persetujuan dibuat, pemrosesan akan berpindah ke latar belakang bila jumlah rekaman yang dipilih untuk disetujui melebihi ambang batas yang ditunjukkan. Gunakan bidang **Ambang Batas Asinkron** untuk mengkonfigurasi ketika pemrosesan persetujuan harus dijalankan secara sinkron atau asinkron.
Nilai yang valid adalah:

  - Nol: Semua permintaan harus diproses secara asinkron. 
  - Angka yang lebih besar dari nol: Persetujuan diproses secara asinkron hanya bila jumlah persetujuan yang diajukan melebihi nilai ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
