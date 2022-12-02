---
title: Menggunakan API jadwal proyek dengan Power Automate
description: Artikel ini menyediakan alur sampel yang menggunakan API (antarmuka penerapan aplikasi) penjadwalan Proyek.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404457"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Menggunakan API jadwal proyek dengan Power Automate

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Artikel ini menjelaskan alur sampel yang menunjukkan cara membuat rencana proyek lengkap menggunakan Microsoft Power Automate, cara membuat Rangkaian Operasi, dan cara memperbarui entitas. Contohnya memperlihatkan cara membuat proyek, anggota tim proyek, Rangkaian Operasi, tugas proyek, dan penugasan sumber daya. Artikel ini juga menjelaskan cara memperbarui entitas dan menjalankan Rangkaian Operasi.

Berikut adalah daftar lengkap langkah-langkah yang didokumentasikan dalam alur sampel di artikel ini:

1. [Buat pemicu PowerApps](#1)
2. [Buat Proyek](#2)
3. [Menginisialisasi variabel untuk anggota tim](#3)
4. [Buat anggota tim generik.](#4)
5. [Buat Rangkaian Operasi](#5)
6. [Membuat wadah proyek](#6)
7. [Menginisialisasi variabel untuk status tautan](#7)
8. [Menginisialisasi variabel untuk nomor tugas](#8)
9. [Menginisialisasi variabel untuk ID tugas proyek](#9)
10. [Lakukan hingga](#10)
11. [Atur Tugas Proyek](#11)
12. [Buat Tugas Proyek](#12)
13. [Buat penugasan Sumber Daya](#13)
14. [Kurangi variabel](#14)
15. [Mengubah tugas proyek.](#15)
16. [Jalankan Rangkaian Operasi](#16)

## <a name="assumptions"></a>Asumsi

Artikel ini mengasumsikan bahwa Anda memiliki pengetahuan dasar tentang platform Dataverse, aliran cloud, dan API (Antarmuka Pemrograman Aplikasi) Penjadwalan Proyek. Untuk informasi lebih lanjut, lihat bagian [Referensi](#references) nanti di artikel ini.

## <a name="create-a-flow"></a>Buat alur

### <a name="select-an-environment"></a>Pilih lingkungan

Anda tidak dapat membuat alur Power Automate dalam lingkungan Anda.

1. Buka <https://flow.microsoft.com> dan gunakan kredensial administrator Anda untuk masuk.
2. Di sudut kanan atas, pilih **Lingkungan**.
3. Di daftar menurun, pilih lingkungan tempat Dynamics 365 Project Operations diinstal.

### <a name="create-a-solution"></a>Membuat solusi

Ikuti langkah berikut untuk membuat [alur sadar solusi](/power-automate/overview-solution-flows). Dengan membuat alur sadar solusi, Anda dapat dengan lebih mudah mengekspor alur tersebut untuk menggunakannya nanti.

1. Di panel navigasi, pilih **Solusi**.
2. Pada halaman **Solusi**, pilih **Solusi Baru**.
3. Di kotak dialog **Solusi baru**, atur bidang yang perlu diisi, lalu pilih **Buat**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Langkah 1: Buat pemicu PowerApps

1. Di halaman **Solusi**, pilih solusi yang ingin Anda buat, lalu pilih **Baru**.
2. Pada panel kiri, pilih **Alur Cloud** \> **Otomatisasi** \> **alur Cloud** \> **Instan**.
3. Di bidang **Nama alur**, masukkan **Alur Demo API Jadwal**.
4. Dalam daftar **Pilih cara memicu alur ini**, pilih **Power Apps**. Bila Anda membuat pemicu Power Apps, logika akan sesuai dengan Anda sebagai penulis. Pada artikel ini, biarkan parameter input kosong untuk tujuan pengujian.
5. Pilih **Buat**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Langkah 2: Buat proyek

Ikuti langkah berikut untuk membuat proyek sampel.

1. Pilih **Langkah baru** di alur yang Anda buat.

    ![Menambahkan langkah baru.](media/newstep.png)

2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tindakan tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.

    ![Memilih operasi.](media/chooseactiontab.png)

3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.

![Mengubah nama langkah.](media/renamestep.png)

4. Ganti nama langkah **Buat Proyek**.
5. Pada bidang **Nama Tindakan**, pilih **msdyn\_CreateProjectV1**.
6. Di bidang bidang **msdyn\_subject**, pilih **Tambah konten dinamis**.
7. Pada tab **Ekspresi**, pada bidang fungsi, masukkan **Nama proyek - utcNow()**.
8. Pilih **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Langkah 3: Menginisialisasi variabel untuk anggota tim

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **Mulai variabel**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Init anggota tim**.
5. Pada bidang **Nama**, masukkan **TeamMemberAction**.
6. Di bidang **jenis**, pilih **String**.
7. Masukkan **msdyn\_CreateTeamMemberV1** pada bidang **Nilai**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Langkah 4: Buat anggota tim generik

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tindakan tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Buat anggota tim**.
5. Untuk bidang **Nama Tindakan**, pilih **TeamMemberAction** dalam kotak dialog **konten dinamis**.
6. Pada bidang **Parameter Tindakan**, masukkan informasi parameter berikut.

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

    Berikut adalah penjelasan tentang parameter:

    - **\@\@odata.type** – Nama entitas. Misalnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – kunci primer ID tim proyek. Nilai adalah ekspresi GUID (pengidentifikasi unik global).   ID dibuat dari tab ekspresi.

    - **msdyn\_project\@odata.bind** – ID proyek dari proyek pemilik. Nilai akan menjadi konten dinamis yang berasal dari respons langkah "Buat Proyek". Pastikan Anda memasukkan jalur lengkap dan menambahkan konten dinamis di antara tanda induk. Tanda kutip diperlukan. Misalnya, masukkan **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Nama anggota tim. Misalnya, masukkan **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Langkah 5: Buat Rangkaian Operasi

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tindakan tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Buat Rangkaian Operasi**.
5. Pada bidang **Nama Tindakan**, pilih tindakan kustom **msdyn\_CreateOperationSetV1** Dataverse.
6. Di bidang **Deskripsi**, masukkan **ScheduleAPIDemoOperationSet**.
7. Di bidang **proyek**, masukkan **/msdyn\_projects(**.
8. Pilih kotak **Konten dinamis**, pilih **msdyn\_CreateProjectV1Response ProjectId**.
9. Pada bidang **Proyek,** masukkan **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Langkah 6: Buat wadah proyek

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tambahkan baris baru**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Buat wadah**.
5. Di bidang **Nama tabel**, pilih **Wadah Proyek**.
6. Di bidang **Nama**, masukkan **ScheduleAPIDemoBucket1**.
7. Untuk bidang **Proyek**, Pilih **msdyn\_CreateProjectV1Response ProjectId** di kotak dialog **Konten dinamis**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Langkah 7: Menginisialisasi variabel untuk status tautan

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **Mulai variabel**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Init linkstatus**.
5. Pada bidang **Nama**, masukkan **linkstatus**.
6. Di bidang **jenis**, pilih **Integer**.
7. Pada bidang **nilai**, masukkan **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Langkah 8: Menginisialisasi variabel untuk nomor tugas

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **Mulai variabel**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Jumlah tugas init**.
5. Pada bidang **Nama**, masukkan **jumlah tugas**.
6. Di bidang **jenis**, pilih **Integer**.
7. Pada bidang **nilai**, masukkan **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Langkah 9: Menginisialisasi variabel untuk ID tugas proyek

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **Mulai variabel**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Init ProjectTaskID**.
5. Pada bidang **Nama**, masukkan **jumlah tugas**.
6. Di bidang **jenis**, pilih **String**.
7. Untuk bidang **Nilai**, masukkan **guid()** dalam Penyusun Ekspresi.

## <a name="step-10-do-until"></a><a id="10"></a>langkah 10: Lakukan hingga

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **lakukan hingga**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Atur nilai pertama dalam pernyataan kondisional ke variabel **jumlah tugas** dari kotak dialog **Konten dinamis**.
4. Atur kondisi ke **kurang dari sama dengan**.
5. Atur nilai kedua dalam pernyataan kondisional ke **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>langkah 11: Atur Tugas Proyek

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **Atur variabel**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah baru, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Atur Tugas Proyek**.
5. Pada bidang **Nama**, pilih **msdyn\_projecttaskid**.
6. Untuk bidang **Nilai**, masukkan **guid()** dalam Penyusun Ekspresi.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Langkah 12: Buat tugas proyek

Ikuti langkah-langkah ini untuk membuat tugas proyek yang memiliki ID unik milik proyek saat ini dan wadah proyek yang Anda buat.

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tindakan tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Buat Tugas Proyek**.
5. Pada bidang **Nama Tindakan**, pilih **msdyn\_PssCreateV1**.
6. Di panel **entitas**, masukkan informasi parameter berikut.

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

    Berikut adalah penjelasan tentang parameter:

    - **\@\@odata.type** – Nama entitas. Misalnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – ID unik tugas. Nilai harus diatur ke variabel dinamis dari **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID proyek dari proyek pemilik. Nilai akan menjadi konten dinamis yang berasal dari respons langkah "Buat Proyek". Pastikan Anda memasukkan jalur lengkap dan menambahkan konten dinamis di antara tanda induk. Tanda kutip diperlukan. Misalnya, masukkan **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Nama tugas apa pun.
    - **msdyn\_projectbucket\@odata.bind** – Wadah Proyek yang berisi tugas. Nilai akan menjadi konten dinamis yang berasal dari respons langkah "Buat wadah". Pastikan Anda memasukkan jalur lengkap dan menambahkan konten dinamis di antara tanda induk. Tanda kutip diperlukan. Misalnya, masukkan **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Konten dinamis untuk tanggal mulai. Misalnya, besok akan dinyatakan sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Tanggal mulai yang dijadwalkan. Misalnya, besok akan dinyatakan sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Tanggal berakhir yang dijadwalkan. Pilih tanggal di masa mendatang. Contohnya, tentukan **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Status Tautan. Misalnya, masukkan **"192350000"**.

7. Untuk bidang **OperationSetId**, Pilih **msdyn\_CreateOperationSetV1Response** di kotak dialog **Konten dinamis**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Langkah 13: Membuat penugasan sumber daya

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tindakan tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Buat penugasan**.
5. Pada bidang **Nama Tindakan**, pilih **msdyn\_PssCreateV1**.
6. Di panel **entitas**, masukkan informasi parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Untuk bidang **OperationSetId**, Pilih **msdyn\_CreateOperationSetV1Response** di kotak dialog **Konten dinamis**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Langkah 14: Kurangi variabel

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **kurangi variabel**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Pada bidang **Nama**, pilih **jumlah tugas**.
4. Pada bidang **nilai**, masukkan **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>langkah 15: Ubah nama Tugas Proyek

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tindakan tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **Ubah nama Tugas Proyek**.
5. Pada bidang **Nama Tindakan**, pilih **msdyn\_PssUpdateV1**.
6. Di panel **entitas**, masukkan informasi parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Untuk bidang **OperationSetId**, Pilih **msdyn\_CreateOperationSetV1Response** di kotak dialog **Konten dinamis**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Langkah 16: Jalankan Rangkaian Operasi

1. Pada langkah, pilih **Langkah baru**.
2. Di kotak dialog **Pilih operasi**, di bidang pencarian, masukkan lakukan **tindakan tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam daftar hasil.
3. Dalam langkah, pilih elipsis (**...**), lalu pilih **Ubah Nama**.
4. Ganti nama langkah **jalankan Rangkaian Operasi**.
5. Pada bidang **Nama Tindakan**, pilih **msdyn\_ExecuteOperationSetV1**.
6. Untuk bidang **OperationSetId**, Pilih **msdyn\_CreateOperationSetV1Response OperationSetId** di kotak dialog **Konten dinamis**.

## <a name="references"></a>Referensi

- [Ikhtisar cara mengintegrasikan alur dengan Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan](schedule-api-preview.md)
- [Ikhtisar alur cloud - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Ikhtisar alur sadar solusi - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
