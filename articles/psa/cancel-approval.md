---
title: Membatalkan entri waktu dan biaya yang disetujui sebelumnya
description: Topik ini menyediakan informasi tentang cara membatalkan transaksi waktu dan biaya proyek yang disetujui.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150582"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Membatalkan entri waktu dan biaya atau disetujui sebelumnya

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Di versi terbaru Dynamics 365 Project Service Automation, pemberi persetujuan dapat membatalkan entri waktu atau biaya yang telah disetujui sebelumnya.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Membatalkan entri waktu dan biaya atau disetujui sebelumnya

Ikuti langkah berikut untuk membatalkan entri waktu atau biaya yang sebelumnya disetujui.

1. Buka **proyek** \> **Pekerjaan Saya** \> **Persetujuan**.
2. Di halaman daftar **persetujuan**, Ubah tampilan menjadi **persetujuan saya sebelumnya**. Daftar entri waktu dan pengeluaran yang telah disetujui sebelumnya ditampilkan.
3. Pilih satu entri atau lebih, lalu pilih **Batalkan persetujuan**. Anda menerima pesan peringatan.
4. Untuk membatalkan persetujuan, pilih **OK**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Memahami dampak membatalkan waktu atau persetujuan entri biaya

Bila persetujuan dibatalkan, ada dampak operasional dan dampak keuangan.

### <a name="operational-impact"></a>Dampak operasional

Di sisi operasi, saat persetujuan dibatalkan, status rekaman diatur ulang ke **draf**, dan persetujuan tidak lagi muncul di tampilan **persetujuan saya sebelumnya**. Namun, persetujuan yang dibatalkan ditampilkan di tampilan **entri waktu untuk persetujuan** maupun tampilan **entri pengeluaran untuk persetujuan**, tergantung pada apakah itu entri waktu atau entri pengeluaran. Selain itu, status entri waktu atau pengeluaran terkait diubah ke **Diajukan**, sehingga entri terkait sesuai dengan persetujuan yang memiliki status **draf**.

Sebagai pemberi izin, Anda dapat mengedit beberapa bidang persetujuan yang memiliki status **draf**. Bidang ini mencakup **jenis penagihan** dan **jam yang dapat ditagih untuk entri waktu**. Setelah membuat perubahan, Anda dapat menyetujui kembali rekaman. Atau, Anda dapat menolak entri. Jika Anda menolak persetujuan untuk entri waktu, status entri akan diubah menjadi **dikembalikan**. Jika Anda menolak persetujuan untuk entri pengeluaran, status akan diubah menjadi **Ditolak**. Secara fungsional, entri yang dikembalikan dan ditolak akan berfungsi sama seperti entri yang memiliki status **draf**. Anggota tim proyek dapat membuat perubahan yang diperlukan pada entri dan kemudian mengirimkannya kembali untuk disetujui, atau menghapus seluruh entri.

### <a name="financial-impact"></a>Dampak keuangan

Proyek juga terpengaruh secara finansial saat persetujuan dibatalkan. Pertama, aktual yang sesuai untuk biaya dan penjualan diperbarui dengan cara berikut:

- Status penyesuaian diatur ke **disesuaikan**.
- Status penagihan diatur ke **Dibatalkan**.

Selanjutnya, entri pembalikan dibuat di dalam tabel aktual. Untuk membuat entri pembalikan, sistem menyalin nilai bidang dari aktual asli. Hanya nilai yang tidak disalin adalah nilai kuantitas. Nilai ini dibalik sebagai gantinya. Aktual terbalik dibuat untuk aktual **biaya** dan **penjualan tidak ditagih**. Bidang **status penyesuaian** pada aktual terbalik diatur ke **tidak dapat disesuaikan**, dan status penagihan diatur ke **dibatalkan**.

Setelah perubahan ini dibuat, jumlah yang tercatat sebagai dibelanjakan pada proyek dan akumulasi pendapatan pada proyek tidak mempertimbangkan lagi jumlah yang diwakili oleh aktual ini.
