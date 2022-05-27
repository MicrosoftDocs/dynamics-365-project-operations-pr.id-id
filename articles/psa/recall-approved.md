---
title: Tarik entri waktu atau pengeluaran yang telah disetujui sebelumnya
description: Topik ini menyediakan informasi tentang cara menarik transaksi waktu atau pengeluaran yang telah disetujui sebelumnya.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
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
ms.openlocfilehash: 457aebb00851a1db3e4aa1068f6a825759b8f2e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578804"
---
# <a name="recall-approved-time-or-expense-entries"></a>Tarik entri waktu atau pengeluaran yang telah disetujui sebelumnya

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anggota tim proyek atau orang lain yang mengajukan entri waktu atau biaya dapat menarik entri waktu atau pengeluaran tersebut setelah disetujui. Proses untuk menarik entri waktu atau pengeluaran yang telah disetujui memiliki dua langkah:

1. Pemohon meminta penarikan.
2. Pemberi izin menyetujui penarikan.

## <a name="request-a-recall"></a>Meminta Penarikan

Ikuti langkah berikut untuk meminta penarikan entri waktu atau pengeluaran yang sebelumnya disetujui.

1. Untuk entri waktu, buka **Proyek** \> **Pekerjaan Saya** \> **Entri waktu**.

    –atau–

    Untuk entri pengeluaran, buka **Proyek** \> **Pekerjaan Saya** \> **Pengeluaran**.

2. Untuk entri waktu, pilih semua entri waktu untuk kombinasi tertentu dari proyek dan tugas. Atau, di kisi, pilih sel individual untuk waktu pada tanggal tertentu untuk proyek tertentu.

    –atau–

    Untuk entri pengeluaran, pilih baris untuk entri pengeluaran, yang akan ditarik.

3. Pilih **Tarik**. Kotak dialog konfirmasi akan ditampilkan. Jika entri waktu dan pengeluaran yang dipilih telah disetujui, Anda akan diminta memasukkan alasan untuk penarikan.
4. Masukkan alasan untuk penarikan, lalu pilih **OK** untuk mengkonfirmasi operasi. Sistem akan mengirim orang yang menyetujui entri permintaan untuk menyetujui penarikan.

> [!NOTE]
> Meskipun entri waktu dan pengeluaran yang disetujui dapat ditarik kembali, jika waktu atau pengeluaran yang disetujui telah ditagih ke pelanggan, permintaan penarikan ulang tidak dapat dibuat. Pengguna yang mencoba membuat permintaan penarikan akan menerima pesan yang menyatakan bahwa waktu atau pengeluaran tidak dapat ditarik karena sudah ditagih.

## <a name="approve-or-reject-a-recall-request"></a>Menyetujui atau menolak permintaan penarikan

Ikuti langkah berikut untuk menyetujui atau menolak permintaan penarikan.

1. Buka **proyek** \> **Pekerjaan Saya** \> **Persetujuan**.
2. Di halaman daftar **persetujuan**, Ubah tampilan menjadi **Tarik permintaan persetujuan**. Daftar Permintaan penarikan yang diajukan akan ditampilkan.
3. Pilih satu entri atau lebih, lalu pilih **Setujui** atau **Tolak**.
4. Jika Anda memilih **setuju**, Anda akan menerima pesan peringatan yang menjelaskan dampak persetujuan. Pilih **OK** untuk mengonfirmasikan operasi. Permintaan penarikan disetujui.

    –atau–

    Jika Anda memilih **Tolak**, permintaan penarikan akan ditolak.

> [!NOTE]
> Saat ada permintaan penarikan ulang, saat penarikan disetujui, sistem memeriksa aktivitas faktur pada entri waktu atau pengeluaran. Jika entri sudah ditagih, atau jika pada faktur draf, pemberi izin akan menerima pesan kesalahan yang menyatakan bahwa waktu atau pengeluaran tidak dapat disetujui untuk ditarik, karena sudah ditagih.

## <a name="impact-of-a-recall-request"></a>Dampak dari permintaan penarikan

Bila persetujuan ditarik, ada dampak operasional dan dampak keuangan.

### <a name="operational-impact"></a>Dampak operasional

Jika permintaan penarikan ulang disetujui, rekaman persetujuan ditandai sebagai **ditolak**. Status entri akan diubah **Dikembalikan** maupun **Ditolak**, tergantung pada apakah entri waktu atau entri pengeluaran.

Anggota tim proyek dapat melihat entri, mengedit, dan kemudian mengajukan kembali entri, atau menghapus entri seluruhnya.

Jika permintaan penarikan ulang ditolak, status entri tetap **disetujui**, dan entri tidak dapat diedit oleh anggota tim proyek atau pemberi izin untuk proyek.

### <a name="financial-impact"></a>Dampak keuangan

Jika permintaan penarikan disetujui, aktual yang sesuai untuk biaya dan penjualan diperbarui dengan cara berikut:

- Bidang **Status penyesuaian** diperbarui ke **disesuaikan**.
- Bidang **Status Penagihan** diperbarui ke **Dibatalkan**.

Selanjutnya, entri pembalikan dibuat di dalam tabel aktual. Untuk membuat entri pembalikan, sistem menyalin nilai bidang dari aktual asli. Hanya nilai yang tidak disalin adalah nilai kuantitas. Nilai ini dibalik sebagai gantinya. Aktual terbalik dibuat untuk aktual **biaya** dan **penjualan tidak ditagih**. Bidang **status penyesuaian** pada aktual terbalik diatur ke **tidak dapat disesuaikan**, dan **status penagihan** diatur ke **dibatalkan**. Karena perubahan ini, pengeluaran yang tercatat dan akumulasi pendapatan pada proyek tidak akan mempertimbangkan lagi jumlah yang diwakili oleh aktual ini.

Jika permintaan penarikan ulang ditolak, tidak ada dampak keuangan pada proyek.

## <a name="changes-to-time-entry-records"></a>Perubahan pada rekaman entri waktu

Ilustrasi berikut menunjukkan perubahan yang terjadi untuk entri waktu yang disetujui saat mereka ditarik.

![Transisi status entri waktu.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Perubahan pada rekaman entri pengeluaran

Ilustrasi berikut menunjukkan perubahan yang terjadi untuk entri pengeluaran yang disetujui saat mereka ditarik.

![Transisi status entri pengeluaran.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
