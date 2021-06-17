---
title: Mengonfigurasi peran pada template struktur rincian kerja
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi informasi peran pada template struktur rincian kerja.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997605"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Mengonfigurasi peran pada template struktur rincian kerja

[!include [banner](../includes/banner.md)]

Manajer proyek dapat mengkonfigurasi template struktur rincian kerja (WBS) yang dapat diterapkan saat membuat WBS untuk proyek baru. Manajer proyek dapat menambahkan peran saat membuat template. Gunakan prosedur berikut untuk menetapkan peran ke template WBS.

1. Pilih **manajemen Proyek dan akuntansi** > **konfigurasi** > **Proyek** > **template struktur rincian kerja**.
2. Pilih **rincian** untuk template WBS yang dipilih.
3. Pilih tugas dalam daftar, lalu di bidang **peran**, pilih peran yang akan ditetapkan ke tugas.

## <a name="work-with-a-wbs"></a>Menggunakan WBS

Anda dapat membuat WBS baru, atau Anda dapat menyalin WBS dari template WBS yang ada. Manajer proyek dapat dengan mudah mengelola sumber daya dengan menetapkan peran untuk tugas baru di WBS. Peran dapat digantikan setelah sumber daya diperoleh atau setelah sumber daya yang dikonfirmasi untuk bekerja pada tugas teridentifikasi. Fleksibilitas ini memungkinkan manajer proyek melakukan tugas berikut:

- Mengidentifikasi jumlah sumber daya yang diperlukan untuk paket kerja WBS.
- Estimasi biaya proyek.
- Tentukan anggaran awal.
- Perkirakan durasi aktivitas, berdasarkan peran dan sumber daya.
- Kembangkan beberapa rencana manajemen proyek, berdasarkan informasi proyek yang tersedia.

Pilihan tambahan telah ditambahkan dalam WBS untuk lebih baik menggunakan fungsi sumber daya.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opsi</th>
<th>Deskripsi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Penetapan sumber daya</td>
<td>Lihat sumber daya yang ditetapkan, tanggal, jumlah jam, dan jenis Pemesanan untuk tugas di WBS.</td>
</tr>
<tr class="even">
<td>Buat otomatis tim</td>
<td>Secara otomatis menambahkan sumber daya terencana dengan menggunakan peran yang terkait dengan tugas. Finance secara otomatis menyarankan sumber daya terencana dengan menggunakan analisis keputusan multi-kriteria yang didasarkan pada peran. Setelah peran dan upaya (jam) telah ditetapkan untuk tugas di WBS, dan setelah struktur telah dirilis, pilih <strong>otomatis membuat tim</strong>. Jumlah sumber daya terencana yang diperlukan ditambahkan ke WBS dan tab <strong>penjadwalan proyek dan tim</strong>.</td>
</tr>
<tr class="odd">
<td>Sumber daya (Daftar tarik-turun)</td>
<td>Pada halaman <strong>peluncuran penugasan sumber daya</strong>, Anda dapat memilih sumber daya untuk definitif atau tentatif, berdasarkan durasi yang ditentukan. Anda dapat menyesuaikan pengaturan tampilan untuk melihat dan mengatur durasi aktivitas sumber daya. Anda dapat memilih dan menetapkan sumber daya pada tingkat paket kerja dengan menggunakan pilihan berikut:
<ul>
<li><strong>Terima</strong> – konfirmasikan perubahan pada sumber daya yang ditetapkan ke tugas.</li>
<li><strong>Batalkan</strong> – Batalkan perubahan pada sumber daya yang ditetapkan ke tugas.</li>
<li><strong>Tetapkan secara otomatis</strong> -sumber daya tersedia yang memiliki peran pencocokan dipilih secara otomatis dan ditetapkan ke tugas yang dipilih.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Pada halaman **semua proyek**, pilih proyek **peningkatan XYZ fase 2**.
2. Pilih **skema** > **aktivitas** > **struktur rincian kerja**.
3. Pilih **baru** untuk menambahkan aktivitas satu tingkat berikut ke WBS:

    - Memulai
    - Perencanaan
    - Menjalankan
    - Pemantauan dan Kontrol
    - Tutup

4. Atur tanggal dan upaya (jam), seperti ditunjukkan dalam ilustrasi berikut.

    [![Mengatur tanggal dan upaya](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pilih baris tugas **memulai**, lalu di bidang **peran**, pilih **manajer proyek senior**.
6. Pilih **Terbitkan**.
7. Pada baris yang sama, di bidang **sumber daya**, pilih **Daniel goldschmidt**, lalu pilih **terima**.
8. Pilih baris tugas **perencanaan**, lalu di bidang **peran**, pilih **analis bisnis**.
9. Pilih **publikasikan**, lalu pilih **Buat otomatis tim**.
10. Dalam kotak pesan yang ditampilkan, pilih **Ya**.
11. Di bidang **sumber daya**, Verifikasikan bahwa nilai adalah **analis bisnis 1**.
12. Untuk sumber daya **Analisis bisnis 1**, buka pencarian, dan pilih **peluncuran tugas sumber daya**. Kemudian pilih pekerja untuk tugas.
13. Pilih **Penugasan tentatif** &gt; **kapasitas penuh**.

    > [!NOTE] 
    > Anda tidak menerima peringatan bahwa sumber daya yang ditentukan sekarang 2, karena jumlah sumber daya tetap 1.

14. Pada halaman **struktur rincian kerja**, validasi tugas sumber daya pada WBS, dan kemudian pilih **Simpan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]