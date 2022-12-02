---
title: Log penjadwalan proyek
description: Artikel ini menyediakan informasi dan sampel yang akan membantu Anda menggunakan log Penjadwalan Proyek untuk melacak kegagalan yang terkait dengan Layanan Penjadwalan Proyek dan API Penjadwalan Proyek.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923699"
---
# <a name="project-scheduling-logs"></a>Log penjadwalan proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-persediaan, penyebaran Lite - faktur penawaran hingga proforma_, _Project for the Web_

Microsoft Dynamics 365 Project Operations menggunakan [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) sebagai mesin penjadwalan utamanya. Alih-alih menggunakan API (antarmuka penerapan Web standar) Microsoft Dataverse, Project Operations menggunakan API Penjadwalan Proyek baru untuk membuat, memperbarui, dan menghapus tugas proyek, penugasan sumber daya, dependensi tugas, kelompok proyek, dan anggota tim proyek. Namun, saat operasi membuat, memperbarui, atau menghapus dijalankan secara programmatis pada entitas WBS (struktur perincian kerja), kesalahan dapat terjadi. Untuk melacak kesalahan ini dan riwayat operasi, dua log administratif baru telah diimplementasikan: **Rangkaian Operasi** dan **Layanan Penjadwalan Proyek (PSS)**. Untuk mengakses log ini, buka **Pengaturan** \> **Integrasi Jadwal**.

Ilustrasi berikut menampilkan model data untuk log penjadwalan proyek.

![Model data untuk log penjadwalan proyek.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Log rangkaian operasi

Log Rangkaian Operasi melacak eksekusi rangkaian operasi yang digunakan untuk menjalankan satu atau beberapa operasi pembuatan, pembaruan, atau penghapusan dalam Batch pada proyek, tugas proyek, penugasan sumber daya, dependensi tugas, kelompok proyek, atau anggota tim proyek. Bidang **Operasi dalam Status** menunjukkan status keseluruhan rangkaian operasi. Rincian muatan rangkaian operasi tertangkap di rekaman detail rangkaian operasi terkait.

### <a name="operation-set"></a>Rangkaian operasi

Tabel berikut Menampilkan bidang yang terkait dengan entitas **Rangkaian Operasi**.

| Nama Skema            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Tanggal/waktu ketika rangkaian operasi selesai atau gagal.                                                | CompletedOn            |
| msdyn_correlationid   | Nilai **correlationId** permintaan.                                                                  | CorrelationId          |
| msdyn_description     | Deskripsi rangkaian operasi.                                                                        | Description            |
| msdyn_executedon      | Tanggal/waktu saat rekaman dijalankan.                                                                       | Dijalankan Pada            |
| msdyn_operationsetId  | Pengidentifikasi unik instans entitas.                                                                   | OperationSet           |
| msdyn_Project         | Proyek yang terkait dengan rangkaian operasi.                                                            | Project                |
| msdyn_projectid       | Nilai **projectId** permintaan.                                                                      | ProjectId (Tidak Digunakan Lagi) |
| msdyn_projectName     | Tidak berlaku.                                                                                              | Tidak berlaku         |
| msdyn_PSSErrorLog     | Pengidentifikasi unik log kesalahan Layanan Penjadwalan Proyek yang terkait dengan rangkaian operasi. | Log Kesalahan PSS          |
| msdyn_PSSErrorLogName | Tidak berlaku.                                                                                              | Tidak berlaku         |
| msdyn_status          | Status rangkaian operasi.                                                                             | Status                 |
| msdyn_statusName      | Tidak berlaku.                                                                                              | Tidak berlaku         |
| msdyn_useraadid       | ID Objek Azure Active Directory (Azure AD) dari Pengguna yang memiliki permintaan ini.                     | UserAADID              |

### <a name="operation-set-detail"></a>Rincian Rangkaian Operasi

Tabel berikut Menampilkan bidang yang terkait dengan entitas **Rincian Rangkaian Operasi**.

| Nama Skema                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Bidang berseri Dataverse untuk permintaan.                                            | CdsPayload            |
| msdyn_entityname           | Nama entitas untuk permintaan.                                                     | EntityName            |
| msdyn_httpverb             | Metode permintaan.                                                                         | Kata Kerja HTTP (Tidak digunakan lagi) |
| msdyn_httpverbName         | Tidak berlaku.                                                                             | Tidak berlaku        |
| msdyn_operationset         | Pengidentifikasi unik untuk rangkaian operasi yang memiliki rekaman ini.                      | OperationSet          |
| msdyn_operationsetdetailId | Pengidentifikasi unik instans entitas.                                                  | Rincian OperationSet   |
| msdyn_operationsetName     | Tidak berlaku.                                                                             | Tidak berlaku        |
| msdyn_operationtype        | Jenis operasi rincian rangkaian operasi.                                             | OperationType         |
| msdyn_operationtypeName    | Tidak berlaku.                                                                             | Tidak berlaku        |
| msdyn_psspayload           | Bidang Penjadwalan Proyek berseri untuk permintaan.                           | PssPayload            |
| msdyn_recordid             | Pengidentifikasi rekaman permintaan.                                                       | ID Rekaman             |
| msdyn_requestnumber        | Nomor yang dibuat secara otomatis yang mengidentifikasi pesanan yang mana permintaan diterima di dalamnya. | Nomor Permintaan        |

## <a name="project-scheduling-service-error-logs"></a>Log kesalahan Layanan Penjadwalan proyek

Log kesalahan Layanan Penjadwalan Proyek mencatat kegagalan yang terjadi saat Layanan Penjadwalan Proyek mencoba operasi **Simpan** atau **Buka**. Ada tiga skenario yang didukung di mana log ini dibuat:

- Tindakan yang diawali pengguna sangat gagal (misalnya, penugasan tidak dapat dibuat karena hak istimewa tidak ada).
- Layanan Penjadwalan Proyek tidak dapat secara programatis membuat, memperbarui, menghapus, atau melakukan operasi berantai lainnya pada entitas.
- Kesalahan pengalaman pengguna saat rekaman gagal terbuka (contohnya, ketika proyek dibuka atau informasi anggota tim diperbarui).

### <a name="project-scheduling-service-log"></a>Log Layanan Penjadwalan proyek

Tabel berikut Menampilkan bidang yang tercakup dalam log Layanan penjadwalan Proyek.

| Nama Skema          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Tumpukan panggilan pengecualian.                                               | Tumpukan Panggilan     |
| msdyn_correlationid | ID korelasi kesalahan.                                               | CorrelationId  |
| msdyn_errorcode     | Bidang yang digunakan untuk menyimpan kode kesalahan Dataverse atau kode kesalahan HTTP. | Kode Kesalahan     |
| msdyn_HelpLink      | Tautan ke dokumentasi bantuan publik.                                       | Tautan Bantuan      |
| msdyn_log           | Log dari Layanan Penjadwalan Proyek.                                   | Log            |
| msdyn_project       | Proyek yang terkait dengan log kesalahan.                             | Project        |
| msdyn_projectName   | Nama proyek jika muatan dari rangkaian operasi akan terus ada. | Tidak berlaku |
| msdyn_psserrorlogId | Pengidentifikasi unik instans entitas.                                     | Log Kesalahan PSS  |
| msdyn_SessionId     | ID sesi proyek.                                                        | ID Sesi     |

## <a name="error-log-cleanup"></a>Pembersihan Log Kesalahan

Secara default, log kesalahan Layanan Penjadwalan Proyek dan log Rangkaian Operasi dapat dibersihkan setiap 90 hari. Segala rekaman yang lebih tua dari 90 hari akan dihapus. Namun, dengan mengubah nilai bidang **msdyn_StateOperationSetAge** pada halaman **Parameter Proyek**, administrator dapat menyesuaikan rentang pembersihan sehingga rentangnya antara 1 hingga 120 hari. Tersedia beberapa metode untuk mengubah nilai ini:

- Sesuaikan entitas **Parameter Proyek** dengan membuat halaman kustom dan menambahkan **bidang Rangkaian Operasi Basi**.
- Gunakan kode klien yang menggunakan [SDK (kit pengembangan perangkat lunak) WebApi](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Gunakan kode SDK Layanan yang menggunakan metode **updateRecord** Xrm SDK (referensi Client API) di aplikasi berdasarkan model. Power Apps mencakup deskripsi dan parameter yang didukung untuk metode **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
