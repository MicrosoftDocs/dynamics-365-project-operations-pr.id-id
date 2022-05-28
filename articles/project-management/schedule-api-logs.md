---
title: Log penjadwalan proyek
description: Ini topik memberikan informasi dan sampel yang akan membantu Anda menggunakan log Penjadwalan Proyek untuk melacak kegagalan yang terkait dengan Layanan Penjadwalan Proyek dan API Penjadwalan Proyek.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589522"
---
# <a name="project-scheduling-logs"></a>Log penjadwalan proyek

_**Berlaku Untuk:** Operasi Proyek untuk skenario berbasis sumber daya/non-stok, penyebaran Lite - kesepakatan untuk faktur_ proforma, _Proyek untuk Web_

Microsoft Dynamics 365 Project Operations menggunakan [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) sebagai mesin penjadwalan utamanya. Alih-alih menggunakan antarmuka pemrograman aplikasi Web (API) standar Microsoft Dataverse, Operasi Proyek menggunakan API Penjadwalan Proyek baru untuk membuat, memperbarui, dan menghapus tugas proyek, tugas sumber daya, dependensi tugas, bucket proyek, dan anggota tim proyek. Namun, ketika operasi buat, perbarui, atau hapus dijalankan secara terprogram pada entitas struktur perincian kerja (WBS), kesalahan mungkin terjadi. Untuk melacak kesalahan ini dan riwayat operasi, dua log administratif baru telah diterapkan: **Operation Set** dan **Project Scheduling Service (PSS)**. Untuk mengakses log ini, buka **Pengaturan** \> **Jadwal Integrasi.**

Ilustrasi berikut menunjukkan model data untuk log Penjadwalan Proyek.

![Model data untuk log Penjadwalan Proyek.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Log Set Operasi

Log Set Operasi melacak eksekusi kumpulan operasi yang digunakan untuk menjalankan satu atau banyak membuat, memperbarui, atau menghapus operasi dalam batch pada proyek, tugas proyek, penetapan sumber daya, dependensi tugas, bucket proyek, atau anggota tim proyek. Bidang **Operasi dalam Status** menunjukkan status keseluruhan set operasi. Detail payload set operasi ditangkap dalam catatan Detail Set Operasi terkait.

### <a name="operation-set"></a>Set Operasi

Tabel berikut menunjukkan bidang yang terkait dengan **entitas Set** Operasi.

| SchemaName            | Deskripsi                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Tanggal/waktu ketika set operasi selesai atau gagal.                                                | CompletedOn            |
| msdyn_correlationid   | Nilai **correlationId** dari permintaan.                                                                  | CorrelationId          |
| msdyn_description     | Deskripsi set operasi.                                                                        | Deskripsi            |
| msdyn_executedon      | Tanggal/waktu saat rekaman dijalankan.                                                                       | Dijalankan Pada            |
| msdyn_operationsetId  | Pengidentifikasi unik instans entitas.                                                                   | OperationSet           |
| msdyn_Project         | Proyek yang terkait dengan set operasi.                                                            | Project                |
| msdyn_projectid       | Nilai **projectId** dari permintaan.                                                                      | ProjectId (Tidak Digunakan Lagi) |
| msdyn_projectName     | Tidak berlaku.                                                                                              | Tidak berlaku         |
| msdyn_PSSErrorLog     | Pengidentifikasi unik dari log kesalahan Layanan Penjadwalan Proyek yang terkait dengan kumpulan operasi. | Log Kesalahan PSS          |
| msdyn_PSSErrorLogName | Tidak berlaku.                                                                                              | Tidak berlaku         |
| msdyn_status          | Status operasi yang ditetapkan.                                                                             | Status                 |
| msdyn_statusName      | Tidak berlaku.                                                                                              | Tidak berlaku         |
| msdyn_useraadid       | Azure Active Directory(Azure AD) ID objek pengguna tempat permintaan tersebut berada.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detail Set Operasi

Tabel berikut menunjukkan bidang yang terkait dengan **entitas Detail** Set Operasi.

| SchemaName                 | Deskripsi                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Bidang serial untuk Dataverse permintaan.                                            | CdsPayload            |
| msdyn_entityname           | Nama entitas untuk permintaan tersebut.                                                     | EntityName            |
| msdyn_httpverb             | Metode permintaan.                                                                         | Kata Kerja HTTP (Tidak digunakan lagi) |
| msdyn_httpverbName         | Tidak berlaku.                                                                             | Tidak berlaku        |
| msdyn_operationset         | Pengidentifikasi unik dari set operasi tempat catatan itu berada.                      | OperationSet          |
| msdyn_operationsetdetailId | Pengidentifikasi unik instans entitas.                                                  | Rincian OperationSet   |
| msdyn_operationsetName     | Tidak berlaku.                                                                             | Tidak berlaku        |
| msdyn_operationtype        | Jenis operasi operasi mengatur detail.                                             | OperationType         |
| msdyn_operationtypeName    | Tidak berlaku.                                                                             | Tidak berlaku        |
| msdyn_psspayload           | Bidang Layanan Penjadwalan Proyek serial untuk permintaan tersebut.                           | PssPayload            |
| msdyn_recordid             | Pengidentifikasi catatan permintaan.                                                       | ID Rekaman             |
| msdyn_requestnumber        | Nomor yang dibuat secara otomatis yang mengidentifikasi urutan permintaan diterima. | Nomor Permintaan        |

## <a name="project-scheduling-service-error-logs"></a>Log kesalahan Layanan Penjadwalan Proyek

Log kesalahan Layanan Penjadwalan Proyek menangkap kegagalan yang terjadi saat Layanan Penjadwalan Proyek mencoba **operasi Simpan** atau **Buka**. Ada tiga skenario yang didukung di mana log ini dihasilkan:

- Tindakan yang dimulai pengguna gagal secara kritis (misalnya, tugas tidak dapat dibuat karena hak istimewa yang hilang).
- Layanan Penjadwalan Proyek tidak dapat secara terprogram membuat, memperbarui, menghapus, atau melakukan operasi cascading lainnya pada entitas.
- Pengguna mengalami kesalahan saat rekaman gagal dibuka (misalnya, saat proyek dibuka atau informasi anggota tim diperbarui).

### <a name="project-scheduling-service-log"></a>Log Layanan Penjadwalan Proyek

Tabel berikut menunjukkan bidang yang disertakan dalam log Layanan Penjadwalan Proyek.

| SchemaName          | Deskripsi                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Tumpukan panggilan pengecualian.                                               | Tumpukan Panggilan     |
| msdyn_correlationid | ID korelasi kesalahan.                                               | CorrelationId  |
| msdyn_errorcode     | Bidang yang digunakan untuk menyimpan Dataverse kode kesalahan atau kode kesalahan HTTP. | Kode Kesalahan     |
| msdyn_HelpLink      | Tautan ke dokumentasi Bantuan publik.                                       | Tautan Bantuan      |
| msdyn_log           | Log dari Layanan Penjadwalan Proyek.                                   | Log            |
| msdyn_project       | Proyek yang terkait dengan log kesalahan.                             | Project        |
| msdyn_projectName   | Nama proyek jika muatan set operasi akan dipertahankan. | Tidak berlaku |
| msdyn_psserrorlogId | Pengidentifikasi unik instans entitas.                                     | Log Kesalahan PSS  |
| msdyn_SessionId     | ID sesi proyek.                                                        | ID Sesi     |

## <a name="error-log-cleanup"></a>Pembersihan log kesalahan

Secara default, log kesalahan Layanan Penjadwalan Proyek dan log Set Operasi dapat dibersihkan setiap 90 hari. Setiap rekaman yang lebih tua dari 90 hari akan dihapus. Namun, dengan mengubah nilai **bidang msdyn_StateOperationSetAge** pada **halaman Parameter** Proyek, administrator dapat menyesuaikan rentang pembersihan sehingga antara 1 dan 120 hari. Beberapa metode untuk mengubah nilai ini tersedia:

- **Sesuaikan entitas Parameter** Proyek dengan membuat halaman kustom dan menambahkan **bidang Stale Operations Set Age**.
- Gunakan kode klien yang menggunakan [kit pengembangan perangkat lunak WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Gunakan kode SDK Layanan yang menggunakan metode Xrm SDK **updateRecord** (referensi API Klien) di aplikasi berdasarkan model. Power Apps menyertakan deskripsi dan parameter yang didukung untuk **metode updateRecord**.

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
