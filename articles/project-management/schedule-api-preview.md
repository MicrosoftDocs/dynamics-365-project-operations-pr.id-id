---
title: Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan
description: Artikel ini memberikan informasi dan sampel untuk menggunakan API jadwal Proyek.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541128"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


**Entitas Penjadwalan**

API jadwal proyek memberikan kemampuan untuk melakukan operasi pembuatan, pembaruan, dan penghapusan dengan **entitas Penjadwalan**. Entitas ini dikelola melalui mesin Penjadwalan di Project for the Web. Membuat, memperbarui, dan menghapus operasi dengan **entitas Penjadwalan** dibatasi di rilis Dynamics 365 Project Operations sebelumnya.

Tabel berikut menyediakan daftar lengkap entitas jadwal Proyek.

| **Nama entitas**         | **Nama logika entitas**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tugas Proyek            | msdyn_projecttask           |
| Dependensi Tugas Proyek | msdyn_projecttaskdependency |
| Penetapan Sumber Daya     | msdyn_resourceassignment    |
| Wadah Proyek          | msdyn_projectbucket         |
| Anggota Tim Proyek     | msdyn_projectteam           |
| Daftar Periksa Proyek      | msdyn_projectchecklist      |
| Label Proyek           | msdyn_projectlabel          |
| Tugas Proyek yang akan Dilabeli   | msdyn_projecttasktolabel    |
| Sprint Proyek          | msdyn_projectsprint         |

**OperationSet**

OperationSet adalah pola unit kerja yang dapat digunakan ketika beberapa jadwal yang mempengaruhi permintaan harus diproses dalam transaksi.

**API Jadwal proyek**

Berikut adalah daftar API jadwal Proyek saat ini.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | API ini digunakan untuk membuat proyek. Proyek dan wadah proyek default segera dibuat.                         |
| **msdyn_CreateTeamMemberV1**            | API ini digunakan untuk membuat anggota tim proyek. Rekaman anggota tim akan segera dibuat.                                  |
| **msdyn_CreateOperationSetV1**          | API ini digunakan untuk menjadwalkan beberapa permintaan yang harus dilakukan dalam transaksi.                                        |
| **msdyn_PssCreateV1**                   | API ini digunakan untuk membuat entitas. Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi pembuatan. |
| **msdyn_PssUpdateV1**                   | API ini digunakan untuk memperbarui entitas. Entitas dapat berupa entitas penjadwalan Proyek apa pun yang mendukung operasi pembaruan  |
| **msdyn_PssDeleteV1**                   | API ini digunakan untuk menghapus entitas. Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi penghapusan. |
| **msdyn_ExecuteOperationSetV1**         | API ini digunakan untuk mengeksekusi semua operasi dalam rangkaian operasi yang ditentukan.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | API ini digunakan untuk memperbarui kontur kerja terencana Penugasan Sumber Daya.                                                        |



**Menggunakan API jadwal proyek dengan OperationSet**

Karena rekaman dengan **CreateProjectV1** dan **CreateTeamMemberV1** dibuat dengan segera, API ini tidak dapat digunakan di **OperationSet** secara langsung. Namun, Anda dapat menggunakan API untuk membuat rekaman yang diperlukan, membuat **OperationSet**, dan kemudian menggunakan rekaman yang dibuat sebelumnya di **OperationSet**.

**Operasi yang Didukung**

| **Entitas Penjadwalan**   | **Buat** | **Pembaruan** | **Delete** | **Pertimbangan penting**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tugas proyek            | Ya        | Ya        | Ya        | Bidang **Progres**, **EffortCompleted**, dan **EffortRemaining** dapat diedit di Project for the Web, namun tidak dapat diedit dalam Project Operations.                                                                                                                                                                                             |
| Dependensi Tugas Proyek | Ya        | No         | Ya        | Rekaman dependensi tugas proyek tidak diperbarui. Sebagai gantinya, rekaman lama dapat dihapus, dan rekaman baru dapat dibuat.                                                                                                                                                                                                                                 |
| Penetapan Sumber Daya     | Ya        | Ya\*      | Ya        | Operasi dengan bidang berikut tidak didukung: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, dan **PlannedWork**. Rekaman penetapan sumber daya tidak diperbarui. Sebagai gantinya, rekaman lama dapat dihapus, dan rekaman baru dapat dibuat. API terpisah telah diberikan untuk memperbarui kontur Penugasan Sumber Daya. |
| Wadah Proyek          | Ya        | Ya        | Ya        | Wadah default dibuat dengan menggunakan API **CREATEKainyV1**. Dukungan untuk membuat dan menghapus wadah proyek telah ditambahkan dalam Pembaruan Release 16.                                                                                                                                                                                                   |
| Anggota Tim Proyek     | Ya        | Ya        | Ya        | Untuk operasi pembuatan, gunakan API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Ya        | Ya        |            | Operasi dengan bidang berikut tidak didukung: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, dan **Duration**.                                                                                       |
| Daftar Periksa Proyek      | Ya        | Ya        | Ya        |                                                                                                                                                                                                                                                                                                                                                         |
| Label Proyek           | No         | Ya        | No         | Nama label dapat diubah. Fitur ini tersedia hanya tersedia untuk Project for the Web                                                                                                                                                                                                                                                                      |
| Tugas Proyek yang akan Dilabeli   | Ya        | No         | Ya        | Fitur ini tersedia hanya tersedia untuk Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint Proyek          | Ya        | Ya        | Ya        | Bidang **Mulai** harus memiliki tanggal lebih awal dari bidang **Selesai**. Sprint untuk proyek yang sama tidak boleh tumpang tindih satu sama lain. Fitur ini tersedia hanya tersedia untuk Project for the Web                                                                                                                                                                    |




Properti ID bersifat opsional. Jika diberikan, sistem mencoba menggunakannya dan memberikan pengecualian jika tidak dapat digunakan. Jika tidak disediakan, sistem akan membuatnya.

**Masalah dan batasan yang diketahui**

Berikut adalah daftar batasan dan masalah umum:

-   API Jadwal Proyek hanya dapat digunakan oleh **Pengguna dengan Lisensi Microsoft Project**. Tidak dapat digunakan oleh:
    -   Pengguna Aplikasi
    -   Pengguna Sistem
    -   Pengguna Integrasi
    -   Pengguna lain yang tidak memiliki lisensi yang diperlukan
-   Setiap **OperationSet** hanya dapat memiliki maksimum 100 operasi.
-   Setiap pengguna hanya dapat membuka maksimum 10 **OperationSet** terbuka.
-   Project Operations saat ini mendukung maksimum 500 tugas total pada proyek.
-   Setiap operasi Memperbarui Kontur Penugasan Sumber Daya dihitung sebagai satu operasi.
-   Setiap daftar kontur yang diperbarui dapat berisi maksimum 100 potongan waktu.
-   Status kegagalan dan log kegagalan **OperationSet** saat ini tidak tersedia.
-   Tersedia maksimum 400 sprint per proyek.
-   [Batas dan batasan pada proyek dan tugas](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Fitur ini sekarang hanya tersedia untuk Project for the Web

**Penanganan kesalahan**

-   Untuk memeriksa kesalahan yang dihasilkan dari Rangkaian Operasi, buka **Pengaturan** \> **Integrasi Jadwal** \> **Rangkaian Operasi**.
-   Untuk memeriksa kesalahan yang dihasilkan dari Layanan Jadwal Proyek, buka **pengaturan** \> **integrasi Jadwal** \> **Log Kesalahan PSS**.

**Mengedit Kontur Penugasan Sumber Daya**

Tidak seperti semua API penjadwalan proyek lainnya yang memperbarui entitas, API konstur penugasan sumber daya bertanggung jawab penuh untuk pembaruan ke satu bidang, msdyn_plannedwork, pada satu entitas, msydn_resourceassignment.

Mode jadwal yang ditentukan adalah:

-   **unit tetap**
-   kalender proyek 9-5p adalah 9-5pst, Senin, Selasa, Kamis, Jumat (RABU LIBUR)
-   dan kalender sumber daya 9-1p PST Senin hingga Jumat

Penugasan ini adalah untuk satu minggu, empat jam sehari. Hal ini karena kalender sumber daya dari 9-1 PST, atau empat jam sehari.

| &nbsp;     | Tugas | Tanggal Mulai | Tanggal Akhir  | Jumlah | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Pekerja 9-1 |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Misalnya, jika Anda ingin agar pekerja hanya bekerja tiga jam setiap hari di minggu ini dan memungkinkan selama satu jam untuk tugas lainnya.

#### <a name="updatedcontours-sample-payload"></a>Payload sampel UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Ini adalah penugasan setelah API Jadwal Kontur Pembaruan dijalankan.

| &nbsp;     | Tugas | Tanggal Mulai | Tanggal Akhir  | Jumlah | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Pekerja 9-1 | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Contoh Skenario**

Dalam skenario ini, Anda akan membuat proyek, anggota tim, empat tugas, dan dua penugasan sumber daya. Selanjutnya, Anda akan memperbarui satu tugas, memperbarui proyek, menghapus satu tugas, menghapus satu penetapan sumber daya, dan membuat dependensi tugas.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

** Sampel tambahan

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
   
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
