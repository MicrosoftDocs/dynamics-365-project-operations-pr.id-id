---
title: Menggunakan Add-in Project Service untuk merencanakan pekerjaan Anda di Microsoft Project | MicrosoftDocs
description: Topik ini menyediakan informasi tentang cara menambah, mengkonfigurasikan, dan menggunakan add-in Microsoft project untuk Microsoft project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 86b676a0cf74e0257fd76cf32271497eebc06e75
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642772"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Menggunakan Add-in Project Service Automation untuk merencanakan pekerjaan Anda di Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] membuatnya lebih mudah bagi Anda untuk melakukan perencanaan proyek, termasuk perkiraan. Anda bisa mendefinisikan pekerjaan sehingga biaya, tenaga, dan nilai penjualan jelas saat proposal final diajukan.  

 Sekarang Anda dapat menginstal [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] dan melakukan pekerjaan perencanaan Anda di lingkungan akrab dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Gunakan kemampuan perencanaan dan manajemen yang kuat dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan kemudian memperbarui rencana proyek Anda di Project service automation.  

> [!IMPORTANT]
> - Untuk menggunakan manajemen dokumen SharePoint untuk menyimpan file [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Anda untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], admin [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Anda akan perlu untuk mengaktifkan manajemen dokumen. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] hanya kompatibel dengan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Men-download dan menginstal pengaya  
 Siapkan informasi masuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Anda. Anda akan memerlukan informasi ini untuk menghubungkan dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Dari pusat Unduhan, unduh add-in untuk versi project service yang didukung, baik [v2.X](https://go.microsoft.com/fwlink/?linkid=828268) atau [v3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Klik tautan download.  

3.  Jika download selesai, klik **ya** untuk menginstal pengaya (add-in).  

## <a name="configure-the-add-in"></a>Mengonfigurasi pengaya  

1. Buka [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan klik tab **Project Service**.  

2. Klik **Hubungkan**.  

3. Masukkan informasi masuk Anda dan kemudian klik **masuk**.  

   Sekarang Anda dapat mulai menggunakan pengaya.  

## <a name="read-from-a-template"></a>Membaca dari template  
 Baca dari template yang Anda buat dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dan salin ke [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] untuk memulai perencanaan proyek Anda. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Membuat template proyek (Project Service Automation)](../psa/create-project-template.md)  

1.  Dari tab **Project service**, klik **Baca** > **Template proyek Project service automation**.  

2.  Pilih template proyek dari daftar dan kemudian klik **buka**.  

    > [!NOTE]
    >  Secara default, tugas-tugas yang disalin dari template ke dalam proyek ditetapkan seperti dijadwalkan secara manual.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Menetapkan peran [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ke sumber daya proyek  

1.  Buka sebuah proyek dan klik pita **tugas**.  

2.  Klik menu **Gantt Chart** menu dan kemudian pilih **lembar sumber daya**.  

3.  Pada lembar sumber daya, klik menu drop-down **peran Project Service Resource** dan pilih peran Project service automation.  

## <a name="staff-your-project-with-resources"></a>Lengkapi proyek Anda dengan sumber daya  

1.  Dari tab Project Service pilih baris dan klik **Temukan sumber daya**.  

2.  Pada layar **Pesan sumber daya**, pilih sumber daya yang ingin Anda gunakan untuk proyek.  

3.  Klik **Buku** dan kemudian klik **OK**.  

## <a name="publish-your-project"></a>Publikasikan proyek Anda.  
Setelah perencanaan proyek Anda selesai, langkah berikutnya adalah untuk mengimpor dan mempublikasikan proyek di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Proyek akan diimpor ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Harga dan proses pembuatan tim diterapkan. Buka proyek di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk melihat bahwa tim, estimasi proyek, dan struktur rincian kerja telah dihasilkan. Tabel berikut menunjukkan lokasi untuk mencari hasil:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Diagram Gantt**   | Impor ke layar **struktur rincian kerja** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. |
| **Lembar sumber daya** [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] |   Impor ke layar **anggota tim proyek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].   |
|   **Menggunakan penggunaan** [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]    |    Impor ke layar **Estimasi Proyek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Untuk mengimpor dan mempublikasikan proyek Anda**  
1. Dari tab **Project service**, klik **Terbitkan** > **proyek Project Service Automation baru**.  

2. Pada kotak dialog **Terbitkan ke sebuah proyek baru dalam Project Service**, masukkan **nama proyek** dan pilih **pelanggan**.  

3. Bisa juga periksa **tautkan rencana proyek ke Project service automation** untuk menautkan file rencana proyek ke Project service automation.  

4. Klik **Terbitkan**.  

   Menghubungkan file proyek ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] membuat file proyek sebagai master dan menetapkan struktur rincian kerja dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadi baca-saja.  Untuk membuat perubahan rencana proyek, Anda harus membuat mereka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan mempublikasikan mereka sebagai pembaruan kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Mengedit sebuah proyek yang telah diimpor  
 Untuk membuat perubahan ke rencana proyek yang telah diimpor ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], Anda memiliki dua pilihan:  

- Buka master file dan edit di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Batalkan tautan file dan edit langsung di Project Service. Secara default, sebuah proyek yang telah di-upload dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] terkunci dan hanya bisa diedit dalam proyek. Untuk mengedit file dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], file tersebut harus tidak tertaut.  

### <a name="edit-in-pn_microsoft_project"></a>Edit di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Dari menu utama, klik **Project Service** > **Proyek**.  

2. Dari daftar proyek, buka satu yang dibuat di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klik **buka di MS Project** dari pita. Ini akan membuka master file yang tertaut di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Batalkan tautan file dan edit di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Dari menu utama, klik **Project Service** > **Proyek**.  

2. Dari daftar proyek, buka satu yang dibuat di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klik **hapus tautan dari MS Project** dari pita.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Mengunggah berkas proyek ke SharePoint atau Office Groups  
 Anda bisa mengupload file proyek ke SharePoint dan menemukannya di bawah dokumen yang terkait untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Anda.  Anda perlu meminta administrator Anda mengkonfigurasi manajemen dokumen SharePoint dan menyalakannya untuk entitas proyek. 

 Anda juga dapat mengunggah berkas proyek untuk [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jika Anda telah mengonfigurasikan Office Groups.

### <a name="upload-a-file-for-sharepoint"></a>Unggah file untuk SharePoint  

1. Dari menu utama, klik **Project Service** > **Unggah**.  

2. Pilih **Ke Dokumen Proyek Project service automation**.  

3. Pada dialog **Aktifkan buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, pilih **ya** atau **Tidak**.  

   - Jika Anda mengklik **ya** Anda akan dapat memilih tombol **buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** di Project Service Automation, meluncurkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuat file proyek dari perpustakaan dokumen SharePoint.  

   - Jika Anda mengklik **Tidak**, tautan **Buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan aktif.  

4. File [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dapat ditemukan di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **dokumen** untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] spesifik.  

### <a name="upload-a-file-for-office-groups"></a>Unggah file untuk Office Groups  

1. Dari menu utama, klik **Project Service** > **Unggah**.  

2. Pilih **Ke Dokumen Proyek Project service automation**.  

3. Pada dialog **Aktifkan buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, pilih **ya** atau **Tidak**.  

   - Jika Anda mengklik **ya** Anda akan dapat memilih tombol **buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** di Project Service Automation, meluncurkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuat file proyek dari perpustakaan dokumen SharePoint.  

   - Jika Anda mengklik **Tidak**, tautan **Buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan aktif.  

4. File [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dapat ditemukan di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **dokumen** untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] spesifik.  

## <a name="publish--your-project-as-a-template"></a>Mempublikasikan proyek Anda sebagai template  
 Anda dapat menyimpan proyek Anda dan menggunakannya kembali dengan menyimpannya sebagai template proyek di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Template proyek adalah rencana proyek yang dapat digunakan kembali di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Membuat template proyek (Project Service Automation)](../psa/create-project-template.md)  

1. Dari tab **Project service**, klik **Terbitkan** > **Template proyek Project service automation baru**.  

2. Di kotak dialog **Terbitkan ke sebuah proyek baru dalam template Project Service**, masukkan **nama template proyek**.  

3. Bisa juga periksa **tautkan rencana proyek ke Project service automation** untuk menautkan file proyek ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Klik **Terbitkan**.  

Menghubungkan file proyek ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] membuat file proyek sebagai master dan menetapkan struktur rincian kerja dalam template [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadi baca-saja.  Untuk membuat perubahan rencana proyek, Anda harus membuat mereka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan mempublikasikan mereka sebagai pembaruan kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Membaca jadwal sumber daya yang dimuat

Saat membaca proyek dari Project Service Automation, kalender sumber daya tidak disinkronisasikan ke klien desktop. Jika terdapat perbedaan dalam durasi tugas, upaya, atau pengakhiran, mungkin karena sumber daya dan klien desktop tidak memiliki kalender template jam kerja yang sama yang diterapkan pada proyek.


## <a name="data-synchronization"></a>Sinkronisasi Data

Tabel berikut menguraikan cara menyinkronkan data antara Project Service Automation dan add-in desktop Microsoft Project.

| **Entitas** | **Bidang** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Tugas Proyek | Tenggat Waktu | ● | - |
| Tugas Proyek | Perkiraan Upaya | ● | - |
| Tugas Proyek | ID Klien MS Project | ● | - |
| Tugas Proyek | Tugas Induk | ● | - |
| Tugas Proyek | Project | ● | - |
| Tugas Proyek | Tugas proyek | ● | - |
| Tugas Proyek | Nama Tugas Proyek | ● | - |
| Tugas Proyek | Unit sumber daya (Ditolak pada v3.0) | ● | - |
| Tugas Proyek | Durasi Terjadwal | ● | - |
| Tugas Proyek | Tanggal Mulai | ● | - |
| Tugas Proyek | ID WBS | ● | - |

| **Entitas** | **Bidang** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Anggota Tim | ID Klien MS Project | ● | - |
| Anggota Tim | Nama Posisi | ● | - |
| Anggota Tim | proyek | ● | ● |
| Anggota Tim | Tim Proyek | ● | ● |
| Anggota Tim | Unit Sumber Daya | - | ● |
| Anggota Tim | Peran | - | ● |
| Anggota Tim | Jam Kerja | Tidak disinkronkan | Tidak disinkronkan |

| **Entitas** | **Bidang** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Penetapan Sumber Daya | Tanggal Mulai | ● | - |
| Penetapan Sumber Daya | Jam | ● | - |
| Penetapan Sumber Daya | ID Klien MS Project | ● | - |
| Penetapan Sumber Daya | Pekerjaan Terencana | ● | - |
| Penetapan Sumber Daya | Project | ● | - |
| Penetapan Sumber Daya | Tim Proyek | ● | - |
| Penetapan Sumber Daya | Penetapan Sumber Daya | ● | - |
| Penetapan Sumber Daya | Tugas | ● | - |
| Penetapan Sumber Daya | Tanggal Selesai | ● | - |

| **Entitas** | **Bidang** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Dependensi Tugas Proyek | Dependensi Tugas Proyek | ● | - |
| Dependensi Tugas Proyek | Tipe Tautan | ● | - |
| Dependensi Tugas Proyek | Tugas Pendahulu | ● | - |
| Dependensi Tugas Proyek | Project | ● | - |
| Dependensi Tugas Proyek | Tugas Penerus | ● | - |

### <a name="see-also"></a>Lihat Juga  
 [Panduan Manajer Proyek](../psa/project-manager-guide.md)
