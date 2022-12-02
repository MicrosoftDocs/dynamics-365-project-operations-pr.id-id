---
title: Menetapkan sumber daya untuk tugas
description: Artikel ini menyediakan informasi tentang cara menetapkan sumber daya untuk tugas.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: dae5a81c51f34b9115ac8c267452b167a6d7bef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913486"
---
# <a name="assign-a-resource-to-a-task"></a>Menetapkan sumber daya untuk tugas

[!include [banner](../includes/psa-now-project-operations.md)]

Ada tiga cara untuk menetapkan sumber daya tugas di Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Pesan sumber daya sebagai anggota tim lalu tetapkan sumber daya untuk tugas

Anda dapat menambahkan sumber daya untuk tim proyek dan kemudian menetapkan sumber daya untuk tugas dalam jadwal proyek.

1. Pada tab **Team Member**, Anda dapat menambahkan anggota tim baru dengan memilih **baru**. 

2. Panel **Team Member Quick Create** terbuka, di mana Anda dapat memilih nama sumber daya dapat dipesan dan menetapkan peran. 

    Pilih salah satu metode alokasi berikut untuk pemesanan sumber daya:

    - **Kapasitas Penuh** Metode ini memesan kapasitas penuh sumber daya untuk tanggal dari dan hingga yang ditentukan.
    - **Kapasitas Persentase** memesan sumber daya untuk persentase kapasitas sumber daya untuk tanggal dari dan hingga yang ditentukan.
    - **Distribusi merata Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, menyebarkannya secara merata setiap hari lebih dari yang ditentukan tanggal dari dan hingga.
    - **Muat Depan Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, memuat dulu jam per hari lebih dari yang ditentukan tanggal dari dan hingga.
    - **Tidak ada** menambahkan sumber daya ke tim, namun tidak membuat pemesanan yang menyerap kapasitas mereka.

3. Pada kisi **jadwal** untuk tugas, pilih ikon **sumber daya** di sel sumber daya, dan kemudian pilih anggota tim yang baru saja ditambahkan di **Team Members**. 

> [!NOTE]
> Pada tab **Team Member** dan tab **rekonsiliasi**, sumber daya menunjukkan jam dipesan dan ditetapkan. Jam harus sama, tetapi tidak wajib karena Pemesanan dan tugas tidak berhubungan erat. Tab **rekonsiliasi** menyediakan rincian saat mereka berbeda, seperti saat Anda menetapkan sumber daya lebih lama dibandingkan Anda memesan. Jika dibutuhkan Anda dapat mengoreksi informasi dengan memperluas Pemesanan sumber daya atau mengubah tugas.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Membuat anggota tim generik melalui penetapan tugas

Saat membuat anggota tim generik melalui penetapan tugas, Anda membuat placeholder atau sumber daya generik yang menjelaskan karakteristik sumber daya bernama yang pada akhirnya akan bekerja pada tugas. Anda kemudian menghasilkan persyaratan (atau mengirimkan permintaan menggunakan persyaratan) yang digunakan untuk mencari dan memesan sumber daya bernama.

1. Pada kisi **jadwal** untuk tugas, pilih ikon sumber daya di sel **sumber daya**.

2. Masukkan nama untuk berfungsi sebagai nama sumber daya. Misalnya, manajer program.

3. Pada **Buat**, dan di bidang **Buat cepat anggota tim proyek**, atur peran sumber daya generik.

4. Anda dapat terus menetapkan tugas ke sumber daya placeholder ini dengan memilih sumber daya pada **pemilih sumber daya** untuk tugas. Mereka terdaftar di bawah **Team Members**.

5. Setelah selesai menetapkan sumber daya generik, pilih sumber daya generik di **tim** tab kemudian pilih **menghasilkan persyaratan** untuk membuat persyaratan sumber daya untuk sumber daya generik.

6. Pilih **Pesan** untuk sumber daya generik. Anda dapat menggunakan papan jadwal untuk mencari dan memesan sumber daya nyata. Anda juga dapat mengirimkan persyaratan untuk pemenuhannya dengan manajer sumber daya.

7. Ketika sumber daya generik dipenuhi dengan sumber daya bernama, sumber daya generik dihilangkan dari tim dan penugasan tugas untuk sumber daya generik ditetapkan ke sumber daya bernama yang memenuhi persyaratan sumber daya generik itu.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Menetapkan sumber daya bernama dari daftar semua sumber daya yang dapat dipesan

Anda dapat menggunakan kotak pencarian di **pemilih sumber daya** untuk mencari semua sumber daya dapat dipesan dan menetapkan mereka untuk tugas.

Sumber daya yang ditetapkan dengan cara ini ditambahkan ke tim tanpa pemesanan. Hal ini mirip dengan menambahkan anggota tim dan memilih tidak ada sebagai metode alokasi. Sumber daya ditampilkan dalam tab **tim** dan tab **rekonsiliasi** sebagai sumber daya dengan hanya tugas dan defisit pemesanan. Pesan mereka jika Anda ingin menggunakan ketersediaan mereka.

1. Pada kisi **jadwal** untuk tugas, pilih ikon sumber daya di sel **sumber daya**.

2. Mulai mengetik nama. Hasil pencarian untuk nama akan ditampilkan di **pemilih sumber daya** dalam **sumber daya lainnya**.

3. Pilih sumber daya yang akan ditetapkan ke tugas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
