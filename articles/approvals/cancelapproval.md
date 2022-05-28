---
title: Membatalkan persetujuan entri yang disetujui sebelumnya
description: Ini topik menjelaskan bagaimana manajer proyek dapat membatalkan persetujuan waktu, biaya, atau entri penggunaan material yang disetujui sebelumnya.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584784"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Membatalkan persetujuan entri yang disetujui sebelumnya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Manajer proyek atau pemberi persetujuan yang sebelumnya telah menyetujui waktu, biaya, atau entri penggunaan material dapat membatalkan persetujuan mereka atas entri tersebut. 

Ikuti langkah-langkah ini untuk membatalkan persetujuan waktu, biaya, atau entri penggunaan material yang disetujui sebelumnya.

1. Buka **proyek** \> **Pekerjaan Saya** \> **Persetujuan**.
2. Halaman **daftar Persetujuan** menampilkan semua entri waktu yang sedang menunggu persetujuan. Ubah tampilan ke **persetujuan saya sebelumnya**.
3. Pilih waktu, biaya, atau persetujuan material untuk dibatalkan. Kemudian, pada Panel Tindakan, pilih **Batalkan Persetujuan**.
4. Dalam kotak pesan konfirmasi yang muncul, pilih **OK** untuk mengonfirmasi operasi.

> [!IMPORTANT]
> Anda tidak dapat membatalkan persetujuan waktu, biaya, dan entri penggunaan material yang disetujui sebelumnya yang telah ditagih kepada pelanggan. Jika anda mencoba, anda akan menerima pesan yang menyatakan bahwa persetujuan tersebut tidak dapat dibatalkan karena sudah ditagih. Dalam hal ini, Anda dapat membatalkan persetujuan hanya jika faktur korektif digunakan untuk mengeluarkan kredit penuh atau pengembalian uang kepada pelanggan pada faktur asli.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Dampak pembatalan persetujuan entri yang disetujui sebelumnya

Bila persetujuan dibatalkan, ada dampak operasional dan dampak keuangan.

### <a name="operational-impact"></a>Dampak operasional

Jika persetujuan entri dibatalkan, catatan persetujuan ditandai sebagai **Diserahkan**. Status entri diubah menjadi **Dikirimkan**. Pada tahap ini, anggota tim proyek dapat mengingat entri tanpa mengirimkan permintaan penarikan.

Pemberi persetujuan dapat mengubah **jumlah** yang dapat ditagih dan **nilai jenis** Penagihan, lalu menyetujui entri sekali lagi.

### <a name="financial-impact"></a>Dampak keuangan

Jika persetujuan entri dibatalkan, aktual yang sesuai untuk biaya dan penjualan diperbarui dengan cara berikut:

- Bidang **Status penyesuaian** diperbarui ke **disesuaikan**.
- Bidang **Status Penagihan** diperbarui ke **Dibatalkan**.

Selanjutnya, entri pembalikan dibuat di dalam tabel aktual. Untuk membuat entri pembalikan, sistem menyalin nilai bidang dari aktual asli. Hanya nilai yang tidak disalin adalah nilai kuantitas. Nilai ini dibalik sebagai gantinya. Aktual terbalik dibuat untuk aktual **biaya** dan **penjualan tidak ditagih**. Bidang **status penyesuaian** pada aktual terbalik diatur ke **tidak dapat disesuaikan**, dan **status penagihan** diatur ke **dibatalkan**. Karena perubahan ini, pengeluaran yang tercatat dan akumulasi pendapatan pada proyek tidak akan mempertimbangkan lagi jumlah yang diwakili oleh aktual ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
