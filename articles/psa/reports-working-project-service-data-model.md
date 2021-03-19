---
title: Bekerja dengan model data Project Service Automation
description: Topik ini menyediakan informasi tentang cara bekerja dengan model data.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25f1af15c03001a92f96689ff36a3159a5352a46
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283237"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Bekerja dengan model data Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation memperluas entitas aplikasi lain dan memperkenalkan entitas sendiri di model data Common Data Service. Topik ini menjelaskan beberapa entitas yang akan anda temui dalam skenario pelaporan PSA biasa.

## <a name="reporting-on-opportunities"></a>Melaporkan peluang

Project Service Automation memperluas entitas **peluang** Dynamics 365 Sales dengan menambahkan bidang yang memungkinkan skenario berbasis proyek. Bidang ini diidentifikasi dengan nama skema yang diawali dengan **msdyn\_**. Salah satu bidang baru yang penting untuk pelaporan peluang PSA adalah **jenis pesanan**. Nilai **berbasis pekerjaan** untuk bidang ini menunjukkan bahwa peluang adalah peluang PSA. Bidang lain yang telah ditambahkan ke entitas mencakup **organisasi yang melakukan kontrak**, yang akan merekam organisasi yang memegang peluang, dan **manajer akun**, yang akan merekam nama manajer akun yang bertanggung jawab atas peluang.

Entitas **baris peluang** juga mencakup bidang yang terkait dengan Project Service. **Metode penagihan** menunjukkan apakah baris peluang harus ditagih berdasarkan waktu dan bahan atau basis harga tetap, dan **proyek** menangkap nama proyek yang mendukung peluang. Bidang lain yang dapat Anda laporkan tentang biaya perekaman dan jumlah anggaran pelanggan untuk item baris.

## <a name="reporting-on-quotes"></a>Melaporkan tentang kuotasi

PSA memperluas entitas **kuotasi** penjualan dengan menambahkan bidang yang terkait dengan proyek. **Jenis pesanan** membedakan kuotasi PSA dari kuotasi non-PSA. Nilai **berbasis pekerjaan** untuk bidang ini menunjukkan bahwa kuotasi adalah kuotasi PSA. Bidang lain yang dapat relevan dengan pelaporan pada harga PSA mencakup bidang jumlah, seperti **biaya yang dibebankan**, **biaya yang tidak dibebankan**, **margin kotor**, **perkiraan**, dan **anggaran**. Bidang berguna lainnya menunjukkan apakah kuotasi menguntungkan, apakah akan selesai sesuai jadwal, dan apakah memenuhi ekspektasi anggaran pelanggan.

PSA juga memperluas entitas **baris kuotasi** penjualan. Satu bidang yang ditambahkan PSA adalah **metode penagihan**, yang menunjukkan bagaimana baris kuotasi akan ditagih (waktu dan material atau harga tetap). Bidang lain yang telah ditambahkan ke entitas merekam proyek terkait yang mendukung baris kuotasi, faktur, biaya, dan anggaran.

PSA juga menambahkan entitas baru yang berhubungan dengan kuotasi untuk model data Dynamics 365. Berikut adalah beberapa contoh:

- **Rincian baris kuotasi** – entitas ini berisi rincian perkiraan proyek baris kuotasi. Ia memiliki dua rekaman untuk setiap baris kuotasi. Satu rekaman menyimpan biaya dan rincian biaya baris kuotasi, dan rekaman lain menyimpan jumlah penjualan dan rincian penjualan baris kuotasi.
- **Jadwal faktur baris kuotasi** - entitas ini berisi jadwal penagihan untuk baris kuotasi. Jadwal ini dihasilkan berdasarkan frekuensi faktur yang ditetapkan ke baris kuotasi.
- **Tonggak waktu baris kuotasi** - entitas ini berisi tonggak waktu penagihan untuk baris kuotasi harga tetap.
- **Perincian Analisis baris kuotasi** – entitas ini berisi rincian keuangan baris kuotasi. Rincian ini mungkin bermanfaat untuk pelaporan kuotasi penjualan dan perkiraan jumlah biaya dari berbagai dimensi.

Entitas lain yang ditambahkan PSA untuk kuotasi adalah **daftar harga proyek baris kuotasi**, **kategori sumber daya kuotasi baris**, dan **kategori transaksi kuotasi**.

![Diagram yang menampilkan kuotasi, baris kuotasi, dan Relasi proyek](media/PS-Reporting-image2.png "Diagram yang menampilkan kuotasi, baris kuotasi, dan Relasi proyek")

## <a name="reporting-on-project-contracts"></a>Melaporkan kontrak proyek

PSA memperluas entitas **pesanan** penjualan yang digunakan saat kontrak proyek direkam. Ia menambahkan bidang baru yang penting, **jenis pesanan**, yang mengidentifikasi kontrak sebagai kontrak proyek PSA, bukan pesanan penjualan. Nilai **berbasis pekerjaan** untuk bidang ini menunjukkan bahwa pesanan adalah kontrak proyek PSA. Bidang baru lainnya yang ditambahkan ke rincian perekaman entitas **pesanan** adalah tentang biaya, status kontrak PSA, dan organisasi yang memiliki kontrak.

PSA juga memperluas entitas **baris pesanan Penjualan**. Di antara bidang yang ditambahkan adalah bidang yang merekam metode penagihan (waktu dan material atau harga tetap), jumlah anggaran pelanggan, dan proyek yang mendasari.

PSA juga menambahkan entitas baru yang dirancang untuk kontrak proyek. Berikut adalah beberapa contoh:

- **Rincian baris kontrak proyek** - entitas ini berisi rincian tingkat baris yang diakumulasikan ke jumlah baris kontrak. Ini dapat seterperinci item baris yang dihasilkan dari jadwal proyek di tingkat tugas.
- **Jadwal faktur baris kontrak** – entitas ini berisi jadwal penagihan yang dihasilkan berdasarkan frekuensi faktur yang ditetapkan ke baris kontrak.
- **Tonggak waktu kontrak** – entitas ini berisi tonggak waktu penagihan untuk baris kontrak yang memiliki ketentuan penagihan harga tetap.

Entitas lain yang ditambahkan PSA untuk kontrak adalah **daftar harga proyek kontrak proyek**, **kategori sumber daya kontrak kategori**, dan **kategori transaksi baris kontrak proyek**.

![Diagram yang menampilkan pesanan, baris pesanan, dan Relasi proyek](media/PS-Reporting-image3.png "Diagram yang menampilkan pesanan, baris pesanan, dan Relasi proyek")

## <a name="reporting-on-projects"></a>Melaporkan proyek

Entitas **proyek** dan entitas terkaitnya eksklusif untuk PSA. **Proyek** adalah entitas tingkat atas yang digunakan untuk merekam sisi pekerjaan dan biaya operasi. Berikut adalah daftar entitas yang terkait:

- **Anggota tim proyek** – entitas ini berisi rincian tentang sumber daya dapat dipesan yang ditetapkan ke proyek. Sumber daya tersebut dapat berupa sumber daya dapat dipesan generik atau dapat berupa sumber daya bernama dapat dipesan yang dimasukkan oleh manajer proyek atau dihasilkan dari jadwal proyek.
- **Tugas proyek** - entitas ini berisi tugas yang membentuk rencana proyek atau jadwal.
- **Tugas sumber daya** - entitas ini berisi penetapan tugas untuk sumber daya yang dapat dipesan.
- **Persyaratan sumber daya** - entitas ini berisi persyaratan untuk setiap anggota tim sumber daya generik.
- **Baris perkiraan** dan **perkiraan** – entitas ini memiliki relasi header/baris dan berisi perkiraan pengeluaran untuk proyek. Perkiraan tugas disimpan pada entitas **perkiraan sumber daya**.

![Diagram yang menampilkan persyaratan sumber daya dan Relasi proyek](media/PS-Reporting-image4.png "Diagram yang menampilkan persyaratan sumber daya dan Relasi proyek")

## <a name="reporting-on-resources"></a>Melaporkan sumber daya

Sumber daya proyek menggunakan entitas **sumber daya dapat dipesan** dari Universal Resource Scheduling (URS) yang dibagikan dengan aplikasi lain, seperti Microsoft Dynamics 365 Field Service. Berikut adalah daftar entitas yang mungkin harus Anda gunakan saat melaporkan sumber daya proyek:

- **Sumber daya yang dapat dipesan** – entitas ini mewakili pengguna, kontak, sumber daya generik, akun, grup, atau perlengkapan yang digunakan pada tim proyek.
- **Karakteristik sumber daya yang dapat dipesan** - entitas ini mencakup keahlian, sertifikasi, atau pendidikan sumber daya. Karakteristik dapat memiliki nilai peringkat yang ditentukan berdasarkan model peringkat.
- **Kategori sumber daya dapat dipesan** - entitas ini menunjukkan peran sumber daya yang dapat dipesan.
- **Pemesanan sumber daya yang dapat dipesan** – entitas ini menunjukkan waktu yang dipesan pada proyek untuk sumber daya. Setiap Pemesanan memiliki entitas header dan entitas baris, dan setiap baris memiliki status yang menunjukkan status pemesanan.

![Diagram yang menampilkan relasi karakteristik sumber daya yang dapat dipesan](media/PS-Reporting-image5.png "Diagram yang menampilkan relasi karakteristik sumber daya yang dapat dipesan")

## <a name="reporting-on-actual-transactions"></a>Pelaporan transaksi aktual

Bila Anda menyetujui lembar waktu atau biaya, atau faktur kontrak di PSA, transaksi bisnis akan direkam di entitas **Aktual**. Entitas ini dapat berfungsi sebagai dasar untuk hampir semua laporan terkait keuangan di PSA. Entitas **aktual** merekam biaya dan transaksi penjualan untuk aktivitas bisnis. Ini juga merekam banyak atribut yang relevan.

Saat Anda bekerja dengan entitas **aktual**, penting bagi Anda untuk memahami transaksi atau transaksi yang direkam di entitas, dan ketika transaksi direkam. Berikut adalah aliran tipikal saat Anda bekerja dengan entri waktu (alur untuk entri pengeluaran adalah serupa):

1. Bila entri waktu disimpan, tidak ada rekaman yang dibuat di entitas **aktual**.
2. Bila entri waktu diajukan, tidak ada rekaman yang dibuat di entitas **aktual**.
3. Bila entri waktu disetujui, satu rekaman akan dibuat di entitas yang **Aktual**, dan rekaman kedua juga dapat dibuat. Rekaman pertama menyimpan biaya entri waktu. Rekaman kedua menyimpan jumlah penjualan yang belum ditagih pada entri waktu. Rekaman kedua tergantung pada proyek baik telah menetapkan pelanggan, kuotasi, atau baris kontrak padanya.

    | Tanggal Dokumen | Jenis Transaksi | Kelas Transaksi | Pelanggan         | Kontrak   | Sumber daya     | Peran sumber daya | Jenis Penagihan | Kuantitas | Harga per Unit | Jumlah |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Biaya             | Time              | Alpine ski house | Alpine CRM | Latisha Aquina | Manajer Proyek   | Dikenakan biaya   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Penjualan Belum Tertagih   | Time              | Alpine ski house | Alpine CRM | Latisha Aquina | Manajer Proyek   | Dikenakan biaya   | 8.0      | 100.00     | 800.00 |

    Kedua rekaman terpisah namun merupakan rekaman terkait. Mereka tidak debit atau kredit.

4. Jika kontrak dikaitkan dengan proyek, bila entri waktu ditagih, dua rekaman lainnya dibuat di entitas yang **Aktual**. Pertama, jumlah negatif untuk rekaman penjualan yang belum ditagih dibuat. Rekaman ini pada dasarnya akan membalikkan penjualan yang belum ditagih. Kedua, transaksi penjualan yang ditagih dibuat. Sekali lagi, rekaman ini terpisah namun rekaman terkait, bukan debit dan kredit.

    | Tanggal Dokumen | Jenis Transaksi | Kelas Transaksi | Pelanggan         | Kontrak   | Sumber daya     | Peran sumber daya | Jenis Penagihan | Kuantitas | Harga per Unit | Jumlah   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Penjualan Belum Tertagih   | Time              | Alpine ski house | Alpine CRM | Latisha Aquina | Manajer Proyek   | Dikenakan biaya   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Penjualan yang Ditagih     | Time              | Alpine ski house | Alpine CRM | Latisha Aquina | Manajer Proyek   | Dikenakan biaya   | 8.0      | 100.00     | 800.00   |

Entitas **asal transaksi** merekam asal rekaman **aktual**, dan entitas **sambungan transaksi** merekam rekaman terkait untuk rekaman **aktual**. Selain itu, rekaman **aktual** berisi referensi proyek, kontrak proyek (pesanan), sumber daya dapat dipesan, dan pelanggan.

![Diagram yang menunjukkan koneksi transaksi, asal dan Relasi aktual](media/PS-Reporting-image6.png "Diagram yang menunjukkan koneksi transaksi, asal dan Relasi aktual")


[!INCLUDE[footer-include](../includes/footer-banner.md)]