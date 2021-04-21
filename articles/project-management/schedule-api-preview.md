---
title: Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan
description: Pembaruan topik memberikan informasi dan sampel untuk menggunakan API Jadwal.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868133"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

> [!IMPORTANT] 
> Beberapa atau semua fungsi yang tercantum dalam topik ini tersedia sebagai bagian dari rilis pratinjau. Konten dan fungsi ini dapat berubah. 

## <a name="scheduling-entities"></a>Entitas Penjadwalan

API jadwal memberikan kemampuan untuk melakukan operasi pembuatan, pembaruan, dan penghapusan dengan **entitas Penjadwalan**. Entitas ini dikelola melalui mesin Penjadwalan di Project for the Web. Membuat, memperbarui, dan menghapus operasi dengan **entitas Penjadwalan** dibatasi di rilis Dynamics 365 Project Operations sebelumnya.

Tabel berikut menyediakan daftar lengkap **entitas Penjadwalan**.

| Nama entitas  | Nama logika entitas |
| --- | --- |
| Project | msdyn_project |
| Tugas Proyek  | msdyn_projecttask  |
| Dependensi Tugas Proyek  | msdyn_projecttaskdependency  |
| Penetapan Sumber Daya | msdyn_resourceassignment |
| Wadah Proyek  | msdyn_projectbucket |
| Anggota Tim Proyek | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet adalah pola unit kerja yang dapat digunakan ketika beberapa jadwal yang mempengaruhi permintaan harus diproses dalam transaksi.

## <a name="schedule-apis"></a>API Jadwal

Berikut adalah daftar API Jadwal saat ini.

- **msdyn_CreateProjectV1**: API ini dapat digunakan untuk membuat proyek. Proyek dan wadah proyek default dibuat dengan segera.
- **msdyn_CreateTeamMemberV1**: API ini dapat digunakan untuk membuat anggota tim proyek. Rekaman anggota tim akan segera dibuat.
- **msdyn_CreateOperationSetV1**: API ini dapat digunakan untuk menjadwalkan beberapa permintaan yang harus dilakukan dalam transaksi.
- **msdyn_PSSCreateV1**: API ini dapat digunakan untuk membuat entitas. Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi pembuatan.
- **msdyn_PSSUpdateV1**: API ini dapat digunakan untuk memperbarui entitas. Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi pembaruan.
- **msdyn_PSSDeleteV1**: API ini dapat digunakan untuk menghapus entitas. Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi penghapusan.
- **msdyn_ExecuteOperationSetV1**: API ini digunakan untuk mengeksekusi semua operasi dalam rangkaian operasi yang ditentukan.

## <a name="using-schedule-apis-with-operationset"></a>Menggunakan API Jadwal dengan OperationSet

Karena rekaman dengan **CreateProjectV1** dan **CreateTeamMemberV1** dibuat dengan segera, API ini tidak dapat digunakan di **OperationSet** secara langsung. Namun, Anda dapat menggunakan API untuk membuat rekaman yang diperlukan, membuat **OperationSet**, dan kemudian menggunakan rekaman yang dibuat sebelumnya di **OperationSet**.

## <a name="supported-operations"></a>Operasi yang Didukung

| Entitas Penjadwalan | Buat | Pembaruan | Delete | Pertimbangan penting |
| --- | --- | --- | --- | --- |
Tugas proyek | Ya | Ya | Ya | Tidak Ada |
| Dependensi Tugas Proyek | Ya | Ya | | Rekaman dependensi tugas proyek tidak diperbarui. Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat. |
| Penetapan Sumber Daya | Ya | Ya | | Operasi dengan bidang berikut tidak didukung: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, dan **PlannedWork**. Rekaman penetapan sumber daya tidak diperbarui. Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat. |
| Wadah Proyek | Tidak Tersedia | Tidak Tersedia | Tidak Tersedia | Seeer default dibuat menggunakan API **CREATEKainyV1**. |
| Anggota Tim Proyek | Ya | Ya | Ya | Untuk operasi pembuatan, gunakan API **CreateTeamMemberV1**. |
| Project | Ya | Ya | Tidak Tersedia | Operasi dengan bidang berikut tidak didukung: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, dan **Duration**. |

API ini dapat dipanggil dengan objek entitas yang mencakup bidang kustom.

Properti ID bersifat opsional. Jika diberikan, sistem mencoba menggunakannya dan memberikan pengecualian jika tidak dapat digunakan. Jika tidak disediakan, sistem akan membuatnya.

## <a name="limitations-and-known-issues"></a>Masalah dan batasan yang diketahui
Berikut adalah daftar batasan dan masalah umum:

- API jadwal hanya dapat digunakan oleh **Pengguna dengan Lisensi Microsoft Project.** Tidak dapat digunakan oleh:
    - Pengguna Aplikasi
    - Pengguna Sistem
    - Pengguna Integrasi
    - Pengguna lain yang tidak memiliki lisensi yang diperlukan
- Setiap **OperationSet** hanya dapat memiliki maksimum 100 operasi.
- Setiap pengguna hanya dapat membuka maksimum 10 **OperationSet** terbuka.
- Project Operations saat ini mendukung maksimum 500 tugas total pada proyek.
- Status kegagalan dan log kegagalan **OperationSet** saat ini tidak tersedia.
- API Jadwal ada dalam pratinjau umum. Menggunakan API ini di lingkungan Produksi tidak didukung oleh Microsoft.

## <a name="sample-scenario"></a>Contoh Skenario

Dalam skenario ini, Anda akan membuat proyek, anggota tim, empat tugas, dan dua penugasan sumber daya. Selanjutnya, Anda akan memperbarui satu tugas, memperbarui proyek, menghapus satu tugas, menghapus satu penetapan sumber daya, dan membuat dependensi tugas.

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Contoh tambahan

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
