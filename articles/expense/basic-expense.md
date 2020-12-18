---
title: Entri pengeluaran (sederhana)
description: Topik ini menyediakan informasi tentang cara menangani entri pengeluaran di penyebaran sederhana.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590950"
---
# <a name="expense-entry-lite"></a>Entri pengeluaran (sederhana)

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Basic, atau Lite, manajemen pengeluaran adalah kemampuan untuk merekam biaya sederhana. Anda dapat merekam biaya terhadap proyek, dan kemudian pemberi izin proyek akan meninjau dan menyetujuinya.

Untuk informasi lebih lanjut tentang kapabilitas pengeluaran di Dynamics 365 Project Operations, lihat [Ikhtisar pengeluaran](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Mengambil biaya dasar

Anda dapat mengambil pengeluaran Anda sehingga Anda dapat mengirimkannya ke pemberi izin.

1. Buka **pengeluaran**, lalu pilih **baru**.
2. Pada halaman **pengeluaran baru**, masukkan informasi pengeluaran yang diperlukan, lalu pilih **Simpan**.

## <a name="submit-a-basic-expense"></a>Ajukan pengeluaran dasar

Setelah selesai menangkap semua pengeluaran, dan siap disetujui, Anda harus menyerahkannya.

1. Buka **pengeluaran**, lalu pilih pengeluaran. Atau, pilih semua pengeluaran menggunakan kotak centang di header.
2. Pilih **kirim**. Sistem memproses entri yang dipilih dan kemudian membuat permintaan persetujuan pengeluaran.

## <a name="add-an-attachment"></a>Tambahkan lampiran

Anda mungkin harus memberikan dokumentasi tambahan tentang pengeluaran Anda kepada pemberi izin. Anda dapat melampirkan tanda terima di garis waktu entri pengeluaran. Pilih **Edit** dan di bagian **Garis waktu**, lalu pilih ikon penjepit kertas untuk melampirkan tanda terima Anda.

## <a name="recall-a-basic-expense"></a>Tarik pengeluaran dasar

Bila Anda mengirimkan pengeluaran secara tidak sengaja, Anda dapat menariknya. Waktu yang diperlukan untuk menarik entri pengeluaran tergantung pada tingkat persetujuannya.  Jika pemberi izin belum menyetujui entri, penarikan dapat terjadi segera. Namun, jika entri telah disetujui, pemberi izin diminta untuk menyetujui penarikan dan membalikkan transaksi.

1. Buka **pengeluaran**, lalu, dalam daftar pengeluaran, pilih biaya yang akan ditarik.
2. Pilih **Tarik**. Jika entri biaya belum disetujui, sistem segera akan menariknya. Jika entri pengeluaran telah disetujui, permintaan penarikan dibuat untuk memberi tahu pemberi persetujuan bahwa Anda ingin membalikkan pengeluaran. Pemberi persetujuan kemudian akan mengkonfirmasi bahwa pembalikan dapat dilakukan, dan entri akan dikembalikan.

## <a name="delete-a-basic-expense"></a>Menghapus pengeluaran dasar

Pengeluaran yang belum diajukan dapat dihapus. Untuk menghapus pengeluaran yang telah dikirim, Anda harus menariknya terlebih dahulu.

## <a name="see-also"></a>Lihat juga

- [Sekilas persetujuan](../approvals/approvals-overview.md)
