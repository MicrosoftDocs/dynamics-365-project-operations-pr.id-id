---
title: Entri pengeluaran (sederhana)
description: Artikel ini menyediakan informasi tentang cara bekerja dengan entri biaya dalam penyebaran lite.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b69cc4ec0a4b51cd1d27f8b8a4a94248ae884797
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917948"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]