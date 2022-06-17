---
title: Menggunakan API jadwal proyek dengan Power Automate
description: Artikel ini menyediakan alur sampel yang menggunakan antarmuka pemrograman aplikasi (API) jadwal Proyek.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916338"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Menggunakan API jadwal proyek dengan Power Automate

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Artikel ini menjelaskan alur sampel yang menunjukkan cara membuat rencana proyek lengkap dengan menggunakan Microsoft Power Automate, cara membuat Set Operasi, dan cara memperbarui entitas. Contoh ini menunjukkan cara membuat proyek, anggota tim proyek, Set Operasi, tugas proyek, dan penugasan sumber daya. Artikel ini juga menjelaskan cara memperbarui entitas dan menjalankan Set Operasi.

Berikut ini adalah daftar lengkap langkah-langkah yang didokumentasikan dalam alur sampel dalam artikel ini:

1. [Membuat PowerApps pemicu](#1)
2. [Buat Proyek](#2)
3. [Menginisialisasi variabel untuk anggota tim](#3)
4. [Membuat anggota tim generik](#4)
5. [Membuat Set Operasi](#5)
6. [Membuat bucket proyek](#6)
7. [Menginisialisasi variabel untuk status tautan](#7)
8. [Menginisialisasi variabel untuk jumlah tugas](#8)
9. [Menginisialisasi variabel untuk ID tugas proyek](#9)
10. [Lakukan sampai](#10)
11. [Mengatur tugas proyek](#11)
12. [Membuat tugas proyek](#12)
13. [Membuat penetapan sumber daya](#13)
14. [Menurunkan variabel](#14)
15. [Mengganti nama tugas proyek](#15)
16. [Menjalankan Set Operasi](#16)

## <a name="assumptions"></a>Asumsi

Artikel ini mengasumsikan bahwa Anda memiliki pengetahuan dasar tentang Dataverse platform, alur cloud, dan Antarmuka Pemrograman Aplikasi (API) Jadwal Proyek. Untuk informasi selengkapnya, lihat bagian [Referensi](#references) nanti di artikel ini.

## <a name="create-a-flow"></a>Buat alur

### <a name="select-an-environment"></a>Pilih lingkungan

Anda dapat membuat Power Automate alur di lingkungan Anda.

1. Buka <https://flow.microsoft.com>, dan gunakan kredensial administrator Anda untuk masuk.
2. Di sudut kanan atas, pilih **Lingkungan**.
3. Dalam daftar, pilih lingkungan tempat Dynamics 365 Project Operations diinstal.

### <a name="create-a-solution"></a>Membuat solusi

Ikuti langkah-langkah ini untuk membuat [alur](/power-automate/overview-solution-flows) yang sadar solusi. Dengan membuat alur yang sadar solusi, Anda dapat lebih mudah mengekspor aliran untuk menggunakannya nanti.

1. Di panel navigasi, pilih **Solusi**.
2. Pada halaman **Solusi**, pilih **Solusi baru**.
3. Dalam kotak **dialog Solusi** baru, atur bidang yang diperlukan, lalu pilih **Buat**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Langkah 1: Buat PowerApps pemicu

1. Pada halaman **Solusi**, pilih solusi yang Anda buat, lalu pilih **Baru**.
2. Di panel kiri, pilih **Cloud flows** \> **Automation** \> **Cloud flow** \> **Instant.**
3. **Di bidang Nama** alur, masukkan **Jadwalkan Alur** Demo API.
4. Di **daftar Pilih cara memicu alur** ini, pilih **Power Apps**. Saat Anda membuat Power Apps pemicu, logikanya terserah Anda sebagai penulis. Pada artikel ini, biarkan parameter input kosong untuk tujuan pengujian.
5. Pilih **Buat**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Langkah 2: Buat proyek

Ikuti langkah-langkah ini untuk membuat proyek sampel.

1. Di alur yang Anda buat, pilih **Langkah baru**.

    ![Menambahkan langkah baru.](media/newstep.png)

2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **melakukan tindakan tidak terikat**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.

    ![Memilih operasi.](media/chooseactiontab.png)

3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.

![Mengganti nama langkah.](media/renamestep.png)

4. Ganti nama langkah **Buat Proyek**.
5. **Di bidang Nama** Tindakan, pilih **msdyn\_ CreateProjectV1**.
6. **Di bawah bidang subjek\_ msdyn**, pilih **Tambahkan konten** dinamis.
7. Pada tab **Ekspresi**, di bidang fungsi, masukkan **Nama proyek - utcNow()**.
8. Pilih **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Langkah 3: Inisialisasi variabel untuk anggota tim

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **inisialisasi variabel**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **anggota** tim Init.
5. **Di bidang Nama**, masukkan **TeamMemberAction**.
6. **Di bidang Tipe**, pilih **String**.
7. **Di bidang Nilai**, masukkan **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Langkah 4: Buat anggota tim generik

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **melakukan tindakan tidak terikat**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Buat Anggota** Tim.
5. **Untuk bidang Nama** Tindakan, pilih **TeamMemberAction** dalam kotak **dialog Konten** dinamis.
6. Di **bidang Parameter** Tindakan, masukkan informasi parameter berikut.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Berikut adalah penjelasan parameternya:

    - **\@\@ odata.type** – Nama entitas. Misalnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – Kunci utama ID tim proyek. Nilainya adalah ekspresi pengidentifikasi unik global (GUID).   ID dihasilkan dari tab ekspresi.

    - **msdyn\_ project\@ odata.bind** – ID proyek dari proyek pemilik. Nilainya adalah konten dinamis yang berasal dari respons langkah "Buat Proyek". Pastikan Anda memasukkan jalur lengkap dan menambahkan konten dinamis di antara tanda kurung. Tanda kutip diperlukan. Misalnya, masukkan **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **nama\_ msdyn**– Nama anggota tim. Misalnya, masukkan **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Langkah 5: Buat Set Operasi

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **melakukan tindakan tidak terikat**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Buat Set** Operasi.
5. **Di bidang Nama** Tindakan, pilih **tindakan kustom msdyn\_ CreateOperationSetV1** Dataverse.
6. **Di bidang Deskripsi**, masukkan **ScheduleAPIDemoOperationSet**.
7. **Di bidang Proyek**, masukkan **/msdyn\_ projects(**.
8. Dalam kotak **dialog Konten** dinamis, pilih **msdyn\_ CreateProjectV1Response ProjectId**.
9. **Di bidang Proyek**, masukkan **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Langkah 6: Buat bucket proyek

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **tambahkan baris** baru. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Buat Bucket**.
5. Di **bidang Nama** Tabel, pilih **Bucket** Proyek.
6. **Di bidang Nama**, masukkan **ScheduleAPIDemoBucket1**.
7. **Untuk bidang Proyek**, pilih **msdyn\_ CreateProjectV1Response ProjectId** di **kotak dialog Konten** dinamis.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Langkah 7: Inisialisasi variabel untuk status tautan

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **inisialisasi variabel**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Init linkstatus**.
5. **Di bidang Nama**, masukkan **linkstatus**.
6. Di **bidang Tipe**, pilih **Bilangan Bulat**.
7. Di **bidang Nilai**, masukkan **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Langkah 8: Inisialisasi variabel untuk jumlah tugas

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **inisialisasi variabel**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Init Jumlah tugas**.
5. Di **bidang Nama**, masukkan **jumlah tugas**.
6. Di **bidang Tipe**, pilih **Bilangan Bulat**.
7. Di **bidang Nilai**, masukkan **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Langkah 9: Inisialisasi variabel untuk ID tugas proyek

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **inisialisasi variabel**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Init ProjectTaskID**.
5. Di **bidang Nama**, masukkan **jumlah tugas**.
6. **Di bidang Tipe**, pilih **String**.
7. **Untuk bidang Nilai**, masukkan **guid()** di penyusun ekspresi.

## <a name="step-10-do-until"></a><a id="10"></a> Langkah 10: Lakukan hingga

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **lakukan hingga**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Atur nilai pertama dalam pernyataan bersyarat ke **variabel jumlah tugas** dari kotak **dialog Konten** dinamis.
4. Atur kondisi menjadi **kurang dari sama dengan**.
5. Atur nilai kedua dalam pernyataan bersyarat ke **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Langkah 11: Tetapkan tugas proyek

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **variabel** set. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di langkah baru, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Atur Tugas** Proyek.
5. **Di bidang Nama**, pilih **msdyn\_ projecttaskid**.
6. **Untuk bidang Nilai**, masukkan **guid()** di penyusun ekspresi.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Langkah 12: Membuat tugas proyek

Ikuti langkah-langkah ini untuk membuat tugas proyek yang memiliki ID unik milik proyek saat ini dan bucket proyek yang Anda buat.

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **melakukan tindakan tidak terikat**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Pada langkah tersebut, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Buat Tugas** Proyek.
5. **Di bidang Nama** Tindakan, pilih **msdyn\_ PssCreateV1**.
6. Di **bidang Entitas**, masukkan informasi parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Berikut adalah penjelasan parameternya:

    - **\@\@ odata.type** – Nama entitas. Misalnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – ID unik dari tugas tersebut. Nilai harus diatur ke variabel dinamis dari **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – ID proyek dari proyek pemilik. Nilainya adalah konten dinamis yang berasal dari respons langkah "Buat Proyek". Pastikan Anda memasukkan jalur lengkap dan menambahkan konten dinamis di antara tanda kurung. Tanda kutip diperlukan. Misalnya, masukkan **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **subjek\_ msdyn**– Nama tugas apa pun.
    - **msdyn\_ projectbucket\@ odata.bind** – Bucket proyek yang berisi tugas. Nilainya adalah konten dinamis yang berasal dari respons langkah "Buat Bucket". Pastikan Anda memasukkan jalur lengkap dan menambahkan konten dinamis di antara tanda kurung. Tanda kutip diperlukan. Misalnya, masukkan **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ start** – Konten dinamis untuk tanggal mulai. Misalnya, besok akan direpresentasikan sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** – Tanggal mulai yang dijadwalkan. Misalnya, besok akan direpresentasikan sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – Tanggal akhir yang dijadwalkan. Pilih tanggal di masa mendatang. Misalnya, tentukan **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – Status tautan. Misalnya, masukkan **"192350000"**.

7. Untuk bidang **OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response** di **kotak dialog Konten** dinamis.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Langkah 13: Membuat penetapan sumber daya

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **melakukan tindakan tidak terikat**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Pada langkah tersebut, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Buat Penugasan**.
5. **Di bidang Nama** Tindakan, pilih **msdyn\_ PssCreateV1**.
6. Di **bidang Entitas**, masukkan informasi parameter berikut.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Untuk bidang **OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response** di **kotak dialog Konten** dinamis.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Langkah 14: Menurunkan variabel

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **variabel penurunan.** Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Di **bidang Nama**, pilih **jumlah tugas**.
4. Di **bidang Nilai**, masukkan **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Langkah 15: Mengganti nama tugas proyek

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **melakukan tindakan tidak terikat**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Pada langkah tersebut, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Ganti Nama Tugas** Proyek.
5. **Di bidang Nama** Tindakan, pilih **msdyn\_ PssUpdateV1**.
6. Di **bidang Entitas**, masukkan informasi parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Untuk bidang **OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response** di **kotak dialog Konten** dinamis.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Langkah 16: Jalankan Set Operasi

1. Di alur, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, di bidang pencarian, masukkan **melakukan tindakan tidak terikat**. Kemudian, pada **tab Tindakan**, pilih operasi dalam daftar hasil.
3. Pada langkah tersebut, pilih elipsis (**...**), lalu pilih **Ganti Nama**.
4. Ganti nama langkah **Jalankan Set** Operasi.
5. **Di bidang Nama** Tindakan, pilih **msdyn\_ ExecuteOperationSetV1**.
6. **Untuk bidang OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response OperationSetId** di **kotak dialog Konten** Dynamid.

## <a name="references"></a>Referensi

- [Gambaran umum tentang cara mengintegrasikan alur dengan Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan](schedule-api-preview.md)
- [Gambaran umum alur cloud - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Gambaran umum alur sadar solusi - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
