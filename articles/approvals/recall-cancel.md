---
title: Menarik kembali entri yang disetujui sebelumnya
description: Artikel ini menjelaskan bagaimana anggota tim proyek dapat meminta peringatan dari rekaman waktu, pengeluaran, dan penggunaan bahan yang dikirim dan disetujui sebelumnya, serta cara manajer proyek dapat menyetujui atau menolak permintaan penarikan.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930368"
---
# <a name="recall-previously-approved-entries"></a>Menarik kembali entri yang disetujui sebelumnya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anggota tim proyek yang mengajukan entri waktu, pengeluaran, atau penggunaan bahan dapat menarik entri tersebut setelah disetujui. Proses penarikan memiliki dua langkah utama:

1. Pemohon meminta penarikan.
2. Pemberi izin menyetujui permintaan penarikan.

## <a name="request-a-recall"></a>Meminta Penarikan

Ikuti langkah berikut untuk meminta penarikan entri waktu, pengeluaran, atau penggunaan bahan yang disetujui.

1. Ikuti salah satu langkah ini, tergantung pada jenis entri yang ingin Anda tarik:

    - Untuk entri waktu buka **Proyek** \> **Pekerjaan Saya** \> **entri waktu**, pilih semua entri waktu untuk kombinasi tertentu dari proyek dan tugas. Atau, di kisi, pilih sel individual untuk waktu pada tanggal tertentu untuk proyek tertentu.
    - Untuk entri pengeluaran, buka **proyek** \> **Pekerjaan Saya** \> **Pengeluaran**, dan pilih baris untuk entri pengeluaran, yang akan ditarik.
    - Untuk entri penggunaan bahan, buka **proyek** \> **Pekerjaan Saya** \> **Log Penggunaan Bahan**, dan pilih baris untuk entri penggunaan bahan yang akan ditarik.

2. Pilih **Tarik**. Kotak dialog konfirmasi akan ditampilkan. Jika entri waktu, pengeluaran, atau penggunaan bahan yang dipilih telah disetujui, Anda akan diminta memasukkan alasan untuk penarikan.
3. Masukkan alasan untuk penarikan, lalu pilih **OK** untuk mengkonfirmasi operasi. Sistem akan mengirim orang yang menyetujui entri permintaan untuk menyetujui penarikan.

> [!IMPORTANT]
> Anda tidak dapat membuat permintaan penarikan untuk entri waktu, pengeluaran, atau penggunaan bahan yang telah disetujui sebelumnya yang telah ditagihkan kepada pelanggan. Jika Anda mencobanya, Anda akan menerima pesan yang menyatakan bahwa entri waktu, pengeluaran, atau penggunaan bahan tidak dapat ditarik karena sudah ditagih. Dalam kasus ini, Anda dapat meminta penarikan entri hanya jika faktur perbaikan digunakan untuk memberikan kredit penuh atau pengembalian dana kepada pelanggan pada faktur asli.

## <a name="approve-or-reject-a-recall-request"></a>Menyetujui atau menolak permintaan penarikan

Ikuti langkah berikut untuk menyetujui atau menolak permintaan penarikan.

1. Buka **proyek** \> **Pekerjaan Saya** \> **Persetujuan**.
2. Di halaman daftar **persetujuan**, Ubah tampilan menjadi **Tarik permintaan persetujuan**. Daftar Permintaan penarikan yang diajukan akan ditampilkan.
3. Pilih satu entri atau lebih, lalu pilih **Setujui** atau **Tolak**.
4. Jika Anda memilih **setuju**, Anda akan menerima pesan peringatan yang menjelaskan dampak persetujuan. Pilih **OK** untuk mengonfirmasikan operasi. Permintaan penarikan disetujui.

    –atau–

    Jika Anda memilih **Tolak**, permintaan penarikan akan ditolak.

> [!IMPORTANT]
> Ji penarikan disetujui, tepat saat diminta, sistem memeriksa aktivitas faktur pada entri waktu, pengeluaran, atau penggunaan bahan. Jika entri sudah ditagih, atau jika pada faktur draf, pemberi izin akan menerima pesan kesalahan yang menyatakan bahwa waktu atau pengeluaran tidak dapat disetujui untuk ditarik, karena sudah ditagih. Dalam kasus ini, pemberi persetujuan dapat menyetujui penarikan hanya jika faktur perbaikan digunakan untuk memberikan kredit penuh atau pengembalian dana kepada pelanggan pada faktur asli.

## <a name="impact-of-a-recall-request"></a>Dampak dari permintaan penarikan

Bila persetujuan ditarik, ada dampak operasional dan dampak keuangan.

### <a name="operational-impact"></a>Dampak operasional

Jika permintaan penarikan ulang disetujui, rekaman persetujuan ditandai sebagai **ditolak**. Status entri akan diubah **Dikembalikan** maupun **Ditolak**, tergantung pada apakah entri waktu atau entri pengeluaran atau penggunaan bahan.

Anggota tim proyek dapat melihat entri, mengedit, dan kemudian mengajukan kembali entri, atau menghapus seluruhnya.

Jika permintaan penarikan ulang ditolak, status entri tetap **disetujui**, dan entri tidak dapat diedit oleh anggota tim proyek atau pemberi izin untuk proyek.

### <a name="financial-impact"></a>Dampak keuangan

Jika permintaan penarikan disetujui, aktual yang sesuai untuk biaya dan penjualan diperbarui dengan cara berikut:

- Bidang **Status penyesuaian** diperbarui ke **disesuaikan**.
- Bidang **Status Penagihan** diperbarui ke **Dibatalkan**.

Selanjutnya, entri pembalikan dibuat di dalam tabel aktual. Untuk membuat entri pembalikan, sistem menyalin nilai bidang dari aktual asli. Hanya nilai yang tidak disalin adalah nilai kuantitas. Nilai ini dibalik sebagai gantinya. Aktual terbalik dibuat untuk aktual **biaya** dan **penjualan tidak ditagih**. Bidang **status penyesuaian** pada aktual terbalik diatur ke **tidak dapat disesuaikan**, dan **status penagihan** diatur ke **dibatalkan**. Karena perubahan ini, pengeluaran yang tercatat dan akumulasi pendapatan pada proyek tidak akan mempertimbangkan lagi jumlah yang diwakili oleh aktual ini.

Jika permintaan penarikan ulang ditolak, tidak ada dampak keuangan pada proyek.

## <a name="changes-to-time-entry-records"></a>Perubahan pada rekaman entri waktu

Ilustrasi berikut menunjukkan perubahan yang terjadi untuk entri waktu yang disetujui dan rekaman persetujuan terkait saat ditarik.

![Transisi status entri waktu.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Perubahan pada rekaman entri penggunaan bahan dan pengeluaran

Ilustrasi berikut menunjukkan perubahan yang terjadi untuk entri pengeluaran dan penggunaan bahan yang disetujui dan rekaman persetujuan terkait saat ditarik.

![Transisi status entri pengeluaran.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
