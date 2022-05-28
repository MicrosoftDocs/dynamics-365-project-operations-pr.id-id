---
title: Membuat dan mengonfirmasi jurnal koreksi
description: Topik ini menyediakan informasi tentang cara membuat dan mengonfirmasikan jurnal koreksi.
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
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582807"
---
# <a name="create-and-confirm-correction-journals"></a>Membuat dan mengonfirmasi jurnal koreksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Terkadang, entri waktu atau biaya mungkin salah dimasukkan. Misalnya, konsultan mungkin memilih tanggal yang salah ketika mereka membuat entri waktu, atau mereka mungkin memilih proyek yang salah ketika mereka memasukkan biaya. Jika konsultan tidak dapat memperbarui entri yang dikirimkan, admin back-end dapat langsung memperbaiki aktual untuk proyek.

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

7. Setelah Mengonfirmasi jurnal koreksi, kembali ke proyek atau proyek yang Diperbarui untuk melihat perubahan.

8. Pada halaman proyek, pada **tab Aktual**, tinjau **daftar Tampilan** Terkait Aktual. Entri asli dan entri yang dikoreksi didaftarkan.


## <a name="correct-approved-material-usage-logs"></a>Memperbaiki log penggunaan material yang disetujui

Selesaikan langkah-langkah berikut untuk memperbaiki satu atau beberapa entri log penggunaan material.

1. **Di area Penjualan**, di panel navigasi kiri, di bawah **Transaksi**, pilih **Aktual**.

2. **Dalam daftar Aktual**, gunakan filter kolom untuk memilih **kelas Transaksi material**, sehingga hanya aktual untuk materi yang ditampilkan. Gunakan filter kolom lain untuk lebih membatasi aktual yang ditampilkan. Setelah Anda dapat menemukan kumpulan aktual yang diinginkan, pilih aktual, lalu pilih **Entri yang benar**. Jurnal koreksi baru dibuat secara otomatis, dan **jenis koreksi** Material ditetapkan.

3. **Pada halaman Jurnal** Baru, di **bidang Deskripsi**, masukkan deskripsi untuk koreksi. Kemudian, pada **tab Koreksi** Material, di **bagian Nilai Baru untuk Materi**, pilih bidang data untuk mengoreksi baris materi yang dipilih. Misalnya, Anda dapat menetapkan materi ke proyek lain, atau memperbaiki produk, tanggal material, atau subkontrak.

4. pilih **Pratinjau**. Kemudian, dalam kotak dialog, pilih **OK**.

5. **Pada tab Baris** jurnal, verifikasi koreksi. Anda dapat melihat daftar aktual asli yang terkait dengan entri materi yang dipilih yang telah dibalik dan baris yang sesuai yang telah dibuat.

6. Jika nilai yang dikoreksi adalah seperti yang diharapkan, pilih **konfirmasikan**. Kemudian, dalam kotak dialog, pilih **OK**. Jika nilai tidak seperti yang diharapkan, pilih **Batalkan** untuk kembali ke **daftar Aktual**. Kemudian ulangi langkah 2 sampai 5.

7. Setelah Mengonfirmasi jurnal koreksi, kembali ke proyek atau proyek yang Diperbarui untuk melihat perubahan.

8. Pada halaman proyek, pada **tab Aktual**, tinjau **daftar Tampilan** Terkait Aktual. Entri asli dan entri yang dikoreksi didaftarkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
