---
title: Lihat pemanfaatan sumber daya yang dikenakan biaya
description: Topik ini menyediakan informasi tentang tampilan pemanfaatan sumber daya.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752384"
---
# <a name="view-chargeable-utilization-for-resources"></a>Lihat pemanfaatan sumber daya yang dikenakan biaya
 
**Tampilan pemanfaatan** pada halaman **pemanfaatan sumber daya Project Service** menampilkan pemanfaatan yang dikenai biaya untuk setiap sumber daya yang dapat dipesan. Karena tampilan didasarkan pada papan jadwal, Anda akan menemukan banyak fungsi yang sama.

> ![Tangkapan layar tampilan pemanfaatan](media/FAQ-utilization-1.png)
 

Perhitungan pemanfaatan dikenakan biaya berfungsi sebagai berikut:

   Pemanfaatan dikenakan biaya = (Jam aktual kena biaya)/(kapasitas sumber daya )

Sel menyatakan pemanfaatan dikenakan biaya dihitung selama periode yang dipilih (hari, Minggu, atau bulan).

Warna dalam setiap sel menampilkan pemanfaatan sumber daya dikenakan biaya dibandingkan dengan pemanfaatan dikenakan biaya target mereka. 

Pemanfaatan target dapat mengatur default peran sumber daya atau pada masing-masing sumber daya itu sendiri. Perhitungan terlihat pada individual untuk target pertama, lalu default peran sumber daya.

## <a name="set-target-on-a-resource"></a>Menetapkan target pada sumber daya

1. Buka **Sumber Daya** \> **Sumber daya**. 
2. Pilih sumber daya untuk membuka rekaman. 
3. Di tab **Project Service**, Anda dapat mengatur pemanfaatan target sumber daya.

> ![Tangkapan layar menggunakan tab Project Service untuk menetapkan target pemanfaatan](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Menetapkan target pemanfaatan peran

1. Buka **Sumber Daya** \> **Peran Sumber daya**. 
2. Pilih peran dan buka rekaman. 
3. Atur pemanfaatan target untuk peran.

> ![Tangkapan layar menggunakan peran sumber daya untuk menetapkan target pemanfaatan](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Hitung pemanfaatan yang dikenakan biaya untuk sumber daya

Menghitung pemanfaatan sumber daya yang bisa ditagih, Anda harus menyelesaikan beberapa prasyarat. 

### <a name="set-default-role-for-individual-resource"></a>Mengatur peran default untuk sumber daya individual

Pertama, Pemanfaatan target harus diatur di sumber daya individual atau pada peran sumber daya. Jika Anda menggunakan peran sumber daya untuk target, setiap sumber daya individual harus memiliki peran default. 

1. Untuk menetapkan ini, buka **sumber daya** \> **sumber daya**. 
2. Pilih sumber daya, buka rekaman, lalu pilih tab **Project Service**. 
3. Di kisi **peran sumber daya**, pastikan ada satu peran untuk sumber daya dan **Is Default** diatur ke **ya**.
 
### <a name="change-billing-type-for-resource-role"></a>Ubah jenis penagihan untuk peran sumber daya

Peran sumber daya harus diatur untuk memiliki jenis penagihan **dikenakan biaya**. 

1. Buka **Sumber Daya** \> **Peran Sumber daya**. 
2. Buka rekaman yang ingin diperbarui, kemudian tetapkan jenis penagihan default ke **Dikenakan biaya**.

### <a name="set-working-hours-for-resource-role"></a>Mengatur jam kerja untuk peran sumber daya
 
Sumber daya harus memiliki jam kerja untuk perhitungan kapasitas. 

1. Buka **Sumber Daya** \> **Sumber daya**. 
2. Pilih sumber daya untuk membuka rekaman, lalu pilih **Tampilkan Jam Kerja**. 
3. Anda dapat melakukan pembaruan massal daftar sumber daya dengan menerapkan **Template jam kerja** dari tampilan **daftar sumber daya**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Mengatasi masalah jam aktual kena biaya

Jam aktual dikenakan biaya bersumber dari entitas **aktual**. Nilai aktual dengan jenis penagihan **dikenakan biaya** tercakup dalam perhitungan ini, dan untuk alasan ini, Anda harus memiliki proyek dengan nilai aktual dikenakan biaya.

Jika Anda tidak melihat pemanfaatan dikenakan biaya, berikut adalah beberapa hal yang Anda dapat memeriksa:

- Sumber daya memiliki jam kerja yang ditentukan untuk kapasitas.
- Sumber daya memiliki target pemanfaatan yang ditentukan secara individual atau memiliki peran default yang ditetapkan ke dalamnya. Peran memiliki target pemanfaatan yang ditentukan untuk itu.
- Nilai aktual memiliki jenis penagihan **dikenakan biaya** selama periode yang Anda harapkan perhitungan pemanfaatannya. Periksa yang berikut ini jika Anda melihat nilai aktual dengan tagihan jenis selain dikenakan biaya:

  - Peran yang digunakan di aktual memiliki jenis default penagihan sesuatu selain dari dikenakan biaya.
  - Peran pada baris kontrak proyek yang mendukung proyek telah ditetapkan untuk tidak dikenakan biaya.
  - Proyek tidak memiliki baris kontrak terkait.

