---
title: Sekilas mode manajemen sumber daya
description: Topik ini menyediakan informasi tentang fungsi manajemen sumber daya di Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: f30bac95b2beb92345cbe25332963c58d2bde4bb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585060"
---
# <a name="resource-management-modes-overview"></a>Sekilas mode manajemen sumber daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Dynamics 365 Project Operations mendukung dua mode agar Anda dapat menjalankan alur pemesanan secara keseluruhan. Mode manajemen didefinisikan sebagai parameter proyek dan dapat dimodifikasi jika bisnis Anda memerlukan perubahan.    

## <a name="central-mode"></a>Mode Pusat
Untuk organisasi yang memusatkan alokasi sumber daya ke proyek, mode pusat menyediakan cara untuk memastikan manajer proyek dapat menentukan persyaratan sumber daya di tingkat proyek. Pemenuhan persyaratan sumber daya didelegasikan ke manajer sumber daya. Manajer proyek dapat menerima atau menolak sumber daya yang diusulkan oleh Manajer sumber daya.

![Mode Pusat.](./media/resource-management-central.png)

Untuk mengelola sumber daya dengan mode pusat, lihat:

- [Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya](/dynamics365/project-service/assign-generic-bookable-resource)
- [Memesan sumber daya bernama dari persyaratan sumber daya](/dynamics365/project-service/book-named-resource)
- [Mengajukan permintaan sumber daya](/dynamics365/project-service/submit-resource-request)
- [Memenuhi permintaan sumber daya.](/dynamics365/project-service/resource-management-fulfill-requests)
- [Menerima atau menolak sumber daya proyek yang diusulkan dari permintaan sumber daya](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Mode hibrida
Untuk organisasi yang memerlukan fleksibilitas dalam alokasi sumber daya, mode hibrida memungkinkan untuk manajer proyek dan manajer sumber daya kemampuan untuk memesan sumber daya.

![Mode hibrida.](./media/resource-management-hybrid.png)

Selain proses mode pusat yang didukung, lihat topik berikut untuk mengelola semua alur Pemesanan yang didukung lainnya dalam mode hibrida:

Pesan sumber daya langsung untuk proyek:
- [Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas](/dynamics365/project-service/assign-named-bookable-resource)

Pesan sumber daya dari persyaratan sumber daya:
- [Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya](/dynamics365/project-service/assign-generic-bookable-resource)
- [Memesan sumber daya bernama dari persyaratan sumber daya](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]