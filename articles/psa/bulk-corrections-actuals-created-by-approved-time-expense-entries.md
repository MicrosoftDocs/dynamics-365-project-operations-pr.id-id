---
title: Koreksi massal aktual yang dibuat berdasarkan entri waktu dan pengeluaran yang disetujui
description: Artikel ini menjelaskan bagaimana administrator dapat melakukan koreksi tunggal atau massal terhadap entri waktu atau pengeluaran yang disetujui sebelumnya jika penagihan tidak selesai.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 82c9b38e4c79511fe3b6abfcb973fff8b56f1522
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916293"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Koreksi massal aktual yang dibuat berdasarkan entri waktu dan pengeluaran yang disetujui

[!include [banner](../includes/psa-now-project-operations.md)]

Terkadang entri waktu atau biaya dapat dimasukkan dengan benar. Contohnya, konsultan mungkin memilih tanggal yang salah saat membuat entri waktu atau mereka mungkin mentransposisi angka saat memasukkan pengeluaran. Jika konsultan tidak dapat melakukan pembaruan terhadap entri yang diajukan, administrator dapat secara langsung mengoreksi entri untuk proyek.

Untuk menyelesaikan prosedur dalam artikel ini, Anda memerlukan izin Administrator.

## <a name="correct-approved-time-entries"></a>Mengoreksi entri waktu yang disetujui     

Menyelesaikan langkah-langkah berikut untuk mengoreksi entri atau beberapa satu waktu untuk proyek.

1. Di area **penjualan**, pilih **transaksi**, lalu pilih **waktu yang disetujui**. 

2. Di daftar **waktu disetujui**, Cari dan pilih satu atau beberapa entri waktu yang disetujui untuk dikoreksi. Anda dapat menggunakan filter untuk menemukan entri terkait. Misalnya, Anda dapat memfilter ID proyek, dan memilih semua entri waktu yang disetujui dengan ID proyek tersebut.

3. Pilih **Koreksi Entri**. Jurnal koreksi baru dibuat secara otomatis dengan **koreksi waktu** jenis yang ditetapkan. Entri yang Anda pilih ditambahkan ke jurnal. 

4. Pada halaman **jurnal baru**, masukkan **Deskripsi** jurnal koreksi, lalu pilih tab **koreksi entri waktu**.  
5. Di bagian **nilai baru untuk entri waktu**, Perbarui bidang dengan informasi yang benar yang diperlukan. Misalnya, Anda dapat mengubah proyek yang ditetapkan atau sumber daya yang dapat dipesan.

6. pilih **Pratinjau**. Pilih **Oke** di kotak dialog. Pada tab **lini jurnal**, Anda dapat melihat daftar aktual asli yang terkait dengan entri waktu yang dipilih dan telah dibalik dan dikoreksi sesuai baris yang telah dibuat. Jika koreksi tambahan perlu dilakukan, ulangi langkah 5 dan 6. 

> [!NOTE]
> Semua aktual yang dikoreksi akan memiliki nilai yang sama dengan yang Anda pilih di bagian **nilai baru untuk entri waktu**.

7. Jika koreksi ditampilkan seperti yang diharapkan, pilih **konfirmasikan**. Pilih **Oke** di kotak dialog.

8. Kembali ke area **penjualan**, pilih **proyek** , lalu buka proyek yang baru saja Anda gunakan untuk memasukkan entri waktu. 

9. Pada halaman **proyek**, pada tab **aktual**, lihat perubahan yang Anda buat. 

> [!NOTE]
> Jika tab **aktual** tidak terlihat, pilih **terkait** > **aktual**.  

10. Di daftar **tampilan terkait aktual**, Anda dapat melihat bahwa entri waktu asli yang telah dibalik masih terdaftar, seperti entri waktu dikoreksi yang sesuai. 


## <a name="correct-approved-expense-entries"></a>Mengoreksi entri pengeluaran yang disetujui

Selesaikan langkah-langkah berikut untuk mengoreksi satu atau beberapa entri pengeluaran. 

1. Di area **penjualan**, di panel navigasi kiri, dalam **transaksi**, pilih **Pengeluaran yang disetujui**.

2. Dalam daftar **pengeluaran yang disetujui**, pilih proyek yang ingin Anda Perbaiki, lalu pilih **Koreksi entri**. Jurnal koreksi baru akan dibuat secara otomatis dengan **koreksi pengeluaran** jenis yang ditetapkan. 

3. Pada halaman **jurnal baru**, masukkan **Deskripsi** untuk koreksi, dan di tab **koreksi pengeluaran**, di bagian **nilai baru untuk pengeluaran**, pilih bidang data yang ingin Anda Perbaiki untuk baris pengeluaran yang dipilih. Misalnya, Anda dapat menetapkan pengeluaran untuk **proyek** lain, atau memperbaiki **kategori pengeluaran**, **tanggal pengeluaran**, atau **sumber daya yang dapat dipesan**.

4. pilih **Pratinjau**. Pilih **Oke** di kotak dialog. 

5. Verifikasi koreksi di tab **lini jurnal**. Anda dapat melihat daftar aktual asli yang terkait dengan entri pengeluaran yang dipilih dan telah dibalik dan dikoreksi sesuai baris yang telah dibuat.

6. Jika nilai yang dikoreksi adalah seperti yang diharapkan, pilih **konfirmasikan**. Di kotak dialog, Pilih **Oke.** Jika nilai tidak ditampilkan sebagaimana mestinya, pilih **Batalkan** untuk kembali ke daftar **pengeluaran yang disetujui**. Ulangi langkah 2 hingga 5. 

> [!NOTE]
> Aktual yang dikoreksi akan memiliki nilai yang sama dengan yang Anda pilih di bagian **nilai baru untuk pengeluaran**.

7. Setelah Anda mengkonfirmasi jurnal koreksi, navigasikan kembali ke proyek atau proyek yang Anda diperbarui, untuk melihat perubahan Anda.  

8. Di halaman proyek, pada tab **aktual**, Tinjau **tampilan terkait aktual**. Entri asli dan entri yang dikoreksi didaftarkan. Grafik berikut menunjukkan jumlah entri pengeluaran asli dan jumlah entri pengeluaran yang sesuai yang dikoreksi. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
