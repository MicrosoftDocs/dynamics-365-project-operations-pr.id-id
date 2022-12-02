---
title: Terapkan bidang kustom untuk aplikasi seluler Microsoft Dynamics 365 Project Timesheet di IOS dan Android
description: Artikel ini menyediakan pola umum untuk menggunakan ekstensi untuk menerapkan bidang kustom.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 03b79d58d1f91e07034b8c9efb408e6d7a9c29a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913716"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Terapkan bidang kustom untuk aplikasi seluler Microsoft Dynamics 365 Project Timesheet di IOS dan Android

[!include [banner](../includes/banner.md)]

Artikel ini menyediakan pola umum untuk menggunakan ekstensi untuk menerapkan bidang kustom. Artikel berikut ini tercakup:

- Berbagai jenis data yang didukung kerangka kerja bidang kustom
- Cara menampilkan bidang yang dapat diedit atau hanya baca di entri lembar waktu, dan menyimpan nilai yang disediakan pengguna kembali ke database
- Cara menampilkan bidang baca-saja pada header lembar waktu
- Cara mengintegrasikan logika bisnis kustom lainnya untuk memasukkan nilai default di bidang dan melakukan validasi tambahan

## <a name="audience"></a>Audiens

Artikel ini ditujukan untuk pengembang yang mengintegrasikan bidang kustom mereka ke aplikasi seluler Microsoft Dynamics 365 Project Timesheet yang tersedia untuk Apple iOS dan Google Android. Asumsinya adalah bahwa pembaca terbiasa dengan pengembangan X++ dan fungsi lembar waktu proyek.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Kontrak data – TSTimesheetCustomField kelas X++

Kelas **TSTimesheetCustomField** adalah kelas kontrak data X++ yang mewakili informasi tentang bidang kustom untuk fungsi lembar waktu. Daftar objek lapangan kustom diteruskan pada kontrak data TSTimesheetDetails dan kontrak data TSTimesheetEntry untuk menampilkan bidang kustom di aplikasi ponsel.

- **TSTimesheetDetails** -kontrak header lembar waktu.
- **TSTimesheetEntry** -kontrak transaksi lembar waktu. Grup objek ini yang memiliki informasi proyek dan nilai **timesheetLineRecId** yang sama merupakan baris.

### <a name="fieldbasetype-types"></a>fieldBaseType (Jenis)

Properti **fieldbasetype** pada objek **tstimesheetcustom** menentukan jenis bidang yang muncul di aplikasi. Nilai **jenis** berikut didukung.

| Nilai jenis | Jenis              | Catatan |
|-------------|-------------------|-------|
| 0           | String (dan Enum) | Bidang muncul sebagai bidang teks. |
| 1           | Bilangan bulat           | Nilai ditampilkan sebagai angka tanpa tempat desimal. |
| 2           | Riil              | Nilai ditampilkan sebagai angka yang tidak memiliki tempat desimal.<p>Untuk menampilkan nilai riil sebagai mata uang di aplikasi, gunakan properti **fieldExtenededType**. Anda dapat menggunakan properti **numberOfDecimals** untuk mengatur jumlah tempat desimal yang ditampilkan.</p> |
| 3           | Tanggal              | Format tanggal ditentukan berdasarkan pengaturan **tanggal, waktu, dan format nomor** pengguna yang ditentukan dalam preferensi **bahasa dan negara/kawasan** dalam **pilihan pengguna**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Jika properti **stringoptions** tidak diberikan pada objek **tstimesheetcustomfield**, bidang teks bebas diberikan kepada pengguna.

    Properti **stringlength** dapat digunakan untuk mengatur panjang maksimum string yang dapat dimasukkan pengguna.

- Jika properti **stringoptions** diberikan pada objek **tstimesheetcustomfield**, elemen daftar tersebut adalah satu-satunya nilai yang dapat dipilih pengguna dengan menggunakan tombol pilihan (tombol radio).

    Dalam kasus ini, bidang string dapat bertindak sebagai nilai enum untuk tujuan entri pengguna. Untuk menyimpan nilai ke database sebagai enum, secara manual petakan nilai string kembali ke nilai enum sebelum anda menyimpan database dengan menggunakan rantai perintah (lihat bagian "gunakan rantai perintah pada kelas TSTimesheetEntryService untuk menyimpan entri lembar waktu dari aplikasi kembali ke database" kemudian di artikel ini misalnya).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Anda dapat menggunakan properti ini untuk memformat nilai riil sebagai mata uang. Pendekatan ini berlaku hanya bila nilai **fieldbasetype** itu **Riil**.

- **TSCustomFieldExtendedType:None** -pemformatan tidak diterapkan.
- **TSCustomFieldExtendedType::Currency** – memformat nilai sebagai mata uang.

    Bila pemformatan mata uang aktif, bidang **stringvalue** dapat digunakan melewati kode mata uang yang harus ditampilkan di aplikasi. Nilai adalah nilai baca-saja.

    Bidang **realvalue** berisi jumlah uang yang akan disimpan ke database.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Anda dapat menggunakan properti ini menentukan lokasi bidang kustom yang akan muncul di aplikasi.

- **TSCustomFieldSection::header** -bidang ini akan muncul di bagian **Lihat rincian lainnya** dalam aplikasi. Bidang ini selalu hanya baca.
- **TSCustomFieldSection::Line** – bidang akan muncul setelah semua bidang baris bawaan pada entri lembar waktu. Bidang ini dapat diedit atau hanya baca.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Properti ini mengidentifikasi bidang saat nilai yang disediakan aplikasi disimpan kembali ke database.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Properti ini mengidentifikasi bidang saat nilai yang disediakan aplikasi disimpan kembali ke database.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Atur properti ini ke **ya** untuk menentukan bahwa bidang di bagian entri lembar waktu harus dapat diedit oleh pengguna. Atur properti ke **tidak** untuk membuat bidang hanya baca.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Atur properti ini ke **ya** untuk menentukan bahwa bidang di bagian entri lembar waktu harus wajib.

### <a name="label-str"></a>label (str)

Properti ini menentukan label yang ditampilkan di bidang berikutnya dalam aplikasi.

### <a name="stringoptions-list-of-strings"></a>stringOptions (daftar String)

Properti ini hanya berlaku bila **fieldbasetype** diatur ke **string**. Jika **stringoptions** diatur, nilai string yang tersedia untuk pilihan melalui tombol pilihan (tombol radio) ditentukan oleh string dalam daftar. Jika tidak ada string yang disediakan, entri teks bebas di bidang string diizinkan (lihat bagian "gunakan rantai perintah pada kelas tstimesheetentryservice untuk menyimpan entri lembar waktu dari aplikasi kembali ke database" nanti di artikel ini sebagai contoh).

### <a name="stringlength-int"></a>stringLength (int)

Properti ini menentukan panjang maksimum untuk bidang string. Ini hanya berlaku bila **fieldbasetype** diatur ke **string**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Properti ini menentukan jumlah tempat desimal yang ditampilkan untuk bidang riil. Ini hanya berlaku bila **fieldbasetype** diatur ke **Riil**.

### <a name="ordersequence-int"></a>orderSequence (int)

Properti ini mengontrol urutan bidang kustom yang ditampilkan di aplikasi saat lebih dari satu bidang kustom ditentukan. Bidang yang memiliki angka lebih rendah ditampilkan lebih dulu.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Untuk bidang jenis **Boolean**, properti ini meneruskan nilai Boolean bidang antara server dan aplikasi.

### <a name="guidvalue-guid"></a>guidValue (guid)

Untuk bidang jenis **GUID**, properti ini meneruskan nilai pengidentifikasi unik global (GUID) bidang antara server dan aplikasi.

### <a name="int64value-int64"></a>int64Value (int64)

Untuk bidang jenis **Int64**, properti ini meneruskan nilai Int64 bidang antara server dan aplikasi.

### <a name="intvalue-int"></a>intValue (int)

Untuk bidang jenis **Int**, properti ini meneruskan nilai Int bidang antara server dan aplikasi.

### <a name="realvalue-real"></a>realValue (riil)

Untuk bidang jenis **Riil**, properti ini meneruskan nilai riil bidang antara server dan aplikasi.

### <a name="stringvalue-str"></a>stringValue (Str)

Untuk bidang jenis **String**, properti ini meneruskan nilai String bidang antara server dan aplikasi. Juga digunakan untuk bidang jenis **Riil** yang diformat sebagai mata uang. Untuk bidang tersebut, properti akan digunakan untuk meneruskan kode mata uang ke aplikasi.

### <a name="datevalue-date"></a>dateValue (tanggal)

Untuk bidang jenis **Tanggal**, properti ini meneruskan nilai tanggal bidang antara server dan aplikasi.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Menampilkan dan menyimpan bidang kustom di bagian entri lembar waktu

Di bawah ini adalah screenshot dari aplikasi seluler pembuatan entri lembar waktu. Menampilkan bidang siap pakai dan bidang kustom di bagian "entri waktu" yang disebut "uji string" dengan nilai enum "pilihan kedua" yang telah ditetapkan.

![Uji bidang kustom string dalam aplikasi.](media/timesheet-entry.jpg)



Di bawah ini adalah screenshot dari aplikasi perangkat bergerak pengguna yang memilih salah satu pilihan enum yang tersedia untuk bidang kustom "string uji".  Dua pilihan adalah "pilihan pertama" dan "pilihan kedua" ditampilkan sebagai tombol radio. Pilihan kedua saat ini dipilih.

![Tombol pilihan (tombol radio) untuk bidang kustom uji string.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Perluas tabel TSTimesheetLine sehingga memiliki bidang kustom

Dalam skenario umum, kemungkinan data untuk bidang kustom di bagian entri lembar waktu akan disimpan ke tabel TSTimesheetLine. Namun, tabel lainnya dapat digunakan jika data dapat diambil berdasarkan rekaman TSTimesheetTrans yang disediakan, atau jika ia tidak memiliki konteks rekaman tertentu (misalnya, jika bidang diatur sebagai hanya baca dalam parameter proyek).

Perhatikan bahwa bidang kustom tidak harus memiliki rekaman database dukungan. Mereka dapat dibuat secara dinamis berdasarkan logika X++. Pendekatan ini dapat berguna dalam skenario hanya baca (Lihat bagian "Gunakan rantai perintah pada kelas TSTimesheetDetails, metode buildCustomFieldListForHeader untuk mengisi rincian lembar waktu" untuk contoh nilai bidang kustom yang dihasilkan secara dinamis.)

Di bawah ini adalah screenshot dari Visual Studio pohon objek aplikasi. Ini menunjukkan perpanjangan dari tabel TSTimesheetLine dengan bidang TestLineString ditambahkan sebagai bidang kustom.

![String baris.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Gunakan rantai perintah pada metode buildCustomFieldList kelas TSTimesheetSettings untuk menampilkan bidang di bagian entri lembar waktu

Kode ini mengontrol pengaturan tampilan untuk bidang di aplikasi. Contohnya, kontrol jenis bidang, label, Apakah bidang wajib, dan di bagian apa bidang ditampilkan.

Contoh berikut menunjukkan bidang string pada entri waktu. Bidang ini memiliki dua pilihan, **pilihan pertama** dan **pilihan kedua**, yang tersedia melalui tombol pilihan (tombol radio). Bidang di aplikasi dikaitkan dengan bidang **testlinestring** yang ditambahkan ke tabel TSTimesheetLine.

Ingat penggunaan metode **tstimesheetcustomfield::newfrommetatdata()** untuk menyederhanakan inisialisasi properti bidang kustom: **fieldbasetype**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, dan **numberOfDecimals**. Anda juga dapat mengatur parameter ini secara manual, seperti yang Anda inginkan.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Gunakan rantai perintah pada metode buildCustomFieldListForEntry kelas TSTimesheetEntry untuk memasukkan nilai di entri lembar waktu

Metode **buildCustomFieldListForEntry** digunakan untuk memasukkan nilai baris lembar waktu yang tersimpan di aplikasi ponsel. Dibutuhkan rekaman TSTimesheetTrans sebagai parameter. Bidang dari rekaman tersebut dapat digunakan untuk mengisi nilai bidang kustom di aplikasi.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Gunakan rantai perintah pada kelas TSTimesheetEntryService untuk menyimpan entri lembar waktu dari aplikasi kembali ke database

Untuk menyimpan bidang kustom kembali ke database dalam penggunaan umum, Anda harus memperpanjang beberapa metode:

- Metode **timesheetLineNeedsUpdating** digunakan untuk menentukan apakah rekaman baris telah diubah oleh pengguna di aplikasi dan harus disimpan ke database. Jika performa tidak menjadi masalah, metode ini dapat disederhanakan agar selalu menghasilkan **True**.
- Metode **populateTimesheetLineFromEntryDuringCreate** dan **populateTimesheetLineFromEntryDuringUpdate** dapat diperpanjang sehingga mereka memasukkan nilai pada rekaman database TSTimesheetLine dari rekaman kontrak data TSTimesheetEntry yang disediakan. Pada contoh berikut, perhatikan bagaimana pemetaan antara bidang database dan bidang entri secara manual dilakukan melalui kode X++.
- Metode **populateTimesheetWeekFromEntry** juga dapat diperpanjang Jika bidang kustom yang dipetakan ke objek **TSTimesheetEntry** harus menulis kembali ke tabel database TSTimesheetLineweek.

> [!NOTE]
> Contoh berikut menyimpan nilai **firstoption** atau **secondoption** yang dipilih pengguna ke database sebagai nilai string mentah. Jika bidang database adalah bidang dari jenis **Enum**, nilai tersebut dapat secara manual dipetakan ke nilai Enum dan kemudian disimpan ke bidang Enum pada tabel database.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Menampilkan bidang kustom di bagian header lembar waktu

Di bawah ini adalah screenshot dari aplikasi seluler pengguna yang melihat lembar waktu. Tombol "informasi selengkapnya" telah dipilih di sudut kanan atas untuk menampilkan pilihan "Lihat rincian lainnya".  

![Perintah lihat rincian lainnya.](media/show-more.png)

Di bawah ini adalah screenshot dari aplikasi seluler yang menampilkan bagian "Lainnya" dari lembar waktu. Bidang kustom yang disebut "tingkat pemanfaatan lembar waktu ini (bidang kustom dihitung)" telah ditambahkan ke bagian header lembar waktu. Nilai baca-saja "0,667" diatur pada bidang kustom.

![Bagian lainnya.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Perluas tabel TSTimesheetTable sehingga memiliki bidang kustom

Dalam skenario umum, kemungkinan data untuk bidang kustom di bagian header akan ditarik dari tabel TSTimesheetHeader. Namun, tabel lainnya dapat digunakan jika data dapat diambil berdasarkan rekaman TSTimesheetTable yang disediakan, atau jika ia tidak memiliki konteks rekaman tertentu (misalnya, jika bidang diatur sebagai hanya baca dalam parameter proyek).

Perhatikan bahwa bidang kustom tidak harus memiliki rekaman database dukungan. Mereka dapat dibuat secara dinamis berdasarkan logika X++. Contoh yang berikut menunjukkan pendekatan ini.

Bidang di bagian header selalu hanya baca di aplikasi.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Gunakan rantai perintah pada metode buildCustomFieldList kelas TSTimesheetSettings untuk menampilkan bidang di bagian entri header

Kode ini mengontrol pengaturan tampilan untuk bidang di aplikasi. Contohnya, kontrol jenis bidang, label, Apakah bidang wajib, dan di bagian apa bidang ditampilkan.

Contoh berikut menunjukkan nilai yang dihitung di bagian header di aplikasi.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Gunakan rantai perintah pada metode buildCustomFieldListForHeader kelas TSTimesheetDetails untuk mengisi detail di lembar waktu

Metode **buildCustomFieldListForHeader** digunakan untuk mengisi detail header lembar waktu di aplikasi ponsel. Dibutuhkan rekaman TSTimesheetTable sebagai parameter. Bidang dari rekaman tersebut dapat digunakan untuk mengisi nilai bidang kustom di aplikasi. Contoh berikut tidak membaca nilai apa pun dari database. Sebaliknya, ia menggunakan logika X++ untuk menghasilkan nilai yang dihitung yang kemudian ditampilkan di aplikasi.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Peluang konfigurasi/ekstensibilitas lainnya

### <a name="adding-additional-validation-for-the-app"></a>Menambahkan validasi tambahan untuk aplikasi

Logika yang ada untuk fungsi lembar waktu di tingkat database akan tetap berfungsi sebagaimana mestinya. Untuk menghentikan penyelesaian operasi Simpan atau kirim dan menampilkan pesan kesalahan tertentu, Anda dapat menambahkan **throw error("message to user")** ke kode melalui rantai ekstensi perintah. Berikut adalah tiga contoh metode bisa diperluas yang berguna:

- Jika **validateWrite** pada tabel TSTimesheetLine mengembalikan **false** selama operasi Simpan untuk baris lembar waktu, pesan kesalahan ditampilkan di aplikasi mobile.
- Jika **validateSubmit** pada tabel TSTimesheetTable mengembalikan **false** selama pengiriman dalam aplikasi, pesan kesalahan ditampilkan pada pengguna.
- Logika yang mengisi dalam bidang (misalnya, **properti baris**) selama metode **insert** pada tabel TSTimesheetLine masih akan berjalan.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Menyembunyikan dan menandai bidang bawaan sebagai hanya baca melalui konfigurasi

Dari parameter proyek, Anda dapat membuat bidang bawaan hanya baca, atau tersembunyi di aplikasi seluler. Atur pilihan di bagian **lembar waktu Mobile** pada tab **lembar waktu** halaman **parameter manajemen proyek dan akuntansi**.

![Parameter Proyek.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Mengubah aktivitas yang tersedia untuk dipilih melalui ekstensi

Aktivitas yang tersedia untuk pemilihan proyek diisi melalui metode **getActivitiesForProject()** dan **getActivityQuery()** di kelas **TsTimesheetProjectService**. Anda dapat menggunakan rantai perintah untuk mengubah perilaku ini agar sesuai dengan skenario bisnis Anda untuk aktivitas yang tersedia untuk pilihan proyek tertentu.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Memasukkan kategori default proyek pada entri lembar waktu

Entri kategori proyek default pada entri lembar waktu terjadi pada tiga tingkat. Anda dapat menggunakan rantai perintah untuk memperluas perilaku pada salah satu atau semua tingkat ini untuk mencapai perilaku yang diinginkan. Hierarki berikut digunakan:

1. Aplikasi akan mencoba memasukkan kategori default dari sumber daya proyek. Kategori default ini diatur dalam metode **getCurrentUserResource** dan **getDelegatedResourcesForCurrentUser** dalam kelas **TSTimesheetSettingsService**.
2. Jika kategori default tidak tersedia di tingkat sumber daya proyek, aplikasi akan mencoba menariknya dari aktivitas proyek. Kategori default ini diatur dalam metode **getActivitiesForProject** dalam kelas **TSTimesheetProjectService**.
3. Jika kategori default tidak tersedia di tingkat aktivitas proyek, kategori default diambil dari parameter proyek. Kategori default ini diatur dalam metode **getProjectDetailsbyRule** dalam kelas **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]