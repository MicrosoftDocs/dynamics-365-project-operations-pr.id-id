---
title: Sekilas mode manajemen sumber daya
description: Topik ini menyediakan informasi tentang fungsionalitas manajemen sumber daya di Dynamics 365 Project operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930095"
---
# <a name="resource-management-modes-overview"></a>Sekilas mode manajemen sumber daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Dynamics 365 Project Operations mendukung dua mode agar Anda dapat mengeksekusi alur Pemesanan secara keseluruhan. Mode manajemen didefinisikan sebagai parameter proyek dan dapat dimodifikasi jika bisnis Anda memerlukan perubahan.    

## <a name="central-mode"></a>Mode Pusat
Untuk organisasi yang memusatkan alokasi sumber daya ke proyek, mode pusat menyediakan cara untuk memastikan manajer proyek dapat menentukan persyaratan sumber daya di tingkat proyek. Pemenuhan persyaratan sumber daya didelegasikan ke manajer sumber daya. Manajer proyek dapat menerima atau menolak sumber daya yang diusulkan oleh Manajer sumber daya.

![Mode Pusat](./media/resource-management-central.png)

Untuk mengelola sumber daya dengan mode pusat, lihat:

- [Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Memesan sumber daya bernama dari persyaratan sumber daya](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Mengajukan permintaan sumber daya](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Memenuhi permintaan sumber daya.](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Menerima atau menolak sumber daya proyek yang diusulkan dari permintaan sumber daya](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Mode hibrida
Untuk organisasi yang memerlukan fleksibilitas dalam alokasi sumber daya, mode hibrida memungkinkan untuk manajer proyek dan manajer sumber daya kemampuan untuk memesan sumber daya.

![Mode hibrida](./media/resource-management-hybrid.png)

Selain proses mode pusat yang didukung, lihat topik berikut untuk mengelola semua alur Pemesanan yang didukung lainnya dalam mode hibrida:

Pesan sumber daya langsung untuk proyek:
- [Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Pesan sumber daya dari persyaratan sumber daya:
- [Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Memesan sumber daya bernama dari persyaratan sumber daya](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
