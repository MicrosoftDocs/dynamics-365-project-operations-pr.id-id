---
title: Bagaimana cara menyesuaikan alur proses bisnis tahapan proyek?
description: Ikhtisar cara menyesuaikan alur proses bisnis Tahapan Proyek.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752391"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Bagaimana cara menyesuaikan alur proses bisnis tahapan proyek?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Ada batasan umum di versi sebelumnya dari aplikasi Project Service bahwa nama tahapan di alur proses bisnis tahapan proyek harus sama persis dengan nama bahasa Inggris yang diharapkan (**kuotasi**, **merencanakan**, **Tutup**). Jika tidak, logika bisnis, yang mengandalkan nama bahasa Inggris tahapan, tidak berfungsi sebagaimana yang diharapkan. Karena itu Anda tidak akrab dengan tindakan seperti **beralih proses** atau **Edit proses** yang tersedia di formulir proyek, dan menyesuaikan alur proses bisnis tidak didukung. 

Keterbatasan ini telah diatasi di versi 2.4.5.48 dan kemudian. Artikel ini memberikan solusi yang disarankan jika Anda harus menyesuaikan alur proses bisnis default untuk versi sebelumnya.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Logika bisnis memerlukan pencocokan sama persis dengan nama bahasa Inggris tahapan

Alur proses bisnis tahapan proyek mencakup logika bisnis yang menggerakkan perilaku berikut dalam aplikasi:
- Bila proyek terkait dengan kuotasi, kode mengatur alur proses bisnis untuk **Quote** tahapan.
- Bila proyek terkait dengan kontrak, kode mengatur alur proses bisnis untuk tahapan **Plan**.
- Bila alur proses bisnis dilanjutkan ke tahapan **Close**, rekaman proyek akan dinonaktifkan. Bila proyek dinonaktifkan, formulir proyek dan struktur rincian kerja (WBS) diatur ke hanya baca, Pemesanan sumber daya bernama dirilis, dan daftar harga terkait apa pun dinonaktifkan.

Logika bisnis ini mengandalkan nama bahasa Inggris tahapan proyek. Dependensi pada nama tahapan bahasa Inggris ini adalah alasan utama mengapa penyesuaian alur proses bisnis tahapan proyek tidak didukung, serta mengapa Anda tidak melihat alur proses bisnis umum seperti **beralih proses** atau **Mengedit proses** di entitas proyek.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Apa yang terjadi jika nama tahapan tidak cocok dengan nama bahasa Inggris?

Di versi aplikasi Project Service 1.x platform 8,2, ketika nama tahapan dalam alur proses bisnis tidak cocok nama bahasa Inggris dengan sama persis, logika bisnis yang mengatur kuotasi atau kontrak, atau yang menyelesaikan proyek, diabaikan. Tidak ada pesan kesalahan ditampilkan. Oleh karena itu sepertinya Anda dapat menyesuaikan alur proses bisnis tahapan proyek. Padahal, Anda tidak akan melihat proses otomatis yang berfungsi untuk kuotasi, kontrak, dan tutup proyek.

Di versi aplikasi Project Service 2.4.4.30 atau sebelumnya di 9.0 platform, ada perubahan arsitektural yang signifikan untuk alur proses bisnis yang mengharuskan penulisan ulang logika bisnis alur proses bisnis. Oleh karena itu, jika nama tahapan proses tidak cocok dengan nama bahasa Inggris yang diharapkan, Anda menerima pesan kesalahan. 

Oleh karena itu, jika Anda ingin menyesuaikan alur proses bisnis tahapan proyek untuk entitas proyek, Anda hanya dapat menambahkan tahapan baru untuk alur proses bisnis default untuk entitas proyek, sambil menjaga tahap **kuotasi**, **merencanakan**, dan **tutup** sebagaimana adanya. Batasan ini memastikan bahwa Anda tidak mendapatkan kesalahan dari logika bisnis yang mengharapkan nama bahasa Inggris tahapan di alur proses bisnis.

Di versi 2.4.5.48 atau lebih baru, logika bisnis yang dijelaskan di artikel ini telah dihapus dari alur proses bisnis default untuk entitas proyek. Meningkatkan ke versi tersebut atau nanti akan memungkinkan Anda menyesuaikan atau mengganti alur proses bisnis default dengan punya Anda sendiri. 

## <a name="workarounds-for-earlier-versions"></a>Solusi untuk versi sebelumnya

Jika meningkatkan bukan pilihan, Anda dapat menyesuaikan alur proses bisnis tahapan proyek untuk entitas proyek dengan salah satu dari dua cara berikut:

1. Menambahkan tahapan tambahan untuk konfigurasi default, sementara tetap mempertahankan nama bahasa Inggris tahapan untuk **kuotasi**, **merencanakan**, dan **tutup**.

   > [!div class="mx-imgBorder"] 
   > ![Tangkapan layar menambahkan tahapan ke konfigurasi default](media/FAQ-Customize-BPF-1.png)
 
2. Buat alur proses bisnis Anda sendiri dan jadikan itu alur proses bisnis utama untuk entitas proyek, yang memungkinkan Anda memiliki nama tahapan apa pun yang Anda inginkan. Namun, jika Anda ingin menggunakan tahapan standar proyek yang sama **kuotasi**, **merencanakan**, dan **tutup**, Anda harus melakukan beberapa penyesuaian yang didorong oleh nama tahapan kustom Anda. Logika yang lebih kompleks adalah penutup proyek, yang mana Anda tetap dapat memicu dengan hanya menonaktifkan rekaman proyek.

   > [!div class="mx-imgBorder"] 
   > ![Potret layar Penyesuaian BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Pertimbangan tambahan untuk Project Service aplikasi versi 2.4.4.30 atau sebelumnya di platform 9.0

Project Service 2.4.4.30 atau sebelumnya di platform 9.0, dengan alur proses bisnis kustom, bidang **nama tahapan** di entitas proyek yang digunakan dalam bagan **proyek menurut tahapan**, dan tampilan daftar proyek tidak akan diperbarui, karena digabungkan ke default alur proses bisnis tahapan proyek. Anda dapat mengatasi masalah ini dengan langkah-langkah berikut:

- Tambahkan bidang kustom untuk mengambil tahapan alur proses bisnis saat ini yang akan diperbarui saat pengguna melalui alur proses bisnis kustom.

- Modifikasikan diagram **proyek menurut tahapan** untuk berfungsi pada bidang kustom Anda, bukan konfigurasi default.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Langkah-langkah untuk membuat bisnis alur proses bisnis Anda sendiri untuk entitas proyek

Untuk membuat bisnis alur proses bisnis Anda sendiri untuk entitas proyek, lakukan yang berikut ini:

1. Buka **Pengaturan** > **Pusat Proses**. Jangan menyalin alur proses bisnis tahapan proyek karena juga menyalin logika bisnis Project Service.

   > [!div class="mx-imgBorder"] 
   > ![Potret layar Penyesuaian BPF](media/FAQ-Customize-BPF-3.png)

2. Gunakan desainer proses untuk membuat nama tahapan yang Anda inginkan. Jika Anda ingin fungsi yang sama seperti tahapan default untuk **kuotasi**, **merencanakan**, dan **tutup**, Anda harus membuatnya berdasarkan nama tahapan alur proses bisnis kustom Anda.

   > [!div class="mx-imgBorder"] 
   > ![Gambar layar desainer proses yang digunakan untuk menyesuaikan BPF](media/FAQ-Customize-BPF-4.png) 

3. Dalam desainer proses, klik **alur proses pesanan** untuk membuat proses bisnis kustom sebagai alur proses bisnis utama untuk entitas proyek dengan memindahkannya di alur proses bisnis tahapan proyek ke atas daftar.

   > [!div class="mx-imgBorder"] 
   > ![Tangkapan layar menggunakan alur proses pesanan](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Langkah-langkah berikut berlaku untuk aplikasi Project Service 2.4.4.30 atau sebelumnya di 9.0 platform

4. Tambahkan bidang kustom baru untuk entitas proyek untuk mengambil tahapan kustom di alur proses bisnis kustom Anda. Anda harus menambahkan logika bisnis (plugin/alur kerja) untuk memperbarui bidang ini saat tahapan pada alur proses bisnis kustom diperbarui.

   > [!div class="mx-imgBorder"] 
   > ![Tangkapan layar penyesuaian entitas proyek](media/FAQ-Customize-BPF-6-720.png)

5. Modifikasikan **proyek menurut tahapan** diagram untuk menggunakan bidang kustom baru untuk tahapan.

   > [!div class="mx-imgBorder"] 
   > ![Tangkapan layar menggunakan diagram proyek menurut tahapan](media/FAQ-Customize-BPF-7-720.png)

6. Modifikasikan apa pun tampilan untuk entitas proyek untuk memasukkan bidang kustom baru untuk tahapan.

   > [!div class="mx-imgBorder"] 
   > ![Tangkapan layar memodifikasi tampilan di entitas proyek](media/FAQ-Customize-BPF-8-720.png)

