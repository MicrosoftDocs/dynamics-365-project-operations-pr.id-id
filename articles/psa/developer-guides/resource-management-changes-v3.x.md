---
title: Perubahan manajemen Sumber Daya (Project Service Automation 3.x)
description: Artikel ini menyediakan informasi tentang perubahan area manajemen sumber daya.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916016"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Perubahan manajemen Sumber Daya (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Bagian dari artikel ini memberikan informasi tentang perubahan yang telah dibuat ke area manajemen sumber daya dari Dynamics 365 Project Service Automation versi 3. x.

## <a name="project-estimates"></a>Perkiraan proyek

Alih-alih berdasarkan entitas **msdyn\_projecttask** (**tugasproyek**), perkiraan proyek didasarkan pada entitas **msdyn\_resourceassignment** (**penetapan sumber daya**). Tugas sumber daya telah menjadi "sumber kebenaran" untuk penjadwalan tugas dan harga.

## <a name="line-tasks"></a>Baris tugas

Dalam PSA 3. x, Baris tugas sudah usang (ditolak). Tugas sekarang diarahkan ke tugas keseluruhan dan bukan baris tugas.

Contoh berikut menunjukkan cara kerja yang bernama "tes tugas" ditetapkan untuk anggota tim A dan B di versi sebelumnya PSA dan PSA 3.x.

- **Sebelum PSA 3.x:**

    - tes tugas

        - tes tugas – baris tugas 1

            - Penetapan ke A

        - tes tugas – baris tugas 2

            - Penetapan ke B

- **PSA 3.x:**

    - tes tugas

        - Penetapan ke A
        - Penetapan ke B

## <a name="unassigned-assignment"></a>Penugasan yang belum ditetapkan

Dalam PSA 3. x, tugas yang belum ditetapkan adalah tugas yang ditetapkan ke anggota tim **null** dan sumber daya **null**. Tugas yang tidak ditetapkan dapat terjadi dalam beberapa skenario:

- Jika tugas dibuat, namun belum ditetapkan ke anggota tim, tugas yang belum ditetapkan akan selalu dibuat. 
- Jika semua penerima tugas dihapus, tugas yang belum ditetapkan akan dibuat ulang untuk tugas tersebut.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Bidang penjadwalan pada entitas tugas proyek

Bidang entitas **msdyn\_projecttask** telah ditolak atau dipindahkan ke entitas **msdyn\_resourceassignment**, atau mereka sekarang dirujuk dari entitas **msdyn\_projectteam** (**anggota tim proyek**).

| Bidang ditolak pada msdyn\_projecttask (tugas proyek) | Bidang baru pada msdyn\_resourceassignment (penetapan sumber daya) | Komentar |
|---|---|---|
| msdyn\_assignedresources | Tidak ada | |
| msdyn\_assignedteammembers | Tidak ada | |
| msdyn\_numberofresources | Tidak ada | |
| msdyn\_scheduledhours | Tidak ada | |
| msdyn\_effortcontour | msdyn\_plannedwork | Format struktur data notasi objek JavaScript (JSON) yang disimpan di bidang telah diubah. |

## <a name="schedule-contour"></a>Kontur jadwal

Kontur jadwal disimpan di bidang **kerja yang direncanakan** (**msdyn\_plannedwork**) dari setiap entitas **penetapan sumber daya** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktur

Struktur baru kontur jadwal terdiri dari potongan waktu fleksibel yang ditentukan untuk setiap hari jadwal. Setiap potongan waktu memiliki properti berikut:

- **Mulai** – dimulainya jam kerja untuk hari tersebut, sesuai kalender proyek.
- **Akhir** – akhir jam kerja untuk hari tersebut, sesuai kalender proyek.
- **Jam** – jumlah jam yang ditetapkan pada hari.

**Contoh**

Contoh ini menggunakan kalender proyek dengan hari kerja adalah dari jam 9 hingga 5 sore di zona waktu UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Penjadwalan otomatis dan penjadwalan manual

Jika tugas dijadwalkan otomatis, jam dimasukkan di depan, dan durasi tugas mungkin dikurangi.

**Contoh**

Tugas berikut dijadwalkan otomatis selama 18 jam selama tiga hari (3 Desember 2018, hingga 5 Desember 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Jika tugas dijadwalkan secara manual, jam akan didistribusikan secara merata ke semua tanggal.

**Contoh**

Tugas berikut dijadwalkan secara manual selama 18 jam selama tiga hari (3 Desember 2018, hingga 5 Desember 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unit Penetapan

Unit penetapan telah ditolak dalam PSA 3. x. Jam kerja tugas sekarang terbagi rata, per hari, di antara semua sumber daya yang ditetapkan.

**Contoh**

Dalam contoh ini, tugas ditetapkan ke dua sumber daya dan dijadwalkan otomatis untuk 36 jam selama tiga hari (3 Desember 2018, 5 Desember 2018).

- Penetapan 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Penetapan 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensi Harga

Di PSA 3.x, bidang dimensi harga spesifik sumber daya (seperti **peran** dan **unit organisasi**) telah dihapus dari entitas **msdyn\_projecttask**. Bidang ini sekarang dapat diperoleh dari anggota tim proyek terkait (**msdyn\_projectteam**) dari tugas sumber daya (**msdyn\_resourceassignment**) saat perkiraan proyek dibuat. Bidang baru , **msdyn\_organizationalunit**, telah ditambahkan ke entitas **msdyn\_projectteam**.

| Bidang ditolak pada msdyn\_projecttask (tugas proyek) | Bidang dari msdyn\_projectteam (anggota tim proyek) yang digunakan sebagai gantinya |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Kontur

Bidang kontur harga dan perkiraan telah ditolak pada entitas **msdyn\_projecttask**. Mereka telah dipindahkan ke entitas **msdyn\_resourceassignment**.

| Bidang ditolak pada msdyn\_projecttask (tugas proyek) | Bidang baru pada msdyn\_resourceassignment (penetapan sumber daya) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Bidang berikut ini telah ditambahkan ke entitas **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Bidang berikut untuk biaya dan penjualan yang direncanakan, aktual, dan tersisa tidak berubah pada entitas **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
