---
title: Pertimbangan peningkatan untuk struktur rincian kerja
description: Topik ini menyediakan informasi tentang cara meningkatkan struktur rincian kerja dari Project Service Automation 2.x hingga 3.x.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078566"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Pertimbangan peningkatan untuk struktur rincian kerja
Topik ini menyediakan informasi tentang cara meningkatkan struktur rincian kerja dari Project Service Automation 2.x hingga 3.x. Topik ini menentukan status sehat proyek di project Service Automation (PSA) yang diperlukan untuk peningkatan yang berhasil. Ada juga informasi tentang kondisi pemblokiran umum yang akan menyebabkan peningkatan gagal. Untuk informasi lebih lanjut tentang mendefinisikan tugas proyek dan fungsinya dalam jadwal proyek, lihat [jadwal proyek](project-creating.md).

## <a name="key-entities"></a>Entitas utama
Untuk struktur rincian kerja yang akurat yang telah dimuat dengan sumber daya, entitas berikut diperlukan:

- [Proyek](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Tim Proyek](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Tugas Proyek](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Penetapan Sumber Daya](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dependensi Tugas Proyek](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Sumber Daya yang Dapat Dipesan](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Untuk menentukan struktur rincian kerja yang dimuat sumber daya, Anda harus menyelesaikan langkah-langkah berikut:

1. Buat proyek baru. Untuk informasi lebih lanjut tentang cara membuat proyek baru, lihat [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Buat satu atau beberapa tugas. Untuk informasi lebih lanjut tentang cara membuat tugas baru, lihat [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Tentukan dependensi tugas. Untuk informasi lebih lanjut, Lihat [ketergantungan tugas proyek](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Tetapkan anggota tim proyek ke proyek. Untuk informasi selengkapnya, lihat [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Tetapkan anggota tim proyek ke tugas. Untuk informasi selengkapnya, lihat [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relasi tim proyek

Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:
- Semua anggota tim proyek harus dikaitkan dengan sumber daya yang dapat dipesan.
- Semua anggota tim proyek harus dikaitkan dengan proyek yang sama. 

## <a name="project-task-relationships"></a>Relasi tugas proyek
Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:

- Tugas terkait harus dikaitkan dengan proyek yang sama.
- Setiap tugas baris harus memiliki tugas induk.
- Setiap tugas harus memiliki proyek induk.

### <a name="valid-conditions"></a>Tambah valid

- Semua durasi tugas harus lebih dari atau sama dengan (> =) satu jam dan kurang dari 1.800.000 menit (1.250 hari). *
- Semua tugas harus memiliki tanggal mulai tidak lebih dari 01/01/2000. *
- Semua tugas harus memiliki tanggal mulai selambat-lambatnya 17 tahun dari hari ini. *
- Semua tugas harus memiliki tanggal mulai sebelumnya atau sama dengan tanggal selesai.
- Semua jenis transaksi pada klasifikasi (pengeluaran, material, pajak, dan waktu) harus memiliki nilai untuk **unit default** dan **grup unit**.
- Format tanggal dengan huruf harus dihindari.

### <a name="potential-mitigation-steps"></a>Langkah-langkah mitigasi potensial
- Gunakan pencarian tingkat lanjut untuk mengidentifikasi tugas proyek yang tidak berisi ID proyek.
- Gunakan pencarian tingkat lanjut untuk mengidentifikasi tugas proyek dengan durasi yang dijadwalkan lebih besar dari > 1.800.000.
- Sebelum membuat perubahan data apa pun, Anda harus menyelidiki penyesuaian apa pun yang terkait dengan entitas yang mungkin menyebabkan data menjadi status buruk. Penyesuaian ini harus ditangani sebelum melanjutkan dengan pembaruan terkait data.
- Untuk tugas yang teridentifikasi yang tidak memiliki keterkaitan, pertimbangkan untuk menghapus tugas ini jika tidak diperlukan atau jika mereka harus dikaitkan dengan proyek induk yang benar.
- Untuk tugas yang durasinya lebih dari 1.250 hari, pertimbangkan untuk menambahkan beberapa tugas untuk menunjukkan total durasi, jika memungkinkan.

> [!NOTE]
> Item yang diperhatikan dengan tanda bintang (\*) memiliki batas yang disebabkan oleh fakta bahwa manajemen hubungan pelanggan (CRM) hanya mendukung perluasan pengulangan 7.320. Anda harus tetap berada di bawah batas ini.

## <a name="resource-assignment-relationships"></a>Relasi Penetapan Sumber Daya
Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:

- Semua tugas sumber daya dalam struktur rincian kerja harus terkait dengan proyek yang sama.
- Semua tugas sumber daya dalam struktur rincian kerja harus terkait dengan anggota tim proyek dalam proyek yang sama.

### <a name="potential-mitigation-steps"></a>Langkah-langkah mitigasi potensial
- Identifikasi semua tugas yang berada di luar kondisi yang dijelaskan di atas.  
- Tugas sumber daya yang tidak lagi valid harus dihapus.

## <a name="project-task-dependency-relationships"></a>Relasi Dependensi Tugas Proyek
Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:

- Semua dependensi tugas proyek harus terkait dengan proyek yang sama.
- Tugas tidak dapat memiliki dependensi yang sama yang dirujuk lebih dari satu kali.
