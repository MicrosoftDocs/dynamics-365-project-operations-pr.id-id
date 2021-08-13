---
title: Sekilas persetujuan
description: Topik ini menyediakan informasi topik tentang bekerja dengan nilai persetujuan dalam Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: d77c62455c346d6d427d71af4b01d62b5132a2377c2c1a0a64f56fb313219c46
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991715"
---
# <a name="approvals-overview"></a>Sekilas persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Pengajuan penggunaan bahan, waktu, dan pengeluaran akan melalui alur kerja yang telah disetujui. Setelah entri disetujui, transaksi dicatat dalam aktual atau waktu dipesan dalam jadwal.

## <a name="approvals-workflow"></a>Alur kerja persetujuan
Saat Anda membuat dan mengajukan entri penggunaan bahan, waktu, atau pengeluaran, rekaman persetujuan dibuat. Pemberi izin proyek atau manajer meninjau dan menyetujui entri. Jika entrinya terkait dengan proyek, aktual akan dibuat saat disetujui. Hal ini memungkinkan biaya dan penagihan dilacak.

## <a name="approve-an-entry"></a>Setujui entri
Halaman **Persetujuan** memungkinkan Anda beralih antara tampilan yang berbeda sehingga Anda dapat melihat berbagai jenis persetujuan.
  
1. Buka halaman **Persetujuan**, lalu pilih **Pengeluaran**, **Waktu**, **Penggunaan Bahan**, atau **Penarikan**.
2. Tinjau setiap persetujuan, dan pilih yang ingin Anda setujui.
3. Pilih **setujui** untuk menyetujui entri yang dipilih.
Sistem memproses entri ini dan membuat aktual.

## <a name="reject-an-entry"></a>Menolak entri
Sebagai pemberi izin proyek, Anda mungkin harus mengirim entri kembali ke pengguna untuk koreksi.
  
1. Buka halaman **Persetujuan**, lalu pilih entri untuk ditolak. 
2. Pilih **Tolak**.
3. Opsional, tambahkan komentar dalam kotak dialog **Komentar Penolakan** untuk memberitahukan pengguna alasan ditolaknya entri.
4. Pilih **OK**. Entri akan dikembalikan kepada pengguna.
  
## <a name="cancel-approval"></a>Batalkan Persetujuan
Dalam kasus tertentu, Anda mungkin harus membatalkan entri yang disetujui sebelumnya. Membatalkan entri yang disetujui sebelumnya akan memiliki dampak keuangan. 

## <a name="approving-recall-requests"></a>Menyetujui permintaan penarikan
Dalam kasus tertentu, seorang konsultan mungkin harus menarik entri yang disetujui sebelumnya. Membatalkan entri yang disetujui sebelumnya akan memiliki dampak keuangan. Pemberi izin proyek harus menyetujui penarikan untuk membatalkan transaksi dalam Aktual.

## <a name="specify-project-approvers"></a>Menentukan Pemberi persetujuan proyek
Setiap proyek memiliki sejumlah anggota tim proyek. Anda dapat menentukan anggota tim yang juga pemberi persetujuan proyek.

1. Buka halaman **Proyek**, lalu buka proyek dari daftar.
2. Pada tab **tim**, pilih anggota tim yang akan menjadi pemberi izin proyek dan kemudian pilih **Edit**.
3. Atur **bidang pemberi izin proyek** ke **ya**.
4. Pilih **Simpan**.
5. Ulangi langkah 2-4 untuk menambahkan pemberi izin proyek tambahan.

## <a name="configure-the-users-manager"></a>Mengkonfigurasi manajer pengguna

1. Buka **Pengaturan** > **Keamanan** > **Pengguna**.
2. Pilih pengguna yang akan Anda tetapkan manajer dan di area **informasi organisasi**, pilih manajer dari daftar. 
3. Pilih **Simpan**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
