---
title: Konfigurasi proyek faktur antarperusahaan
description: Topik ini menunjukkan cara menyiapkan faktur proyek antara dua perusahaan di organisasi anda.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288383"
---
# <a name="configure-intercompany-project-invoicing"></a>Konfigurasi proyek faktur antarperusahaan

[!include [banner](../../includes/banner.md)]

Topik ini menunjukkan cara menyiapkan faktur proyek antara dua perusahaan di organisasi anda. Tugas ini menggunakan himpunan data USSI.

1. Di panel navigasi, buka **modul > piutang > vendor > semua vendor**.
2. Di Daftar **semua vendor**, Cari dan pilih rekaman yang diinginkan.
3. Pada panel tindakan, pilih **umum**.
4. Pilih **Antarperusahaan**.
5. Atur **aktif** ke **ya** untuk mengaktifkan perdagangan antarperusahaan.
6. Di bidang **Perusahaan pelanggan**, masukkan atau pilih nilai.
7. Di bidang **Akun saya**, masukkan atau pilih nilai.
8. Pilih **Simpan**.
9. Tutup halaman untuk kembali ke halaman Beranda.
10. Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > parameter manajemen proyek dan akuntansi**.
11. Pilih tab **Antarperusahaan**.
12. Pindahkan slider ke **ya** untuk mengaktifkan penjadwalan dan lembar waktu sumber daya antarperusahaan.
13. Di daftar, Tandai baris yang dipilih.
14. Pilih **baru**.
15. Di bidang **Entitas hukum pinjaman**, masukkan atau pilih nilai.
16. Pilih kotak centang **Akumulasikan penghasilan**.
17. Di bidang **Kategori lembar waktu default**, masukkan atau pilih nilai.
18. Di bidang **Kategori pengeluaran default**, masukkan atau pilih nilai.
19. Pilih **Simpan**.
20. Tutup halaman.
21. Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Posting > Konfigurasi posting buku besar**.
22. Di bidang **jenis akun buku besar**, pilih pilihan.
23. Pilih **baru**.
24. Di bidang **akun utama** baris baru, tentukan nilai yang diinginkan.
25. Pilih **Simpan**.
26. Tutup halaman.
27. Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Harga > Harga transfer**.
28. Pilih **baru**.
29. Di bidang **Tanggal efektif**, masukkan tanggal.
30. Di bidang **Entitas hukum pinjaman**, masukkan atau pilih nilai.
31. Di bidang **model harga transfer**, pilih salah satu pilihan.
32. Di bidang **harga**, masukkan angka.
33. Pilih **Simpan**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]