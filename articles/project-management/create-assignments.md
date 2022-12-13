---
title: Buat Penetapan Sumber Daya
description: artikel ini menyediakan informasi tentang pembuatan penetapan sumber daya generik dan bernama.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811997"
---
# <a name="create-resource-assignments"></a>Buat Penetapan Sumber Daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Penetapan sumber daya adalah asosiasi langsung anggota tim proyek ke tugas node leaf. artikel ini menyediakan informasi tentang berbagai cara menetapkan sumber daya.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Membuat anggota tim generik melalui penetapan tugas


Saat membuat anggota tim generik melalui penetapan tugas, Anda membuat placeholder, atau sumber daya generik. Sumber daya generik ini menjelaskan karakteristik sumber daya bernama yang pada akhirnya ingin Anda kerjakan pada tugas tersebut. Anda kemudian membuat persyaratan, atau Anda mengirimkan permintaan dengan menggunakan persyaratan yang digunakan untuk mencari dan memesan sumber daya bernama.

1. Pada kisi jadwal untuk tugas, pilih ikon sumber daya di sel **sumber daya**.
2. Ketikkan nama untuk berfungsi sebagai nama sumber daya tempat penampung. Misalnya, manajer program.
3. Pada **Buat**, dan di bidang **Buat cepat anggota tim proyek**, atur peran sumber daya generik.
4. Tetapkan tugas sesuai kebutuhan ke sumber daya placeholder ini dengan memilih sumber daya pada **pemilih sumber daya** untuk tugas. Sumber daya yang terdaftar di bawah **Anggota Tim**.
5. Setelah selesai menetapkan sumber daya generik, pada **tab Tim**, pilih sumber daya generik, lalu pilih **Buat Persyaratan untuk** membuat persyaratan sumber daya untuk sumber daya generik.
6. Pilih **Pesan** untuk sumber daya generik, dan kemudian gunakan papan jadwal untuk mencari dan memesan sumber daya nyata. Anda juga dapat mengirimkan persyaratan untuk pemenuhannya dengan manajer sumber daya.
7. Ketika sumber daya generik sepenuhnya dipenuhi dengan sumber daya bernama, sumber daya generik dihapus dari tim. (Pemenuhan persyaratan sumber daya parsial tidak akan menghasilkan penugasan sumber daya.) Penetapan tugas untuk sumber daya generik ditetapkan ke sumber daya bernama yang memenuhi persyaratan sumber daya sumber daya generik.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Menetapkan sumber daya bernama dari daftar semua sumber daya yang dapat dipesan

Anda dapat menggunakan kotak pencarian di **pemilih sumber daya** untuk mencari semua sumber daya aktif dapat dipesan dan menetapkan mereka tugas node leaf. Sumber daya yang ditetapkan dengan cara ini ditambahkan ke tim tanpa pemesanan. Hal ini mirip dengan menambahkan anggota tim dan memilih **tidak ada** sebagai metode alokasi. Sumber daya ditampilkan dalam tab **tim**, **Penetapan Sumber daya**, dan tab **rekonsiliasi** sebagai sumber daya dengan hanya tugas dan defisit pemesanan. Pesan mereka jika Anda ingin menggunakan ketersediaan mereka.

1. Dari kisi tugas, papan, atau kronologi, navigasi ke sel **ditetapkan ke**.
2. Di kotak pencarian, mulai ketik nama. Hasil pencarian untuk nama akan ditampilkan di **pemilih sumber daya** dalam **sumber daya lainnya**.
3. Pilih sumber daya yang akan ditetapkan ke tugas atau pilih nama sumber daya di bawah **sumber daya tim lainnya**.

## <a name="editing-resource-assignment-contours"></a>Edit kontur penugasan sumber daya

Secara default, ketika sumber daya ditetapkan ke tugas dalam jadwal, upaya mereka didistribusikan secara linier ke setiap sumber daya, berdasarkan jam kerja sumber daya tersebut dan mode jadwal proyek. Manajer proyek dapat menggunakan kisi penugasan sumber daya untuk memperbaiki perkiraan upaya setiap sumber daya yang ditetapkan ke satu atau banyak tugas di berbagai skala waktu. Fitur ini membantu manajer proyek menghasilkan perkiraan biaya dan penjualan yang lebih akurat, yang didorong oleh kontur penugasan sumber daya yang dihasilkan saat sumber daya ditetapkan ke tugas. Selain itu, manajer proyek dapat lebih mudah mencerminkan permintaan sumber daya yang diperlukan untuk membangun permintaan dalam kebutuhan sumber daya.

### <a name="navigation"></a>Navigasi

Untuk mengakses kisi pengeditan kontur, manajer proyek pertama-tama **memilih tab Tugas** di halaman utama proyek lalu memilih **tab Tugas** .

![Tab Tugas pada tab Tugas di halaman utama proyek.](media/AssignmentGrid.png)

Kisi mendukung dua metode untuk pengelompokan: **grup menurut sumber daya** dan **grup berdasarkan tugas**. Tidak seperti dalam tampilan kisi, kolom tidak dapat dikonfigurasi. Satu-satunya kolom yang terlihat adalah **Ditugaskan Ke**, Nama **Tugas, Mulai** Penugasan, Tugas Selesai **,** **dan** **Upaya** Penugasan.

Ketika grid awalnya dirender, itu dimulai pada kontur penugasan paling awal. Jika jadwal Anda tidak berisi tugas apa pun yang memiliki usaha, kisi akan kosong dan tidak akan merender apa pun.

![Kisi tugas kosong.](media/emptyassignmentgrid.png)

Jika Anda ingin melihat kontur dan skala waktu yang berbeda, kisi penetapan sumber daya baca-saja dan kisi rekonsiliasi sumber daya juga tersedia.

### <a name="resource-calendars"></a>Kalender sumber daya

Kemampuan untuk mengedit kontur untuk hari tertentu diatur oleh hari kerja sumber daya, sebagaimana tercermin dalam kalender mereka. Jika sel dinonaktifkan untuk sumber daya tertentu, sumber daya tersebut tidak memiliki hari kerja selama periode tersebut.

Kontur sumber daya dapat melampaui tanggal mulai dan akhir tugas yang ditetapkan saat ini. Jika kontur diperbarui sehingga setelah tanggal akhir tugas terbaru atau tanggal mulai tugas paling awal, tanggal akhir atau tanggal mulai tugas akan diubah sebagaimana mestinya. Namun, jika kontur diperbarui sehingga lebih awal dari tanggal mulai tugas yang ditautkan ke pendahulunya, pembaruan akan gagal karena tugas akan memicu tugas untuk memulai sebelum pendahulunya selesai, dan perilaku tersebut saat ini tidak didukung.

### <a name="co-authoring"></a>Penulisan bersama

Perubahan pada kisi penetapan sumber daya secara otomatis tercermin dalam tampilan terkait, termasuk tampilan bagan, garis waktu, papan, dan kisi. Jika beberapa pengguna meninjau proyek secara bersamaan, setiap perubahan yang dibuat oleh satu pengguna akan tercermin dalam kisi. Sebaliknya, setiap perubahan yang dibuat dalam kisi penetapan sumber daya akan ditampilkan kepada semua pengguna lain yang melihat proyek dalam sesi yang sama.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
