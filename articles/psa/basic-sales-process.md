---
title: Proses Penjualan
description: Artikel ini memberikan informasi tentang proses penjualan dasar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 18a5ca0592dfefb611094685087351149a0f5e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923514"
---
# <a name="sales-processes"></a>Proses Penjualan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proses penjualan yang digunakan dalam organisasi berbasis proyek berbeda dari proses penjualan yang digunakan dalam organisasi berbasis produk. Perbedaan ini terjadi karena siklus penjualan untuk organisasi berbasis proyek lebih lama dan memerlukan perkiraan teknik yang disesuaikan untuk menganalisis dan membuat kuotasi untuk setiap transaksi. Dynamics 365 Project Service Automation menggunakan beberapa fungsi yang sama yang digunakan dalam proses penjualan for Dynamics 365 Sales. Berikut adalah beberapa contoh:

- Entitas prospek digunakan untuk melacak proses penjualan.
- Kualifikasi prospek dilacak sebagai peluang. Proses penjualan juga dapat dimulai dengan peluang.
- Semua artefak terkait untuk peluang diakses. Artefak ini mencakup tim penjualan, pemangku kepentingan, probabilitas, peringkat, tahapan penjualan, dan proses bisnis.
- Beberapa kuotasi dibuat untuk peluang.
- Kuotasi ditandai **ditutup sebagai pemenang** untuk membuat pesanan penjualan. Dalam PSA, pesanan penjualan disesuaikan dan disebut kontrak proyek.

Ilustrasi berikut menunjukkan proses penjualan biasa dalam organisasi berbasis proyek.

> ![Proses penjualan di organisasi berbasis proyek.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Memperkirakan penjualan
Nilai penjualan dapat diperkirakan berdasarkan proyek yang sebelumnya telah dikirim dan kompleksitas proyek. Untuk proyek yang melibatkan ekstensi ke proyek sebelumnya, atau proyek di mana keahlian Penjual tinggi dan template kerja yang telah dikenal digunakan, Anda dapat menggunakan proses estimasi yang lebih sederhana. Proyek yang lebih kompleks biasanya memiliki proses pembelian lebih lama. Oleh karena itu, ada lebih banyak tahapan dalam proses estimasi penjualan. Di awal proses, tim penjualan menggunakan input manajer akun dan ahli (UKM) untuk mulai membuat perkiraan tingkat tinggi untuk setiap komponen pekerjaan yang berbeda yang dibuat kuotasinya. Komponen pekerjaan ini diwakili oleh baris kuotasi. 

Anda dapat membuat perkiraan kuotasi tingkat tinggi. Akhirnya, perkiraan tingkat tinggi ini akan digantikan dengan perkiraan lebih rinci berdasarkan rencana proyek yang Anda buat menggunakan template proyek standar. Template ini membantu Anda membuat jadwal dan menentukan nilai moneter pada kuotasi dan komponennya (baris kuotasi). 

Anda dapat membuat beberapa kuotasi untuk proyek dan mengelompokkannya dalam satu jenis entitas peluang. Akhirnya, salah satu kuotasi ditandai **ditutup sebagai menang**, dan kontrak proyek atau pernyataan pekerjaan (Sow) dibuat. Kontrak proyek berisi nilai kontrak untuk setiap komponen (baris kontrak) yang diterima oleh pelanggan untuk pelaksanaan. SOW biasanya dibuat sebagai dokumen Microsoft Word. Semua faktur yang dikirim ke pelanggan selama periode pengiriman proyek merujuk pada kontrak proyek atau SOW.

Anda juga dapat membuat kuotasi alternatif dalam satu jenis entitas peluang atau mengkonfigurasi sistem sehingga kontrak proyek dibuat saat kuotasi dimenangkan. Dalam kasus ini, Anda dapat melampirkan dokumen Word yang mewakili SOW untuk rekaman kontrak proyek.

![Menutup kuotasi untuk membuat kontrak proyek.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Mengkonfigurasi proses penjualan
Anda dapat menggunakan alur proses bisnis (BPF) di Microsoft Dynamics 365 untuk mengkonfigurasi proses penjualan Anda. BPF memberikan antarmuka visual terpandu kepada staf penjualan yang dapat digunakan untuk meneruskan kesepakatan melalui tahapan tipikal perusahaan Anda.

Misalnya, perusahaan Anda mungkin memiliki enam tahapan berikut dalam proses penjualan:

1. Kualifikasi
2. Perkirakan
3. Pemeriksaan Internal
4. Kontrak
5. Laksanakan
6. Tutup

Keenam tahapan ini diwakili oleh chevron (\>) yang Anda pilih untuk diperluas di setiap jenis entitas peluang yang Anda buat.

![Konfigurasi proses bisnis di Dynamics 365.](media/basic-guide-3.png)
 
Organisasi Anda mungkin menggunakan entitas yang berbeda untuk menunjukkan kesepakatan yang sama seiring perkembangannya. Di awal proses penjualan, kesepakatan diwakili oleh entitas peluang. Seiring berjalannya waktu dan rincian lainnya muncul, Anda dapat menggunakan perkiraan tingkat tinggi untuk membuat satu atau beberapa kuotasi. Jika salah satu dari kuotasi ini ditinjau oleh pemangku kepentingan internal dan pelanggan, entitas kuotasi menunjukkan transaksi. Setelah pelanggan menerima kuotasi, kontrak proyek atau SOW menunjukkan kesepakatan. Untuk mendukung perilaku ini, BPF distrukturkan sehingga setiap tahapan dalam proses dihubungkan dengan tabel database yang berbeda.

Tahapan **kualifikasi** dalam proses penjualan dapat didukung oleh entitas peluang. Tahapan **estimasi** dan **peninjauan internal** dapat didukung oleh entitas kuotasi. Tahapan **kontrak**, **Pelaksanaan**, dan **penutupan** dapat didukung oleh entitas kontrak proyek.

Saat Anda meneruskan transaksi melalui tahapan, Anda akan diminta membuat rekaman entitas yang sesuai untuk membantu dan memandu Anda melakukan proses. Tahapan dapat kondisional. Misalnya, jika Anda memerlukan peninjauan internal pada kuotasi hanya jika kuotasi menggunakan daftar harga kustom, Anda dapat mengkonfigurasikan kondisi tersebut dalam tahapan proses bisnis yang sesuai. Tahap **peninjauan internal** kemudian ditampilkan hanya untuk kuotasi yang menggunakan daftar harga kustom. Untuk semua transaksi dan kuotasi lainnya, tahapan **estimasi** diikuti oleh tahapan **kontrak**.

> [!NOTE]
> PSA memiliki halaman tertentu untuk entitas peluang, kuotasi, pesanan, dan faktur. Anda harus membuat peluang, kuotasi, pesanan, dan faktur Project Service menggunakan halaman informasi proyek untuk entitas ini. Jika Anda menggunakan halaman lain untuk membuat rekaman, Anda tidak dapat membuka rekaman dari halaman **informasi proyek**. Jika Anda ingin membuka rekaman dari halaman **informasi proyek**, Anda harus menghapus rekaman, dan membuatnya kembali menggunakan halaman **informasi proyek**. Pada halaman **informasi proyek**, logika bisnis untuk masing-masing jenis entitas ini memastikan bahwa bidang **jenis** rekaman diatur dengan benar, dan semua konsep wajib diinisialisasi dengan benar.

> ![Informasi proyek untuk pesanan baru.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Perbedaan antara Project Service Automation dan Sales
Walaupun proses penjualan dalam PSA menggunakan kemampuan dasar dari proses penjualan di penjualan, namun memiliki beberapa perbedaan penting karena variasi praktik bisnis organisasi berbasis proyek. Berikut adalah beberapa contoh:

- **Kuotasi proyek** – di Project Service Automation, kuotasi ditutup setelah kontrak proyek dibuat dari kuotasi. Di Sales, Anda dapat menyimpan kuotasi secara terbuka setelah Anda menang. Alasan untuk perbedaan ini adalah kecocokan antara kuotasi dan kontrak proyek lebih baik untuk organisasi berbasis proyek. 
- **Aktivasi dan revisi** – dalam PSA, aktivasi dan revisi tidak didukung untuk kuotasi proyek. Dalam Sales, kuotasi dapat dikunci untuk mencegah pengeditan tambahan.
- **Menutup kuotasi sebagai kalah atau menang** – dalam PSA, saat kuotasi proyek ditutup karena menang atau kalah, peluang tetap terbuka. Semua kuotasi lain pada peluang ditutup sebagai kalah. Di Sales, saat kuotasi ditutup sebagai menang, atau kalah, pengguna diminta untuk melakukan tindakan pada peluang. Tergantung pada input pengguna, peluang yang mendasari mungkin ditutup atau dibiarkan terbuka.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Melacak revisi untuk kuotasi dan rencana proyek dalam siklus penjualan
Dalam PSA, Anda tidak dapat melacak revisi yang dibuat ke kuotasi. Namun, Anda harus menandai kuotasi yang ada **ditutup sebagai kalah**, lalu membuat kuotasi baru. Anda dapat menyalin kuotasi atau mengkloning kuotasi berbasis proyek menggunakan PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Melacak komentar dan persetujuan kuotasi dan kontrak proyek
Anda dapat mengelola peninjauan dan persetujuan kuotasi dan kontrak proyek menggunakan posting dan dinding rekaman. Organisasi Anda dapat membuat alur kerja dan plug-in kustom untuk menetapkan, mengalihkan, melaporkan, dan mengelola pemberitahuan tentang item kerja peninjauan dan persetujuan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
