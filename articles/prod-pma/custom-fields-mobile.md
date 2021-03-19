---
title: Terapkan bidang kustom untuk aplikasi seluler Microsoft Dynamics 365 Project Timesheet di IOS dan Android
description: Topik ini menyediakan pola umum untuk menggunakan ekstensi untuk menerapkan bidang kustom.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270997"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="95610-103">Terapkan bidang kustom untuk aplikasi seluler Microsoft Dynamics 365 Project Timesheet di IOS dan Android</span><span class="sxs-lookup"><span data-stu-id="95610-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95610-104">Topik ini menyediakan pola umum untuk menggunakan ekstensi untuk menerapkan bidang kustom.</span><span class="sxs-lookup"><span data-stu-id="95610-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="95610-105">Topik berikut ini tercakup:</span><span class="sxs-lookup"><span data-stu-id="95610-105">The following topics are covered:</span></span>

- <span data-ttu-id="95610-106">Berbagai jenis data yang didukung kerangka kerja bidang kustom</span><span class="sxs-lookup"><span data-stu-id="95610-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="95610-107">Cara menampilkan bidang yang dapat diedit atau hanya baca di entri lembar waktu, dan menyimpan nilai yang disediakan pengguna kembali ke database</span><span class="sxs-lookup"><span data-stu-id="95610-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="95610-108">Cara menampilkan bidang baca-saja pada header lembar waktu</span><span class="sxs-lookup"><span data-stu-id="95610-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="95610-109">Cara mengintegrasikan logika bisnis kustom lainnya untuk memasukkan nilai default di bidang dan melakukan validasi tambahan</span><span class="sxs-lookup"><span data-stu-id="95610-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="95610-110">Audiens</span><span class="sxs-lookup"><span data-stu-id="95610-110">Audience</span></span>

<span data-ttu-id="95610-111">Topik ini ditujukan untuk pengembang yang mengintegrasikan bidang kustom mereka ke aplikasi seluler Microsoft Dynamics 365 Project Timesheet yang tersedia untuk Apple iOS dan Google Android.</span><span class="sxs-lookup"><span data-stu-id="95610-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="95610-112">Asumsinya adalah bahwa pembaca terbiasa dengan pengembangan X++ dan fungsi lembar waktu proyek.</span><span class="sxs-lookup"><span data-stu-id="95610-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="95610-113">Kontrak data – TSTimesheetCustomField kelas X++</span><span class="sxs-lookup"><span data-stu-id="95610-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="95610-114">Kelas **TSTimesheetCustomField** adalah kelas kontrak data X++ yang mewakili informasi tentang bidang kustom untuk fungsi lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="95610-115">Daftar objek lapangan kustom diteruskan pada kontrak data TSTimesheetDetails dan kontrak data TSTimesheetEntry untuk menampilkan bidang kustom di aplikasi ponsel.</span><span class="sxs-lookup"><span data-stu-id="95610-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="95610-116">**TSTimesheetDetails** -kontrak header lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="95610-117">**TSTimesheetEntry** -kontrak transaksi lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="95610-118">Grup objek ini yang memiliki informasi proyek dan nilai **timesheetLineRecId** yang sama merupakan baris.</span><span class="sxs-lookup"><span data-stu-id="95610-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="95610-119">fieldBaseType (Jenis)</span><span class="sxs-lookup"><span data-stu-id="95610-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="95610-120">Properti **fieldbasetype** pada objek **tstimesheetcustom** menentukan jenis bidang yang muncul di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="95610-121">Nilai **jenis** berikut didukung.</span><span class="sxs-lookup"><span data-stu-id="95610-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="95610-122">Nilai jenis</span><span class="sxs-lookup"><span data-stu-id="95610-122">Types value</span></span> | <span data-ttu-id="95610-123">Jenis</span><span class="sxs-lookup"><span data-stu-id="95610-123">Type</span></span>              | <span data-ttu-id="95610-124">Catatan</span><span class="sxs-lookup"><span data-stu-id="95610-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="95610-125">0</span><span class="sxs-lookup"><span data-stu-id="95610-125">0</span></span>           | <span data-ttu-id="95610-126">String (dan Enum)</span><span class="sxs-lookup"><span data-stu-id="95610-126">String (and Enum)</span></span> | <span data-ttu-id="95610-127">Bidang muncul sebagai bidang teks.</span><span class="sxs-lookup"><span data-stu-id="95610-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="95610-128">1</span><span class="sxs-lookup"><span data-stu-id="95610-128">1</span></span>           | <span data-ttu-id="95610-129">Bilangan bulat</span><span class="sxs-lookup"><span data-stu-id="95610-129">Integer</span></span>           | <span data-ttu-id="95610-130">Nilai ditampilkan sebagai angka tanpa tempat desimal.</span><span class="sxs-lookup"><span data-stu-id="95610-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="95610-131">2</span><span class="sxs-lookup"><span data-stu-id="95610-131">2</span></span>           | <span data-ttu-id="95610-132">Riil</span><span class="sxs-lookup"><span data-stu-id="95610-132">Real</span></span>              | <span data-ttu-id="95610-133">Nilai ditampilkan sebagai angka yang tidak memiliki tempat desimal.</span><span class="sxs-lookup"><span data-stu-id="95610-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="95610-134">Untuk menampilkan nilai riil sebagai mata uang di aplikasi, gunakan properti **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="95610-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="95610-135">Anda dapat menggunakan properti **numberOfDecimals** untuk mengatur jumlah tempat desimal yang ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="95610-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="95610-136">3</span><span class="sxs-lookup"><span data-stu-id="95610-136">3</span></span>           | <span data-ttu-id="95610-137">Tanggal</span><span class="sxs-lookup"><span data-stu-id="95610-137">Date</span></span>              | <span data-ttu-id="95610-138">Format tanggal ditentukan berdasarkan pengaturan **tanggal, waktu, dan format nomor** pengguna yang ditentukan dalam preferensi **bahasa dan negara/kawasan** dalam **pilihan pengguna**.</span><span class="sxs-lookup"><span data-stu-id="95610-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="95610-139">4</span><span class="sxs-lookup"><span data-stu-id="95610-139">4</span></span>           | <span data-ttu-id="95610-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="95610-140">Boolean</span></span>           | |
| <span data-ttu-id="95610-141">15</span><span class="sxs-lookup"><span data-stu-id="95610-141">15</span></span>          | <span data-ttu-id="95610-142">GUID</span><span class="sxs-lookup"><span data-stu-id="95610-142">GUID</span></span>              | |
| <span data-ttu-id="95610-143">16</span><span class="sxs-lookup"><span data-stu-id="95610-143">16</span></span>          | <span data-ttu-id="95610-144">Int64</span><span class="sxs-lookup"><span data-stu-id="95610-144">Int64</span></span>             | |

- <span data-ttu-id="95610-145">Jika properti **stringoptions** tidak diberikan pada objek **tstimesheetcustomfield**, bidang teks bebas diberikan kepada pengguna.</span><span class="sxs-lookup"><span data-stu-id="95610-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="95610-146">Properti **stringlength** dapat digunakan untuk mengatur panjang maksimum string yang dapat dimasukkan pengguna.</span><span class="sxs-lookup"><span data-stu-id="95610-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="95610-147">Jika properti **stringoptions** diberikan pada objek **tstimesheetcustomfield**, elemen daftar tersebut adalah satu-satunya nilai yang dapat dipilih pengguna dengan menggunakan tombol pilihan (tombol radio).</span><span class="sxs-lookup"><span data-stu-id="95610-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="95610-148">Dalam kasus ini, bidang string dapat bertindak sebagai nilai enum untuk tujuan entri pengguna.</span><span class="sxs-lookup"><span data-stu-id="95610-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="95610-149">Untuk menyimpan nilai ke database sebagai enum, secara manual petakan nilai string kembali ke nilai enum sebelum anda menyimpan database dengan menggunakan rantai perintah (lihat bagian "gunakan rantai perintah pada kelas TSTimesheetEntryService untuk menyimpan entri lembar waktu dari aplikasi kembali ke database" kemudian di topik ini misalnya).</span><span class="sxs-lookup"><span data-stu-id="95610-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="95610-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="95610-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="95610-151">Anda dapat menggunakan properti ini untuk memformat nilai riil sebagai mata uang.</span><span class="sxs-lookup"><span data-stu-id="95610-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="95610-152">Pendekatan ini berlaku hanya bila nilai **fieldbasetype** itu **Riil**.</span><span class="sxs-lookup"><span data-stu-id="95610-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="95610-153">**TSCustomFieldExtendedType:None** -pemformatan tidak diterapkan.</span><span class="sxs-lookup"><span data-stu-id="95610-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="95610-154">**TSCustomFieldExtendedType::Currency** – memformat nilai sebagai mata uang.</span><span class="sxs-lookup"><span data-stu-id="95610-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="95610-155">Bila pemformatan mata uang aktif, bidang **stringvalue** dapat digunakan melewati kode mata uang yang harus ditampilkan di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="95610-156">Nilai adalah nilai baca-saja.</span><span class="sxs-lookup"><span data-stu-id="95610-156">The value is a read-only value.</span></span>

    <span data-ttu-id="95610-157">Bidang **realvalue** berisi jumlah uang yang akan disimpan ke database.</span><span class="sxs-lookup"><span data-stu-id="95610-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="95610-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="95610-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="95610-159">Anda dapat menggunakan properti ini menentukan lokasi bidang kustom yang akan muncul di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="95610-160">**TSCustomFieldSection::header** -bidang ini akan muncul di bagian **Lihat rincian lainnya** dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="95610-161">Bidang ini selalu hanya baca.</span><span class="sxs-lookup"><span data-stu-id="95610-161">These fields are always read-only.</span></span>
- <span data-ttu-id="95610-162">**TSCustomFieldSection::Line** – bidang akan muncul setelah semua bidang baris bawaan pada entri lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="95610-163">Bidang ini dapat diedit atau hanya baca.</span><span class="sxs-lookup"><span data-stu-id="95610-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="95610-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="95610-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="95610-165">Properti ini mengidentifikasi bidang saat nilai yang disediakan aplikasi disimpan kembali ke database.</span><span class="sxs-lookup"><span data-stu-id="95610-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="95610-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="95610-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="95610-167">Properti ini mengidentifikasi bidang saat nilai yang disediakan aplikasi disimpan kembali ke database.</span><span class="sxs-lookup"><span data-stu-id="95610-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="95610-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="95610-168">isEditable (NoYes)</span></span>

<span data-ttu-id="95610-169">Atur properti ini ke **ya** untuk menentukan bahwa bidang di bagian entri lembar waktu harus dapat diedit oleh pengguna.</span><span class="sxs-lookup"><span data-stu-id="95610-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="95610-170">Atur properti ke **tidak** untuk membuat bidang hanya baca.</span><span class="sxs-lookup"><span data-stu-id="95610-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="95610-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="95610-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="95610-172">Atur properti ini ke **ya** untuk menentukan bahwa bidang di bagian entri lembar waktu harus wajib.</span><span class="sxs-lookup"><span data-stu-id="95610-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="95610-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="95610-173">label (str)</span></span>

<span data-ttu-id="95610-174">Properti ini menentukan label yang ditampilkan di bidang berikutnya dalam aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="95610-175">stringOptions (daftar String)</span><span class="sxs-lookup"><span data-stu-id="95610-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="95610-176">Properti ini hanya berlaku bila **fieldbasetype** diatur ke **string**.</span><span class="sxs-lookup"><span data-stu-id="95610-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="95610-177">Jika **stringoptions** diatur, nilai string yang tersedia untuk pilihan melalui tombol pilihan (tombol radio) ditentukan oleh string dalam daftar.</span><span class="sxs-lookup"><span data-stu-id="95610-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="95610-178">Jika tidak ada string yang disediakan, entri teks bebas di bidang string diizinkan (lihat bagian "gunakan rantai perintah pada kelas tstimesheetentryservice untuk menyimpan entri lembar waktu dari aplikasi kembali ke database" nanti di topik ini sebagai contoh).</span><span class="sxs-lookup"><span data-stu-id="95610-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="95610-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="95610-179">stringLength (int)</span></span>

<span data-ttu-id="95610-180">Properti ini menentukan panjang maksimum untuk bidang string.</span><span class="sxs-lookup"><span data-stu-id="95610-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="95610-181">Ini hanya berlaku bila **fieldbasetype** diatur ke **string**.</span><span class="sxs-lookup"><span data-stu-id="95610-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="95610-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="95610-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="95610-183">Properti ini menentukan jumlah tempat desimal yang ditampilkan untuk bidang riil.</span><span class="sxs-lookup"><span data-stu-id="95610-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="95610-184">Ini hanya berlaku bila **fieldbasetype** diatur ke **Riil**.</span><span class="sxs-lookup"><span data-stu-id="95610-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="95610-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="95610-185">orderSequence (int)</span></span>

<span data-ttu-id="95610-186">Properti ini mengontrol urutan bidang kustom yang ditampilkan di aplikasi saat lebih dari satu bidang kustom ditentukan.</span><span class="sxs-lookup"><span data-stu-id="95610-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="95610-187">Bidang yang memiliki angka lebih rendah ditampilkan lebih dulu.</span><span class="sxs-lookup"><span data-stu-id="95610-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="95610-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="95610-188">booleanValue (boolean)</span></span>

<span data-ttu-id="95610-189">Untuk bidang jenis **Boolean**, properti ini meneruskan nilai Boolean bidang antara server dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="95610-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="95610-190">guidValue (guid)</span></span>

<span data-ttu-id="95610-191">Untuk bidang jenis **GUID**, properti ini meneruskan nilai pengidentifikasi unik global (GUID) bidang antara server dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="95610-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="95610-192">int64Value (int64)</span></span>

<span data-ttu-id="95610-193">Untuk bidang jenis **Int64**, properti ini meneruskan nilai Int64 bidang antara server dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="95610-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="95610-194">intValue (int)</span></span>

<span data-ttu-id="95610-195">Untuk bidang jenis **Int**, properti ini meneruskan nilai Int bidang antara server dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="95610-196">realValue (riil)</span><span class="sxs-lookup"><span data-stu-id="95610-196">realValue (real)</span></span>

<span data-ttu-id="95610-197">Untuk bidang jenis **Riil**, properti ini meneruskan nilai riil bidang antara server dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="95610-198">stringValue (Str)</span><span class="sxs-lookup"><span data-stu-id="95610-198">stringValue (str)</span></span>

<span data-ttu-id="95610-199">Untuk bidang jenis **String**, properti ini meneruskan nilai String bidang antara server dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="95610-200">Juga digunakan untuk bidang jenis **Riil** yang diformat sebagai mata uang.</span><span class="sxs-lookup"><span data-stu-id="95610-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="95610-201">Untuk bidang tersebut, properti akan digunakan untuk meneruskan kode mata uang ke aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="95610-202">dateValue (tanggal)</span><span class="sxs-lookup"><span data-stu-id="95610-202">dateValue (date)</span></span>

<span data-ttu-id="95610-203">Untuk bidang jenis **Tanggal**, properti ini meneruskan nilai tanggal bidang antara server dan aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="95610-204">Menampilkan dan menyimpan bidang kustom di bagian entri lembar waktu</span><span class="sxs-lookup"><span data-stu-id="95610-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="95610-205">Di bawah ini adalah screenshot dari aplikasi seluler pembuatan entri lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="95610-206">Menampilkan bidang siap pakai dan bidang kustom di bagian "entri waktu" yang disebut "uji string" dengan nilai enum "pilihan kedua" yang telah ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="95610-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Uji bidang kustom string dalam aplikasi](media/timesheet-entry.jpg)



<span data-ttu-id="95610-208">Di bawah ini adalah screenshot dari aplikasi perangkat bergerak pengguna yang memilih salah satu pilihan enum yang tersedia untuk bidang kustom "string uji".</span><span class="sxs-lookup"><span data-stu-id="95610-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="95610-209">Dua pilihan adalah "pilihan pertama" dan "pilihan kedua" ditampilkan sebagai tombol radio.</span><span class="sxs-lookup"><span data-stu-id="95610-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="95610-210">Pilihan kedua saat ini dipilih.</span><span class="sxs-lookup"><span data-stu-id="95610-210">The second option is currently selected.</span></span>

![Tombol pilihan (tombol radio) untuk bidang kustom uji string](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="95610-212">Perluas tabel TSTimesheetLine sehingga memiliki bidang kustom</span><span class="sxs-lookup"><span data-stu-id="95610-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="95610-213">Dalam skenario umum, kemungkinan data untuk bidang kustom di bagian entri lembar waktu akan disimpan ke tabel TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="95610-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="95610-214">Namun, tabel lainnya dapat digunakan jika data dapat diambil berdasarkan rekaman TSTimesheetTrans yang disediakan, atau jika ia tidak memiliki konteks rekaman tertentu (misalnya, jika bidang diatur sebagai hanya baca dalam parameter proyek).</span><span class="sxs-lookup"><span data-stu-id="95610-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="95610-215">Perhatikan bahwa bidang kustom tidak harus memiliki rekaman database dukungan.</span><span class="sxs-lookup"><span data-stu-id="95610-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="95610-216">Mereka dapat dibuat secara dinamis berdasarkan logika X++.</span><span class="sxs-lookup"><span data-stu-id="95610-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="95610-217">Pendekatan ini dapat berguna dalam skenario hanya baca (Lihat bagian "Gunakan rantai perintah pada kelas TSTimesheetDetails, metode buildCustomFieldListForHeader untuk mengisi rincian lembar waktu" untuk contoh nilai bidang kustom yang dihasilkan secara dinamis.)</span><span class="sxs-lookup"><span data-stu-id="95610-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="95610-218">Di bawah ini adalah screenshot dari Visual Studio pohon objek aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="95610-219">Ini menunjukkan perpanjangan dari tabel TSTimesheetLine dengan bidang TestLineString ditambahkan sebagai bidang kustom.</span><span class="sxs-lookup"><span data-stu-id="95610-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![String baris](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="95610-221">Gunakan rantai perintah pada metode buildCustomFieldList kelas TSTimesheetSettings untuk menampilkan bidang di bagian entri lembar waktu</span><span class="sxs-lookup"><span data-stu-id="95610-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="95610-222">Kode ini mengontrol pengaturan tampilan untuk bidang di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="95610-223">Contohnya, kontrol jenis bidang, label, Apakah bidang wajib, dan di bagian apa bidang ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="95610-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="95610-224">Contoh berikut menunjukkan bidang string pada entri waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="95610-225">Bidang ini memiliki dua pilihan, **pilihan pertama** dan **pilihan kedua**, yang tersedia melalui tombol pilihan (tombol radio).</span><span class="sxs-lookup"><span data-stu-id="95610-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="95610-226">Bidang di aplikasi dikaitkan dengan bidang **testlinestring** yang ditambahkan ke tabel TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="95610-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="95610-227">Ingat penggunaan metode **tstimesheetcustomfield::newfrommetatdata()** untuk menyederhanakan inisialisasi properti bidang kustom: **fieldbasetype**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, dan **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="95610-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="95610-228">Anda juga dapat mengatur parameter ini secara manual, seperti yang Anda inginkan.</span><span class="sxs-lookup"><span data-stu-id="95610-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="95610-229">Gunakan rantai perintah pada metode buildCustomFieldListForEntry kelas TSTimesheetEntry untuk memasukkan nilai di entri lembar waktu</span><span class="sxs-lookup"><span data-stu-id="95610-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="95610-230">Metode **buildCustomFieldListForEntry** digunakan untuk memasukkan nilai baris lembar waktu yang tersimpan di aplikasi ponsel.</span><span class="sxs-lookup"><span data-stu-id="95610-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="95610-231">Dibutuhkan rekaman TSTimesheetTrans sebagai parameter.</span><span class="sxs-lookup"><span data-stu-id="95610-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="95610-232">Bidang dari rekaman tersebut dapat digunakan untuk mengisi nilai bidang kustom di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="95610-233">Gunakan rantai perintah pada kelas TSTimesheetEntryService untuk menyimpan entri lembar waktu dari aplikasi kembali ke database</span><span class="sxs-lookup"><span data-stu-id="95610-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="95610-234">Untuk menyimpan bidang kustom kembali ke database dalam penggunaan umum, Anda harus memperpanjang beberapa metode:</span><span class="sxs-lookup"><span data-stu-id="95610-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="95610-235">Metode **timesheetLineNeedsUpdating** digunakan untuk menentukan apakah rekaman baris telah diubah oleh pengguna di aplikasi dan harus disimpan ke database.</span><span class="sxs-lookup"><span data-stu-id="95610-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="95610-236">Jika performa tidak menjadi masalah, metode ini dapat disederhanakan agar selalu menghasilkan **True**.</span><span class="sxs-lookup"><span data-stu-id="95610-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="95610-237">Metode **populateTimesheetLineFromEntryDuringCreate** dan **populateTimesheetLineFromEntryDuringUpdate** dapat diperpanjang sehingga mereka memasukkan nilai pada rekaman database TSTimesheetLine dari rekaman kontrak data TSTimesheetEntry yang disediakan.</span><span class="sxs-lookup"><span data-stu-id="95610-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="95610-238">Pada contoh berikut, perhatikan bagaimana pemetaan antara bidang database dan bidang entri secara manual dilakukan melalui kode X++.</span><span class="sxs-lookup"><span data-stu-id="95610-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="95610-239">Metode **populateTimesheetWeekFromEntry** juga dapat diperpanjang Jika bidang kustom yang dipetakan ke objek **TSTimesheetEntry** harus menulis kembali ke tabel database TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="95610-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="95610-240">Contoh berikut menyimpan nilai **firstoption** atau **secondoption** yang dipilih pengguna ke database sebagai nilai string mentah.</span><span class="sxs-lookup"><span data-stu-id="95610-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="95610-241">Jika bidang database adalah bidang dari jenis **Enum**, nilai tersebut dapat secara manual dipetakan ke nilai Enum dan kemudian disimpan ke bidang Enum pada tabel database.</span><span class="sxs-lookup"><span data-stu-id="95610-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="95610-242">Menampilkan bidang kustom di bagian header lembar waktu</span><span class="sxs-lookup"><span data-stu-id="95610-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="95610-243">Di bawah ini adalah screenshot dari aplikasi seluler pengguna yang melihat lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="95610-244">Tombol "informasi selengkapnya" telah dipilih di sudut kanan atas untuk menampilkan pilihan "Lihat rincian lainnya".</span><span class="sxs-lookup"><span data-stu-id="95610-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Perintah lihat rincian lainnya](media/show-more.png)

<span data-ttu-id="95610-246">Di bawah ini adalah screenshot dari aplikasi seluler yang menampilkan bagian "Lainnya" dari lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="95610-247">Bidang kustom yang disebut "tingkat pemanfaatan lembar waktu ini (bidang kustom dihitung)" telah ditambahkan ke bagian header lembar waktu.</span><span class="sxs-lookup"><span data-stu-id="95610-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="95610-248">Nilai baca-saja "0,667" diatur pada bidang kustom.</span><span class="sxs-lookup"><span data-stu-id="95610-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Bagian lainnya](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="95610-250">Perluas tabel TSTimesheetTable sehingga memiliki bidang kustom</span><span class="sxs-lookup"><span data-stu-id="95610-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="95610-251">Dalam skenario umum, kemungkinan data untuk bidang kustom di bagian header akan ditarik dari tabel TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="95610-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="95610-252">Namun, tabel lainnya dapat digunakan jika data dapat diambil berdasarkan rekaman TSTimesheetTable yang disediakan, atau jika ia tidak memiliki konteks rekaman tertentu (misalnya, jika bidang diatur sebagai hanya baca dalam parameter proyek).</span><span class="sxs-lookup"><span data-stu-id="95610-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="95610-253">Perhatikan bahwa bidang kustom tidak harus memiliki rekaman database dukungan.</span><span class="sxs-lookup"><span data-stu-id="95610-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="95610-254">Mereka dapat dibuat secara dinamis berdasarkan logika X++.</span><span class="sxs-lookup"><span data-stu-id="95610-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="95610-255">Contoh yang berikut menunjukkan pendekatan ini.</span><span class="sxs-lookup"><span data-stu-id="95610-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="95610-256">Bidang di bagian header selalu hanya baca di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="95610-257">Gunakan rantai perintah pada metode buildCustomFieldList kelas TSTimesheetSettings untuk menampilkan bidang di bagian entri header</span><span class="sxs-lookup"><span data-stu-id="95610-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="95610-258">Kode ini mengontrol pengaturan tampilan untuk bidang di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="95610-259">Contohnya, kontrol jenis bidang, label, Apakah bidang wajib, dan di bagian apa bidang ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="95610-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="95610-260">Contoh berikut menunjukkan nilai yang dihitung di bagian header di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="95610-261">Gunakan rantai perintah pada metode buildCustomFieldListForHeader kelas TSTimesheetDetails untuk mengisi detail di lembar waktu</span><span class="sxs-lookup"><span data-stu-id="95610-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="95610-262">Metode **buildCustomFieldListForHeader** digunakan untuk mengisi detail header lembar waktu di aplikasi ponsel.</span><span class="sxs-lookup"><span data-stu-id="95610-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="95610-263">Dibutuhkan rekaman TSTimesheetTable sebagai parameter.</span><span class="sxs-lookup"><span data-stu-id="95610-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="95610-264">Bidang dari rekaman tersebut dapat digunakan untuk mengisi nilai bidang kustom di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="95610-265">Contoh berikut tidak membaca nilai apa pun dari database.</span><span class="sxs-lookup"><span data-stu-id="95610-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="95610-266">Sebaliknya, ia menggunakan logika X++ untuk menghasilkan nilai yang dihitung yang kemudian ditampilkan di aplikasi.</span><span class="sxs-lookup"><span data-stu-id="95610-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="95610-267">Peluang konfigurasi/ekstensibilitas lainnya</span><span class="sxs-lookup"><span data-stu-id="95610-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="95610-268">Menambahkan validasi tambahan untuk aplikasi</span><span class="sxs-lookup"><span data-stu-id="95610-268">Adding additional validation for the app</span></span>

<span data-ttu-id="95610-269">Logika yang ada untuk fungsi lembar waktu di tingkat database akan tetap berfungsi sebagaimana mestinya.</span><span class="sxs-lookup"><span data-stu-id="95610-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="95610-270">Untuk menghentikan penyelesaian operasi Simpan atau kirim dan menampilkan pesan kesalahan tertentu, Anda dapat menambahkan **throw error("message to user")** ke kode melalui rantai ekstensi perintah.</span><span class="sxs-lookup"><span data-stu-id="95610-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="95610-271">Berikut adalah tiga contoh metode bisa diperluas yang berguna:</span><span class="sxs-lookup"><span data-stu-id="95610-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="95610-272">Jika **validateWrite** pada tabel TSTimesheetLine mengembalikan **false** selama operasi Simpan untuk baris lembar waktu, pesan kesalahan ditampilkan di aplikasi mobile.</span><span class="sxs-lookup"><span data-stu-id="95610-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="95610-273">Jika **validateSubmit** pada tabel TSTimesheetTable mengembalikan **false** selama pengiriman dalam aplikasi, pesan kesalahan ditampilkan pada pengguna.</span><span class="sxs-lookup"><span data-stu-id="95610-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="95610-274">Logika yang mengisi dalam bidang (misalnya, **properti baris**) selama metode **insert** pada tabel TSTimesheetLine masih akan berjalan.</span><span class="sxs-lookup"><span data-stu-id="95610-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="95610-275">Menyembunyikan dan menandai bidang bawaan sebagai hanya baca melalui konfigurasi</span><span class="sxs-lookup"><span data-stu-id="95610-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="95610-276">Dari parameter proyek, Anda dapat membuat bidang bawaan hanya baca, atau tersembunyi di aplikasi seluler.</span><span class="sxs-lookup"><span data-stu-id="95610-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="95610-277">Atur pilihan di bagian **lembar waktu Mobile** pada tab **lembar waktu** halaman **parameter manajemen proyek dan akuntansi**.</span><span class="sxs-lookup"><span data-stu-id="95610-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parameter Proyek](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="95610-279">Mengubah aktivitas yang tersedia untuk dipilih melalui ekstensi</span><span class="sxs-lookup"><span data-stu-id="95610-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="95610-280">Aktivitas yang tersedia untuk pemilihan proyek diisi melalui metode **getActivitiesForProject()** dan **getActivityQuery()** di kelas **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="95610-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="95610-281">Anda dapat menggunakan rantai perintah untuk mengubah perilaku ini agar sesuai dengan skenario bisnis Anda untuk aktivitas yang tersedia untuk pilihan proyek tertentu.</span><span class="sxs-lookup"><span data-stu-id="95610-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="95610-282">Memasukkan kategori default proyek pada entri lembar waktu</span><span class="sxs-lookup"><span data-stu-id="95610-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="95610-283">Entri kategori proyek default pada entri lembar waktu terjadi pada tiga tingkat.</span><span class="sxs-lookup"><span data-stu-id="95610-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="95610-284">Anda dapat menggunakan rantai perintah untuk memperluas perilaku pada salah satu atau semua tingkat ini untuk mencapai perilaku yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="95610-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="95610-285">Hierarki berikut digunakan:</span><span class="sxs-lookup"><span data-stu-id="95610-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="95610-286">Aplikasi akan mencoba memasukkan kategori default dari sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="95610-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="95610-287">Kategori default ini diatur dalam metode **getCurrentUserResource** dan **getDelegatedResourcesForCurrentUser** dalam kelas **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="95610-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="95610-288">Jika kategori default tidak tersedia di tingkat sumber daya proyek, aplikasi akan mencoba menariknya dari aktivitas proyek.</span><span class="sxs-lookup"><span data-stu-id="95610-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="95610-289">Kategori default ini diatur dalam metode **getActivitiesForProject** dalam kelas **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="95610-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="95610-290">Jika kategori default tidak tersedia di tingkat aktivitas proyek, kategori default diambil dari parameter proyek.</span><span class="sxs-lookup"><span data-stu-id="95610-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="95610-291">Kategori default ini diatur dalam metode **getProjectDetailsbyRule** dalam kelas **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="95610-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]