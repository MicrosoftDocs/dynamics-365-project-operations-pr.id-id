---
title: Membuat dan mengonfirmasi jurnal koreksi
description: Topik ini menyediakan informasi tentang cara membuat dan mengonfirmasikan jurnal koreksi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127759"
---
# <a name="create-and-confirm-correction-journals"></a>Membuat dan mengonfirmasi jurnal koreksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Terkadang entri waktu atau biaya dapat dimasukkan dengan benar. Contohnya, konsultan mungkin memilih tanggal yang salah saat membuat entri waktu atau mereka mungkin mentransposisi angka saat memasukkan pengeluaran. Jika konsultan tidak dapat melakukan pembaruan terhadap entri yang diajukan, administrator dapat secara langsung mengoreksi entri untuk proyek.

Untuk menyelesaikan prosedur dalam topik ini, anda memerlukan izin Administrator.

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

Misalnya, pada grafik berikut, ada dua item baris dengan kuantitas 8,00 yang memiliki debit yang tercantum di kolom jumlah. Selain itu, ada dua item baris dengan kuantitas-8,00 yang menunjukkan jumlah dikreditkan di kolom jumlah. Koreksi ini membawa kuantitas ke nol.

 
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


