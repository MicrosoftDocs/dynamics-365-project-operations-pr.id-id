---
title: Membatalkan persetujuan entri yang disetujui sebelumnya
description: Artikel ini menjelaskan bagaimana manajer proyek dapat membatalkan persetujuan entri waktu, pengeluaran, atau penggunaan materi yang telah disetujui sebelumnya.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930460"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Membatalkan persetujuan entri yang disetujui sebelumnya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Manajer proyek atau pemberi persetujuan yang sebelumnya telah menyetujui entri waktu, pengeluaran, atau penggunaan materi dapat membatalkan persetujuan mereka atas entri tersebut. 

Ikuti langkah-langkah ini untuk membatalkan persetujuan waktu, pengeluaran, atau entri penggunaan material yang telah disetujui sebelumnya.

1. Buka **proyek** \> **Pekerjaan Saya** \> **Persetujuan**.
2. Halaman **daftar Persetujuan** menampilkan semua entri waktu yang sedang menunggu persetujuan. Ubah tampilan menjadi **Persetujuan saya sebelumnya**.
3. Pilih waktu, pengeluaran, atau persetujuan materi untuk dibatalkan. Kemudian, pada Panel Tindakan, pilih **Batalkan Persetujuan**.
4. Dalam kotak pesan konfirmasi yang muncul, pilih **OK** untuk mengonfirmasi operasi.

> [!IMPORTANT]
> Anda tidak dapat membatalkan persetujuan waktu, pengeluaran, dan entri penggunaan material yang telah disetujui sebelumnya yang telah ditagihkan kepada pelanggan. Jika mencoba, Anda menerima pesan yang menyatakan bahwa persetujuan tidak dapat dibatalkan karena sudah ditagih. Dalam hal ini, Anda dapat membatalkan persetujuan hanya jika faktur korektif digunakan untuk mengeluarkan kredit penuh atau pengembalian dana kepada pelanggan pada faktur asli.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Dampak pembatalan persetujuan entri yang disetujui sebelumnya

Bila persetujuan dibatalkan, ada dampak operasional dan dampak keuangan.

### <a name="operational-impact"></a>Dampak operasional

Jika persetujuan entri dibatalkan, catatan persetujuan ditandai sebagai **Dikirim**. Status entri diubah menjadi **Dikirim**. Pada tahap ini, anggota tim proyek dapat menarik kembali entri tanpa mengirimkan permintaan penarikan kembali.

Pemberi persetujuan dapat mengubah **nilai Kuantitas** yang dapat ditagih dan **Jenis** penagihan, lalu menyetujui entri sekali lagi.

### <a name="financial-impact"></a>Dampak keuangan

Jika persetujuan entri dibatalkan, aktual yang sesuai untuk biaya dan penjualan diperbarui dengan cara berikut:

- Bidang **Status penyesuaian** diperbarui ke **disesuaikan**.
- Bidang **Status Penagihan** diperbarui ke **Dibatalkan**.

Selanjutnya, entri pembalikan dibuat di dalam tabel aktual. Untuk membuat entri pembalikan, sistem menyalin nilai bidang dari aktual asli. Hanya nilai yang tidak disalin adalah nilai kuantitas. Nilai ini dibalik sebagai gantinya. Aktual terbalik dibuat untuk aktual **biaya** dan **penjualan tidak ditagih**. Bidang **status penyesuaian** pada aktual terbalik diatur ke **tidak dapat disesuaikan**, dan **status penagihan** diatur ke **dibatalkan**. Karena perubahan ini, pengeluaran yang tercatat dan akumulasi pendapatan pada proyek tidak akan mempertimbangkan lagi jumlah yang diwakili oleh aktual ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
