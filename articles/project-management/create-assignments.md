---
title: Buat Penetapan Sumber Daya
description: Topik ini menyediakan informasi tentang pembuatan penetapan sumber daya generik dan bernama.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2b918392fbcde1071aa52ffa7834938be1acd383
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576550"
---
# <a name="create-resource-assignments"></a>Buat Penetapan Sumber Daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Penetapan sumber daya adalah asosiasi langsung anggota tim proyek ke tugas node leaf. Topik ini menyediakan informasi tentang berbagai cara menetapkan sumber daya.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Membuat anggota tim generik melalui penetapan tugas


Saat membuat anggota tim generik melalui penetapan tugas, Anda membuat placeholder, atau sumber daya generik. Sumber daya generik ini menjelaskan karakteristik sumber daya bernama yang pada akhirnya akan bekerja pada tugas. Anda kemudian menghasilkan persyaratan (atau mengirimkan permintaan menggunakan persyaratan) yang digunakan untuk mencari dan memesan sumber daya bernama.

1. Pada kisi jadwal untuk tugas, pilih ikon sumber daya di sel **sumber daya**.
2. Masukkan nama untuk berfungsi sebagai nama sumber daya. Misalnya, manajer program.
3. Pada **Buat**, dan di bidang **Buat cepat anggota tim proyek**, atur peran sumber daya generik.
4. Tetapkan tugas sesuai kebutuhan ke sumber daya placeholder ini dengan memilih sumber daya pada **pemilih sumber daya** untuk tugas. Sumber daya yang terdaftar di bawah **Anggota Tim**.
5. Setelah selesai menetapkan sumber daya generik, pilih sumber daya generik di tab **tim** kemudian pilih **menghasilkan persyaratan** untuk membuat persyaratan sumber daya untuk sumber daya generik.
6. Pilih **Pesan** untuk sumber daya generik, dan kemudian gunakan papan jadwal untuk mencari dan memesan sumber daya nyata. Anda juga dapat mengirimkan persyaratan untuk pemenuhannya dengan manajer sumber daya.
7. Bila sumber daya generik terpenuhi sepenuhnya (pemenuhan persyaratan sumber daya sebagian tidak akan mengakibatkan penetapan sumber daya) dengan sumber daya bernama, sumber daya generik akan dihapus dari tim. Penetapan tugas untuk sumber daya generik ditetapkan ke sumber daya bernama yang memenuhi persyaratan sumber daya generik.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Menetapkan sumber daya bernama dari daftar semua sumber daya yang dapat dipesan

Anda dapat menggunakan kotak pencarian di **pemilih sumber daya** untuk mencari semua sumber daya aktif dapat dipesan dan menetapkan mereka tugas node leaf. Sumber daya yang ditetapkan dengan cara ini ditambahkan ke tim tanpa pemesanan. Hal ini mirip dengan menambahkan anggota tim dan memilih **tidak ada** sebagai metode alokasi. Sumber daya ditampilkan dalam tab **tim**, **Penetapan Sumber daya**, dan tab **rekonsiliasi** sebagai sumber daya dengan hanya tugas dan defisit pemesanan. Pesan mereka jika Anda ingin menggunakan ketersediaan mereka.

1. Dari kisi tugas, papan, atau kronologi, navigasi ke sel **ditetapkan ke**.
2. Di kotak pencarian, mulai ketik nama. Hasil pencarian untuk nama akan ditampilkan di **pemilih sumber daya** dalam **sumber daya lainnya**.
3. Pilih sumber daya yang akan ditetapkan ke tugas atau pilih nama sumber daya di bawah **sumber daya tim lainnya**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]