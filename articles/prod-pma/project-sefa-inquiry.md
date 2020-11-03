---
title: Jadwal pengeluaran dari penyelidikan dana pemberian Federal
description: Topik ini menyediakan informasi tentang jadwal pengeluaran dari penyelidikan dana pemberian Federal.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078468"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Jadwal pengeluaran dari penyelidikan dana pemberian Federal

[!include [banner](../includes/banner.md)]

Menurut Surat edaran kantor manajemen dan anggaran A-133, lembaga yang menerima dana Federal tunduk pada persyaratan audit, yang juga dikenal sebagai audit tunggal. Proses audit digunakan untuk melaporkan pendapatan dan pengeluaran hibah Federal secara berulang. Bagian dari Laporan Audit tunggal mencakup jadwal pengeluaran dana pemberian Federal (SEFA).

Jadwal pengeluaran dari penyelidikan dana pemberian Federal mencakup judul Katalog bantuan domestik Federal (CFDA) dan nomor, nomor hibah, tahun hibah, nama badan federal yang menyediakan dana, dan nama entitas penerusan. Penyelidikan adalah untuk periode tertentu. Biasanya, periode tersebut sama dengan periode laporan keuangan, yang merupakan tahun fiskal.

Penyelidikan mencakup hibah yang memiliki tanggal proyeksi dalam rentang tanggal yang dipilih. Kolom **lembaga pemberi hibah** dari penyelidikan menunjukkan pelanggan hibah atau, untuk lembaga penerusan hibah, pemberi hibah. Untuk penerusan hibah, kolom **lembaga penerusan** menampilkan pelanggan hibah. Jika hibah bukan penerusan hibah, kolom **lembaga penerusan** kosong.

## <a name="set-up-the-cfda-clusters"></a>Konfigurasikan kluster CFDA

Anda harus mengkonfigurasi kluster CFDA yang dapat dikaitkan dengan nomor CFDA dalam Penyelidikan jadwal pengeluaran pemberian dana federal.

1. Buka **manajemen proyek dan konfigurasi akuntansi \> Konfigurasi \> hibah \> Katalog kluster bantuan domestik Federal**.
2. Untuk membuat kluster CFDA, pilih **Baru**.
3. Masukkan nama kluster.
4. Pilih **Simpan** untuk menerapkan perubahan.

## <a name="set-up-cfda-numbers"></a>Mengkonfigurasi nomor CFDA

Anda harus mengkonfigurasi nomor CFDA yang dapat ditambahkan ke hibah dan disertakan dalam Penyelidikan jadwal pengeluaran pemberian dana federal.

1. Buka **manajemen proyek dan konfigurasi akuntansi \> Konfigurasi \> hibah \> nomor Katalog bantuan domestik Federal**.
2. Untuk membuat nomor CFDA, pilih **Baru**.
3. Dalam kolom **nomor** , masukkan nomor CFDA.
4. Tekan tombol **tab**.
5. Dalam kolom **Deskripsi** , masukkan judul CFDA.
6. Tekan tombol **tab**.
7. Opsional: di bidang **kluster program** , tambahkan kluster cfda yang sesuai.
8. Pilih **Simpan** untuk menerapkan perubahan.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Atur hibah yang akan dilaporkan untuk Penyelidikan jadwal pengeluaran pemberian dana federal

1. Buka **manajemen proyek dan akuntansi \> hibah \> hibah** , lalu pilih hibah yang ada.
2. Pada fasttab **konfigurasi** , di bidang **Katalog Bantuan domestik Federal** , tetapkan nomor CFDA. Nomor CFDA pada hibah menentukan kluster CFDA untuk pelaporan.
3. Pada fasttab **informasi kontak** , masukkan informasi pemberi dengan mengikuti langkah berikut:

    1. Di bidang **pelanggan hibah** , masukkan Pelanggan yang bertanggung jawab atas hibah. Untuk hibah yang ada, informasi ini mungkin sudah dimasukkan.
    2. Menunjukkan apakah pelanggan hibah adalah penyandang dana. Jika pelanggan hibah adalah penyandang dana, biarkan kotak centang **Penerusan** dikosongkan. Jika pelanggan lain adalah penyandang dana, dan pelanggan hibah bertanggung jawab atas pembelanjaan dan pelacakan uang, pilih kotak centang **Penerusan**.

4. Jika Anda memilih kotak centang **Penerusan** di langkah sebelumnya, di bidang **agen pemberi** , masukkan Pelanggan yang memberikan hibah. Agen pemberi dan pelanggan hibah tidak dapat menjadi Pelanggan yang sama.

Berikut adalah contoh dari hibah penerusan:

Pemerintah federal mendanai proyek infrastruktur untuk suatu negara bagian. Pemerintah federal memberikan uang kepada negara bagian itu untuk dibelanjakan. Dalam kasus ini, pemerintah federal adalah agen pemberi, dan negara bagian itu adalah pelanggan hibah.

> [!NOTE] 
> Saat pertama kali mengaktifkan fitur, nomor CFDA awal akan dimasukkan menggunakan nomor yang ada pada hibah.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Kecualikan hibah dari pelaporan SEFA berdasarkan jenis hibah

1. Buka **manajemen proyek dan akuntansi \> Konfigurasi \> Hibah \> jenis Hibah**.
2. Pada fasttab **informasi default** , pilih kotak centang **Kecualikan dari jadwal pengeluaran pemberian dana Federal**.
3. Pilih **Simpan** untuk menerapkan perubahan.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Jalankan Jadwal pengeluaran dari penyelidikan dana pemberian Federal

1. Buka **manajemen proyek dan akuntansi \> Penyelidikan dan laporan \> Penyelidikan hibah \> jadwal pengeluaran pemberian dana Federal**.
2. Di bagian **Parameter** , ikuti langkah berikut:

    1. Pada bidang **interval tanggal** , pilih kode untuk interval tanggal. Atau, di bidang **dari tanggal** dan **hingga tanggal** , tentukan interval tanggal.
    2. Opsional: untuk mencakup hanya transaksi yang ditagih sebagai pendapatan dalam penyelidikan, atur pilihan **sertakan hanya pendapatan yang ditagihkan** ke **ya**.

## <a name="columns"></a>Kolom

Penyelidikan jadwal pengeluaran pemberian dana Federal mencakup kolom berikut:

- Katalog nama kluster bantuan domestik Federal
- Lembaga pemberi
- Lembaga penerusan
- Nama hibah
- ID hibah
- ID Aplikasi hibah
- Katalog bantuan domestik Federal
- Tanda Terima
- Pengeluaran
