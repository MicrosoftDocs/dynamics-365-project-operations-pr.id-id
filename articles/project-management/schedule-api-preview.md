---
title: Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan
description: Artikel ini menyediakan informasi dan sampel untuk menggunakan API jadwal Proyek.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3248a057b831d81fdc2bc198b4ed4da5e46462f2
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230319"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_



## <a name="scheduling-entities"></a>Entitas Penjadwalan

API jadwal proyek memberikan kemampuan untuk melakukan operasi pembuatan, pembaruan, dan penghapusan dengan **entitas Penjadwalan**. Entitas ini dikelola melalui mesin Penjadwalan di Project for the Web. Membuat, memperbarui, dan menghapus operasi dengan **entitas Penjadwalan** dibatasi di rilis Dynamics 365 Project Operations sebelumnya.

Tabel berikut menyediakan daftar lengkap entitas jadwal Proyek.

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

## <a name="project-schedule-apis"></a>API Jadwal proyek

Berikut adalah daftar API jadwal Proyek saat ini.

- **msdyn_CreateProjectV1**: API ini dapat digunakan untuk membuat proyek. Bucket proyek dan proyek default segera dibuat.
- **msdyn_CreateTeamMemberV1**: API ini dapat digunakan untuk membuat anggota tim proyek. Rekaman anggota tim akan segera dibuat.
- **msdyn_CreateOperationSetV1**: API ini dapat digunakan untuk menjadwalkan beberapa permintaan yang harus dilakukan dalam transaksi.
- **msdyn_PssCreateV1**: API ini dapat digunakan untuk membuat entitas. Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi pembuatan.
- **msdyn_PssUpdateV1**: API ini dapat digunakan untuk memperbarui entitas. Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi pembaruan.
- **msdyn_PssDeleteV1**: API ini dapat digunakan untuk menghapus entitas. Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi penghapusan.
- **msdyn_ExecuteOperationSetV1**: API ini digunakan untuk mengeksekusi semua operasi dalam rangkaian operasi yang ditentukan.

## <a name="using-project-schedule-apis-with-operationset"></a>Menggunakan API jadwal proyek dengan OperationSet

Karena rekaman dengan **CreateProjectV1** dan **CreateTeamMemberV1** dibuat dengan segera, API ini tidak dapat digunakan di **OperationSet** secara langsung. Namun, Anda dapat menggunakan API untuk membuat rekaman yang diperlukan, membuat **OperationSet**, dan kemudian menggunakan rekaman yang dibuat sebelumnya di **OperationSet**.

## <a name="supported-operations"></a>Operasi yang Didukung

| Entitas Penjadwalan | Buat | Update | Delete | Pertimbangan penting |
| --- | --- | --- | --- | --- |
Tugas proyek | Ya | Ya | Ya | Bidang **Progress**, **EffortCompleted**, dan **EffortRemaining** dapat diedit di Project for the Web, tetapi tidak dapat diedit di Project Operations.  |
| Dependensi Tugas Proyek | Ya |  | Ya | Rekaman dependensi tugas proyek tidak diperbarui. Sebagai gantinya, catatan lama dapat dihapus, dan catatan baru dapat dibuat. |
| Penetapan Sumber Daya | Ya | Ya | | Operasi dengan bidang berikut tidak didukung: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, dan **PlannedWork**. Rekaman penetapan sumber daya tidak diperbarui. Sebagai gantinya, catatan lama dapat dihapus, dan catatan baru dapat dibuat. |
| Wadah Proyek | Ya | Ya | Ya | Bucket default dibuat dengan **menggunakan API CreateProjectV1**. Dukungan untuk membuat dan menghapus bucket proyek ditambahkan di Rilis Pembaruan 16. |
| Anggota Tim Proyek | Ya | Ya | Ya | Untuk operasi pembuatan, gunakan API **CreateTeamMemberV1**. |
| Project | Ya | Ya |  | Operasi dengan bidang berikut tidak didukung: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, dan **Duration**. |

API ini dapat dipanggil dengan objek entitas yang mencakup bidang kustom.

Properti ID bersifat opsional. Jika diberikan, sistem mencoba menggunakannya dan memberikan pengecualian jika tidak dapat digunakan. Jika tidak disediakan, sistem akan membuatnya.

## <a name="restricted-fields"></a>Bidang dibatasi

Tabel berikut ini menentukan bidang yang dibatasi dari **Buat** dan **Edit**.

### <a name="project-task"></a>Tugas proyek

| Nama logika                           | Dapat membuat     | Dapat mengedit         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | No             | No               |
| msdyn_actualcost_base                  | No             | No               |
| msdyn_actualend                        | No             | No               |
| msdyn_actualsales                      | No             | No               |
| msdyn_actualsales_base                 | No             | No               |
| msdyn_actualstart                      | No             | No               |
| msdyn_costatcompleteestimate           | No             | No               |
| msdyn_costatcompleteestimate_base      | No             | No               |
| msdyn_costconsumptionpercentage        | No             | No               |
| msdyn_effortcompleted                  | Tidak (ya untuk Proyek)             | Tidak (ya untuk Proyek)               |
| msdyn_effortremaining                  | Tidak (ya untuk Proyek)              | Tidak (ya untuk Proyek)                |
| msdyn_effortestimateatcomplete         | No             | No               |
| msdyn_iscritical                       | No             | No               |
| msdyn_iscriticalname                   | No             | No               |
| msdyn_ismanual                         | No             | No               |
| msdyn_ismanualname                     | No             | No               |
| msdyn_ismilestone                      | No             | No               |
| msdyn_ismilestonename                  | No             | No               |
| msdyn_LinkStatus                       | No             | No               |
| msdyn_linkstatusname                   | No             | No               |
| msdyn_msprojectclientid                | No             | No               |
| msdyn_plannedcost                      | No             | No               |
| msdyn_plannedcost_base                 | No             | No               |
| msdyn_plannedsales                     | No             | No               |
| msdyn_plannedsales_base                | No             | No               |
| msdyn_pluginprocessingdata             | No             | No               |
| msdyn_progress                         | Tidak (ya untuk Proyek)             | Tidak (ya untuk Proyek) |
| msdyn_remainingcost                    | No             | No               |
| msdyn_remainingcost_base               | No             | No               |
| msdyn_remainingsales                   | No             | No               |
| msdyn_remainingsales_base              | No             | No               |
| msdyn_requestedhours                   | No             | No               |
| msdyn_resourcecategory                 | No             | No               |
| msdyn_resourcecategoryname             | No             | No               |
| msdyn_resourceorganizationalunitid     | No             | No               |
| msdyn_resourceorganizationalunitidname | No             | No               |
| msdyn_salesconsumptionpercentage       | No             | No               |
| msdyn_salesestimateatcomplete          | No             | No               |
| msdyn_salesestimateatcomplete_base     | No             | No               |
| msdyn_salesvariance                    | No             | No               |
| msdyn_salesvariance_base               | No             | No               |
| msdyn_scheduleddurationminutes         | No             | No               |
| msdyn_scheduledend                     | No             | No               |
| msdyn_scheduledstart                   | No             | No               |
| msdyn_schedulevariance                 | No             | No               |
| msdyn_skipupdateestimateline           | No             | No               |
| msdyn_skipupdateestimatelinename       | No             | No               |
| msdyn_summary                          | No             | No               |
| msdyn_varianceofcost                   | No             | No               |
| msdyn_varianceofcost_base              | No             | No               |

### <a name="project-task-dependency"></a>Dependensi Tugas Proyek

| Nama logika                  | Dapat membuat     | Dapat mengedit     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | No             | No           |
| msdyn_linktypename            | No             | No           |
| msdyn_predecessortask         | Ya            | No           |
| msdyn_predecessortaskname     | Ya            | No           |
| msdyn_project                 | Ya            | No           |
| msdyn_projectname             | Ya            | No           |
| msdyn_projecttaskdependencyid | Ya            | No           |
| msdyn_successortask           | Ya            | No           |
| msdyn_successortaskname       | Ya            | No           |

### <a name="resource-assignment"></a>Penetapan Sumber Daya

| Nama logika                 | Dapat membuat     | Dapat mengedit     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Ya            | No           |
| msdyn_bookableresourceidname | Ya            | No           |
| msdyn_bookingstatusid        | No             | No           |
| msdyn_bookingstatusidname    | No             | No           |
| msdyn_committype             | No             | No           |
| msdyn_committypename         | No             | No           |
| msdyn_effort                 | No             | No           |
| msdyn_effortcompleted        | No             | No           |
| msdyn_effortremaining        | No             | No           |
| msdyn_finish                 | No             | No           |
| msdyn_plannedcost            | No             | No           |
| msdyn_plannedcost_base       | No             | No           |
| msdyn_plannedcostcontour     | No             | No           |
| msdyn_plannedsales           | No             | No           |
| msdyn_plannedsales_base      | No             | No           |
| msdyn_plannedsalescontour    | No             | No           |
| msdyn_plannedwork            | No             | No           |
| msdyn_projectid              | Ya            | No           |
| msdyn_projectidname          | No             | No           |
| msdyn_projectteamid          | No             | No           |
| msdyn_projectteamidname      | No             | No           |
| msdyn_start                  | No             | No           |
| msdyn_taskid                 | No             | No           |
| msdyn_taskidname             | No             | No           |
| msdyn_userresourceid         | No             | No           |

### <a name="project-team-member"></a>Anggota Tim Proyek

| Nama logika                                     | Dapat membuat     | Dapat mengedit     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | No             | No           |
| msdyn_creategenericteammemberwithrequirementname | No             | No           |
| msdyn_deletestatus                               | No             | No           |
| msdyn_deletestatusname                           | No             | No           |
| msdyn_effort                                     | No             | No           |
| msdyn_effortcompleted                            | No             | No           |
| msdyn_effortremaining                            | No             | No           |
| msdyn_finish                                     | No             | No           |
| msdyn_hardbookedhours                            | No             | No           |
| msdyn_hours                                      | No             | No           |
| msdyn_markedfordeletiontimer                     | No             | No           |
| msdyn_markedfordeletiontimestamp                 | No             | No           |
| msdyn_msprojectclientid                          | No             | No           |
| msdyn_percentage                                 | No             | No           |
| msdyn_requiredhours                              | No             | No           |
| msdyn_softbookedhours                            | No             | No           |
| msdyn_start                                      | No             | No           |

### <a name="project"></a>Project

| Nama logika                           | Dapat membuat     | Dapat mengedit     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | No             | No           |
| msdyn_actualexpensecost_base           | No             | No           |
| msdyn_actuallaborcost                  | No             | No           |
| msdyn_actuallaborcost_base             | No             | No           |
| msdyn_actualsales                      | No             | No           |
| msdyn_actualsales_base                 | No             | No           |
| msdyn_contractlineproject              | Ya            | No           |
| msdyn_contractorganizationalunitid     | Ya            | No           |
| msdyn_contractorganizationalunitidname | Ya            | No           |
| msdyn_costconsumption                  | No             | No           |
| msdyn_costestimateatcomplete           | No             | No           |
| msdyn_costestimateatcomplete_base      | No             | No           |
| msdyn_costvariance                     | No             | No           |
| msdyn_costvariance_base                | No             | No           |
| msdyn_duration                         | No             | No           |
| msdyn_effort                           | No             | No           |
| msdyn_effortcompleted                  | No             | No           |
| msdyn_effortestimateatcompleteeac      | No             | No           |
| msdyn_effortremaining                  | No             | No           |
| msdyn_finish                           | Ya            | Ya          |
| msdyn_globalrevisiontoken              | No             | No           |
| msdyn_islinkedtomsprojectclient        | No             | No           |
| msdyn_islinkedtomsprojectclientname    | No             | No           |
| msdyn_linkeddocumenturl                | No             | No           |
| msdyn_msprojectdocument                | No             | No           |
| msdyn_msprojectdocumentname            | No             | No           |
| msdyn_plannedexpensecost               | No             | No           |
| msdyn_plannedexpensecost_base          | No             | No           |
| msdyn_plannedlaborcost                 | No             | No           |
| msdyn_plannedlaborcost_base            | No             | No           |
| msdyn_plannedsales                     | No             | No           |
| msdyn_plannedsales_base                | No             | No           |
| msdyn_progress                         | No             | No           |
| msdyn_remainingcost                    | No             | No           |
| msdyn_remainingcost_base               | No             | No           |
| msdyn_remainingsales                   | No             | No           |
| msdyn_remainingsales_base              | No             | No           |
| msdyn_replaylogheader                  | No             | No           |
| msdyn_salesconsumption                 | No             | No           |
| msdyn_salesestimateatcompleteeac       | No             | No           |
| msdyn_salesestimateatcompleteeac_base  | No             | No           |
| msdyn_salesvariance                    | No             | No           |
| msdyn_salesvariance_base               | No             | No           |
| msdyn_scheduleperformance              | No             | No           |
| msdyn_scheduleperformancename          | No             | No           |
| msdyn_schedulevariance                 | No             | No           |
| msdyn_taskearlieststart                | No             | No           |
| msdyn_teamsize                         | No             | No           |
| msdyn_teamsize_date                    | No             | No           |
| msdyn_teamsize_state                   | No             | No           |
| msdyn_totalactualcost                  | No             | No           |
| msdyn_totalactualcost_base             | No             | No           |
| msdyn_totalplannedcost                 | No             | No           |
| msdyn_totalplannedcost_base            | No             | No           |

### <a name="project-bucket"></a>Wadah Proyek

| Nama logika          | Dapat membuat      | Dapat mengedit     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | Ya             | No           |
| msdyn_name            | Ya             | Ya          |
| msdyn_project         | Ya             | No           |
| msdyn_projectbucketid | Ya             | No           |

## <a name="limitations-and-known-issues"></a>Masalah dan batasan yang diketahui
Berikut adalah daftar batasan dan masalah umum:

- API Jadwal Proyek hanya dapat digunakan oleh **Pengguna dengan Lisensi** Microsoft Project. Tidak dapat digunakan oleh:

    - Pengguna Aplikasi
    - Pengguna Sistem
    - Pengguna Integrasi
    - Pengguna lain yang tidak memiliki lisensi yang diperlukan

- Setiap **OperationSet** hanya dapat memiliki maksimum 100 operasi.
- Setiap pengguna hanya dapat membuka maksimum 10 **OperationSet** terbuka.
- Project Operations saat ini mendukung maksimum 500 tugas total pada proyek.
- Status kegagalan dan log kegagalan **OperationSet** saat ini tidak tersedia.
- [Batas dan batasan pada proyek dan tugas](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Penanganan kesalahan

- Untuk memeriksa kesalahan yang dihasilkan dari Rangkaian Operasi, buka **Pengaturan** \> **Integrasi Jadwal** \> **Rangkaian Operasi**.
- Untuk memeriksa kesalahan yang dihasilkan dari Layanan Jadwal Proyek, buka **pengaturan** \> **integrasi Jadwal** \> **Log Kesalahan PSS**.

## <a name="sample-scenario"></a>Contoh Skenario

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

## <a name="additional-samples"></a>Contoh tambahan

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
