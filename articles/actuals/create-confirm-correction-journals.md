---
title: Membuat dan mengonfirmasi jurnal koreksi
description: artikel ini menyediakan informasi tentang cara membuat dan mengonfirmasikan jurnal koreksi.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928068"
---
# <a name="create-and-confirm-correction-journals"></a>Membuat dan mengonfirmasi jurnal koreksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Terkadang entri waktu atau biaya dapat dimasukkan dengan benar. Contohnya, konsultan mungkin memilih tanggal yang salah saat mereka membuat entri waktu atau mereka mungkin memilih proyek yang salah saat memasukkan pengeluaran. Jika konsultan tidak memperbarui entri yang diajukan, admin backend dapat secara langsung mengoreksi aktual untuk proyek.

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

7. Setelah Anda mengkonfirmasi jurnal koreksi, kembalilah ke proyek atau proyek yang Anda diperbarui, untuk melihat perubahan Anda.

8. Di halaman proyek, pada tab **aktual**, Tinjau daftar **tampilan terkait aktual**. Entri asli dan entri yang dikoreksi didaftarkan.


## <a name="correct-approved-material-usage-logs"></a>Memperbaiki log penggunaan bahan yang disetujui

Selesaikan langkah-langkah berikut untuk mengoreksi satu atau beberapa entri log pengg bahan.

1. Di area **penjualan**, di panel navigasi kiri, dalam **transaksi**, pilih **Aktual**.

2. Dalam daftar **Aktual**, gunakan filter kolom untuk memilih kelas transaksi **Bahan**, sehingga hanya aktual untuk bahan yang ditampilkan. Gunakan filter kolom lain untuk membatasi lebih lanjut aktual yang ditampilkan. Setelah Anda dapat menemukan rangkaian aktual yang diinginkan, pilih aktual, lalu pilih **Koreksi entri**. Jurnal koreksi baru dibuat secara otomatis dan jenis **koreksi bahan** yang ditetapkan.

3. Pada halaman **Jurnal baru** pada bidang **Deskripsi**, masukkan deskripsi untuk koreksi. Selanjutnya, pada tab **Koreksi Bahan**, di bagian **Nilai Baru untuk bahan**, pilih bidang data untuk mengoreksi untuk baris bahan yang dipilih. Contohnya, Anda dapat menetapkan bahan ke proyek lain, atau mengoreksi produk, tanggal bahan, atau subkontrak.

4. pilih **Pratinjau**. Kemudian, Pilih **OK** di kotak dialog.

5. Pada tab **Baris Jurnal**, verifikasikan koreksi. Anda dapat melihat daftar aktual asli yang terkait dengan entri bahan yang dipilih dan telah dibalik dan dikoreksi sesuai baris yang telah dibuat.

6. Jika nilai yang dikoreksi adalah seperti yang diharapkan, pilih **konfirmasikan**. Kemudian, Pilih **OK** di kotak dialog. Jika nilai tidak ditampilkan sebagaimana mestinya, pilih **Batalkan** untuk kembali ke daftar **Aktual**. kemudian ulangi langkah 2 hingga 5.

7. Setelah Anda mengkonfirmasi jurnal koreksi, kembalilah ke proyek atau proyek yang Anda diperbarui, untuk melihat perubahan Anda.

8. Di halaman proyek, pada tab **aktual**, Tinjau daftar **tampilan terkait aktual**. Entri asli dan entri yang dikoreksi didaftarkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
