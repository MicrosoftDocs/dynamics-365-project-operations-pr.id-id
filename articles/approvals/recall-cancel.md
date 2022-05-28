---
title: Mengingat entri yang disetujui sebelumnya
description: Ini topik menjelaskan bagaimana anggota tim proyek dapat meminta penarikan kembali catatan waktu, biaya, dan penggunaan material yang diajukan sebelumnya dan disetujui, dan bagaimana manajer proyek dapat menyetujui atau menolak permintaan penarikan kembali.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586578"
---
# <a name="recall-previously-approved-entries"></a>Mengingat entri yang disetujui sebelumnya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anggota tim proyek yang mengirimkan entri waktu, biaya, atau penggunaan material dapat mengingat entri tersebut setelah disetujui. Proses penarikan kembali memiliki dua langkah utama:

1. Pemohon meminta penarikan.
2. Pemberi persetujuan menyetujui permintaan penarikan kembali.

## <a name="request-a-recall"></a>Meminta Penarikan

Ikuti langkah-langkah ini untuk meminta penarikan kembali waktu, biaya, atau entri penggunaan material yang disetujui.

1. Ikuti salah satu langkah ini, tergantung pada jenis entri yang ingin Anda ingat:

    - Untuk entri waktu, buka **Project** \> **My Work** \> **Time Entry**, dan pilih semua entri waktu untuk kombinasi proyek dan tugas tertentu. Atau, di kisi, pilih sel individual untuk waktu pada tanggal tertentu untuk proyek tertentu.
    - Untuk entri pengeluaran, buka **Projects** \> **My Work** \> **Expenses**, dan pilih baris untuk entri pengeluaran untuk diingat.
    - Untuk entri penggunaan material, buka **Log** \> **Penggunaan** Materi Kerja \>**Saya**, dan pilih baris untuk entri penggunaan material untuk diingat.

2. Pilih **Tarik**. Kotak dialog konfirmasi akan ditampilkan. Jika waktu, biaya, atau entri penggunaan material yang dipilih sudah disetujui, Anda akan diminta untuk memasukkan alasan penarikan kembali.
3. Masukkan alasan untuk penarikan, lalu pilih **OK** untuk mengkonfirmasi operasi. Sistem akan mengirim orang yang menyetujui entri permintaan untuk menyetujui penarikan.

> [!IMPORTANT]
> Anda tidak dapat membuat permintaan penarikan untuk waktu, biaya, atau entri penggunaan material yang disetujui yang telah ditagih kepada pelanggan. Jika Anda mencoba, Anda menerima pesan yang menyatakan bahwa waktu, biaya, atau entri penggunaan material tidak dapat ditarik kembali karena sudah ditagih. Dalam hal ini, Anda dapat meminta penarikan kembali entri hanya jika faktur korektif digunakan untuk mengeluarkan kredit penuh atau pengembalian uang kepada pelanggan pada faktur asli.

## <a name="approve-or-reject-a-recall-request"></a>Menyetujui atau menolak permintaan penarikan

Ikuti langkah berikut untuk menyetujui atau menolak permintaan penarikan.

1. Buka **proyek** \> **Pekerjaan Saya** \> **Persetujuan**.
2. Di halaman daftar **persetujuan**, Ubah tampilan menjadi **Tarik permintaan persetujuan**. Daftar Permintaan penarikan yang diajukan akan ditampilkan.
3. Pilih satu entri atau lebih, lalu pilih **Setujui** atau **Tolak**.
4. Jika Anda memilih **setuju**, Anda akan menerima pesan peringatan yang menjelaskan dampak persetujuan. Pilih **OK** untuk mengonfirmasikan operasi. Permintaan penarikan disetujui.

    –atau–

    Jika Anda memilih **Tolak**, permintaan penarikan akan ditolak.

> [!IMPORTANT]
> Ketika penarikan disetujui, sama seperti ketika diminta, sistem memeriksa aktivitas faktur apa pun pada waktu, biaya, atau entri penggunaan material. Jika entri sudah ditagih, atau jika ada di draf faktur, pemberi persetujuan menerima pesan kesalahan yang menyatakan bahwa waktu atau biaya tidak dapat disetujui untuk ditarik kembali karena sudah ditagih. Dalam hal ini, pemberi persetujuan dapat menyetujui penarikan hanya jika faktur korektif digunakan untuk mengeluarkan kredit penuh atau pengembalian uang kepada pelanggan pada faktur asli.

## <a name="impact-of-a-recall-request"></a>Dampak dari permintaan penarikan

Bila persetujuan ditarik, ada dampak operasional dan dampak keuangan.

### <a name="operational-impact"></a>Dampak operasional

Jika permintaan penarikan ulang disetujui, rekaman persetujuan ditandai sebagai **ditolak**. Status entri diubah menjadi Dikembalikan **atau** **Ditolak**, tergantung pada apakah itu entri waktu atau entri biaya atau penggunaan material.

Anggota tim proyek dapat melihat entri, mengedit, lalu mengirimkan kembali entri, atau menghapus entri sepenuhnya.

Jika permintaan penarikan ulang ditolak, status entri tetap **disetujui**, dan entri tidak dapat diedit oleh anggota tim proyek atau pemberi izin untuk proyek.

### <a name="financial-impact"></a>Dampak keuangan

Jika permintaan penarikan disetujui, aktual yang sesuai untuk biaya dan penjualan diperbarui dengan cara berikut:

- Bidang **Status penyesuaian** diperbarui ke **disesuaikan**.
- Bidang **Status Penagihan** diperbarui ke **Dibatalkan**.

Selanjutnya, entri pembalikan dibuat di dalam tabel aktual. Untuk membuat entri pembalikan, sistem menyalin nilai bidang dari aktual asli. Hanya nilai yang tidak disalin adalah nilai kuantitas. Nilai ini dibalik sebagai gantinya. Aktual terbalik dibuat untuk aktual **biaya** dan **penjualan tidak ditagih**. Bidang **status penyesuaian** pada aktual terbalik diatur ke **tidak dapat disesuaikan**, dan **status penagihan** diatur ke **dibatalkan**. Karena perubahan ini, pengeluaran yang tercatat dan akumulasi pendapatan pada proyek tidak akan mempertimbangkan lagi jumlah yang diwakili oleh aktual ini.

Jika permintaan penarikan ulang ditolak, tidak ada dampak keuangan pada proyek.

## <a name="changes-to-time-entry-records"></a>Perubahan pada rekaman entri waktu

Ilustrasi berikut menunjukkan perubahan yang terjadi untuk entri waktu yang disetujui dan catatan persetujuan yang sesuai ketika mereka dipanggil kembali.

![Transisi status entri waktu.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Perubahan pada catatan entri pengeluaran dan penggunaan material

Ilustrasi berikut menunjukkan perubahan yang terjadi untuk biaya yang disetujui dan entri penggunaan material dan catatan persetujuan yang sesuai ketika mereka dipanggil kembali.

![Transisi status entri biaya.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
