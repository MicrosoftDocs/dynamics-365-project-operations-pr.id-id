---
title: Sekilas persetujuan
description: Topik ini menyediakan informasi topik tentang bekerja dengan nilai persetujuan dalam Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a7573b95998387453b72dbcb73c3de977ed7d913
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290363"
---
# <a name="approvals-overview"></a>Sekilas persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Pengajuan waktu dan pengeluaran berpindah melalui alur kerja persetujuan. Setelah entri disetujui, transaksi dicatat dalam aktual atau waktu dipesan dalam jadwal.

## <a name="approvals-workflow"></a>Alur kerja persetujuan
Bila Anda membuat dan mengirimkan entri waktu atau pengeluaran, entri persetujuan dibuat. Pemberi izin proyek atau manajer Anda meninjau dan menyetujui entri Anda. Jika entri terkait dengan proyek, saat disetujui, aktual akan dibuat. Hal ini memungkinkan biaya dan penagihan dilacak. 

## <a name="approve-an-entry"></a>Setujui entri
Formulir **persetujuan** memungkinkan Anda beralih antara tampilan yang berbeda sehingga Anda dapat melihat jenis persetujuan yang berbeda.
  
1. Buka formulir **persetujuan** dan pilih **pengeluaran**, **waktu**, atau **penarikan**.
2. Tinjau setiap persetujuan, dan pilih yang ingin Anda setujui.
3. Pilih **setujui** untuk menyetujui entri yang dipilih.
Sistem akan memproses entri ini dan membuat aktual atau pemesanan.

## <a name="reject-an-entry"></a>Menolak entri
Sebagai pemberi izin proyek, Anda mungkin harus mengirim entri kembali ke pengguna untuk koreksi.
  
1. Buka formulir **persetujuan** dan pilih entri untuk ditolak. 
2. Pilih **Tolak**.
3. Opsional-Tambah Komentar di dialog **komentar penolakan** untuk menginformasikan pengguna mengapa entri ditolak.
4. Pilih **OK**. Entri akan dikembalikan kepada pengguna.
  
## <a name="recall-entries"></a>Tarik kembali entri
Pada titik tertentu, Anda mungkin perlu mengingat entri yang diajukan. Jika entri belum disetujui, maka akan dikembalikan segera. Namun, entri yang disetujui mungkin memiliki dampak material. Pemberi persetujuan proyek diperlukan untuk menyetujui penarikan agar dapat membalikkan transaksi dalam aktual.

## <a name="specify-project-approvers"></a>Menentukan Pemberi persetujuan proyek
Setiap proyek memiliki sejumlah anggota tim proyek. Anda dapat menentukan anggota tim yang juga pemberi persetujuan proyek.

1. Buka formulir **proyek** dan buka proyek dari daftar.
2. Pada tab **tim**, pilih anggota tim yang akan menjadi pemberi izin proyek dan kemudian pilih **Edit**.
3. Atur **bidang pemberi izin proyek** ke **ya**.
4. Pilih **Simpan**.
5. Ulangi langkah 2-4 untuk menambahkan pemberi izin proyek tambahan.

## <a name="configure-the-users-manager"></a>Mengkonfigurasi manajer pengguna

1. Buka **Pengaturan** > **Keamanan** > **Pengguna**.
2. Pilih pengguna yang akan Anda tetapkan manajer dan di area **informasi organisasi**, pilih manajer dari daftar. 
3. Pilih **Simpan**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]