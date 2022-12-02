---
title: Perkiraan Penjualan dan Proyek
description: Artikel ini menyediakan informasi tentang cara memanfaatkan jadwal dan perkiraan dalam proses penjualan.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 957c2337cce3b3bf65a0bfef7c1aee6a730971fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925400"
---
# <a name="sales-estimates-and-projects"></a>Perkiraan Penjualan dan Proyek

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Selama proses penjualan, Anda dapat membuat perkiraan penjualan dengan menautkan proyek ke kuotasi penjualan. Dengan cara ini, perkiraan deterministik dapat terjadi selama proses penjualan, untuk memanfaatkan kemampuan penjadwalan dan estimasi proyek. Jika penjualan disetujui, jadwal yang digunakan untuk perkiraan penjualan dapat digunakan sebagai dasar untuk penyempurnaan lebih lanjut dari rencana proyek.

## <a name="linking-a-project-to-a-quote-line"></a>Menautkan proyek ke baris kuotasi

Saat membuat baris kuotasi berbasis proyek, Anda dapat membuat proyek baru atau mengaitkannya proyek yang ada di halaman **baris kuotasi**. 

> ![Formulir Baris kuotasi.](media/project-8.png)
 
Bila Anda membuat proyek baru dari rincian baris kuotasi, Anda dapat memanfaatkan template proyek. Template proyek adalah proyek model yang menunjukkan rencana proyek standar dan perkiraan keuangan yang tipikal dalam suatu organisasi. Mereka juga dapat menunjukkan salinan rencana proyek dan perkiraan dari proyek sebelumnya.

> ![Rincian Baris Kuotasi.](media/project-9.png)
  
Ketika Anda membuat proyek Anda dari kuotasi, proyek ini otomatis dikaitkan dengan baris kuotasi.

## <a name="components-of-estimates-in-a-project"></a>Komponen perkiraan dalam proyek

Jadwal memungkinkan Anda membagi pekerjaan ke dalam tugas, mengelola hierarki tugas, menentukan sumber daya yang diperlukan untuk menyelesaikan tugas, dan menetapkan perkiraan upaya yang diperlukan untuk menyelesaikan tugas.

Anda dapat menentukan perkiraan upaya kerja dan jadwal dengan menggunakan bidang pada tab **jadwal** halaman **proyek**. Karena daftar harga terkait dengan proyek, perkiraan keuangan dihitung menggunakan harga dan harga penjualan yang ditentukan dalam daftar harga.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Mengimpor perkiraan dari sebuah proyek ke kuotasi

Setelah menentukan perkiraan proyek, Anda dapat mengimpornya ke baris kuotasi. Pada halaman **detail baris kuotasi**, pilih **impor dari perkiraan** pada pita untuk meringkas perkiraan proyek berdasarkan jenis transaksi, peran, atau tingkat tugas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
